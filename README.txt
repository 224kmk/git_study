git_study - 팀 개발을 위한 Git, GitHub 시작하기 - 한빛미디어 / 정호영,진유림 지음

by sourcetree, VScode, CLI

# Sourcetree
- git 사용을 도와주는 GUI 프로그램
- 버튼을 클릭하는 방식으로 필요한 명령을 실행할 수 있도록 도와주기때문에 편리
- Git의 핵심인 커밋, 푸시, 브랜치 등 눈으로 쉽게 확인 가능

==========================================================

- 폴더에 git 파일 생성
$ git init

- 커밋 생성
$ git config --global user.email "본인 로그인 이멜"

$ git config --global user.name "본인 깃허브 이름"

- 커밋 추가
$ git add 파일이름.형식

- 커밋 상세 내용(설명)
- m --> message
$ git commit -m "설명 내용"

- 다른 커밋으로 이동하기
$ git log

commit 이름 및 번호 확인 후
ex) commit 5813bb5~~~
 
$ git checkout commit번호

가장 최근 커밋으로 돌아가는 방법은 - 붙이면 됨
$ git checkout -

- 원격 저장소에 커밋 올리기
$ git remote add origin "깃허브 리포지토리 주소"

==============remote error=============
$ git remote remove origin -> remove 로 삭제

$ git remote add origin "깃허브 리포지토리 주소"

$ git remote -v 로 확인

$ git push origin master
==================================

-- 로컬 저장소에서 원격저장소로 올리기
$ git push origin master

-- 원격저장소의 커밋을 로컬저장소에 내려받기
-> 다른 폴더에 github 홈페이지 자료 다운
$ git clone 다운받을 github주소 .  --> 한칸 띄우고 마침표

- 새로운 원격저장소에서 github 푸쉬하기
1. 커밋
$ git add README.txt

2. 코멘트 추가
$ git commit -m "코멘트"

3. 푸쉬
$ git push origin master

-- 원격 저장소의 새로운 커밋을 로컬 저장소에 갱신하기. --> 항상 폴더를 헷갈리지 않도록 주의
$ git pull origin master

================error: failed to push some refs to============
원격저장소(github)에 내 로컬에는 없는 파일이 있을 때 내 파일(작업 내용)을 push 할때 발생함 -> 로컬저장소에 pull을 하고 원격저장소에 다시 push를 하면 해결됨.

$ git pull origin master

$ git push origin mater
==================================================

--- branch : 다수의 협업자들의 프로젝트를 진행하기 편하게 하기 위함

-- 1. 협업자는 커밋에 올릴 branch 생성
-- 2. 자신이 만든 branch 생성
-- 3. branch에 커밋을 올림
-- 4. 코딩이 완료되면 branch를 모두 다 합침.

-- branch checkout
- bracnh를 이동하여 체크아웃을 할 수 있음.

-- branch 병합
- 여러 branch를 하나로 통합 할 수 있다.

- branch 병합 충돌
