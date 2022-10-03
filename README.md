# csnote
면접을 위한 전공지식 CS노트의 레퍼지토리입니다. 
 - ebook의 경우 페이지번호가 단말기마다 다릅니다. 페이지의 기준은 인쇄본 1쇄를 기준으로 말씀을 드립니다. 
 - 현재 4쇄까지 아래의 내용이 모두 반영되어있습니다. 추후 반영되는 사항은 [new] 키워드를 붙입니다.

# 오탈자 및 추가 및 변경 사항
1쇄와는 달리 달라진 점이 있습니다. 해당 부분은 다음과 같습니다. 

## 143, 148, 150, 182페이지  
> before

SDD

> after

SSD


## 17페이지 
> before

싱글톤패턴은 하나의 클래스에 오직 하나의 인스턴스만 가지는 패턴입니다. 보통 데이터베이스 연결모듈에 많이 사용합니다.

> after

싱글톤 패턴(singleton pattern)은 하나의 클래스에 오직 하나의 인스턴스만 가지는 패턴입니다. 하나의 클래스를 기반으로 여러 개의 개별적인 인스턴스를 만들 수 있지만 그렇게 하지 않고 하나의 클래스를 기반으로 단 하나의 인스턴스를 만들어 이를 기반으로 로직을 만드는데 쓰이며 보통 데이터베이스 연결모듈에 많이 사용합니다.

## 18페이지 
> before

앞의 코드에서 볼 수 있듯이 obj와 obj2는 다른 인스턴스를 가집니다.  

> after

앞의 코드에서 볼 수 있듯이 obj와 obj2는 다른 인스턴스를 가집니다. 
이 또한 new Object라는 클래스에서 나온 단 하나의 인스턴스니 어느정도 싱글톤패턴이라 볼 수 있습니다만 실제 싱글톤패턴은 보통 다음과 같은 코드로 구성됩니다. 

## 20페이지 
> before

`public static synchronized Singleton getInstance()`

> after

`public static Singleton getInstance()` 

## 24페이지 설명 변경
> before

의존성 주입은 의존성 주입원칙을 지키며 만들어야 하며 원칙은 다음과 같습니다
 - 상위 모듈은 하위 모듈에서 어떠한 것도 가져오지 않아야 합니다. 둘 다 추상화에 의존해야 하며, 이때 추상화는 세부 사항에 의존하지 말아야 합니다. 

> after

의존성 주입 원칙

의존성 주입은 "상위 모듈은 하위 모듈에서 어떠한 것도 가져오지 않아야 합니다. 
또한 둘 다 추상화에 의존해야 하며, 이 때 추상화는 세부사항에 의존하지 말아야 합니다." 라는 의존성 주입원칙을 지켜주면서 만들어야 합니다. 

## 52페이지 설명 변경
> before

a와 b는 다른 모듈에서 사용할 수 있는 변수나 함수인 privat 범위를 ...(생략)

> after

a와 b는 다른 모듈에서 사용할 수 없는 변수나 함수이며 private 범위를 가집니다. c와 d는 다른 모듈에서 사용할 수 있는 변수나 함수이며 public 범위를 가집니다. 참고로 위와 같은 노출모듈패턴을 기반으로 만든 자바스크립트 모듈 방식으로는 CJS(CommonJS) 모듈 방식이 있습니다. 


## 68페이지 설명 변경
> before

네트워크란 노드(node)와 링크(link)가 서로 연결되어 있거나 연결되어 있지 않은 집합체를 의미합니다. 

> after

네트워크란 노드(node)와 링크(link)가 서로 연결되어 있으며 리소스를 공유하는 집합을 의미합니다.
 


## 82페이지 설명 변경

> before

전송(transport) 계층은 송신자와 수신자를 연결하는 ... (생략)

> after

전송(transport) 계층은 송신자와 수신자를 연결하는 통신 서비스를 제공하며 연결 지향 데이터 스트림 지원, 신뢰성, 흐름 제어를 제공할 수 있으며 애플리케이션과 인터넷 계층 사이의 데이터가 전달될 때 중계 역할을 합니다. 대표적으로 TCP와 UDP가 있습니다. 

## 99페이지 오타
> before

로드밸런서로는 L7 스위치뿐만 아니라.. (생략)

> after

로드밸런서로는 L7 스위치뿐만 아니라 L4스위치도 있습니다. L4 스위치는 전송 계층

## 106페이지 설명 변경
> before

IP주소를 통해 통신하는 과정을 홉바이홉... (생략)


> after

IP주소를 통해 통신하는 과정을 홉바이홉통신이라고 합니다. 
여기서 홉(hop)이란 영어 뜻 자체로는 건너뛰는 모습을 의미합니다. 이는 통신망에서 각 패킷이 여러 개의 라우터를 건너가는 모습을 비유적으로 표현한 것입니다. 앞의 그림처럼 수많은 서브네트워크 안에 있는 라우터의 라우팅테이블의 IP를 기반으로 패킷을 전달하고 또 전달해나가며 라우팅을 수행하며 최종 목적지까지 패킷을 전달합니다.
## 109페이지 오타
> before

