## TCP / IP의 이해 

+ 네트워크는 서로 다른 기종의 컴퓨터로 구성되어 있어 각 네트워크 간에 공통적으로 사용할 수 있는 프로토콜의 필요성이 대두되었다.
+ 아예 따라 인터넷에서 컴퓨터 간의 통신이 가능하도록 표준화하여 채택한 통신규약이 바로 TCP /IP이다.
+ 네트워크와 네트워크를 연결하는 데 사용하는 프로토콜인 TCP / IP는 '전송 제어 프로토콜'과 '인터넷 프로토콜'을 의미한다.
+ 인터넷에서 사용하는 응용 프로그램은 대부분 이 TCP / IP 프로토콜을 이용하여 데이터를 교환한다.



#### 네트워크 접속 계층

+ TCP/IP에서는 하위 계층인 물리 계층과 데이터 링크 계층을 특별히 정의하지 않았으며, 단지 모든 표준 및 임의. 네트워크를 지원할 수 있도록 하고 있다.
+ 데이터 링크 계층의 역할을 하는 TCP/IP프로토콜에서느 이더넷, 802.11x,MAC/LLc 등이 있다.
+ 네트워크 접속 걔층의 송신 측 컴퓨터에서는 상위 계층에서 전달받은 페킷에 물리적 주소인 MAC 주소 정보가 있는 헤더를 추가하여 플레임을 만든 후 그 프레임을 하위 계층인 물리 계층에 전달한다.

#### 네트워크 계층

+ 네트워크 계층은 '인터넷 계층'이라고도 하며, 네트워크의 패킷 전송을 제어한다. 데이터를 전송할 때 경로는 네트워크 계층에서 선택하는데 , TCP/IP 프로토콜에는 IP와 ARP, ICMP,IGMP 가 있다.
+ TCP/IP 에서 가장 중요한 프로토콜 중 하나인 IP는 네트워크 주소 체계를 관리하고, 데이터그램을 정의하며, 전송에 필요한 경로를 결정한다.

