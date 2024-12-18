- Database (DB)
    - Database의 정의는 무엇일까요?
        - 데이터를 체계적으로 저장하고 관리하는 시스템. 여러 데이터를 빠르게 조회, 삽입, 수정, 삭제할 수 있도록 도움
    - Database는 어디서 주로 사용될까요?
        - 웹 서비스, 모바일 앱, IoT 기기 등 데이터를 저장하고 활용하는 모든 곳에서 사용됨
- Database Management System (DBMS)
    - DBMS란 무엇일까요?
        - 데이터를 효율적으로 관리하고 사용할 수 있도록 해주는 소프트웨어 시스템. 데이터의 저장, 조화, 수정, 삭제 등의 작업을 지원
    - 대표적인 DBMS는 무엇이 있을까요?
        - MySQL, PostgreSQL 등
    - 관계형 저장 방식은 무엇일까요?
        - 테이블 형태로 데이터를 저장하며, 데이터 간의 관계를 외래 키(foreign key) 등을 통해 표현
    - 관계형이 아닌 저장 방식에는 무엇이 있을까요?
        - 데이터를 JSON 형식, Key-Value 형식 등으로 저장하며, 관계형 제약이 적음. (e.g. MongoDB)
    - SQL이란 무엇일까요?
        1. DDL(Data Definition Language)
            - 데이터베이스 구조를 정의하는 언어 (`CREATE`, `DROP` 등)
        2. DML(Data Manipulation Language)
            - 데이터베이스에 저장된 데이터를 조작하는 언어 (`INSERT`, `UPDATE`, `DELETE`)
        3. ~~DCL(Data Control Language)~~
- Key-Value 구조
    - Java나 Kotlin에서 Key-Value를 사용하는 대표적인 자료 구조는 무엇인가요?
        - `HashMap`, `Map` 등
        - 해당 구조의 특징에는 무엇이 있을까요?
            - Key와 Value의 쌍으로 데이터를 저장하며, Key를 통해 빠르게 Value를 조회할 수 있음
    - 배열이나 리스트가 아닌 경우 하나의 Key에 여러 값을 넣을 수 있을까요?
        - 일반적으로 Key-Value 구조는 하나의 Key에 하나의 Value만 저장하지만, 값에 `List`나 `Set` 등을 저장하여 여러 값을 가질 수 있음
- SharedPreferences
    - 하나의 Key에 여러 값을 넣는 방법이 있을까요? (Hint: JSON)
        - JSON 형식으로 데이터를 직렬화하여 하나의 Key에 여러 값을 저장할 수 있음
- RoomDB
    - RoomDB는 무엇일까요?
        - 안드로이드에서 SQLite 데이터베이스를 편리하게 사용하도록 돕는 ORM 라이브러리
    - RoomDB 개발 이전에 사용하였고, 현재 RoomDB의 기반인 DBMS는 무엇일까요? → SQLite 기반
    - RoomDB는 어떤 방식으로 값을 저장할까요?
        - RoomDB는 테이블 구조로 데이터를 저장하며, DAO를 통해 데이터를 조작함
- Firebase
    - Firebase는 무엇이고 왜 사용할까요?
        - Google에서 제공하는 모바일 및 웹 애플리케이션 개발 플랫폼
    - Firebase에서 제공해주는 기능은 어떤 것이 있나요?
        - 실시간 데이터베이스, 사용자 인증, 클라우드 스토리지, 푸시 알림, 애널리틱스, 원격 설정, 앱 배포 등의 다양한 기능을 제공