클래스 기반 할당 방식(CIDR)

> after

클래스 기반 할당 방식(classful network addressing)

## 117페이지 설명 추가 
> before

하지만 Base64 문자열로 변환할 경우... (생략)

> after

하지만 Base64 문자열로 변환할 경우 37% 정도 크기가 더 커지는 단점이 있습니다. 자세한 설명은 필자가 만든 영상을 참고하세요. 
 - https://youtu.be/-bxZyTfhoH0 

## 132페이지 Q&A 1개추가  

www.naver.com을 주소창에 입력하면 어떻게 될까요? 

https://www.youtube.com/watch?v=5MM8NDzWHdE 에 영상을 올려놨습니다. 

## 137페이지 오타 및 설명변경
> before

1은 유저모드라고 설정되며, 유저모드일 경우에는 시스템콜을 못하게 막아서 한정된 일만 가능하게 합니다.

> after

1은 유저모드라고 설정됩니다. 

## 143페이지 오타

> before

보조기억장치 : HDD, SDD를 일컬으며 휘발성, 속도낮음, 기억 용량이 많습니다. 


> after

보조기억장치 : HDD, SDD를 일컬으며 비휘발성, 속도낮음, 기억 용량이 많습니다. 

## 149페이지 설명 변경
> before

스와핑

만약 가상 메모리에는 존재하지만 실제 메모리인... (생략)

> after

스와핑

만약 가상 메모리에는 존재하지만 실제 메모리인 RAM에는 현재 없는 데이터나 코드에 접근할 경우 페이지 폴트가 발생합니다. 이 때 메모리의 당장 사용하지 않는 영역을 하드디스크로 옮기고 하드디스크의 일부분을 마치 메모리처럼 불러와쓰는 것을 스와핑(swapping)이라고 합니다. 이를 통해 마치 페이지폴트가 일어나지 않은 것처럼 만듭니다.

페이지 폴트 

페이지 폴트(page fault)란 프로세스의 주소 공간에는 존재하지만 지금 이 컴퓨터의 RAM에는 없는 데이터에 접근했을 경우에 발생합니다. 페이지폴트와 그로 인한 스와핑은 다음 과정으로 이루어집니다.

## 151 페이지 설명 변경
> before

PFF(Page Fault Frequency)는 페이지 폴트 빈도를 조절하는 방법으로 상한선과 하한선을 만드는 방법입니다. 만약 상한선에 도달한다면 페이지를 늘리고 하한선에 도달한다면 페이지를 줄이는 것이죠. 

> after

PFF(Page Fault Frequency)는 페이지 폴트 빈도를 조절하는 방법으로 상한선과 하한선을 만드는 방법입니다. 만약 상한선에 도달한다면 프레임을 늘리고 하한선에 도달한다면 프레임을 줄이는 것이죠.  


## 164페이지 설명 변경
> before

프로세스 스케줄링 상태 : '준비', .... (생략)

> after

프로세스 스케줄링 상태 : '준비', '일시중단' 등 프로세스가 CPU에 대한 소유권을 얻은 이후의 프로세스의 상태

## 173페이지 설명 변경

> before

공유자원에 접근할 때 순서 등의 이유로 ... (생략)

> after

임계 영역

임계영역(critical section)은 둘 이상의 프로세스, 스레드가 공유자원에 접근할 때 순서 등의 이유로 결과가 달라지는 코드 영역을 말합니다. 
임계 영역을 해결하기 위한 방법은 크게 뮤텍스, 세마포어, 모니터 세 가지가 있으며, 이 방법 모두 상호 배제, 한정 대기, 융통성이란 조건을 만족합니다. 
이 방법에 토대가 되는 메커니즘은 잠금(lock)입니다. 예를 들어 임계 영역을 화장실이라고 가정하면 화장실에 A라는 사람이 들어간 다음 문을 잠급니다. 그리고 다음 사람이 이를 기다리다 A가 나오면 화장실을 쓰는 방법입니다.

## 174페이지 설명 변경
> before

뮤텍스(mutext)는 공유 자원을 ... (생략)

> after

뮤텍스

뮤텍스(mutex)는 프로세스나 스레드가 공유 자원을 lock()을 통해 잠금 설정하고 사용한 후에는 unlock()을 통해 잠금해제하는 객체입니다. 잠금이 설정되면 다른 프로세스나 스레드는 잠긴 코드 영역에 접근할 수 없고 해제는 그와 반대입니다. 또한 뮤텍스는 잠금 또는 잠금해제라는 상태만을 가집니다. 

## 175페이지 설명 변경
> before

프로세스가 공유 자원에 접근하면... (생략)

> after

