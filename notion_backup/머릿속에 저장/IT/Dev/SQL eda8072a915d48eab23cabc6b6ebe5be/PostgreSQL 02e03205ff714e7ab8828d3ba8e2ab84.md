# PostgreSQL

[Basic Syntax](PostgreSQL%2002e03205ff714e7ab8828d3ba8e2ab84/Basic%20Syntax%20ffb5055b01bb4043911b598344151b61.md)

---

- Simple Tip
    - 컬럼 데이터가 순차적으로 1 2 3 ... 증가하는 타입이면 serial type 사용가능
    - Postgre는 DESC 사용 불가
    - centos에서는, postgresql-server와 postgresql-contrib 설치가 필요
        
        설치 후 postgresql-setup initdb로 초기 설정
        
        이후 sudo -u postgresql psql로 접속
        
    - Postgresql 커맨드 라인을 빠져나갈 때에는 \q