# 1. 컴퓨터의 구성
하드웨어 : 컴퓨터를 구성하는 기계적 장치 ( ex) SDD 하드, HDD 하드 등 )
* 중앙처리장치 
* 기억장치
* 입출력 장치

소프트웨어 : 하드웨어의 동작을 지시하고 제어하는 명령어 집합 ( ex) 운영체제 등에서 사용하는 프로그램들 )
* 시스템 소프트웨어
* 응용 소프트웨어

중앙처리 장치
* 산술논리연산장치
* 제어장치
* 레지스터

기억 장치
* 주기억장치 
* 보조기억장치

입출력 장치
* 입력 - 키보드, 마우스
* 출력 - 프린터, 모니터, 스피커

```
RAM(Random ACcess Memory) 이란?
- RAM 휘발성 메모리로, 작업 중인 파일을 한시적으로 저장합니다.

ROM(Read Only Memory) 이란?
- 컴퓨터에 지시사항을 영구히 저장하는 비휘발성 메모리
```

시스템 버스
* 데이터 버스 - 데이터 연결 통로
* 주소 버스 - 말 그대로 주소를 정해주는 버스
* 제어 버스 - 모든 장치에 공유되는 부분을 제어하는 수단

컴퓨터의 처리과정
- Read---> Process ---> Write

---

# 2. 중앙처리장치(CPU) 작동 원리

CPU - 인간의 두뇌에 해당

* 연산 장치
* 제어 장치
* 레지스터

연산 장치
- 산술연산과 논리연산을 수행

제어 장치
- 명령어를 순서대로 실행할 수 있도록 제어하는 장치

레지스터
- 고속 기억장치
- 범용 레지스터 / 특수목적 레지스터로 구분

### 특수 목적 레저스터 종류
- MAR(메모리 주소 레지스터) / PC(프로그램 카운터) / IR(명령어 레지스터) / MBR(메모리 버퍼 레지스터) / AC(누산기)
```
MAR(메모리 주소 레지스터)란?
- 데이터의 주소를 기억하는 레지스터

PC(프로그램 카운터)란 ?
- 다음에 실행될 명령어의 주소를 가지고 있어 실행할 기계어 코드의 위치를 지정하기 때문에 명령어 포인터라고도 한다.

IR(명령어 레지스터)란?
- 현재 실행 중인 명령을 기억하는 레지스터

MBR(메모리 버퍼 레지스터)란?
- 데이터를 임시로 기억하는 레지스터로 데이터를 처리하기 위해 반드시 거쳐가게 됨

AC(누산기)란?
- 연산 결과를 임시로 저장하는 레지스터
```


### CPU의 동작 과정
1. 저장된 프로그램을 읽어오고
2. 처리한 데이터를 다시 주기억장치에 저장
3. 처리 결과를 보조기억장치에 저장하거나 출력
4. 제어장치가 1~3의 과정이 순서대로 실행할 수 있도록 제어

#### 명령어 세트 
- CPU가 실행할 명령어의 집합

> 연산 코드(Operation Code) + 피연산자(Operand)로 이루어짐   
> 연산 코드 : 실행할 연산   
> 피연산자 : 필요한 데이터 or 저장 위치

연산 코드 - 연산, 제어, 데이터 전달, 입출력
피연산자 - 주소, 숫자/문자, 논리 데이터 등을 저장

```
명령어 사이클이란?
- CPU가 주기억장치에서 한번에 하나의 명령어를 인출하여 실행하는데 필요한 일련의 활동
- 인출/실행/간접/인터럽트
- 주기억장치에서 하나의 명령어를 가져오고, 실행 사이클에서는 명령어를 실행 후 해당 실행이 완료되면 다음 명령어에 대한 인출 사이클 시작
```

#### 인출 사이클에서 가장 중요한 부분 : PC(프로그램 카운터) 값 증가

1. PC에 저장된 주소를 MAR로 전달

2. 저장된 내용을 토대로 주기억장치의 해당 주소에서 명령어 인출

3. 인출한 명령어를 MBR에 저장

4. 다음 명령어를 인출하기 위해 PC 값 증가시킴

5. 메모리 버퍼 레지스터(MBR)에 저장된 내용을 명령어 레지스터(IR)에 전달
