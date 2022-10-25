<h1>책</h1>


<h2>Chatper 1</h2>



<h2>Chapter 2</h2>

* 동적 파라미터화<br>


변화하는 요구사항에 대응하기 위해<br>
- 첫 번쨰 시도<br>
비슷하고 반복 존재한다면 그 코드를 추상화한다.<br>
- 두 번쨰 시도<br>
- 세 번쨰 시도<br>



개인적으로 전략 패턴이 생각나는 예제 였다.(런타임시에 동작이 결정되어 다양한)<br>

- 네 번째 시도 추상적 조건으로 필터링<br>

 한 개의 파라미터 다양한 동작<br>
 
 Q.2-1<br>
 
 public interface ExampleFormatter{<br>
  String accept(Example ex);<br>
 }<br>
 
 public <br>
 |제목|내용|설명|
|:---:|:---:|:---:|
|

 <br>

- 익명클래스 사용

<h4>람다란 무엇인가?</h4>
람다 표현식은 메서드로 전달할 수 있는 익명 함수를 단순화 한 것이라고 할 수 있다.<br>

<h4>람다의 특징</h4>
 - 익명: 보통의 메서드와 달리 이름이 없으므로 익명이라고 표현한다. (구현해야 할 코드에 대한 걱정거리가 줄어든다.)<br>
 - 함수: 람다는 메서드처럼 특정 클래스에 종속되지 않으므로 함수라고 부른다. 하지만 메서드처럼 파라미터 리스트, 바디, 변환 형식, 가능한 예외 리스트를 포함한다.<br>
 - 전달: 람다 표현식으로 메서드 인수로 전달하거나 변수로 저장할 수 있다.<br>
 - 간결성: 익명 클래스처럼 많은 자질 구레한 코드를 구현할 필요가 없다.<br>

<h4>람다의 표현식</h4>
 - Example : (Test t1, Test t2) -> t1.getLength().compareTo(t2.getLength());<br>
 - 람다 파라미터 : (Test t1, Test t2), 화살표,람다 바디 : t1.getLength().compareTo(t2.getLength()); 으로 이루어진다.<br>

<h4>람다는 어떻게 사용할까?</h4>
함수형 인터페이스라는 문맥에서 람다 표현식을 사용할 수 있다.<br>

<h4>함수형 인터페이스란?</h4>
하나의 추상 메서드를 지정하는 인터페이스를 뜻한다.<br>
예시로 Java API의 함수형 인터페이스로 Comparator,Runnable 등이 있다.<br>
람다 표현식으로 함수형 인터페이스의 추상 메서드를 구현을 직접 전달할 수 있으므로 전체 표현식을 함수형 인터페이스의 인스턴스로 취급할 수 있습니다.<br>
@FunctionalInterface 어노테이션을 통하여 해당 인터페이스가 함수형 인터페이스임을 가리킬 수 있으며 실제로 추상 메서드가 한개 이상일 경우 에러를 발생시킵니다.<br>

<h4>함수 디스크립터</h4>
람다 표현식의 시그니처를 서술하는 메서드를 함수 디스크립터라고 칭합니다. 예를 들어 Runnable의 유일한 추상 메서드 run은 인수와 반환값이 없으므로 이를 시그니처로 생각 할 수 있습니다.<br>
람다 표현식의 형식
