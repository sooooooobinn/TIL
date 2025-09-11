# Security란?
스프링 기반이 애플리케이션 보안(인증, 인가)을 담당하는 스프링 하위 프레임워크이다. 

보안 관련 여러 기능들이 제공되고 개발자가 직접 관련 로직을 작성하지 않아도 된다는 장점이 있다.


## Security 용어 정리
- **접근 주체(principal)** : 보호된 대상에 접근하는 유저
- **인증(Authentication)** : 유저가 id와 password를 이용하여 로그인하는 과정
- **인가(Authorization)** : 어떠한 대상이 특정 목적을 실현하도록 허용하는 것
- **권한(Role)** : 인증된 주체가 애플리케이션의 동작을 수행할 수 있도록 허락되었는지를 결정


## Spring Security Filter
기본적으로 10개 이상 존재한다.


## Security 동작 과정
1. 사용자가 id, password를 입력하면 request에 담겨 보내진다.
2. ``AuthenticationFilter``에서 request를 가로채서 인증용 객체인 ``UsernamePasswordAuthenticationToken``을 생성한다.
> ``AuthenticationFilter`` : 모든 request는 인증과 인가를 위해 이 필터를 거쳐간다.
>
>``UsernamePasswordAuthenticationToken`` : Authentication을 구현한 AbstractAuthenticationToken의 하위 클래스이다.