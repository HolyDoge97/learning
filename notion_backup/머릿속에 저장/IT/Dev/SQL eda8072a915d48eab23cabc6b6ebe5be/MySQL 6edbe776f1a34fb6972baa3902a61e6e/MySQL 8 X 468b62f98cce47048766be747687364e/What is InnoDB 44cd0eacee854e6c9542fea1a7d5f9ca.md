# What is InnoDB?

---

## About …

- MySQL의 DB엔진 중 하나임
- 대용량의 데이터를 처리하거, 트렌젝션을 처리하기 위해선 InnoDB가 효율적임
- InnoDB는 **TableSpace**라는 개념을 사용한다
    
    [TableSpace?](What%20is%20InnoDB%2044cd0eacee854e6c9542fea1a7d5f9ca/TableSpace%209999e36b122c44c0af19308636b8ce1e.md)
    

---

## InnoDB의 특징

1. innoDB는 메인키(PK)를 기준으로 클러스러링을 진행한다
    
    [Index Clustering?](What%20is%20InnoDB%2044cd0eacee854e6c9542fea1a7d5f9ca/Index%20Clustering%202e50acda04344eb8a93a2f61cf5d998e.md)
    
2. 오라클의 아키텍처를 적용했다.
    1. 따라서 오라클이 가지는 특징들 몇몇을 가지고있다
        1. 예를들어 MVCC(특정 작업과 동시에 다른 작업을 진행할 수 있음)과 같은 것.
3. In Memery 구조를 가지고있다. (대충 메모리 버퍼를 가지고 있어서 캐싱을 사용할 수 있다는 의미)
    1. 자주 사용되는 데이터를 버퍼 풀에 유지시켜 더욱 빠르게 처리하도록 도와줌
    
    ![스크린샷 2022-08-05 오전 9.45.50.png](What%20is%20InnoDB%2044cd0eacee854e6c9542fea1a7d5f9ca/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-08-05_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_9.45.50.png)