# Network Basic2

## LAN

LAN은 Local Area Network로 좁은 지역에서의 네트워크다.

LAN은 개인이 책임지고 자유롭게 구축, 관리할 수 있다.

<br>

## WAN

WAN은 Wide Area Network로 넓은 지역에서의 네트워크다.

떨어져 있는 LAN을 이어주기도 한다.

WAN은 나라의 허가를 받은 통신사업자가 구축, 관리한다.

<br>

## OSI 참조 모델

ISO가 데이터 통신의 규격과 프로토콜을 통일하고자 만든 모델이다.

데이터 통신을 여러 단계로 나누고, 각 단계의 프로토콜을 정의하고자 했다.

OSI 참조 모델은 7개의 계층으로 나뉜다.

<br>

<table>
    <tr>
        <td>제7계층</td>
        <td align=center>응용계층</td>
        <td>사용자에게 네트워크 서비스 제공</td>
        <td rowspan="3" align=center>내용 표현</td>
    </tr>
    <tr>
        <td>제6계층</td>
        <td align=center>표현계층</td>
        <td>데이터 형식 결정</td>
    </tr>
    <tr>
        <td>제5계층</td>
        <td align=center>세션계층</td>
        <td>데이터 송수신 순서 등을 관리</td>
    </tr>
    <tr>
        <td>제4계층</td>
        <td align=center>전송계층</td>
        <td>신뢰성이 높은 전송 시행</td>
        <td rowspan="2" align=center>전송물</td>
    </tr>
    <tr>
        <td>제3계층</td>
        <td align=center>네트워크계층</td>
        <td>전송 규칙과 수신처 결정</td>
    </tr>
    <tr>
        <td>제2계층</td>
        <td align=center>데이터링크계층</td>
        <td>인접기기 사이의 데이터 전송 제어</td>
        <td rowspan="2" align=center>전송</td>
    </tr>
    <tr>
        <td>제1계층</td>
        <td align=center>물리계층</td>
        <td>전기, 기계적인 부분의 전송 시행</td>
    </tr>
</table>

<br>

각 계층은 독립적이다.

각 계층에는 각각의 프로토콜이 존재한다.

1. 송신처에서는 7계층부터 1계층까지의 작업을 거쳐 송신한다.

2. 1계층에서 데이터의 물리적 통신이 이루어지고

3. 수신처에서는 1계층부터 7계층까지의 작업을 거쳐 수신한다.

<br>

## PDU

Protocol Data Unit으로 패킷이라 부르기도 한다.

보내고 싶은 데이터와 데이터 통신을 위한 데이터(제어 데이터)가 통합된 것이다.

송신측에서는 계층이 낮아지며 PDU에 각 계층의 제어데이터를 추가한다.

이를 캡슐화라 한다.

수신측에서는 계층이 높아지며 PDU에 각 계층의 제어데이터를 제거한다.

<br>

|계층|호칭|<center>내용<center>|
|:---:|:---:|:---|
|사용자|Data|송수신하는 데이터|
|5, 6, 7계층|Message|데이터를 통신용으로 변환한 것과 7계층 헤더|
|4계층|Segement<br>Datagram|메세지와 4계층 헤더|
|3계층|Datagram<br>(혹은) Packet|세그먼트, 데이터그램과 3계층 헤더|
|2계층|Frame|데이터그램과 2계층 헤더와 테일|
|1계층|신호|프레임을 전송매체로 운반하기 위한 신호로 변환|

<br>

## 인터페이스

인접한 계층 사이에는 상위계층의 프로토콜과 하위계층의 프로토콜을 사용할 수 있게 도와주는 인터페이스가 존재한다.

인터페이스는 중개역, 혹은 매개체의 역할을 한다.

컴퓨터와 통신매체의 매개체 역활을 하는 인터페이스가 있고,

인접한 계층의 프로토콜에서의 매개체 역할을 하는 인터페이스도 있다.

<br>

## 프로토콜군 Protocol Suite

각 계층마다 사용할 프로토콜과 인터페이스의 조합을 프로토콜군이라 한다.

이 프로토콜군이 같은 기기끼리 통신이 가능하다.

<br>

## 프로토콜

- 프로토콜은 헤더와 데이터를 결정한다.

  - 프로토콜에 따라 보내는 데이터의 방식이 다르며,

  - 프로토콜에 따라 붙이는 헤더가 다르다.

- 프로토콜은 데이터의 송수신 형식을 결정한다.

  - 프로토콜에 따라 송수신하는 데이터의 순서와 내용이 다르다.

<br>

## TCP/IP

IETF라는 단체에서 제정했다.

<br>

### TCP/IP 모델과 OSI 참조 모델의 비교

<table>
    <tr>
        <td colspan="2">TCP/IP 모델</td>
        <td colspan="2">OSI 참조 모델</td>
    </tr>
    <tr>
        <td rowspan="3">제4계층</td>
        <td rowspan="3">어플리케이션 계층</td>
        <td>제7계층</td>
        <td>응용 계층</td>
    </tr>
    <tr>
        <td>제6계층</td>
        <td>표현 계층</td>
    </tr>
    <tr>
        <td>제5계층</td>
        <td>세션 계층</td>
    </tr>
    <tr>
        <td>제3계층</td>
        <td>트랜스포트 계층</td>
        <td>제4계층</td>
        <td>전송 계층</td>
    </tr>
    <tr>
        <td>제2계층</td>
        <td>인터넷 계층</td>
        <td>제3계층</td>
        <td>네트워크 계층</td>
    </tr>
    <tr>
        <td rowspan="2">제1계층</td>
        <td rowspan="2">어플리케이션 계층</td>
        <td>제2계층</td>
        <td>데이터링크 계층</td>
    </tr>
    <tr>
        <td>제1계층</td>
        <td>물리 계층</td>
    </tr>
</table>

<br>

### TCP/IP 프로토콜군

<table>
    <tr>
        <td>제4계층</td>
        <td>어플리케이션 계층</td>
        <td>HTTP<br>FTP<br>SMTP 등</td>
    </tr>
    <tr>
        <td>제3계층</td>
        <td>트랜스포트 계층</td>
        <td>TCP<br>UDP</td>
    </tr>
    <tr>
        <td>제2계층</td>
        <td>인터넷 계층</td>
        <td>IP<br>ARP</td>
    </tr>
    <tr>
        <td>제1계층</td>
        <td>어플리케이션 계층</td>
        <td>PPP 등</td>
    </tr>
</table>

<br>

