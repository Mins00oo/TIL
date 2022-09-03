### @RequestBody vs @Model


RequestBody, ModelAttribute, RequestParam이 각각 언제 쓰이는지 차이점들에 대해 알아보자
------------------
 @RequestBody?
 - 요청 본문의 Body부분에 json이나 xml값으로 요청을 하여 Dto객체에 맞는 타입으로 바꿔서 바인딩을 시킨다
  Json Body부분을 통해 보내고자 하는 data전체가 통과한다 
 - 기본 생성자만으로 Java객체로 재구성할 수 있다, ObjectMapper를 통해 JSON객체를 역직렬화하기 때문이다.
  
 @ModelAttribute?
 - Url의 쿼리 파라미터를 받기 위해 사용되기도 한다, 일반적으로 쿼리 스트링에 활용된다
 - 파일을 업로드하기 위해선 ModelAttribute를 사용해야한다.
 - 클라이언트가 보내는 HTTP 파라미터를 특정 Java Object에 매핑한다
 - 따라서 객체의 필드에 접근해 데이터를 바인딩(매핑)할 수 있는 생성자 혹은 SETTER 메서드가 필요하다
