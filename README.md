# interview practice

## CS(컴퓨터 과학)
##### Languge(언어)
###### JAVA 
<details>
<summary>JAVA</summary>
<br>
자바는 오라클에서 제공하는 객체 지향 프로그래밍 언어로,
플랫폼 독립성과 높은 안정성을 가진 언어입니다.
<br>
1.플랫폼 독립성

<br>
JVM(Java Virtual Machine)을 통해 한 번 작성하면 어디서든 실행 가능한 특징을 가집니다.
<br>

2.객체 지향 프로그래밍(OOP)
<br>
캡슐화, 상속, 다형성과 같은 OOP의 특징을 지원하여 유지보수와 재사용성이 뛰어납니다.
<br>

3.메모리 관리
<br>
가비지 컬렉션(Garbage Collection)을 통해 메모리 관리가 자동으로 이루어집니다.
<br>

4.풍부한 라이브러리 및 프레임워크
<br>
스프링(spring), 하이버네이트(Hibernate) 등 강력한 프레임워크로 대규모 시스템 개발이 용이합니다.
<br>

5.멀티스레딩 지원
<br>
멀티스레드를 기본 지원하여 동시성 프로그래밍이 쉽습니다.
<br>

6.보안성
<br>
바이트코드 검증과 샌드박스 실행환경을 제공하여 보안성이 높습니다.
<br>
</details>

<details>
<summary>JAVA의 동작순서(garbage collection)</summary>
<br>

1. 자바 컴파일러(javac)가 자바 소스코드(.java)를 읽어 자바 바이트코드(.class)로 변환시킵니다.
2. Class Loader를 통해 class 파일들을 JVM으로 로딩합니다.
3. 로딩된 class 파일들을 Execution engine을 통해 해석됩니다.
4. 해석된 바이트코드는 Runtime Data Areas에 배치되어 실질적인 수행이 이루어집니다.
<br>
<br>
</details>

<details>
<summary>GC(garbage collection)</summary>
<br>
GC는 힙 영역에서 사용하지 않는 객체들을 제거하는 작업을 총칭합니다.
이 객체를 제거하는 작업이 필요한 이유는 자바는 개발자가 메모리를 직접 해체해줄 수 없는 언어이기 때문입니다.
따라서 객체를 사용하고 제거하는 기능이 필요하게 됩니다.
<br>
<br>
</details>

<details>
<summary>제네릭(generic)</summary>
<br>
제네릭은 자바에서 타입(데이터 형식)을 파라미터화하여 코드의 재사용성,타입 안정성, 유지 보수성을 향상시키는 기능입니다.
<br>
<br>
</details>

<details>
<summary>어노테이션(annotation)</summary>
<br>
어떤 코드에 메타정보를 추가하는 용도로 사용됩니다.
예를 들어, 컴파일러에게 추가 정보를 제공하거나, 특정 도구가 해당 메타정보를 사용하여 코드를 처리하는데 도움을 줍니다.
<br>
<br>
</details>

<details>
<summary>오버라이딩(overriding) vs 오버로딩(overloading)</summary>
<br>
오버라이딩은 상속 관계에서 부모 클래스의 메서드를 자식 클래스에서 재정의하는 것입니다.
오버로딩은 하나의 클래스 내에서 동일한 이름의 메서드를 여러 번 정의하는 것입니다.
<br>
<br>
</details>

<details>
<summary>인테페이스(interface) vs 추상클래스(abstract class)</summary>
<br>
추상클래스는 객체의 추상적인 상위 개념으로 공통된 개념을 표현할 때 사용합니다.
단일 상속만 가능하며, 추상클래스를 상속하는 집합간에는 연관관계가 있습니다.
인터페이스는 구현 객체가 같은 동작을 한다는 것을 보장하기 위해 사용합니다. 다중 상속이 가능합니다. 인터페이스를 구현하는 집합간에는 관계가 없을 수 있습니다.
<br>
<br>
</details>

<details>
<summary>객체(instance) vs 클래스(class)</summary>
<br>
객체는 구별 가능한 식별자, 특징적인 행동, 변경 가능한 상태를 가집니다. 인스턴스들을 통칭하는 용도로 사용합니다.
클래스는 객체를 정의하는 틀 또는 설계도와 같은 의미로 사용됩니다.
<br>
<br>
</details>

<details>
<summary>정적(static)</summary>
<br>
객체 지향 프로그래밍에서 클래스에 속한 멤버(변수, 메서드 등)에 대한 특성을 정의하는 키워드입니다.
static이 붙은 멤버는 객체마다 별도로 존재하는 것이 아니라, 클래스가 로드될 때 한 번만 메모리에 할당되어 모든 객체에서 공유됩니다.
<br>
<br>
</details>

<details>
<summary>기본형(primitive type) vs 참조형(reference type)</summary>
<br>
기본형은 값 자체를 메모리 영역의 스택에 저장하고 참조형은 메모리 영역의 힙에 객체 데이터를 저장하고 스택에는 주소값을 저장한다.

기본형: byte(1), short(2), int(4), long(8), float(4), double(8), char(2), boolean(1)

참조형: class, interface, array, enum, String, Wrapper class(Character, Integer, Double ~), Collection framework(List, Map, Set ~) 
<br>
<br>
</details>

<details>
<summary>접근 제어자(access modifier)</summary>
<br>
접근 제어자를 사용하는 이유는 클래스,변수,메서드 등에 대한 접근 범위를 제한하는 키워드이고 코드의 캡슐화를 강화하고, 보안 및 재사용성을 높이기 위해 사용됩니다.

default: 같은 패키지 내에서만 접근 가능

public: 모든 클래스에서 접근 가능

private: 같은 클래스 내에서만 접근 가능

protected: 같은 패키지와 상속받은 자식 클래스에서 접근 가능
<br>
<br>
</details>

<details>
<summary>컬렉션 프레임워크(collection framework)</summary>
<br>
Java Collection은 널리 알려져 있는 자료구조를 바탕으로 객체, 데이터들을 효율적으로 관리할 수 있는 자료구조들이 있는 라이브러리를 컬렉션 프레임워크라고 합니다.
List, Set은 Collection 인터페이스를 상속받지만, Map 인터페이스는 구조상의 차이라 별도로 정의힙니다.
<br>
<br>
</details>

###### 데이터베이스
<details>
<summary>RDBMS vs NOSQL</summary>
  접히는 내용입니다.  
  여러 줄의 텍스트나 코드 블록도 넣을 수 있습니다.
</details>

##### Framework(프레임워크)
<details>
<summary>SpringBoot(스프링부트)</summary>
  접히는 내용입니다.  
  여러 줄의 텍스트나 코드 블록도 넣을 수 있습니다.
</details>

<details>
<summary>Network(네트워크)</summary>
  접히는 내용입니다.  
  여러 줄의 텍스트나 코드 블록도 넣을 수 있습니다.
</details>

<details>
<summary>Operation(운영체제)</summary>
  접히는 내용입니다.  
  여러 줄의 텍스트나 코드 블록도 넣을 수 있습니다.
</details>

<details>
<summary>Data Structure(자료구조)</summary>
  접히는 내용입니다.  
  여러 줄의 텍스트나 코드 블록도 넣을 수 있습니다.
</details>


## ETC(기타)