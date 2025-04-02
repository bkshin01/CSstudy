# OS 찐기초

## 인터럽트, 트랩
CPU가 프로그램을 실행중인 상황에서 이상징후의 발생으로 인해 프로그램을 잠시 중단하고, 해결한 후에, 다시 실행중인 프로그램으로 돌아와 작업을 이어가는 것을 의미합니다.
- 인터럽트: 주로 하드웨어에 의해 발생합니다. I/O 장치의 이상, 전원 장치에 의한 오류 등이 존재합니다.
- 트랩: 주로 소프트웨어에 의해 발생합니다. 실행 프로그램의 에러인 Exception이나 시스템 콜이 이에 해당합니다.

## 시스템 콜
Application/Process들과 OS 사이에서 발생하는 인터페이스입니다.<br>
사용자 프로그램이 자원이나 서비스를 필요로할 때 운영체제에 요청하는 것입니다.<br>
Process control, File manage,ent, Device management 등이 있습니다.

## Exception
Divided by zero, null pointer exception 등이 있습니다.
