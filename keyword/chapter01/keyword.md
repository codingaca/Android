- 플랫폼
    
    📍 소프트웨어 플랫폼
    
    - PC용 소프트웨어나 애플리케이션이 실행될 수 있는 토대 (= 운영체제)
    - 애플리케이션이 잘 실행될 수 있는 환경을 제공
    - PC → 윈도우, 리눅스, 맥OS 등
    - 스마트폰, 태블릿→ ⭐**Android**⭐, iOS 등
    
    📍 하드웨어 플랫폼
    
    - 여기서 하드웨어 = 컴퓨터 하드웨어가 아니라 자동차/전자제품 등 일반적인 산업 제품
    - 공통으로 들어가는 표준화된 핵심 부분. 핵심부품들의 묶음이 OS의 역할
    
    📍 서비스 플랫폼
    
    - 포털사이트, SNS 등
    - 사전, 블로그, 쇼핑, 채팅, 게임, 광고등 다양한 서비스를 활용할 수 있는 환경
    - 여러 소프트웨어들이 이러한 서비스 플랫폼을 운영체제로 삼는 느낌?
    
- Android OS
    - 정의: 스마트폰, 태블릿 PC 같은 터치스크린 모바일 장치 용으로 디자인된 운영 체제이자 수정된 **리눅스 커널** 버전을 비롯한 오픈 소스 소프트웨어에 기반을 둔 모바일 운영 체제
    - 특징:
        1. 개방형 소스 플랫폼이기 때문에 개발자가 소스코드에 접근하여 운영체제를 커스터마이징하거나 확장할 수 있다 **= 고유의 기기와 애플리케이션을 개발할 수 있다!**
        2. 플레이스토어를 통해 애플리케이션 설치가 가능하다. 즉 **유저는 다양한 앱을 활용하여 기기를 맞춤화할 수 있다!**
        3. 스마트폰 외에도 태블릿, 웨어러블 디바이스, 자동차 시스템등 **다양한 기기에서 작동시킬 수 있다**.
        4. **구글의 서비스**와 통합할 수 있다. Gmail, Google Drive, Google Maps등
        5. 안드로이드 개발을 위한 다양한 개발자 도구와 자원이 제공된다. ex) **⭐Android Studio⭐**

- Android의 Architecture
    - 안드로이드의 권장 아키텍쳐는 무엇일까요?
        
        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/f1912130-0409-4e90-a90f-6091ae253e73/bcb98a89-0182-4d4b-ab3e-4fd7c5728c74/image.png)
        
        📍 UI 레이어 
        
        - 역할 - 화면에 애플리케이션 데이터를 표시. 사용자 상호작용 또는 외부 입력으로 인해 데이터가 변할 때마다 변경사항을 반역하도록 UI가 업데이트 되어야함
        - 화면에 데이터를 렌더링 하는 **UI elements**, 데이터를 보유하고 이를 UI에 노출하며 로직을 처리하는 **State holders** (ex. ViewModel class) 로 구성된다
        
        📍 데이터 레이어
        
        - 비즈니스 로직이 포함되어 있음
        - 비즈니스 로직이란?
            
            👉 앱의 데이터 생성, 저장, 변경 방식을 결정하는 규칙으로 구성됨
            
        - 앱에서 처리하는 다양한 유형의 데이터별로  Repository 클래스를 만들어야함 (ex. 영화 관련 데이터라면 MoviesRepository 클래스, 결제 관련 데이터라면 PaymentsRepository 클래스)
        
        📍 도메인 레이어 (optional)
        
        - 복잡한 비즈니스 로직이나 여러 ViewModel에서 재사용되는 간단한 비즈니스 로직의 캡슐화를 담당
        
    - 안드로이드 아키텍쳐 컴포넌트 (AAC)는 무엇일까요?
        
        ⭐ 테스트와 유지보수가 쉬운 앱을 디자인할 수 있도록 돕는 라이브러리의 모음
        
        - DataBinding
        - Lifecycle
        - Navigation
        - Room
        - Paging
        - WorkManager
        - Livedata
        - ViewModel
        
