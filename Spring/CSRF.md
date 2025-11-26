# CSRF(Cross Site Request Forgery)란 무엇인가?

SpringSecurity를 구현하다 보면 CSRF를 disable해주는 경우가 많다.

CSRF는 웹 보안 취약점의 일종이며, 사용자가 자신의 의지와는 무관하게 공격자가 의도한 행위(데이터 수정, 삭제, 등록 등)을 특정 웹사이트에 요청하게 하는 공격입니다.

## CSRF 동작원리
**CSRF 성공 조건**
- 사용자가 보안이 취약한 서버로부터 이미 로그인이 되어있어야 한다.
- 쿠키 기반의 세션 정보를 획득할 수 있어야 한다.
- 공격자는 서버를 공격하기 위한 요청 방법에 대해 미리 파악하고 있어야 한다.


CSRF Protection은 Spring Security에서 default로 설정되어 있다.
>**CSRF Protection이란?**
>
>GET 요청을 제외한 상태를 변화시킬 수 있는 요청(POST, PUT,DELETE)들로부터 보호한다.

그렇다면 이 CSRF를 왜 disable 하였을까?