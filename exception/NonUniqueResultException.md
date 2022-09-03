 ### NonUniqueResultException
 -----------------------------
 #### 무슨 에러일까 ? 
  - jpa에서 쿼리반환결과값이 1개가 아닌 여러개가 나오게 됐을때 발생하는 에러입니다
  -  ex) javax.persistence.NonUniqueResultException: query did not return a unique result: 11
  -  https://docs.oracle.com/javaee/5/api/javax/persistence/NonUniqueResultException.html

예를 들어 , 저 같은 경우에는 Repository에서 findBy를 통해 반환하는 쿼리의 개수가 안 맞아서 에러가 발생했었습니다. 
오라클 공식 문서에서도 볼 수 있듯이 1개의 쿼리값을 반환할려고 하는데 실제 쿼리문이 실행됐을땐 1개보다 더 많은 결과값이 나와서 그런거같습니다