![참고 자료](https://img1.daumcdn.net/thumb/R720x0.q80/?scode=mtistory2&fname=http%3A%2F%2Fcfile7.uf.tistory.com%2Fimage%2F275DA640585A100F2FD4F1)





#### 전송 계층

+ 전송 계층은 상위 계층에서 볼 때 두 호스트 간의 데이터 전송을 담당하는 계층으로, TCP와 UDP 프로토콜을 사용한다.
+ 전송 계층의 역할은 네트워크 양단의 송수신 호스트 간에 신뢰성 있는 전송 기능을 제공하는 것으로 ,OSI 참조 모델에서는 세션 계층의 일부와 전송 계층에 해당한다.
+ TCP/IP에는 시스템의 논리 주소와 포트가 있어 각 상위 계층의 프로세스를 연결하여 통신한다.



#### 응용 계층

+ TCP/IP 프로토콜의 범위는 응용 계층의 프로토콜까지 포함하는데, 해당 프롴토콜에는 FTP, SMT,SNMP 등이 있다.
+ TCP/IP 프로토콜을 이용한 응용 프로그램 중에서 사용자가 직접 사용하는 인터넷 메일 프로그램이나 웹브라우저 등을 응용 계층으로 분류할 수 있다.



-------

#### TCP/IP 주소의 구조 





+ #### 물리주소

  + 물리주소는 링크 주소 또는 통신망에서 정의된 노드의 주소, 이더넷 네트워크 인터페이스 카드 6바이트 주소 등을 말한다.

+ #### 인터넷 주소

  + 인터넷에서는 기존 물리 주소와는 별도록 각 호스트를 식별하 수 있는 유일한 주소를 지정해야 한다.

+ #### 포트 주소 

  + 수신지 컴퓨터까지 전송하려면 IP주소와 물리 주소가 필요하다.
  + 인터넷 통신의 최종 목적은 한 프로세스가 다른 프로세스와 통신할 수 있도록 하는 것이다.



-------



### IP(인터넷 프로토콜)



+ 인터넷에 연결된 모든 컴퓨터에는 고유의 주소가 부여되는데, 이를 IP주소 라고 한다.

  + 현재 사용하고 있는 IP주소 체계는 IP Ver 4이다.
  + IPwnthsms 8비트 크기의 필드 네 개를 모아서 구성한 32비트 논리 주소이다.
  + 한 바이트가 가질 수 있는 10진수는 0 ~ 255 이므로 , IP 주소의 값은 0.0.0.0 ~ 255.255.255.0 까지이다.

  

+ 일반 우편 주소를 시, 동, 번지 등으로 구분하는 것처럼 IP주소도 네트워크 주소와 호스트 주소로 구분한다.

  + 네트워크 주소는 전체 네트워크를 좀 더 작은 네트워크로 분활하여 각 호스트가 속한 네트워크를 대표한다.
  + 네트워크 주소는 8비트, 16비트, 24비트 크기로 분류한다.

  

  ----------

  

  #### 사설 주소

  

  + 공인 IP주소와 부족으로 외부 네트워크와 내부 네트워크 간에 라우터 같은 장비를 사용하여 연결할 때 모든 컴퓨터에 공인 IP를 주는 것을 대신하여 내부적으로 DHCP 를 통한 사설 IP배분으로 네트워크를 연결하는 것은 사설 IP주소 체계라고 한다.
  + 외부로 나갈때는 라우터에 연결되어 있는 공인 IP주소를 사용하여 나가고 정보가 들어올 때는 라우터가 다시 사설 IP에 맞게 배분하는 방식으로 사용

  

  

  #### IPv6

  + 현재 사용하고 IP 버전은 IPv4로 표현된다. IPv4 주소는 32비트로 구성되며 네트워크 ID와 호스트 ID 부분으로 나뉘어 있다.
  + 또한 2-level 주소 구조로 되어 있다.
  + IP는 네트워크 규모에 따라 세 가지 규모와 클래스에 멀티캐스트 클래스와 예약된 클래스를 합한 총 다섯 가지 클래스로 구성되어 있다.
  + IPv4주소는 산술적으로 주소를 43억 개 할당할 수 있지만 클래스 별 주소 분류 방식 때문에 사용하지 않는 주소가 많다.

  

  ##### 주소 체계

  

  

  ![주소체계](https://한국인터넷정보센터.한국/images/ip_as/imgipasSys05.gif)

  

  

  

  #### IPv4와 IPv6의 차이

  ![차이](https://img1.daumcdn.net/thumb/R800x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F2270873B5715D31315)

  

  + IPv4는 헤더의 길이가 고정되어 있어 헤더 길이 필드가 제거되고 서비스 유형 필드도 제거된다. 
  + 그 기능을 우선 순위와 흐름 레이블 필드가 대체한다.
  + 총 길이 필드 또한 제거되어 페이로드 길이 필드로 대체된다.
  + 식별, 플래그, 옵션 필드는 기본 헤더에서 제거되고, 이 필드는 확장 헤더에 포함된다.

  

  

------

### TCP(전송 제어 프로토콜)



TCP 세그먼트 헤더 구조

![헤더 구조](https://img1.daumcdn.net/thumb/R800x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F16756F4A501722E00B)



#### TCP 연결관리

+ 포트 번호만 사용하여 응용 프로그램을 식별하는 UDP 와는 달리 TCP는 연결을 사용하여 응용 프로그램을 식별한다.



#### 연결 설정(3-Way 핸드셰이킹)



![TCP 연결 성정 과정](https://lh3.googleusercontent.com/proxy/Ogs9Vn8jFiVNbL45CgZ9MC2Myn9t7wGYRh60X4c9PtKEpLcnRwon67gOjR2pHe7l5HXutsvWP_Cf-zSfebS6RgIRkw)