# 스위치의 구조

## 스위치

소규모 네트워크 안에서 컴퓨터, 프린터 등 모든 장치를 서로 연결해서 데이터를 쉽게 공유할 수 있도록 하는 장비

### 스위치에서 MAC 테이블 관리하기

#### MAC 테이블

스위치에 연결된 장비들의 MAC 주소를 관리(등록/수정)함.

#### MAC 테이블에 모든 컴퓨터의 MAC 주소 추가하기

1. 컴퓨터 A는 컴퓨터 C와 통신을 시도함
2. 스위치는 자신의 MAC 테이블에 컴퓨터 C의 MAC 주소가 없다는 것을 확인 후, 컴퓨터 A가 보낸 데이터를 컴퓨터 B, C, D에 보냄 -> 플러딩

- 플러딩(Flooding) : 스위치에 물려 있는 모든 컴퓨터에 데이터를 보내는 것

3. 컴퓨터 B, C, D가 스위치에 응답하면서 자신의 MAC 주소를 알려주고, 스위치는 이렇게 받은 MAC 주소를 MAC 테이블에 업데이트함
4. 스위치는 컴퓨터 C의 MAC 주소를 컴퓨터 A에게 알려줌. 이후 2대의 컴퓨터가 서로 통신함

#### 업데이트된 MAC 테이블 이용하기

컴퓨터 A가 C와 서로 통신하면 컴퓨터 A의 질의는 더 이상 컴퓨터 B, D에게 전달되지 않음 -> MAC 주소 필터링(Filtering)
