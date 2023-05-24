# 리눅스 명령어 과제

**1. top 명령어**
+ 리눅스 우분투(Linux Ubuntu)에서 top 명령어를 사용하여 시스템 사용량을 실시간으로 확인할 수 있다.
+ top 명령어는 리눅스 시스템이 실행되고 난 후 부터 지금까지의 시간과 시스템에 로그인된 사용자 수를 보여준다.
+ top 명령어는 시스템 부하율을 표시하는 명령어인 uptime의 결과를 가장 상단에 표시해주며, 그 아래로 프로세스 수치, CPU 정보, 메모리 정보를 보여주고, 각 프로세스 별 부하율과 상태를 표시해준다.

> 사용 구문
```
top [옵션]
```
```
-b: 배치모드로 정보를 출력한다. 실시간 상화 대화혈모드로 정보를 화면에 일렬로 출력한다.
-d delay: 지정한 시간(delay 초)의 간격으로 정보를 업데이트하여 출력한다.
-i idle: 토글값이 off일 때, idle 프로세스나 좀비 프로세스 정보를 출력하지 않는다.
-n num: 지정한 시간(num)만큼 업데이트 정보를 출력한다.
-p pid: 지정한 프로세스 ID(pid)의 정보만을 출력한다.
-q: 시간의 간격 없이 계속하여 업데이트 정보를 출력한다.
-s: 몇 개의 대화식 명령을 비활성화한다.(시큐어 모드)
-S: 누적된 정보를 출력한다.(cumulative 모드)
```

> top 단축기 명령어
- space: 정보를 업데이트한다.
- ^L: 스크린을 다시 초기화한다.
- F of f: 
  + 필드를 추가하거나 제거한다
  + 확인하고자 하는 항목의 알파벳을 누를 때마다 선택/취소가 반복된다.
- O or o:
  + 출력하는 필드의 정렬 순서를 변경한다.
  + 대문자로 선택한 항목을 누르면 왼쪽으로 이동하고 소문자를 누르면 오른쪽으로 이동한다.
- h on ?: 사용 가능한 명령어를 출력한다.
- k: 프로세스를 종료시킨다.
- n or #: 출력할 프로세스의 수를 지정한다.
- s: 출력할 정보의 업데이트 시간을 지정한다.
- W: ~/.toprc에 설정된 내용을 저장한다.
- q: top을 종료한다.

> top 보기 수정 단축기
- 출력되는 메인 정보 창 중에 상단의 정보를 수정한다.
- r: 프로세스의 우선순위를 변경한다
- N: pid 정보를 기준으로 정렬한다.
- A: age 정보를 기준으로 정렬한다.
- P: CPU 사용량을 기준으로 정렬한다.
- M: 적재된 메모리 사용량을 기준으로 정렬한다.
- T: 시간/누적시간을 기준으로 정렬한다
- u: 지정한 사용자의 정보만을 출력한다.

> top 실행 후 명령어
- shift + p: CPU 사용률 내림차순한다.
- shift + m : 메모리 사용률 내림차순한다.
- shift + t : 프로세스가 돌아가고 있는 시간 순을 보여준다.
- k: kill. k 입력 후 PID 번호 작성한다. signal은 9
- f: sort field 선택화면 -> q 누르면 RES 순으로 정렬한다.
- a: 메모리 사용량에 따라 정렬한다.
- b: Batch 모드로 작동한다.
- 1: CPU Core 별로 사용량 보여준다.

> top 명령을 실행한 사진
<img width="422" alt="top" src="https://github.com/deokhwan12/report/assets/133830093/6a2a310d-2571-4a7f-9b65-8fba98d4173f">

---
**2. ps 명령어**
+ 리눅스에서는 여러 개의 프로세스가 동시에 실행되기 때문에 현재 실행 중인 프로세스의 정보를 얻기 위해 사용된다.
+ 프로세스 중에서 CPU, 메모리 등등을 많이 점유하고 있거나, 지나치게 많은 자식 프로세스를 생셩하는 등등에 시스템에 속도가 느려지는 시스템 오류를 감지할 수 있다.

> 사용 구문
```
ps [옵션]
```

> 전체 프로세스와 관련된 옵션
- -A: 모든 프로세스를 출력한다.
- -N: -A 옵션과 비슷하나 ps 프로세스를 제외하고 출력한다.
- -a: 세션 리더 및 터미널에 속하지 않는 프로세스를 제외하고 출력한다.
- -d: 세션 리더를 제외한 모든 프로세스를 출력한다.
- -e: 커널 프로세스를 제외한 모든 프로세스를 출력한다.
- T: 현재 터미널에서의 모든 프로세스를 출력한다.
- a: 현재 터미널의 사용자 고유 프로세스를 출력한다.
- r: 현재 실행 중인 프로세스를 출력한다.
- x: 터미널이 없는 프로세스를 출력한다.
- --deselect: -N 옵션과 같다.

> 특정 프로세스를 선택하여 보여주는 옵션
- -C: 지정한 명령어의 이름에 관련된 정보를 출력한다.
- -G: 그룹 ID에 관련된 정보를 출력한다.(이름도 지원)
- -U: 사용자 ID에 관련된 정보를 출력한다.(이름도 지원)
- -g: 지정한 세션 리더 혹은 그룹명에 관련한 정보를 출력한다.
- -p: 프로세스 ID를 출력한다.
- -s: 세션에 속한 프로세스를 지정한다.
- -t: tty를 지정한다.
- -u: 사용자 ID를 지정한다.(이름도 지원)
- U: 지정한 사용자의 프로세스를 출력한다.
- P:프로세스 ID를 지정한다.
- t: tty를 지정한다.
- --tty: 터미널을 지정한다.
- --user: 유효 사용자 이름이나 ID를 지정한다.
- -123: --sid 123과 같은 의미이다.
- 123: --pid 123과 같은 의미이다.
