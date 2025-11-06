# Security란?
인증, 권한 관리 그리고 데이터 보호 기능을 포함하여 웹 개발 과정에서 필수적인 사용자 관리 기능을 구현하는데 도움을 주는 Spring의 강력한 프레임워크이다.

**개발자들이 보안 관련 기능을 효율적이고 신속하게 구현할 수 있도록 도움을 주는 것** 

### Security 사용 이유
Spring의 생태계에서 보안에 필요한 기능들을 제공하기 때문이다. Spring Security는 개발 구조가 Spring이라는 프레이워크 안에서 활용하기 적합한 구조로 설계되어 있어, 보안 기능을 추가할 때 활용하기 좋다.



# Security 구현해보기

## Security 설정, Data 설정

``@EnableWebSecurity``어노테이션 : 기본적인 Web 보안을 활성화 하겠다는 의미

추가적인 설정을 위해서는 ``WebSecurityConfigurer``를 implements하거나 ``WebSecurityConfigurerAdapter``를 extends하는 방법이 있다.

>**implements, extends**란?
>
>이 두 가지는 상속의 형태를 나타내는데 구현하는가 사용하는가에 따라서 갈리게 된다
>
>- extends : 부모의 메소드를 그대로 사용할 수 있으며, 오버라이딩 할 필요 없이 부모에 구현되있는 것을 직접 사용 가능하다.
>
>- implements : extends는 다중상속이 안되지만 implements는 다중상속이 된다. 가장 큰 특징은 부모의 메소드를 반드시 오버라이딩해야 한다는 점이다.

``WebSecurityConfigurerAdapter``의 configure 메소드 오버라이드 한다.

``authorizeRequests``는 HttpServletRequest를 사용하는 요청들에 대한 접근제한을 설정하겠다는 의미이다.