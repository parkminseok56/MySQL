## DAO (Data Access Object)

- 데이터베이스나 다른 데이터 저장소에서 데이터를 조작하고 접근하기 위한 객체를 말합니다.

이러한 DAO 객체를 만들 때 getter, setter, 그리고 toString 메서드는 다음과 같은 역할을 합니다:

- Getter와 Setter 메서드:

  - Getter 메서드
    
    DAO 클래스는 데이터를 조회하거나 가져오는 역할을 합니다.
    
    Getter 메서드는 DAO 객체가 가지고 있는 데이터를 외부에서 읽을 수 있도록 해줍니다.
    
     예를 들어, 데이터베이스 레코드를 조회한 결과를 DAO 객체로 가져올 때 해당 데이터를 외부에서 확인하기 위해 Getter 메서드를 사용합니다.
  
  - Setter 메서드
    
    DAO 객체는 데이터를 수정하거나 저장하는 역할도 합니다.
    
    Setter 메서드는 외부에서 DAO 객체에 데이터를 설정하거나 업데이트하기 위해 사용됩니다.
  
- toString 메서드:
  
  toString 메서드는 객체의 문자열 표현을 반환합니다.
  
  주로 객체의 정보를 편리하게 출력하기 위해 사용됩니다.
  
  DAO 객체의 경우, 데이터베이스의 특정 레코드나 데이터를 표현하는 데 사용할 수 있습니다.
  
  -------------------------------------------------------------------------------------------------------------------------

  이를 통해 디버깅이나 로깅 시에 객체의 내용을 쉽게 확인할 수 있습니다.
  
세 가지 메서드의 주요 역할은 다음과 같이 요약할 수 있습니다:

Getter 메서드: 데이터 조회를 위한 정보 제공
Setter 메서드: 데이터 수정 또는 설정을 위한 정보 입력
toString 메서드: 객체의 정보를 문자열로 표현하여 출력 가능한 형태로 제공

## DAO와 Repository의 차이점

- DAO (Data Access Object):
  
    DAO는 데이터베이스나 다른 영구 저장소에서 데이터를 조작하고 접근하기 위한 객체를 말합니다.
    
    DAO는 데이터베이스와의 접근을 추상화하여 비즈니스 로직과 데이터 접근을 분리하는 역할을 합니다.
    
    주로 JDBC나 JPA와 같은 데이터베이스 접근 기술과 함께 사용됩니다.
    
    DAO 패턴은 데이터베이스의 CRUD (Create, Read, Update, Delete) 작업을 수행하는 메서드를 제공하며, 데이터베이스와의 연결, 트랜잭션 관리 등의 로직을 캡슐화합니다.

- Repository:
  
     Repository 역시 DAO와 유사한 개념으로 데이터베이스나 영구 저장소와 상호작용하는 객체를 말합니다.
    
     Repository는 주로 스프링 프레임워크에서 사용되며, JPA와 함께 사용될 때 많이 봅니다. 
     
     스프링의 JpaRepository와 같은 인터페이스를 사용하여 미리 정의된 메서드를 활용하여 데이터 조작을 간편하게 할 수 있습니다.
     
     Repository 역시 데이터 접근과 관련된 로직을 캡슐화하여 비즈니스 로직과 데이터 접근을 분리하는 역할을 합니다.
 
 -------------------------------------------------------------------------------------------------------------------------
 
따라서 DAO와 Repository는 비슷한 목적을 가지고 있으며, 데이터 접근 계층을 추상화하여 비즈니스 로직과 분리하는 데 사용됩니다.

하지만 DAO는 보다 일반적인 개념이며, Repository는 스프링 프레임워크에서 제공하는 데이터 접근 계층 관련 인터페이스를 가리키는 경우가 많습니다.

## DTO (Data Transfer Object)

데이터를 전송하거나 전달하기 위한 객체를 말합니다.

주로 데이터의 저장과 전송을 위해 사용되며, 데이터의 구조를 담고 있는 일종의 데이터 컨테이너입니다. 

DTO는 비즈니스 로직을 가지지 않으며, 주로 데이터의 표현과 전달에 관련된 역할을 수행합니다.

 ## DTO의 주요 특징과 역할

 - 데이터 전송
   - DTO는 서로 다른 계층 또는 시스템 간에 데이터를 전달하는 데 사용됩니다. 예를 들어, 클라이언트와 서버 간의 데이터 교환, 서비스 간의 데이터 전송 등에 활용됩니다.

- 데이터 구조 표현
  - DTO는 데이터의 구조를 표현하기 위해 사용됩니다. 데이터베이스의 특정 테이블 레코드, 외부 API의 응답 데이터 등의 데이터 구조를 정의하여 담을 수 있습니다.

- 비즈니스 로직 없음
  - DTO는 주로 데이터만을 담는 객체로, 비즈니스 로직을 가지지 않습니다. 데이터의 전송과 구조를 위한 용도로 사용되며, 로직은 서비스 또는 다른 컴포넌트에서 처리됩니다.

- 클래스 간 데이터 교환
  -  DTO는 자바의 클래스로 표현되며, 데이터의 교환을 위한 메서드나 기능을 가질 수 있습니다. 주로 멤버 변수와 그에 대한 getter, setter 메서드로 구성됩니다.

- 성능 및 네트워크 효율 향상
  -  데이터 전송 시에 필요한 데이터만을 선택적으로 전달함으로써, 데이터의 크기와 전송 시간을 최적화할 수 있습니다.

DTO는 주로 비즈니스 로직과 데이터 구조를 분리하여 코드의 가독성과 유지보수성을 향상시키는 데 사용됩니다. 주로 웹 애플리케이션에서 클라이언트와 서버 간의 데이터 통신을 위해 사용되며, 복잡한 데이터 변환 및 전달 시 유용합니다.
