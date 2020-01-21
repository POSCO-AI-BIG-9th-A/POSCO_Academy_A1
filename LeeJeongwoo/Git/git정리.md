[로컬 저장소와 원격 저장소]
저장소는 파일이나 디렉토리를 저장하는 장소입니다. 변경 이력을 관리하고자하는 디렉토리 등을 저장소의 관리하에 두는 것으로, 그 디렉토리에있는 파일 등의 변경 내역을 기록 할 수 있습니다.

저장소는 자신의 컴퓨터에있는 "로컬 저장소"고 서버 등 네트워크에있는 "원격 저장소"의 2 개소에 있습니다. 기본적으로 로컬 저장소에서 작업을 수행하고 그 결과를 원격 저장소에 저장하게 됩니다.

[커밋, 푸시]
커밋 (commit) : 파일을 추가하거나 변경 내용을 저장소에 저장하는 작업
푸시 (push) : 파일을 추가하거나 변경 내용을 원격 저장소에 업로드하는 작업

[주요 명령어]
Github에 저장소 작성 (git init) 또는 복제 (git clone)
파일의 작성, 편집
파일의 생성 / 변경 / 삭제를 git 인덱스에 추가 (git add)
변경 결과를 로컬 저장소에 커밋 (git commit)
로컬 저장소를 푸쉬해 원격 저장소에 반영 (git push)

[GitHub에 저장소 작성]
GitHub의 메인화면에서라면, Create New Repository 버튼을 클릭합니다.
Repository name 에 이름을 입력 후 필요에 따라 Description에 저장소의 설명을 입력합니다. 그리고 저장소 유형에는 "Public" 을 선택합니다. "Private"저장소는 유료 회원 만 작성할 수 있습니다.
마지막으로, 저장소에 미리 README 파일을 만들어 놓는 경우는 "Initialize this repository with a README"에 체크합니다. .gitignore이나 license에 대해서는 나중에 추가하거나 변경할 수 있으므로 None을 선택합니다. 필요 항목의 입력이 끝나고 Create repository 버튼을 클릭하면 저장소 생성이 완료됩니다.

[변경 결과를 로컬 저장소에 커밋 (git commit)]
다음으로 인덱스에 추가 된 파일을 커밋합니다. 커밋은 파일이나 디렉토리의 추가 또는 변경을 저장소에 기록하는 작업입니다.

git commit -m "new file"

이제 저장소에 파일 추가가 기록되었습니다. 파일이 추가되어 있는지 확인합니다.

git status

또한 원격 저장소에 반영하기 전에 원격 저장소의 정보를 추가합니다. 이 정보는 방금 GitHub에 표시된 원격 저장소의 주소입니다.

git remote add origin https://github.com/username/repositaryName

[로컬 저장소를 밀어 원격 저장소에 반영 (git push)]
로컬 저장소의 변경 사항을 GitHub에있는 원격 저장소에 반영하기 위해 다음 명령을 실행합니다.

git push origin master

GitHub의 사용자 이름과 암호를 입력하면, GitHub에 푸시하고 원격 저장소에 반영할 수 있습니다. 작업이 끝났으면 github.com페이지로 가서 파일이 잘 푸쉬가 됐는지 확인합니다.

[브랜치]
소프트웨어 개발은 ​​현재 출시하고있는 버전의 유지 보수를하면서 새로운 기능 추가 및 버그 수정을 할 수 있습니다. 이러한 병렬로 수행되는 여러 버전 관리를 위해 Github에는 브랜치 (branch)라는 기능이 있습니다.

지점은 역사의 흐름을 분기하여 기록 해 나가는 것입니다. 분기 한 지점은 다른 지점의 영향을받지 않기 때문에 같은 저장소에서 각 개발을 해 나갈 수 있습니다.

[브랜치 명령어]
git branch
git add 파일이름
git commit -m "~"
git push origin ~
git pull
git checkout master
git push origin master
