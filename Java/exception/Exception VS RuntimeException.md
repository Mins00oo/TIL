## Exception vs RuntimeException

    Exception - Checked Exception
    Runtime Exception - Unchecked Exception
### Checked Exception?

- 반드시 예외처리를 해야한다
- 롤백처리가 되지 않는다 (트랜잭션 롤백)
- 컴파일 중에 예외처리를 확인한다
- 사용자 동작, 운영체제 등 외부 영향으로 인해 발생한다

### Runtime Exception?

- 예외처리를 하지 않아도 된다
- 롤백 진행
- 런타임 중에 예외처리를 확인
- 프로그래머의 실수에 의해서 발생한다