프로세스나 스레드가 공유자원에 접근하면 세마포어에서 wait() 작업을 수행하고 프로세스나 스레드가 공유자원을 해제하면 세마포어에서 signal() 작업을 수행합니다. 세마포어에는 조건 변수가 없고 프로세스나 스레드가 세마포어 값을 수정할 때 다른 프로세스나 스레드는 동시에 세마포어 값을 수정할 수 없습니다. 

바이너리 세마포어

바이너리 세마포어는 0과 1의 두가지 값만 가질 수 있는 세마포어입니다. 구현의 유사성으로 인해 뮤텍스는 바이너리 세마포어라고 할 수 있지만 엄밀히 말하면 뮤텍스는 잠금을 기반으로 상호배제가 일어나는 "잠금 메커니즘"이고, 세마포어는 신호를 기반으로 상호 배제가 일어나는 "신호 메커니즘"입니다. 
여기서 신호 메커니즘은 휴대폰에서 노래를 듣다가 친구로부터 전화가 오면 노래가 중지되고 통화 처리 작업에 관한 인터페이스가 등장하는 것을 상상하면 됩니다.


## 180페이지 설명 변경[

> before

라운드 로빈(RR, Round Robin)은 현대 컴퓨터가 쓰는 스케줄링인 우선순위 스케줄링
(priority scheduling)의 일종으로 각 프로세스는 동일한 할당 시간을 주고 그 시간 안에 끝
나지 않으면 다시 준비 큐(ready queue)의 뒤로 가는 알고리즘입니다.

> after

라운드 로빈(RR, Round Robin)은 현대 컴퓨터가 쓰는 선점형 알고리즘 스케줄링 방법으로 각 프로세스는 동일한 할당 시간을 주고 그 시간 안에 끝
나지 않으면 다시 준비 큐(ready queue)의 뒤로 가는 알고리즘입니다.
 


## 181페이지 오타  

RB > RR

## 182페이지 오타
> before

HDD, SDD를 일컬으며 휘발성,

> after

HDD, SDD를 일컬으며 비휘발성, 

## 186페이지 오타
> before

NoSQL 데이터베이스의 구조는... (생략)

> after

MongoDB 데이터베이스의 구조는 도큐먼트 - 컬렉션 - 데이터베이스로 이루어져 있습니다.

## 191페이지 설명 변경
> before

그렇기 때문에 지정된 형태에 ... (생략)

> after

그렇기 때문에 CHAR의 경우 유동적이지 않은 길이를 가지 데이터의 경우 효율적이며 유동적인 길이를 가진 데이터는 VARCHAR로 저장하는 것이 좋습니다.
 


## 210페이지 오타[new]
 > BEFORE

### REPEATABLE_READ
REPEATABLE_READ는 하나의 트랜잭션이 수정한 행을 다른 트랜잭션이 수정할 수 없
도록 막아주지만 새로운 행을 추가하는 것은 막지 않습니다. 따라서 이후에 추가된 행이
발견될 수도 있습니다. 
 

### READ_COMMITTED
READ_COMMITTED 는 가장 많이 사용되는 격리 수준이며 MySQL8.0, PostgreSQL,
SQL Server, 오라클에서 기본값으로 설정되어 있습니다. READ UNCOMMITTED 와
는 달리 다른 트랜잭션이 커밋하지 않은 정보는 읽을 수 없습니다. 즉, 커밋 완료된 데이
터에 대해서만 조회를 허용합니다.
하지만 어떤 트랜잭션이 접근한 행을 다른 트랜잭션이 수정할 수 있습니다. 예를 들어 트
랜잭션 A가 수정한 행을 트랜잭션 B가 수정할 수도 있습니다. 이 때문에 트랜잭션 A가 같
은 행을 다시 읽을 때 다른 내용이 발견될 수 있습니다.

 > AFTER

### REPEATABLE_READ
REPEATABLE_READ는 하나의 트랜잭션이 수정한 행을 다른 트랜잭션이 수정할 수 없
도록 막아주지만 새로운 행을 추가하는 것은 막지 않습니다. 따라서 이후에 추가된 행이
발견될 수도 있습니다.이는 MySQL8.0의 innoDB 기본값이기도 합니다.

### READ_COMMITTED
READ_COMMITTED 는 가장 많이 사용되는 격리 수준이며 PostgreSQL,
SQL Server, 오라클에서 기본값으로 설정되어 있습니다. READ UNCOMMITTED 와
는 달리 다른 트랜잭션이 커밋하지 않은 정보는 읽을 수 없습니다. 즉, 커밋 완료된 데이
터에 대해서만 조회를 허용합니다.
하지만 어떤 트랜잭션이 접근한 행을 다른 트랜잭션이 수정할 수 있습니다. 예를 들어 트
랜잭션 A가 수정한 행을 트랜잭션 B가 수정할 수도 있습니다. 이 때문에 트랜잭션 A가 같
은 행을 다시 읽을 때 다른 내용이 발견될 수 있습니다. 
