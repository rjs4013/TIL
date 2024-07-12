# 7/12 (Startcamp)


## Remote Repository(원격 저장소)

- 코드와 버전 관리 이력을 온라인 상의 특정 위치에 저장하여 여러 개발자가 협업하고 코드를 공유할 수 있는 저장 공간
- 대표적인 브랜드 → ‘Gitlab, Github, Bitbucket’

## git remote add origin remote_repo_url

- 로컬 저장소에 원격 저장소 추가
- origin → 추가하는 원격 저장소 별칭 , 바꿔도 됨
- remote_repo_url → 추가하는 원격 저장소 주소

## git remote -v

- 등록된 원격 저장소 목록 확인



# push/pull&clone


## git push origin master

- 원격 저장소에 commit 목록을 업로드
- “git아, push해줘  origin이라는 이름의 원격 저장소에 master라는 이름의 브랜치를”


> ***이미 로컬 저장소에 원격 저장소가 추가된 상태에서***
> 

- 파일 만들고 원격 저장소에 올리는 과정
1. **touch**
2. **git add** → staging area 로 이동
3. **git commit -m ‘name’** → repository로 이동
4. **git log** **--oneline** → 확인
5. **git push origin master →** 원격 저장소로  commit에 있는 목록 업로드

***원격 저장소에는 commit이 올라가는 것***

***→ commit 이력이 없다면 push 할 수 없다.***

## git pull origin master

- 원격 저장소의 변경사항만을 받아옴 (업데이트)

## git clone remote_repo_url

- 원격 저장소 전체를 복제 (다운로드)
- clone으로 받은 프로젝트는 이미 git init이 되어 있음
    
    **→  내가 있는 로컬에 .git 폴더가 있으면 안된다.**
    
- 새로운 프로젝트원이 왔을 때 원격 저장소에 있는 걸 clone 해서 로컬로 받아오는 느낌