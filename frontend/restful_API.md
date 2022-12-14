## REST란 무엇인가?

> 자원을 이름으로 구분하여 해당 자원의 상태를 주고 받는 것

REST 란 **Representational State Transfer**의 약자로 URI와 HTTP 메소드를 이용해서 객체화된 서비스에 접근하는 것을 말한다.

REST의 요소로는 크게 리소스, 메소드, 메세지 3가지 요소로 구성되는데 예를 들면 "이름이 jenny인 사용자를 생성한다" 라는 호출이 있을 때 "사용자"는 생성되는 리소스, "생성한다"하는 행위는 메소드, "이름이 jenny인 사용자"는 메시지가 된다.

즉 리소스는 "http://myweb/user/" 라는 형태의 URI로 표현되며, 메소드는 HTTP Post, 메시지는 JSON 문서를 이용해서 표현되며 HTTP에는 여러가지 메소드가 있지만 REST에서는 CRUD에 해당하는 4가지의 메소드 GET, POST, PUT, DELETE를 사용한다.

# RESTFUL API란?

> 즉, **RESTFUL API 란 rest를 통해 확장성과 재사용성, 즉 업무 효율을 올리는 규칙등을 적용하여 서비스 API를 구현하는 것 의미**

Restful하게 API를 디자인한다는 것은 URI를 규칙에 맞게 잘 설계했는지 여부
HTTP 요청을 보낼 때 어떤 URI에 어떤 메소드를 사용할지 개발자들 사이에서 지켜지는 약속

### 규칙

1. 동일한 URI(end-point)의 행위에 맞게 POST, GET, DELETE, PATCH 등의 메소드를 사용
2. 명사를 사용, 리스트를 표현할 때는 복수형을 사용
3. URI Path에 불필요한 파라미터를 넣지 않는다. 즉 단계를 심플하게 설계
4. \_ 은 URI에 사용하지 않는다
5. 파일 확장자는 URI에 포함하지 않는다
6. - (하이픈)은 URI 가독성을 높이는 데 사용

### 응답상태코드

1xx : 정보 응답
2xx : 성공 응답
3xx : 리다이렉션 메시지
4xx : 클라이언트 에러 응답
5xx : 서버 에러 응답
