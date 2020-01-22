* git을 사용하는 이유?

동시에 같은 코드를 업데이팅하며 발생하는 충돌을 방지할 수 있다.  
각자의 수정사항을 업로드할 수 있고, 언제든지 버전을 수정할 수 있다.  

* git관련 개념 정리

version control ; 동시에 수정시 각 스냅샷을 저장하여 원하는 버전으로 변환 가능
commit ; 나의 수정사항 체크 포인트 찍기
branch ; main project를 branch off해서 나만의 버전을 만들고, master dir에 나의 branch를 merge한다.


* 주요 명령어

git init ; rep 초기화
git config ; 설정 내용을 확인하고 변경한다.
	- /etc/gitconfig 파일 ; 모든 사용자와 모든 저장소에 적용되는 설정
	- ~/.gitconfig 파일 ; 특정 사용자에게만 적용되는 설정.
git help ; 가장 자주 사용하는 21개의 명령어를 알려준다.
	- ex ) git help init ; init에 대한 사용하는 방법을 알려준다.
git status ; 어떤 파일이 있는지 확인할 때, 어떤 branch에서 작업하고 있는지를 확인할 수 있다.
git commit ; 변경사항을 스냅샷하기 위한 명령어.
	- ex ) git commit -m "Message hear."
		* -m ; 다음 부분을 메시지로 읽어라!하는 명령어
git branch ; 나만의 변경사항을 위하여 새로운 브랜치를 만들고 commit timeline을 만든다.
	- ex ) git branch New ; 새로운 branch를 "New"라는 이름으로 만든다.
git checkout ; 현재 위치하고 있지 않은 저장소를 살펴본다.
	- ex ) git checkout New ; New라는 브랜치를 들여다본다.
git merge ; 작업이 끝난 후 모든 사람이 볼 수 있는 master branch로 merge한다.
	- ex )  git merge New ; cats branch서 만든 변경사항을 master branch에 추가한다. 
git push ; local에서 작업하고 online으로 보고 싶을 때 사용하는 명령어. 
git pull ; local에서 작업하는 중, rep의 최신 버전을 원할 때 사용하는 명령어.

* git 설정하기 위한 단계

첫 git 설정을 위한 명령어
	- git config --global user.name "input your name"
	- git config --global user.mail "input your email" # 단 git을 가입할때 사용한 email

local rep 만들기
	mkdir ~/MyProject   # mkdir ; make directory # ~/ ; 상위 폴더에 생성
	cd ~/MyProject      # cd ; change dir
	git init	    # 해당 dir이 local git rep임을 선언
			    # git ready 상태
	touch Readme.txt    # touch == create ; Readme.txt파일을 만들어라.
	git status	    # On branch master ; 현재 master에 있음. branched off 해야 list에 나타남
			      untracked	; 아직 git이 해당 파일을 무시하고 있음
	git commit -m "Add Readme.txt" ; 위에서 commit한 내용을 메시지로 입력

* local과 git 연결하기

	git remote add origin https://~ ; 내 깃허브(여기서는 MyProject)가 저장된 저장호 주소
	git remote -v ; origin에 대한 모든 항목을 보여준다. (연결상태 확인)
	git push origin master ; 내 저장소의 master branch지정하기

* 파일 수정하기 ; readme.md를 수정한다면?

1. 연필 아이콘 클릭
2. 내용 수정
3. commit 메시지 작성
4. commit changes 클릭
>> readme edits branch에 수정된 내용이 적용된다. 그러면 master branch와 내용이 달라진다 !

* 수정된 내용을 pull request하기

pull request란? ; 두 branch로부터 다른 저을 보여준다. (수정/추가/빠진것, 빨간색이나 녹색 박스)
1. New pull request
2. compare
3. readme-edits 로 바꾸기
4. 요청에 대한 간단한 설명을 적고 create pull request를 클릭

* merge하기

1. Merge pull request
2. confirm merge
3. 병합 후에는 readme-edits branch가 필요 없으므로 delete branch 하기
	
