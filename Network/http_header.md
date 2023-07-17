## Everything about http header

> HTTP 공통 헤더

    요청 및 응답 메세지 모두에서 사용 가능한 일반 목적의 헤더

    - Date : Http 메세지 생성 일시
    - Connection : 클라이언트와 서버 간 연결에 대한 옵션 설정 (ex. close: 현재 http 에세지 직후에 TCP 접속을 끊음, Keep-Alive: 현재 TCP 커넥션 유지)
    - Cache-Control : 쿠키, 캐시 관련
    - Pragma
    - Trailer

> HTTP Entity Header

    요청 및 응답 메세지 모두에서 사용 가능한 Entity(콘텐츠, 본문, 리소스 등)에 대한 설명 헤더
    HTTP 메세지 내 포함된 선택적인 개체에 대한 구체적인 미디어 타입 등의 설명
    HTTP 메세지는 이미지, 비디오, 오디오, HTML 문서, 전자메일 등의 개체 운반 가능

    - Content-Type
        해당 개체에 포함되는 미디어 타입 정보
        컨텐츠의 타입 및 문자 인코딩 방식을 지정
        타입(type, 10개 정도 표준으로 지정: application, audio, font, image,등) + 서브타입(subtype, 각 타입별로 수십에서 수백개)
        ex: Content-Type: text/html; charset-latin-1
            해당 개체가 html 텍스트 문서이고 iso-latin-1 문자 인코딩 방식으로 표현되는 것을 의미

    - Content-Language
        해당 개체와 가장 잘 어울리는 사용자 언어(자연어)

    - Content-Encoding
        해당 개체의 데이터 압측 방식, 압축되었다면 Content-Encoding, Content-Length 2개의 항목을 토대로 압축 해제
        ex: Content-Encoding: gzip, deflate

    - Content-Length
        전달되는 해당 개체의 바이트 길이 또는 크기(10진수)
        응답 메세지 Body의 길이를 지정하거나 특정 지정된 개체의 길이를 지정

    - Content-Location
        해당 개체의 실제 위치를 알려줌

    - Content-Disposition
        응답 Bodyfmf
    - Content-Security-Policy
    - Location
    - Last-Modified
    - Transfer-Encoding
