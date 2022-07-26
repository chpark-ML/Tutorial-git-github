# Git과 Github!

***

### README.md 
*.md > markdown 확장자*

***
### 지역 저장소 생성 
git init
git config (--global) user.name ["name"]
git config (--global) user.email ["email"]

***
### 지역 저장소에 원격 저장소 주소 등록
git remote add [origin, 원격저장소 식별 이름]

***
### 지역 저장소 --> 원격 저장소 (push)
git add [파일명] : 파일을 커밋에 포함될 파일로 등록 (스테이징 영역으로 이동)

git commit (지역 저장소에 저장)
 -m : 생성하는 커밋의 메세지를 작성하는 기능 제공
 abc

git push [origin, 리모트 저장소 이름] [main, 리모트 저장소의 브랜치 이름] (원격 저장소에 반영)

***
### 원격 저장소 --> 지역 저장소 (clone, pull)

***
### 프로젝트의 현재 파일 상태 확인
git status

***
### 깃 작업 트리
1. 작업 디렉토리 (untracked)
2. 스테이징 영역 (tracked/unmodified <-> tracked/modified)
3. 지역 저장소

***
### Commit
git log : 현재 작업하는 브랜치의 커밋 로그를 확인할 수 있습니다.\
>-p\
>-[숫자]\
>-p -[숫자]\
>--stat\
>--pretty=oneline --graph\

HEAD : 현재 작업하는 브랜치의 최종 커밋을 가리킵니다. (현재 작업의 최종 커밋)\

git commit --amend : 마지막 커밋 메시지 수정\
git commit --amend -m ["내용"]\

git commit --amend --no-edit : 커밋내용 그대로하고 해당 파일 내용만 수정\
git commit --amend --author "username <email>" : 커밋마다 저자 정보가 등록됨, 해당 저자 정보를 수정\


### Branch
git log --pretty=oneline --graph\
git remote update\
git branch \
>-a : 지역 저장소와 원격 저장소의 브랜치 정보 확인\
>-d : ["브랜치"] : 브랜치 삭제 (git push origin -d ["브랜치"])\
>-l : 지역 저장소의 브랜치 정보를 보여줍니다. (옵션 없이 실행하는 것과 동일)\
>-r : 원격 저장소의 브랜치 정보를 보여줍니다.\
>-v : 지역 저장소의 브랜치 정보를 최신 커밋 내역과 함께 보여줍니다.\
    git checkout : 사용할 브랜치를 지정\
>-b \
>-t ["브랜치"] : 생성한 브랜치를 지역 저장소의 작업 브랜치로 설정 # remotes 접두사 제외하고 명령어를 실행\

git merge ['branch']
