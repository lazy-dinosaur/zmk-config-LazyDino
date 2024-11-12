# personal zmk-config

- corne 42키 기반
- cirque trackpad 추가
- urob 유저의 zmk-nodefree 적용
- urob 유저의 개인 설정 기반으로 수정하는중
- Github Action 지원

## feature

기본적으로 대부분의 키맵이 [urob의 키맵](https://github.com/urob/zmk-config)과 동일하나 qwerty 레이아웃을 사용

다음과 같은 부분이 다름

### 불필요한 콤보키 삭제

42키 기반이기 때문에 urob의 키보다 더 많은 키를 할당 가능
따라서 다음에 해당하는 콤보키를 삭제하고 직접 할당

- `Tab`
- `Esc`
- `Return`
- `Backspace`
- `Delete`
- `Repeat`

### 콤보키 추가

- 한국인을 위한 콤보키 추가
  - 'N' 과 'M'을 같이 누르면 'B'로 동작 'ㅠ' 를 입력할때의 불편함 해소
- 마우스레이어의 취소와 Num 레이어 그리고 smart shift 의 동작을 취소할 수 있는 cancel 키를 콤보로 추가
  - 'F' 와 'D' 를 동시입력할때 CANCEL 키가 작동함

### Cirque 트랙패드의 추가

- **[Input behavior module](https://github.com/badjeff/zmk-input-behavior-listener) 적용**
  - Trackpad 동작 시 MOUSE 레이어 자동으로 활성화 (800ms)
  - MOUSE 레이어에서 'D'+'F' 콤보를 사용해서 즉시 레이어 비활성화 MOUSE 레이어 이외에서는 'CANCEL'키로 동작
  - MOUSE 레이어와 기본 레이어에서 'R'키 홀드시 트랙패드의 y축 인풋만 활성화되며 마우스 수직 스크롤로 동작
  - MOUSE 레이어와 기본 레이어에서 'E'키 홀드시 트랙패드의 x축 인풋만 활성화되며 마우스의 수평 스크롤로 동작

### 동글 추가

동글의 사용을 위해 [zmk-split-peripheral-input-relay](https://github.com/badjeff/zmk-split-peripheral-input-relay) 모듈 적용

#### 장점

1. 베터리 수명 향상 - 대략 일주에서 한달정도로 향상
2. 반응속도 향상 - USB로 연결했을때와 동일한 응답속도로 사용(동글을 사용하지 않으면 USB에 연결하여 사용할때보다 블루투스를 사용할때 매우 끊기는 느낌을 받는다)

### USB토글 사용 방법

FN 레이어와 NUM 레이어를 동시에 동작시키면 SYS 레이어로 변경된다. 이때 해당 레이어에서 블루투스 연결 프로파일 키를 클릭한 이후 원하는 기기와 연결한다.
연결이 된 이후에 동글의 USB 와 블루투스 연결을 SYS 레이어의 j 키로 토글할 수 있다.
