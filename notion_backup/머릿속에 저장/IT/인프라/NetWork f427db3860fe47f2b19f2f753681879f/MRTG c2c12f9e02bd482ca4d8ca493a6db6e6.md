# MRTG

---

**필요 패키지**

ㄴ net-snmp

ㄴ net-snmp-utils

ㄴ mrtg

ㄴ httpd

**필요 조건**

ㄴ selinux 비활성화 처리 (/etc/selinux/conf > selinux = disabled)

ㄴ 모니터링 할 스위치의 snmp 커뮤티니 설정 여부 & 커뮤니티 키값

---

1. snmpwalk -v2c -c snmp키값 스위치IP 로 해당스위치에서 모니터링 정보를 가져올 수 있는지 확인
2. cfgmaker --global 'WorkDir: /var/www/mrtg/' --global 'Language: korean' --global 'Options[_]: bits,growright' -output /var/www/mrtg/mrtg.cfg **snmp키값**@**스위치IP**
    - **cfgmaker 명령어 : snmp를 이용해서 장비 및 센서 등록**
    - mrtg.cfg에 아래 구문 추가
        - Target[127.0.0.1_1]: 1:public@127.0.0.1:
        - SetEnv[127.0.0.1_1]: MRTG_INT_IP="127.0.0.1" MRTG_INT_DESCR="lo"
        - MaxBytes[127.0.0.1_1]: 1250000
        - Title[127.0.0.1_1]: Traffic Analysis for local loopback
        - PageTop[127.0.0.1_1]:Traffic Analysis for local loopback
3. indexmaker --title "페이지 타이틀 제목" --output /var/www/mrtg/index.html /var/www/mrtg/mrtg.cfg
    - **indexmaker 파일 : HTTP 출력 페이지 생성 (그래프 이미지 생성)**
4. vi /etc/httpd/conf/httpd.conf > DocumentRoot와 Directory를 /var/www/mrtg로 수정
    - 이후 하단 명령어로 방화벽 80포트에 대한 방화벽 해제
        - firewall-cmd --permanent --add-port=80/tcp
        - firewall-cmd --reload
5. systemctl httpd restart
6. /etc/crontab에서 아래 명령 입력
    - /5 * * * * root /usr/bin/cfgmaker --global 'WorkDir: /var/www/mrtg/' --global 'Language: korean' --global 'Options[_]: bits,growright' -output /var/www/mrtg/mrtg.cfg **snmp키값**@**스위치IP**
    - /5 * * * * root env LANG=C /usr/bin/mrtg /var/www/mrtg/mrtg.cfg
7. vi /etc/httpd/conf/httpd.conf 에서 AddDefaultCharset을 off로 수정해주면 한글 정상 표시

참고 :  [https://tisiphone.tistory.com/184](https://tisiphone.tistory.com/184)

---

ETC..

tail -f /var/log/cron로 크론이 돌고 있는 로그 확인 가능

indexmaker는 최초 한번만 만들어도 됨