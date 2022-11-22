# `체크예외와 언체크 예외(Checked, Unchecked Exception)`

---
자바의 예외는 3가지로 나눌 수 있다.
- 체크 예외(Checked Exception)
- 언체크 예외(Unchecked Exception)
- 에러(Error)

![image](https://user-images.githubusercontent.com/109537583/202938866-b14c3316-95d8-4851-a018-fabd1273dd62.png)
위와 같이 계층 구조로 `에러`, `예외`로 구분된다. 
---
# `에러란 ? `
- 시스템이 비정상적인 상황에서 발생한다. 
- 개발자가 미리 예측할 수도 없고 처리할 방법도 없다.
- 따라서, `Error`에 대한 처리를 신경 쓰지 않아도 된다.
---
# `예외란?`

---
`예외`란 프로그램 실행 중 개발자의 실수로 예기치 않은 상황이 발생했을 때입니다. 
- ArrayIndexOutOfBoundsException, NullPointerException, FileNotFoundException 등이 있다.
- 예외에는 `체크 예외`, `언체크 예외`로 나눌 수 있다.
- RuntimeException의 하위 클래스들이 `Unchecked Exception`이고, Exception클래스의 하위 클래스들을 `Checked Exception`이라고 한다.
---

# `체크  예외`
- 반드시 명시적으로 처리해야한다.
- try catch를 통해 잡거나 throws를 통해 호출한 메소드로 예외를 던져야 한다.
---

# `언체크 예외 `
- 예외 처리를 강제하지 않는 특징이 있다.
- 그렇기 때문에 catch로 잡거나 throw로 예외를 던지지 않아도 상관이 없다.
---
![image](https://user-images.githubusercontent.com/109537583/202942178-e9ac179c-ad2d-497d-b8cf-3810f7222076.png)

---
# `참고`
https://cheese10yun.github.io/checked-exception/

https://www.nextree.co.kr/p3239/
