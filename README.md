### 사용 폰트

[고운돋움](https://fonts.google.com/specimen/Gowun+Dodum?subset=korean#standard-styles)

<br>

# Versions

## 메인 화면
### Front
#### Version 1.0
- 고정 바, 회원님을 위한 추천, 게시글
  - 아직 사용자가 로그인하기 전일 경우에는 회원님을 위한 추천 부분이 사라지고 관련 게시글도 나오지 않음
  - 추천된 사용자 클릭 시 해당 사용자의 페이지로 이동
  - 본인이 작성한 글일 경우에만 수정 버튼 보여짐
#### Version 1.1
- 고정바에 로그아웃, 로그인 아이콘 추가
- Footer에 저작권 표시 추가

### Back
#### Version 1.0
- 사용자가 로그인했을 경우에만 이메일을 받아 사용자 추천과 게시글을 보내줌
  - 사용자 추천
    - 1. 먼저 해당 사용자의 이메일을 기반으로 작성된 포트폴리오가 있는지 확인
    - 2. 포트폴리오가 있다면, 포트폴리오에 보유 기술 스택을 적었는지 확인
    - 3. 보유 기술 스택이 있다면, 해당 사용자의 보유 기술 스택과 동일한 스택을 보유한 사용자의 포트폴리오를 찾음
    - 4. 3에서 찾은 포트폴리오의 이메일을 사용하여 해당 사용자의 정보를 뽑아냄
    - 5. 4의 결과에서 중복을 제거하여 5명보다 적거나 같을 경우에는 모두 반환, 그렇지 않을 경우에는 랜덤으로 5명을 뽑아낸 뒤 반환
  - 게시글
    - 아직 팔로우 기능을 구현하지 않았기 때문에 우선 본인이 적은 글만 찾아서 반환
    - 다음 버전에서 본인의 팔로우 목록을 기반으로 해당 사람들이 적은 글과 본인이 적은 글을 합쳐 반환할 예정

#### Version 1.1
- 메인 화면 게시글을 나와 팔로우 목록의 게시글이 모두 뜨도록 반환

<br>

## 로그인 화면
### Front
#### Version 1.0
- 로그인 모달 창 구현

#### Version 1.1
- 로그인 로직 추가

#### Version 1.2
- (해야할것) 로그인시 자동으로 메인 화면 전환 되어 글들이 올라가게 만들어져야함. 현재는 다른 화면을 갔다가 돌아올때 내가 쓴 글이 생성됨

#### Version 1.3
- 회원가입 버튼 css 수정

### Back
#### Version 1.0
- 로그인 성공/실패 JSON 전송

<br>

## 회원가입 화면
### Front
#### Version 1.0
- 회원가입 모달 창 구현

#### Version 1.1
- 회원가입 로직 추가

### Back
#### Version 1.0
- 회원가입 성공/실패 JSON 전송

#### Version 1.1
- 회원가입 시 이미 존재하는 사용자의 이메일을 입력하였을 경우의 예외처리 부분 추가

<br>

## 프로필 화면
### Front
#### Version 1.0
- 포트폴리오 작성 버튼 존재
- 팔로우 목록, 나의 이름, 이메일, 나의 소개, 기술, 스택, 경력사항, 깃 허브 보여짐
- 팔로우 목록에서 사람의 이름을 클릭하면 상대방 프로필 화면으로 전환
- 맨 아래 로그아웃, 메인 링크 존재 -> 메인을 누르면 메인 화면으로 전환, 로그아웃을 누르면 로그아웃 된 상태로 초기 메인 화면으로 돌아감
- (해야할것) 메인 링크를 눌렀을때 화면이 아래로 내려간 상태로 화면이 전환됨

#### Version 1.1
- 팔로우 목록 및 링크 수정

### Back
#### Version 1.0
- 내 포트폴리오 정보 전달

#### Version 1.1
- 팔로우 목록 전달

<br>

## 상대 프로필 화면
### Front
#### Version 1.0
- 크게 포트폴리오, 게시글 Nav가 존재함.
- 게시글:
- 상대방이 쓴 게시글 보여짐
- (해야할것) 한번 클릭시 화면은 잘 바뀌지만, 게시글을 두번 클릭해야 게시글이 선택되어지는 표시가 보여짐.
- 포트폴리오:
- 팔로우의 이름, 이메일, 소개, 기술/스택, 경력사항, 깃 허브 보여짐
- 마이페이지, 메인 링크 존재 -> 마이페이지를 누르면 메인 화면으로 전환, 로그아웃을 누르면 로그아웃 된 상태로 초기 메인 화면으로 돌아감

#### Version 1.1
- 팔로우 버튼 추가

### Back
#### Version 1.0
- 해당 사용자 정보, 포트폴리오 정보, 게시글 정보 전달

#### Version 1.1
- 팔로우 버튼 클릭 시 해당 사용자와 내가 팔로우되어 있지 않다면 팔로우를 하고, 이미 팔로우가 되어있다면 팔로우 취소를 하는 방식으로 구현

<br>

## 포트폴리오 작성/수정 화면
### Front
#### Version 1.0
- 보유 기술/스택, 경력 사항, 내 소개(마크다운 형식), 본인 깃허브 링크 입력 가능
- 보유 기술/스택 입력 시 Enter를 누르면 자동으로 밑에 입력한 기술들이 추가됨
- 경력 사항에서 추가 버튼 클릭 시 경력을 추가할 수 있는 모달이 뜨며, 입력 후 오케이 버튼을 누르면 작성 페이지의 경력 표에 자동으로 추가됨
- 보유 기술/스택과 경력 사항 모두 옆의 X 버튼 클릭 시 항목 삭제 가능
- 내 소개를 마크다운 형식으로 입력하는 것은 [NHN의 Toast UI](https://ui.toast.com/tui-editor)를 사용함
- 내 계정으로 작성된 포트폴리오가 있을 시 해당 포트폴리오의 내용이 로드되고, 아직 작성된 것이 없을 경우 초기 상태로 시작
- 초기화 버튼 누르면 모든 요소가 초기화됨

#### Version 1.1
- 내가 작성한 포트폴리오가 없을 경우의 예외처리 부분 추가

### Back
#### Version 1.0
- 처음에 사용자 이메일을 사용하여 해당 이메일로 작성된 포트폴리오가 있는지 검색하여 결과를 반환
- 사용자가 본인에 해당하는 요소들을 입력하고 등록 버튼을 누를 시 새로운 포트폴리오가 생성되어 저장되거나, 원래 해당 사용자의 포트폴리오가 있는 경우에는 수정되어 저장됨
- 성공 여부를 JSON 형태로 반환


<br>

## 게시글 작성/수정
### Front
#### Version 1.0
- 사용자가 로그인 하지 않았을 때 로그인 요청 팝업 창 도출, 수정 버튼 사라짐
- 로그인 시 수정 버튼 생성
- 로그인 하지 않았을 때 수정 버튼 없어짐

#### Version 1.1
- Back에 데이터 보내는 부분 추가
- 글 작성, 글 수정 모달 부분에서 아이콘 옆에 사용자의 이름 노출

### Back
#### Version 1.0
- 작성된 글 전달 시 데이터베이스 저장


<br>

## 고정 바
### Front
#### Version 1.0
- 로고, 검색 바, 메시지 버튼, 마이페이지 버튼

### Back
- push test
