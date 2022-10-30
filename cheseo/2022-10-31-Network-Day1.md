# Chapter 1 : 컴퓨터네트워크 기본1
[컴퓨터네트워크 및 인터넷 역사](http://www.kocw.net/home/cview.do?cid=6166c077e545b736)

## 키워드
1. 네트워크 구조

### 1. 네트워크 구조
### 2. packet delay

#### network edge
네트워크 가장자리, 수많은 end system이 존재.

- client/server model: 클라이언트가 정보를 서버에 요청하고 받아오는 형식
- peer-to-peer model (P2P): 양방향 파일 전송 시스템

> 📘 end system?
>
> 네트워크의 끝에서 연결되어 있는 시스템들을 의미. 컴퓨터, 핸드폰, IoT 등이 있음

##### connection-oriented service
TCP protocol
- 안정적이고 순서대로 정보를 전달
- flow control: 송신 측과 수신 측의 데이터 처리 속도 차이를 해결하기 위한 기법
- congestion control: 네트워크가 혼잡할 때 데이터 전송 속도를 늦춤

UDP protocol
- 속도가 빠른 대신 안정적이지 않음

#### network core
네트워크 시스템의 중심, 데이터를 전송하는 핵심적인 역할

- circuit-switching: 하나의 회선을 할당 받아 데이터를 주고 받는 방식. 우선 통신을 연결하고 출발지부터 목적지까지 도착하는데 사용되는 회선 전체를 독점.
- packet-switching: 데이터를 패킷으로 쪼개서 전송하는 방식
- circuit-switching 방식은 한정된 유저만 네트워크를 사용할 수 있으나 packet-switching 방식은 많은 유저가 네트워크 사용 가능

#### access networks, physical media
네트워크에 접근하기 위한 네트워크. end system들이 인터넷을 사용할 수 있게 중앙 네트워크와 연결시켜주는 네트워크 

### 2. packet delay
1. nodal processing (processing delay)
- 처리하는 시간
- 라우터 내에서 패킷이 진행하는 과정, 패킷 내 데이터의 에러 체크와 어디로 갈지 결정
2. queueing
- 큐에 들어오는 순간부터 나갈 때까지의 시간
- 패킷들이 한번에 많이 들어올 경우 큐에서 보관해서 순차적으로 처리하는데 이때 발생하는 지연
3. transmission delay
- 전송하는데 걸리는 시간
- 전송하려는 패킷을 output link로 밀어내는데 걸리는 시간 (link 성능에 따라 delay시간이 결정됨)
4. propagation delay
- 전송 거리에 따른 지연시간 (전파)
