# JDA(Java Discord API)
JDA란 Discord API를 Java로 매핑한 라이브러리이다. 

## - Discord Bot 만들기 
먼저
https://discord.com/developers
이 사이트에들어가서 새로운 애플리케이션을 만든다.

봇을 만든 후 추가 설정을 해주어야 하는데

MESSAGE CONTENT INTENT를 허용해주어야 디스코드에서 메세지를 입력하였을 때 스프링 부트에서 받을 수 있다.

또한 TOKEN도 설정해야 하는데 TOKEN에 COPY를 누르면 봇 관련 TOKEN 값을 얻을 수 있다.

또한 봇 권한도 설정해주면 봇 생성이 끝난다.

## - springboot 코드 작성하기
JDA 의존성 추가