- Manifest의 주요 속성
    
    📍 <Manifest>
    
    - `AndroidManifest.xml` 파일의 루트
    - xmlns:android 및 package 속성 지정
    
    📍 <application>
    
    - 애플리케이션의 선언
    - 애플리케이션의 각 구성요소를 선언하는 하위 요소를 포함
    - **모든 구성요소에 영향**을 줄 수 있는 속성을 가짐
    
    📍 <activity>
    
    - 애플리케이션의 UI 요소를 구현하는 활동을 선언
    - **모든 활동**은 Manifest 파일의 <activity> 요소로 나타내야 함
    - 만약 **선언되지 않으면** 시스템에 **표시되지 않으며 실행도 불가**
    
    📍 <intent-filter>
    
    - 상위 구성요소의 기능, 즉 활동이나 서비스가 할 수 있는 작업과 수신기가 처리할 수 있는 브로드캐스트의 유형을 선언
    
    📍 <action>
    
    - <intent-filter> 요소에 <action> 요소가 하나 이상 포함되어야 함
    
    📍 <permission> 
    
    - 이 애플리케이션이나 다른 애플리케이션의 특정 구성요소 또는 기능에 대한 액세스를 제한하는 데 사용될 수 있는 보안 권한을 선언
    
    📍 <uses-permission>
    
    - 앱이 올바르게 작동하기 위해 사용자가 반드시 부여해야 하는 시스템 권한
    
    📍 <provider>
    
    - 앱에서 관리되는 데이터에 관해 구조화된 액세스를 제공
    
    📍 <receiver>
    
    - 다른 구성요소가 실행되고 있지 않을 때도 시스템이나 다른 애플리케이션에서 브로드캐스트하는 인텐트를 애플리케이션에서 수신 가능
    
    📍 <service>
    
    - activity와 달리 service는 UI가 없음
    - 오래 실행되는 백그라운드 작업이나 다른 앱에서 호출할 수 있는 리치 커뮤니케이션 API를 구현하는 데 사용

- Manifest의 4대 컴포넌트
    - 액티비티 (activity)  - 화면을 구성하는 컴포넌트
    - 서비스 (service) - 백그라운드에서 작업하는 컴포넌트
    - 콘텐츠 프로바이더 (Contents Provider) - 앱의 데이터를 가져오는 컴포넌트
    - 브로드캐스트 리시버 (Broadcast Receiver) - 안드로이드에서 발생하는 이벤트가 발생할 때 실행되는 컴포넌트

- Intent
    - Intent의 역할은 무엇일까요?
        
        👉 어플리케이션 구성요소(컴포넌트) 간에 작업 수행을 위한 정보를 전달하는 역할
        
    - 명시적 Intent와 암시적 Intent의 차이는 무엇일까요?
        
        📍명시적 Intent : 인텐트에서 클래스 객체나 컴포넌트 이름을 지정하여 **호출할 대상을 확실히 알 수 있는 경우**에 사용.  → 주로 앱 내부에서 사용
        
        📍 암시적 Intent : 인텐트의 액션과 데이터를 지정하긴 했지만, **호출할 대상이 달라질 수 있는 경우**에 사용
        
- Android Layout
    1. TextView : 화면에 텍스트 표시
    2. Button : 클릭하여 작업을 수행하는 ui 요소
    3. ImageView : 사진을 표시
    4. RecyclerView : 한 화면에 표시할 수 없는 많은 데이터를 스크롤 가능한 리스트로 표시해주는 위젯
    5. ScrollView : 내용의 높이가 실제 화면의 높이보다 클 때 화면을 스크롤할 수 있게 해줌
    6. NestedScrollView : 한 화면에서 여러 개의 스크롤을 사용할 때 사용
    7. BottomNavigationView : 화면 밑에 있는 네비게이션 역할을 하는 버튼 모
    8. TabLayout : 안드로이드에서 탭으로 구분하는 화면에서 탭 버튼을 배치하는 레이아
    9. FloatingActionButton : 화면 위에 떠있는 듯 보이는 버튼
    10. margin : 바깥 여백
    11. padding : 안쪽 여백
    12. chainStyle : chain이라는 이름처럼 여러 위젯을 한 그룹처럼 만들어주는 역할
    13. id 네이밍 : 뷰의 이름을 정의하는 속성. 코드에서 참조하기 위해서는 id가 꼭 필요하다.