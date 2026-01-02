# PacketTracer-Network-Lab
# 🌐 Packet Tracer Inter-VLAN Routing 실습 ( 2026/01/02 )

## 1. 구성도
![Network t](https://github.com/user-attachments/assets/b0bccd5f-7a54-482f-a409-cc1049e8b6c3)



## 2. 실습 목표
L3 계층 스위칭 이해: L3 스위치(3560)의 no switchport 및 SVI 설정을 통한 라우팅 기능 활성화 이해

Inter-VLAN 및 이기종 간 라우팅: 서로 다른 네트워크 대역(192.168.10.0/24 및 172.10.10.0/24) 간의 데이터 패킷 전달 구현

정적 경로(Static Route) 최적화: 각 라우팅 홉(Hop)별로 인접 넥스트 홉(Next-hop) IP를 지정하여 최적의 통신 경로 수립

## 3. 핵심 설정 코드 (Cisco IOS)
- L3 Switch (Multilayer Switch0) L2 포트를 L3 포트로 전환하고 전역 라우팅을 활성화합니다. *** no switchport
- Routers (Router0 & Router1) 각 인터페이스 활성화 및 원격 네트워크 대역에 대한 경로를 설정합니다. *** ip route x.x.x.x(알고싶은 네트워크 구역) x.x.x.x(서브넷마스크) x.x.x.x(게이트웨이)

## 4. 해당 토폴로지 Config 값 
- L3 Switch
  <img width="719" height="817" alt="image" src="https://github.com/user-attachments/assets/27d8feaa-dbf5-4a5e-af19-8e4f7c0c89ad" />

- Router0
  <img width="715" height="814" alt="image" src="https://github.com/user-attachments/assets/c76f60fd-00d8-4c6f-9709-85abf6433798" />

- Router1
  <img width="720" height="819" alt="image" src="https://github.com/user-attachments/assets/efa835aa-5809-4fb9-86e2-658028fe1af3" />

## 5. 핵심 체크포인트
- L3 스위치:

- 
