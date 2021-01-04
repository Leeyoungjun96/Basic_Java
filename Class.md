다형성 : 같은 타입이지만 실행 결과가 다양한 개체를 대입할 수 있는 성질을 말한다. ex) 자동차(의 바퀴들)

메소드 영역에 class가 메모리에 instance가 만들어짐.

class 하나로 여러가지 객체를 만들 수 있음.

변수를 통해서 객체를 사용.

this. → 현재객체의 참조(객체(instance)가 있을 때 heap영역에서만 사용 가능)

필드(Field) → 객체의 고유 데이터, 객체가 가져야할 부품 객체, 객체의 현재 상태 데이터.

생성자(Constructor) 호출 → ClassName() (객체를 어떻게 만들것인지에 대해 작성, 객체 생성시 초기화)

메소드(Method) → 객체의 동작에 대해 작성 , 메소드는 반드시 객체안에 존재(JAVA), 대부분의 메소드는 객체가 생성된 후에 생성.

함수는 단독으로 실행,

메소드 오버로딩

클래스 내에 같은 이름의 메소드를 여러개 선언하는 것을 말한다.

오버로딩의 조건 : 매개변수의 타입, 개수, 순서가 달라야함.
***
Member :
Instance member

member란 객체(Instance)마다 가지고 있는 필드와 메소드를 말함.

인스턴스 멤버는 객체에 소속된 멤버이기 때문에 객체가 없이는 사용 불가.

필드는 값이 따로따로 저장되어야서 분산될 수 있지만, 메소드는 따로따로 저장될 필요가 없음.

Static member

클래스에 고정된 필드와 메소드. 객체 없이 사용 가능

클래스에 소속된 내부로 객체 내부에 존재하지 않고, 메소드 영역에 존재.

```java
class xxx{                         class xxx{
	int f1;                            Static int f1;
	int f2;                            Static int f2;
} //heap 영역에서만 저장            } //method 영역에서만 저장
```

정적멤버(static member)사용시 클래스 이름과 함께 도트(.) 연산자로 접근 (객체가 있을시 사용 불가, this. 사용 불가)
***
Package
package의 물리적인 형태는 파일 시스템의 폴더이다. (보통 소문자로 쓴다)

전체 클래스 이름 = 상위패키지.하위패키지.클래스 (클래스 이름은 모든 패키지를 포함)

단순한 클래스 이름은 simple name

클래스명이 같아도 패키지명이 다르면 다른 클래스로 취급.

package가 class를 구분 지을수 있는 식별자 역할을 할 수 있음.

package 이름까지 넣어야지 실행

***
접근제한 :
필드와 메소드의 접근 제한 ( 다 붙일 수 있음(public, protected, privat, static)
생성자의 접근제한( 객체를 만들 때 어느 곳에서 만들지 결정)

```java
Math m = new Math();
Math.round();
Math.pow();
```

***
Getter, Setter: 

A   —(method(user);)—>      B

```java
User user = new User();
user.setUid("winter");
user.setUname("한겨울");
user.setUemail("winter@...");

method(user);
```
