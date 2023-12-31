# CISC 와 RISC

> CISC 와 RISC 중 그 어느 것이 더 좋다고 학문적으로 장담하여 말할 수는 없다. 종류에 따라 특성이 구분되기 때문이다.

CISC 는 Complex Instruction Set Computer 로써, **새롭게 Instruction을 만드는 접근 방식 (Register 내의 값을 바로 사용)** 을 가진다.

- 병렬 처리가 어렵다.

> 병렬 처리는 명령별로 길이가 같아야 overlapped하기 용이한데, 이는 새롭게 Instruction을 만들기 때문에 길이가 천차만별이다.

- 이는 시스템 친화적으로 컴파일이 쉽다.

- 새로 만들어서 사용하기 때문에, 전체 명령의 크기가 줄어들어서 메모리 사용량이 감소된다.

- CPU 설계가 더 힘들다. 각 아키텍처에 대응되는 형태로 만들기가 어렵고, 기존에 만들어진게 오래되어 지우려해도 어디에 영향을 끼칠지 알수 없다.

RISC 는 Reduced Instruction Set Computer 로써, **기본적으로 주어진 약 200개의 Instruction을 이용해서 순차적으로 사용하는 잡근 방식 (Register 내의 값을 바로 사용하지 못해서 load 과정을 거침)** 을 가진다.

- 병렬 처리에 용이하다.

> 병렬 처리는 명령별로 길이가 같아야 overlapped하기 용이

- 명령의 추가적으로 설계할 필요가 없이 기본 명령어로 구성되기 때문에 CPU 설계가 간단하다.

- instruction set이 CISC에 비해 훨씬 가볍다.

  > 이는 clock 스피드 증가로 이어진다.

- 기본 명령어로 순차적으로 처리하기 떄문에 전체 코드의 사이즈가 커질 수 밖에없다.

- 실제 적재되는 코드량이 많아서 메모리를 과소모하게 된다.

## 간단한 CISC와 RISC가 지향하는 방향

- CISC

  - 작은 IC(instruction count)를 기대할 수 있지만, CPI 가 상승한다. (이는 명령어1개가 매우 복잡하기 떄문이다.)

- RISC
  - CPI를 감소하는 접근법이지만, 무조건적으로 CISC에 비해 IC 가 크게 나온다.
