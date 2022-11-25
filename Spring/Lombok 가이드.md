# Lombok 사용 시 주의사항

Lombok은 우리 클래스 내에서 코드를 줄여주는 자바 라이브러리다. 편리한 만큼 잘못 사용하기 쉬운 Lombok이기 때문에
사용하는데 있어 조심할 점을 살펴보자.

## 1. @Data는 쓰지 않도록 하자
보통 코드를 작성하는데 있어 @Data부터 작성해주는 개발자들이 있다. 물론 나도 이런 행동을 해왔다.
여기서 핵심은 @Data는 Getter, Setter 뿐만 아니라 equals, hashcode, toString, canEqual과 같은 다른 추가적인 메소드를 제공한다.

그러나, 우린 Getter, Setter만 사용하기 위해서 @Data를 붙여준다면 사용하지 않는 메소드에 대해서도 정의를 하기 때문이다.

![image](https://user-images.githubusercontent.com/109537583/203789040-93692f53-0294-4cd9-a550-8216950980eb.png)

다음과 같이, Data보다는 Getter, Setter로 정의하자.

## 2. 무분별한 Setter는 쓰지 않도록 하자.
Setter는 모든 필드에 대한 Setter를 만들어주는데, 편한 반면 변하지 않아야 할 필드에 대해서도 만들어 줄 수 있기 때문에 주의해야 한다.
엔티티의 식별자와 같은 값은 거의 바뀔 일이 없으므로 주의해야 한다.


## 3. Builder는 클래스에 직접적으로 말고 생성자에 사용하자

## 참고
https://github.com/cheese10yun/TIL/blob/master/Spring/lombok-guide.md
