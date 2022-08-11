# Linux commend

---

## CentOS7.9.2009 기준

**fdisk -c -u /dev/sd***

Disk partition

---

**df -h**

mounted Disk status

---

**source /etc/bashrc**

Apply Alias without shutdown

---

**mount /dev/sd* /{DirectoryName}**

Mount directory to disk partition

---

**mount —bind /{DirectoryName} /{DirectoryName}**

Mount directory to directory

---

**tcpdump** 

-i eth0 : eth0에서 감지되는 패킷에 대하여 출력

-w : 출력되는 결과에 대하여 파일로 저장

-r : w옵션으로 저장된 파일을 읽음 (VIM으로 읽기 불가)

tcp port ** : ** 포트로 통신하는 패킷 출력

host 192.168.0.X : src주소 혹은 dst 주소가 지정된 IP인 패킷을 출력

src 192.168.0.X : src주소 지정된 IP인 패킷을 출력

dst 192.168.0.X : dst 주소가 지정된 IP인 패킷을 출력

net 192.168.0.X/24 : CIDR로 지정

&&,and, ||,or, !, not등의 연산가 사용 가능

 ex) tcpdump src 192.168.0.12 and not dsp port 3306

// 출발지 주소가 0.12이면서 목적지 포트가 3306이 아닌 패킷만 출력

---

**ab** 

(접속 부하테스트 툴) yum install apache2-utils로 설치

-n : 1명당 Request를 요청할 횟수를 지정

-c : Request를 요청할 머릿수를 지정

ab -n 400 -c 10 http://target URL/ 

→ http://target URL/에 10명의 인원이 400번의 Request를 보내도록 테스트

---

---

---

---

---

---

---

---