# Set 컬렉션

-------------
- List컬렉션은 저장 순서를 유지하지만, Set은 유지하지 않는다.
- 객체를 중복해서 저장할 수 없고, 하나의 null만 저장할 수 있다.

![image](https://user-images.githubusercontent.com/109537583/198260967-793de416-c5c0-4a78-b457-2a647cf3d195.png)
- 구슬 주머니와 비슷하다. 동일한 구슬을 2개 넣을 수 없고, 들어갈 때와 나올 때의 순서가 다를 수도 있다.
- 저장, 삭제
  - `Set<String> set = ...;`
  - `set.add("홍길동");`
  - `set.remove("홍길동);`
- set 컬렉션은 인덱스로 객체를 검색할 수 없다.
- 전체 대상을 한번씩 반복해서 가져오는 Iterator를 제공한다.
  - `Iterator<String> iterator = set.iterator();`
- `hasNext()`
  - 가져올 객체가 있으면 true를 리턴하고 없으면 false
- `next()`
  - 컬렉션에서 하나의 객체를 가져온다.
-----------------------
## HashSet
- 생성
  - `Set<String> set = new HashSet<String>();`
- 순서 없이 저장하고 동일한 객체는 중복 저장하지 않는다.
  ![image](https://user-images.githubusercontent.com/109537583/198263588-b2bbe667-afbf-4e32-817c-d1b6731cc52d.png)
- 다음과 같이 hashCode() 메소드를 호출해서 리턴값을 얻어내고 동일하다면 equals() 메소드의 반환값으로 판단한다.
- 문자열을 저장할 경우, 같은 문자열을 갖는 String 객체는 동등한 객체로 간주
