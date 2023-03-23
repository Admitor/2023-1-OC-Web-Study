1. Working Directory / 2. Staging Area / 3. Repositorty
1. - 작업 공간, git에 기록될 준비가 되지 않은 파일이 위치하는 곳. 
2. - 대기 공간, git으로 옯겨질 준비가 된 파일이 위치하는 공간
3. - git에 기록된 파일들이 위치하는 공간

git add란
작업 디렉토리(working directory) 상의 변경 내용을 스테이징 영역(staging area)에 추가하기 위해서 사용하는 Git 명령어
간단하게는 git에 파일을 추가하는 명령어 - 그럼 처음 Working Directory에 만들어진 파일들을 git에 보낼 준비를 하도록
Staging Area에 보내주는 명령어 인듯

git commit이란
Staging Area의 파일들을 Repository로 옮기는 명령어
여러 파일을 묶어서 보낼 수 있는 듯 하다 
commit이란게 일종의 단위인데 commit hash라는 구분자로 끊어서 옯길 수 있는 듯..?

git push란
git push는 원격 저장소(remote repository)에 코드 변경분을 업로드하기 위해서 사용하는 Git 명령어 
원격 저장소 즉, github에 업로드 하는 명령어 인듯 하다

git pull이란
다른 사람이 원격 저장소(Remote repository)에 업데이트한 파일이 있을 때, 원격저장소와 내 로컬저장소의 상태를 동일하게 만들기 위해 pull을 이용한다라고 함
-아마 로컬에서 만들고 리모트로 옯긴 후에, 리모트쪽에서 수정이나 업데이트를 하면 당연히 로컬에서 동시 업데이트는 안되므로
pull로 동기화 시켜주는 듯 하다 - 또 보니까 로컬 저장소를 업데이트하는게 아니라, 리모트 리포지의 클론 리포지를 동기화시켜주는 것 같다    

git fetch란
pull은 바로 동기화 시켜주는 대신, fetch는 업데이트 된 것이 있는지 확인 여부만 알려주는 것 같음

create-react-app은 뭐지
보일러 틀에 여러 개의 보일러를 찍어내듯, 초기 환경을 일일히 설정하지 않고도 리액트 프로젝트를 시작할 수 있도록 셋업을 완료해놓은 틀이라고 보면 된다. - 라고 함

1주차
1주차 www.hongik.ac.kr을 입력했을 뿐인데
리소스를 저장한 주소
예시
리소스 - 허니콤보
허니콤보를 얻을 수 있는 교촌 치킨 신촌점의 주소 - 주소(URL)
URI = Uniform Resource Identifier - 리소스를 식별하는 통일된 방식?
-> 허니콤보를 얻을 수 있느 위치를 알아내기 위한 방식

URL = Uniform Resource Location = 프로토콜(http) + DNS 주소
-위치
예시) 교촌치킨 신촌점 주소

URN = Uniform Resource Name
-이름으로 찾기
예시)도서출판번호 ISBN 

원래는 복잡한 IP를 통해 리소스에 접근해야됨
www.~~이 아닌
[214 243 236 654] - 복잡한 IP

문제점
1. 그 기록 복합한 IP 주소들을 외우거나 관리하기 너무 힘듦
2. IP주소는 상황에 따라 바뀔 수 있음


예시
서버 - 컴퓨터(자료 제공을 위한)
리소스 - 자료
123.235.33.235 - 홍익대학교 서버(외우기 힘듦)
바뀌면 원하는 서버에 접근 못하고, 리소스를 얻을 수 없음

도메인 네임 - IP 주소들의 이름
도메인 네임 서버 - 도메인들을 저장해놓은 서버 IP가 바뀌더라도 다시 연결해줌
EX) 홍익 도메인 입력 - 도메인 네임 서버에서 홍익 도메인에 연결된 IP주소를 연결시켜줌 - 원하는 서버로 접근 가능

리소스의 정체 - 파일들
브라우저(크롬, 익스플로러)가 HTML, CSS, JS를 자료 삼아서 그림을 그림(랜더링)
HTML: 자료(뼈대, 장기)
CSS: UI(살과 옷)
JavaScript: 제어

2주차
GIT - 파일의 변경사항을 추적하고 조율함/ 소스코드 변화를 추적 / 특정시점으로 백업 가능 / 변화추적(버전 관리)

파일 4가지 형태
추적 불가(Untracted)
변경 불가(Unmodified)
변경 가능(Modified)
Staged

코드 작성 공간 - (add command) - staging - dommit - .git directiory (git이 관리하는 공간)
-> 이 모든 작업이 내 컴퓨터 안에서 일어나는 일임
git은 서버 - 내 컴퓨터 밖의 일을 처리하기 위해 필요
-> remote repository가 추가됨 - GITHUB