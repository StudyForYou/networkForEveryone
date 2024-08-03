# 이더넷

다수의 컴퓨터, 허브, 스위치 등을 하나의 인터넷 케이블에 연결한 네트워크 구조

## CSMA/CD(Carrier Sense Multiple Access/Collision Detection)

- 전류의 강도를 통해 케이블이 사용 중인지 확인하여 충돌을 해결하는 방법

  - 충돌(collision) : 2대 이상의 컴퓨터가 동시에 데이터(프레임)을 보내는 상황

- 과정
  1. 송신 전에 케이블이 사용 가능한지 확인(Carrier Sense)
  2. 사용 가능하면 데이터를 전송(Multiple Access)
  3. 전송 후에도 여전히 발생할 수 있는 충돌을 확인(Collision Detection)

### 1-persistent

- 케이블이 사용 중인지 상태를 계속 확인하다가 아무도 사용하지 않는 상태이면 바로 데이터를 전송하는 방식
- 동시에 다른 컴퓨터에서도 데이터를 보낼 가능성이 높기 때문에 충돌 위험성이 가장 높음

### nonpersistent

- 아무도 케이블을 사용하고 있지 않으면 데이터를 보내고, 사용중이라면 임의의 시간을 기다렸다가 상태를 다시 확인하는 방식
- 1-persistent보다는 충돌 위험이 낮음

### p-persistent

- 1-persistent와 non-persistent의 결합
- 케이블이 사용 중이면 기다렸다가 다시 상태를 확인하고 아무도 사용하지 않으면 일정 확률로 데이터를 전송함
