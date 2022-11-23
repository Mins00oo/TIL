# Spring vs Spring Boot

스프링과 스프링부트의 차이점에 대해 살펴보자

## `Spring`이 뭐지 ?
간단하게, `스프링 프레임워크`는 자바 애플리케이션 개발에 있어 포괄적인 인프라 지원을 제공한다.

`의존성 주입 (Dependency Injection)`과 같은 특징이 포함되어 있고, 다음과 같은 모듈을 제공한다.
- Spring JDBC
- Spring MVC
- Spring Security
- Spring AOP
- Spring ORM
- Spring Test

이런 모듈들은 애플리케이션 개발에 소요되는 시간을 크게 감소시켜준다.
예를 들어, 이전에 자바 웹 개발에 있어서 우린 데이터 값을 삽입하기 위해 불필요한 코드로 작성을 해왔는데
Spring JDBC 모듈의 JDBCTemplate를 사용하면서 configuration 몇 줄 만으로 그런 코드들을 줄였다.

## `Spring Boot`는 뭐지?
`스프링 부트`는 기본적으로 스프링 프레임워크의 확장판과 같다. 스프링 애플리케이션 세팅에 있어
불필요하고 비효율적인 configuration 코드들을 줄일 수 있다.

다음과 같이 스프링 부트의 특징을 살펴볼 수 있다.
- `'starter' 의존성`을 통해 build와 애플리케이션 configuration을 간단하게 할 수 있다.
- 애플리케이션 배포에 있어 복잡함을 피하기 위해 `내장되어 있는 서버`
- 자동 Config 설정

-----------
# 예시로 차이점을 살펴보자
## 1. Maven Dependencies
스프링을 사용하면 웹 애플리케이션을 만드는 데 있어 다음과 같이 코드를 작성해줘야한다.

![image](https://user-images.githubusercontent.com/109537583/203453613-3de343fc-fc1b-4c20-862b-e294f54140a7.png)

이와 달리, 스프링 부트는 하나의 의존성을 통해 웹 애플리케이션을 실행시킬 수 있다.

![image](https://user-images.githubusercontent.com/109537583/203453716-6b5d35e1-ea56-4ff5-82aa-5ed012971112.png)


또 다른 예시로는 Spring의 경우 test 프레임워크를 사용하고자 하는 경우, Spring Test, JUnit, Hamcrest, Mockito 등 모든 라이브러리를
추가해줘야 하지만,
Spring Boot의 경우 spring-boot-starter-test만 추가해주면 된다.

## 2. Configuration 
Spring의 경우 configuration 설정을 할 때도 매우 길고, 모든 어노테이션 및 빈 등록을 설정해줘야한다.
반면, Spring Boot의 경우 `application.properties`나 `application.yml`파일에 설정하면 된다.

예를 들어 Thymleaf의 경우, Spring은 다음과 같은 코드와 thymleaf-spring5 의존성이 필요하다.

![image](https://user-images.githubusercontent.com/109537583/203466987-a978ab5b-7387-4102-be40-20180c4fc284.png)


반면, Spring Boot는 오직` spring-boot-starter-thymleaf` 한 줄로 가능하다.

## 3. Spring Security Configuration
Spring을 사용하게 되면 spring-security-web 및 spring-security-config 종속성이 모두 필요하다.
다음으로, WebSecurityConfigureAdapter를 확장하고 @EnableWebSecurity을 사용하는 클래스를 추가해야 한다.

![image](https://user-images.githubusercontent.com/109537583/203467547-92b19c54-e41e-4b01-9ca7-e288f899a8a6.png)

Spring Boot 또한 이러한 의존성들이 필요하지만, spring-boot-starter-security로 의존성을 정의해주면
자동적으로 classpath로 추가해준다.

## 4. 편리한 배포
Spring으로 개발한 경우, war파일을 Web Application Server에 담아 배포했습니다.

Spring Boot의 경우, 내장 WAS를 갖고 있기 떄문에 jar 파일로 간편하게 배포할 수 있다. 

## 5. 결론
Spring Boot는 간단하게 Spring의 확장판으로 개발, 테스트, 배포에 있어 좀 더 편리하게 해준다.
