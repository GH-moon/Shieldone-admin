
 .. index:: SSL, SSL VPN, Remote, Remote VPN, 인증서, CA Server, 원격접속 VPN, 지점간 SSL VPN
SSL Remote VPN
-------------------------------

 SSL VPN의 원격접속VPN 기능은 인터넷이 연결 된 곳이면 집이나 출장 중 언제,

 어디서나 SSL VPN Client를 이용하여 사무실에 있는 것처럼 모든 업무를 처리할 수 있습니다.

CA Server
^^^^^^^^^^^^^^^^^^^


 .. image:: images/3-20.png

1. '지역명' 필드에 지리적 위치를 영문으로 입력합니다.

2. '기관명'에 ShieldOne SIG가 운용중인 기관명을 영문으로 입력합니다.

3. 'E-mail' 필드에 사설 CA서버로 사용될 ShieldOne 장비의 영문이름을 입력합니다.

4. 모든 항목을 정의하고 나서 '확인' 버튼을 클릭하여 CA의 Server인증서를 생성합니다.



그룹 관리
^^^^^^^^^^^^^^^^^^^^^^^

 .. image:: images/3-21.png


 * SSL VPN을 통하여 접근할 때 가상의 IP대역을 설정 해 주는 곳 입니다.

 * 이 화면은 등록 후에는 수정이 불가능 하므로 주의 해야 합니다.

 * B 클래스로 입력합니다.


 .. image:: images/3-22.png


 * 그룹명 필드에 사용할 이름을 입력합니다.

 * 사용자수 필드에 해당 그룹의 최대 사용자 수를 입력합니다.

 * 인증서 리스트 박스에서 생성 할 그룹이 사용 할 인증서를 선택합니다. 이 인증서는 CA Client 메뉴에서 생성한 Client 인증서 목록입니다.


원격접속 VPN
^^^^^^^^^^^^^^^^^^^^^^^^^^^


 .. image:: images/3-23.png



+----------------------+---------------------------------------------------------------------------------------------------+
| 프로토콜             | TCP, UDP 선택을 할 수 있습니다.                                                                   |
+----------------------+---------------------------------------------------------------------------------------------------+
| 접속포트             | 사용할 포트를 설정 할 수 있습니다.                                                                |
+----------------------+---------------------------------------------------------------------------------------------------+
| 기본 할당 IP POOL    | 그룹관리에서 만든 그룹 중 하나를 선택합니다.                                                      |
+----------------------+---------------------------------------------------------------------------------------------------+
| 내부 Subnet          | 내부에서 사용하고 있는 IP 대역을 입력 합니다.                                                     |
|                      |                                                                                                   |
|                      | Ex) 192.168.1.0/24 그리고 ,(콤마)를 사용해 여러대역 등록 가능합니다.                              |
+----------------------+---------------------------------------------------------------------------------------------------+
| 내부 DNS             | 내부에서 사용하고 있는 DNS 주소를 입력합니다.                                                     |
+----------------------+---------------------------------------------------------------------------------------------------+
| VPN G/W 사용         | 원격에 있는 사용자가 인터넷을 사용하고자 할 때 연결된 VPN을 통 해서                               |
|                      |                                                                                                   |
|                      | ShieldOne SIG을 거쳐서 나가도록 하고자 하다면 사용함을 선택합니다.                                |
|                      |                                                                                                   |
|                      | 위에 설정한 내부 Subnet을 갈 때만 VPN을 사용하도록 한다면 사용안함을 선택합니다.                  |
+----------------------+---------------------------------------------------------------------------------------------------+
| MAP IP               | 방화벽에서 NAT 되는 공인 IP 설정합니다.                                                           |
|                      |                                                                                                   |
|                      | Ex) WAN1 IP 218.38.5.53                                                                           |
+----------------------+---------------------------------------------------------------------------------------------------+
| Time out             | 인증 유효성 검사 시간을 설정합니다. Default는 60초로 되어있습니다.                                |
+----------------------+---------------------------------------------------------------------------------------------------+
| 추가인증방법         | 추가로 인증할 방법을 설정 합니다.                                                                 |
|                      |                                                                                                   |
|                      | Ex) 사용자 인증, RADIUS 인증, LDAP 인증                                                           |
+----------------------+---------------------------------------------------------------------------------------------------+
| 사용자 인증          | ShieldOne UTM 시스템상에 사용자 인증DB를 사용합니다.                                              |
+----------------------+---------------------------------------------------------------------------------------------------+
| RADIUS인증           | 별도의 RADIUS인증서버가 있을 때 선택하고 RADIUS서버의 IP주소와 공유키를 정의합니다.               |
+----------------------+---------------------------------------------------------------------------------------------------+


