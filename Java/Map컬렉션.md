# Map컬렉션

--------------
- 키와 값으로 구성된 Entry 객체를 저장
- 키는 중복 저장 불가능하지만 값은 중복 저장 가능
- 기존에 저장된 키와 동일한 키로 값을 저장하면 기존의 값은 없어지고 새로운 값으로 대체

![image](https://user-images.githubusercontent.com/109537583/198281519-706729bd-8b71-45e8-a3e2-e7ec60184523.png)
- 객체 추가
  - `put()`
- 객체 찾기
  - `get()`
- 객체 삭제
  - `remove()`
- 모든 키를 Set 컬렉션으로 얻기
  - `KeySet()`
- 모든 Map.Entry를 Set컬렉션으로 얻기
  - `entrySet()`
----------------
## HashMap
Map 인터페이스를 구현한 대표적인 Map 컬렉션
- 키로 사용할 객체는 hashCode()와 equals() 메소드를 재정의해서 동등 객체가 될 조건을 정해야 함
- 키와 값의 타입은 기본 타입(byte, short, float, int, doulbe ...) 사용 불가하고 클래스 및 인터페이스 타입만 가능
----------------
## Hashtable
HashMap과 동일한 내부 구조
- 동기화된 메소드로 구성되어 있기 때문에 멀티스레드가 동시에 이 메소드들을 실행할 수 없음
- 스레드가 안전함
- 생성
  - `Map<K, V> map = new Hashtable<K, V>();`
-----------------
## getOrDefault(Object key, V DefaultValue)
- key: 값을 가져와야하는 요소의 키
- defaultVale: 키로 매핑된 값이 없다면 반환되어야 하는 기본값
