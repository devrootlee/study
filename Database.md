###### Database

<details>
<summary>RDBMS</summary>
  접히는 내용입니다.  
  여러 줄의 텍스트나 코드 블록도 넣을 수 있습니다.
</details>


<details>
<summary>NoSQL</summary>
</details>

<details>
<summary>MongoDB</summary>
MongoDB는 고성능, 고가용성 및 쉬운 확장성을 제공하는 NoSQL, Document 지향 데이터베이스

데이터를 배열 및 중첩 Document 와 같은 복잡한 데이터 유형을 효율적으로 저장할 수 있는 유연한 JSON 과 유사한 형식인 BSON(Binary JSON)으로 저장합니다.

- 구조
  - Database
    - MongoDB 인스턴스는 여러 개의 데이터베이스를 호스트할 수 있으며 각각의 데이터베이스 컬렉션의 컨테이너로 작용
    - Database 는 디스크의 별도 파일에 데이터를 저장하며 각 데이터베이스에는 고유한 이름 공간 존재
  - Collection
    - MongoDB의 컬렉션은 Document 의 그룹이며 관계형 데이터베이스의 테이블 역할
    - 콜렌션은 데이터베이스 내에 존재하며 스키마를 강제하지 않으므로 컬렉션 내의 Document 는 다른 필드와 구조를 가지고 있습니다.
  - Document
    - MongoDB 에서의 기본 데이터 단위로 관계형 데이터베이스의 행의 역할
    - document 는 BSON 형식에 저장된 필드와 값 쌍으로 구성됩니다.
</details>