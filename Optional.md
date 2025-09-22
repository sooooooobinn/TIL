# Optional
Optional이란 null일 수도 있는 객체의 값을 감싸는 Wrapper 역할을 하며 값이 존재하지 않는 경우에 대한 처리를 표현적으로 표현하는데 유용하다.

> **Wrapper란?**
>
> 자바의 자료형은 크게 기본 타입(char, int, float, double, boolean)과 참조 타입(class, interface)으로 나뉘는데 자료 타입을 객체로 다루기 위해서 사용하는 클래스들을 뜻한다.

Optional 변수 내부에서는 null이 아닌 객체가 있을 수도 있고 null이 있을 수도 있다.

### orElseThrow()
orElseThrow() 메서드는 Optional 객체에서 값을 꺼내오는 메서도로, 값이 존재하는 경우에는 해당 값을 반환하고, 값이 없는 경우에는 지정된 예외를 발생한다. 

### orElseGet()
Optional 클래스의 메서드 중 하나로, orElseThow()와 값이 유사하게 존재하지 않는 경우의 처리를 지원한다.

orElseGet() 메서드는 값이 존재하지 않는 경우, 기본적으로 제공된 람다 표현식 또는 Supplier 함수를 실행하여 대체 값을 생성한다.

> **Supplier 함수란?**
>
> 어떠한 입력도 받지 않고 결과를 반환하는 연산을 수행한다. 이 인터페이스는 주로 요청 시 새로운 객체를 생성하거나, 복잡한 계산이나 조건에 따른 결과를 제공할 때 사용된다.

