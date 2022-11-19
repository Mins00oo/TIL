# Spring의 Transactional Rollback 처리에 대해
#### 기본적으로 스프링 부트는 트랜잭션은 auto-commit 방식이다.
![image](https://user-images.githubusercontent.com/109537583/202832936-d6dab562-ba71-4f13-8941-9a9d0331e308.png)
![image](https://user-images.githubusercontent.com/109537583/202832951-b40774d4-5a8a-434c-a73e-1e2482992e88.png)
위의 예시를 보면, 예외가 발생했음에도 데이터베이스에 상품 데이터가 insert 된것을 볼 수 있다.

### `모든 트랙잭션들은 여러 로직들 사이에서 예외가 발생하지 않았을때만 커밋되어야한다.`

-----
![img_4.png](img_4.png)
- 위와 같이 @Transactional 어노테이션은 예외발생 시 롤백처리를 시킨다.
- 위를 통해 내릴 수 있는 결론은 @Transational 어노테이션을 통해 기본적으로 **unchecked exception**만 롤백처리가 된다는 것이다.
