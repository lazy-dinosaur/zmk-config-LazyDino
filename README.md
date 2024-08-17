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

- sleep 설정 제거
  - sleep 설정 시 마우스를 다시 움직일때 딜레이 발생
- Tap 활성화
  - 한번 탭=왼쪽클릭 두번탭=왼쪽 클릭 후 홀드
- **Input behavior module 적용**
  - NAV 레이어에 진입하면 트랙패드의 y축 인풋만 활성화되며 마우스 스크롤로 동작
  - FN 레이어에 진입하면 트랙패드의 x축 인풋만 활성화되며 마우스의 횡스크롤로 동작
  - Mouse
