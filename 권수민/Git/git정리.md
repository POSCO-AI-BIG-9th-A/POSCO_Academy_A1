A반 1조 권수민_git정리

[ 완전 초보를 위한 깃허브 ]
1. 깃헙
- What is GitHub
다른 개발자와의 협업을 위한 코드 호스팅 플랫폼, 언제 어디서든지 다른 사람들과 프로젝트 작업 가능

1) 저장소 생성
- +버튼 클릭, new repository 선택
- 원하는 저장소 이름 쓰기
- Create repository 버튼 클릭

2) 브랜치
브랜칭: 하나의 저장소에서 서로 다른 버전을 동시에 작업하는 방식
- 좌상단 Branch: master 클릭
- "" 원하는 이름 설정, create branch 클릭

3) 커밋
커밋이란 수정한 것을 저장하는 것이다. 
1. "".md 파일 클릭
2. 파일을 수정하기 위해 연필 아이콘을 클릭한다.
3. README 파일에 내용을 작성한다. 
4. 커밋메시지 작성하고, Commit changes 클릭

4) 풀 요청
풀을 요청하면 수정한 내용을 제안하고 다른 사람의 리뷰를 요청하여 수정된 내용을 브랜치에 병합할 수 있다. 수정된 것과 추가된 것은 녹색, 추가된 것은 빨간색으로 보여진다.

5) 병합(Merge) 하기
- 새로 만든 브랜치를 기존 master 브랜치에 병합한다.
- Merge pull request 클릭
- confirm merge 클릭
- 병합이 완료된 후에는 delete branch를 클릭하여 새로 만들었던 파일을 삭제한다.


[ 완전 초보를 위한 깃허브 요약 ]
*기본 용어
1. 커맨드 라인: 명령어를 입력할 때 사용하는 컴퓨터 프로그램. 프롬프트인 텍스트 기반 명령어를 입력해야함.
2. 저장소: 프로젝트가 거주할 수 있는 저장 공간. 로컬 폴더, 깃허브, 다른 온라인 호스트의 저장 공간이 될 수 있음.
3. 버전관리(Version Control): 깃이 고안된 목적
4. 커밋(Commit): 깃에게 파워를 주는 명령. 
5. 브랜치: 작업자들은 메인 프로젝트의 브랜치를 따와서(branch off), 자신이 변경하고 싶은 자신만의 버전을 만든다. 작업을 끝낸 후, 프로젝트의 메인 디렉토리인 “master”에 브랜치를 다시 “Merge”한다.

*주요 명령어
1. git init: 깃 저장소를 초기화한다.
2. git config: “configure”의 준말, 처음에 깃을 설정할 때 가장 유용하다.
3. git help: 가장 많이 사용하는 깃 명령어를 보여줌
4. git status: 저장소 상태를 체크
5. git add:깃이 새 화일들을 지켜보게 함. 화일을 추가하면, 깃의 저장소 “스냅샷”에 포함됨.
6. git commit: 저장소의 “스냅샷”을 찍기 위해 이것을 입력, 보통 “git commit -m “Message hear.” 형식으로 사용
7.git branch:  명령어는 새로운 브랜치를 만들고, 자신만의 변경사항과 화일 추가 등의 커밋 타임라인을 만든다. 
8.git checkout: 체크하길 원하는 저장소로 옮겨가게 해주는 탐색 명령
9.git merge: 브랜치에서 작업을 끝내고, 모든 협업자가 볼 수 있는 master 브랜치로 병합
10.git push: 로컬 컴퓨터에서 작업하고 당신의 커밋을 깃허브에서 온라인으로도 볼 수 있기를 원한다면, 이 명령어로 깃허브에 변경사항을 “push”한다.
11.git pull: 저장소의 최신 버전을 원할 때, 이 명령어로 깃허브로부터 변경사항 다운로드 한다. 


*처음으로 깃/깃허브 설정시
1.git config --global user.name "Your Name Here"
2.git config --global user.email "your_email@youremail.com"

*온라인 저장소 만들기
Create Repository

*로컬 저장소 만들기
mkdir ~/(저장소명) 
cd ~/(저장소명)
git init

touch (파일명).txt
git status
git add (파일명).txt
git commit -m “(파일명).txt”

*로컬 저장소 깃허브 저장소 연결하기
1) 깃에게 실제 원격 장소가 어디인지 알려주기.
ex) https://github.com/username/myproject.git에 “MyProject”라는 이름의 깃허브 저장소가 있다고 가정
확인: git remote -v
2)변경사항 업로드 or Push
- git push
- 주의메세지가 나오면, 'git push origin master' 입력
3)깃허브에 다시 로그인해보면 로컬 저장소에서 만들었던 파일과 동일한 파일을 가지고 있을 것이다.

*Summary of the all commands
git config --global user.name "이름"
git config --global user.email "깃허브 메일주소" // 매번 물어보는 귀찮음을 피하기 위해 설정.

mkdir ~/MyProject   // 로컬 디렉토리 만들고
cd ~/myproject      // 디렉토리로 들어가서
git init            // 깃 명령어를 사용할 수 있는 디렉토리로 만든다.
git status          // 현재 상태를 훑어보고
git add 화일명.확장자  // 깃 주목 리스트에 화일을 추가하고 or
git add .           // 이 명령은 현재 디렉토리의 모든 화일을 추가할 수 있다.
git commit -m “현재형으로 설명” // 커밋해서 스냅샷을 찍는다.

git remote add origin https://github.com/username/myproject.git // 로컬과 원격 저장소를 연결한다.
git remote -v // 연결상태를 확인한다.
git push origin master // 깃허브로 푸시한다.