CA Client
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

 SSL VPN Client 접속 인증서 파일을 생성 하는 곳입니다.


 .. image:: images/3-46.png


 * 추가 버튼을 클릭하면 인증서를 생성 할 수 있습니다.


 .. image:: images/3-47.png


 * 사용자 이름 설정은 인증서의 이름을 설정하는 부분입니다.

 * 패스워드는 인증서의 패스워드를 설정 하는 부분입니다.


사용자 관리
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

 추가인증방법에서 사용자 인증을 사용할 때 사용자들을 생성/관리 하는 메뉴입니다.


 .. image:: images/3-48.png


 * ID 필드에 사용자 ID를 등록합니다.

 * 그룹 리스트 박스에서 앞서 사용자 그룹에서 설정한 그룹들 중 선택합니다.

 * 사용자의 패스워드를 입력합니다.

 * 사용자에 대한 설명을 입력합니다.

 * 사용자는 이 ID와 패스워드로 접속하면 됩니다.

 * 인증서는 모두 같은 Client 인증서 사용 가능합니다.


SSL 지점간 VPN
-----------------------------
 SSL VPN의 지점간 VPN 기능은 IPSec VPN을 I.SP(인터넷 서비스 제공자) 또는 국제망의 정책으로 사용할 수 없거나, 제한적인 경우 TCP/UDP 등의 일반 인터넷 서비스 포트를 이용하여 원격사업장과 인터넷을 통하여 암호화된 안전한 통신 방안을 제공합니다. 또한 이동 사용자의 인터넷을 통한 안전한 원격접속 채널을 제공함으로써 언제 어디서나 정보를 공유할 수 있는 환경을 제공합니다.


 .. image:: images/3-49.png


 지점간 VPN 상태를 볼 수 있습니다 추가 버튼을 클릭하면 지점간 VPN 설정을 할 수 있습니다.


 .. image:: images/3-49-1.png


 * Static Key : 한쪽에서 키를 생성하여 하나의 키를 가지고 연결 Staic Key 버튼을 누르면 Key 를 가져올 Host를 입력하는 메뉴가 나옵니다. 어느 한쪽에 지점간 VPN 설정이 되어 있어야만 키가 생성되어 가져 올 수 있습니다.



 .. image:: images/3-50.png

+--------------------------+-------------------------------------------------------------------------------------------------+
| 장치 ID                  | 장치의 ID를 입력하는 곳 입니다. 숫자만 입력 가능합니다.                                         |
+--------------------------+-------------------------------------------------------------------------------------------------+
| 프로토콜                 | TCP_SERVER, UDP, TCP_Client 를 선택 할 수 있습니다.                                             |
+--------------------------+-------------------------------------------------------------------------------------------------+
| 연결 IP 또는 도메인명    | 로컬 부분에는 외부로 나가는 장비의 포트 IP를 설정합니다.                                        |
|                          |                                                                                                 |
|                          | Ex) WAN1 IP 218.38.5.53                                                                         |
|                          |                                                                                                 |
|                          | 원격 부분에는 연결할 장비의 외부로 나가는 포트 IP를 입력 합니다.                                |
|                          |                                                                                                 |
|                          | Ex) WAN1 IP 218.38.6.53                                                                         |
+--------------------------+-------------------------------------------------------------------------------------------------+
| 터널 IP                  | 터널 IP로 사용할 IP를 입력합니다. 주로 30bit 서브넷을 사용합니다.                               |
|                          |                                                                                                 |
|                          | Ex) 10.20.0.1/30                                                                                |
+--------------------------+-------------------------------------------------------------------------------------------------+
| 활성화 여부              | 활성화를 하려면 활성화 부분을 체크합니다.                                                       |
+--------------------------+-------------------------------------------------------------------------------------------------+
| 메모                     | VPN에 대한 설명을 적을 수 있습니다. 생략해도 활성화 가능합니다.                                 |
+--------------------------+-------------------------------------------------------------------------------------------------+
