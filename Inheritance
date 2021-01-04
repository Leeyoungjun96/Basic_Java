부모 클래스를 재사용 하여 자식클래스를 빨리 개발

객체의 다형성을 구현

부모 클래스의 private 접근을 갖는 필드와 메소드는 제한

부모 클래스가 다른 패키지에 있을 경우, default 접근을 갖는 필드와 메소드도 제한

```java
public class A{
	inf field1;
	void method1(){...}
}

public class B extends A{
	String field1;
	void method2(){...}
}

class 자식클래스 extends 부모클래스1, 부모클래스2(x){
}
```

자식 객체를 생성할때 부모 객체부터 생성되고, 자식 객체가 나중에 생성됨.

```java
public Cellphone(){} --> public DmbCellphone(){ super(); }
```

부모 생성자가 매개변수를 가질 때 그에 맞게 끔 super(); 작성

***
####Method Override:
부모 클래스의 메소드를 자식클래스에서 수정해서 사용

부모 클래스의 메소드 선언부와 동일해야한다

접근 제한(public. private...)을 더 강하게 재정의 못함

새로운 예외를 throws 못함

@Override : compiler가 재정의를 검사

부모 매소드는 숨겨지는 효과가 발생

super.부모메소드(); : 부모 메소드 호출

***
final 클래스, 메소드 : 상속할 수 없음 (재정의 하지말라)

protected
같은 패키지 - default와 동일

다른 패키지 - 자식 클래스만 접근 허용( 상속일 때만 허용 )

```java
			package1                                       package2
public class A{                               class C{
			protected 멤버                             class A 상속 불가능
}                                             }

class B{                                      class D extends A{
                                                 class A 상속가능
	                                               단 객체를 생성할 수 없음
}                                             }
```
***
####Polymorphism ★: 
같은 타입이지만 실행 결과가 다양한 객체를 대입할 수 있는 성질을 말한다.

부모타입에는 모든 자식 객체가 대입 가능( 자식 타입은 부모 타입으로 자동 변환된다)

객체를 부품화 시킬 수 있음( 부모타입은 규격)

#####자동 타입 변환 - 프로그램 실행 도중 자동적으로 타입변환이 일어나는 것 (중요)
```java
class Parent(){
	void method1(){}
	void method2(){}
}

class Child extends Parent(){
	void method2();
	void method3();
}

class ChildExample{
	public static void main(String[] args){
	Child child = new Child();

	Parent parent = child;

	parent.method1(); // Parent클래스의 method1

	parent.method2(); // Child 클래스의 재정의된 method2

	parent.method3(); // Parent클래스의 타입을 쓰기 때문에 method3은 사용 불가능
}
```
#####매개 변수의 다형성
매개 변수가 class 타입일 경우 해당 클래스의 객체를 대입하는 것이 원칙이나 자식 객체를 대입하는 것도 허용( 자동 변환 때문에 가능)

부모 클래스 변수에 자식 객체를 넣을 수 있음

#####강제 타입 변환:
부모 타입을 자식 타입으로 변환하는 것을 말함

```java
자식클래스 변수 = (자식클래스) 부모클래스타입;
```

자식 타입이 부모 타입으로 자동 변환된 이후, 다시 자식 타입으로 변환할 때만 유효

```java
Animal a = new Dog();
Dog d = (Dog) a;
```

#####객체 타입 확인
부모 타입이면 모두 자식 타입으로 강제 타입 변환할 수 있는 것이 아니다.

```java
Parent parent = new Parent();
Child child = (Child) parent; //강제 타입 변환을 할 수 없다.
```

먼저 자식 타입인지 확인 후 강제 타입을 해야 한다.

```java
boolean result = 좌향(객체)instanceof 우항(타입)

public void method(Parent parent){
 if(parent instanceof Child){ //parent 매개변수가 참조하는게 child인지 조사
		Child child = (Child) parent;
	}
}   
```
####Abstract class
공통된 필드와 메소드의 이름을 통일

실체 클래스 설계 규격을 만들고자 할 때

부모 클래스 안에 넣을것을 정하기 애매하여, 상속받는 자식 클래스에게 강제적으로 내용을 채우게 함

```java
public abstract class 클래스{
	// Abstract Method
	public abstract void method();
}
```

이 때 부모 객체는 완벽하게 만든게 아니라서 부모 객체를 직접받을 수 없음
