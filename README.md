# ***7/11 Startcamp***
## **MARKDOWN**
1. 일반 텍스트로 문서를 작성하는 방법

2. 작성된 Markdown 문서는 다른 프로그램에 의해 변환되어 출력

3. Code block & Inline code block
- ``` 과 `의 차이 구분하기 # 본문에서 함수활용 시 사용

- [단어](주소) -> 링크연결

- ![단어](주소) -> 이미지 삽입

- **이미지의 너비와 높이는 markdown으로 조절할 수 없고 HTML 사용 필요**

## **CLI**
- 명령어를 통해 사용자와 컴퓨터가 상호 작용하는 방식
## **GUI**
- 그래픽을 통해 사용자와 컴퓨터가 상호 작용하는 방식

## **CLI에서 ‘.’의 역할**
- . → 현재 디렉토리 , .. → 현재의 상위 디렉토리(부모 폴더)
- cd . → 현재 폴더 , cd .. → 현재의 상위 폴더

- 위에서 아래 폴더로 내려갈 땐? → cd 가야할 폴더 ex) 내가 바탕화면이라면 → cd layer 1/layer 2

-  layer 2에서 바탕화면으로 갈 땐? →  cd ../..

## **CLI 기초 문법**
- **touch** - 파일 생성, **mkdir** - 새 디렉토리 생성, **ls** - 현재 작업 중인 디렉토리 내부의 폴더/파일 목록 출력

- **cd** - 현재 작업 중인 디렉토리를 변경, **start** - 폴더/파일 열기,  **rm** - 파일 삭제

- 디렉토리를 삭제하고 싶으면 **rm -r 디렉토리명**

- **code 파일명**

---
***CLI에서 가장 중요한 건 내가 어디 있는지(경로)를 알아야 한다.***
---

## **절대 경로**
- Root 디렉토리부터 목적 지점까지 거치는 모든 경로를 전부 작성한 것

- **pwd (print working directory)** 쓰면 보여줌

## **상대 경로**
- 현재 작업하고 있는 디렉토리를 기준으로 계산된 상대적 위치를 작성한 것

- ex) 현재 작업하고 있는 디렉토리가 C:/Users일 때 윈도우 바탕 화면으로의 상대 경로는

ssafy/Desktop

---

# **‘Git ‘**
- ***분산 버전 관리*** 시스템

- 코드의 변경 이력을 기록하고 협업을 원활하게 하는 도구

## **버전 관리**
- 변화를 기록하고 추적하는 것

- 롤백이 가능하다는 장점

## **중앙 vs 분산**
- **중앙집중식**

    - 버전은 중앙 서버에 저장되고 중앙 서버에서 파일을 가져와 다시 중앙에 업로드
- **분산식**

    - 버전을 여러 개의 복제된 저장소에 저장 및 관리

## **분산 구조에서의 장점**

- 중앙 서버에 의존하지 않고도 동시에 다양한 작업을 수행할 수 있음

    - 여러 개발자 동시 작업 가능, 작업 충돌 줄여줌

- 백업, 복구 용이

- 인터넷에 연결되지 않은 환경에서도 작업을 계속할 수 있음

    - 변경 이력을 로컬 저장소에 넣어두고 나중에 중앙 서버와 동기화

## Git의 3가지 영역

1. **Working Directory**

    - 실제 작업 중인 파일들이 위치하는 영역
2. **Staging Area**

    - Working Directory에서 변경된 파일 중, 다음 버전에 포함 시킬 파일들을 선택적으로
    
    추가하거나 제외할 수 있는 중간 준비 영역
    
3. **Repository (저장소)**

    - 버전 이력과 파일들이 영구적으로 저장되는 영역으로 모든 버전과 변경 이력이 기록됨

    - 버전을 찍는다 → **commit**
    
        - commit? → 변경된 파일들을 저장하는 행위

---
# GIT 동작
## Git init

- 로컬 저장소 설정(초기화)
    
    → git의 버전 관리를 시작할 디렉토리에서 진행
    

## Git add

- 변경사항이 있는 파일을 staging area에 추가
- git add *.txt
- git add .
- git add 파일명

## Git commit

- staging area에 있는 파일들을 저장소에 기록

    - 해당 시점의 버전을 생성하고 변경 이력을 남기는 것

- git commit -m “입력 메시지”

git config --global user.email "[rjs401323@gmail.com](mailto:rjs401323@gmail.com)"  ***# 사용자 정보 등록***

git config --global [user.name](http://user.name/) "rjs4013" ***# 사용자 정보 등록***

git commit -m 'first commit’

git log ***# repository에 있는 commit 확인***

git log --oneline ***# 한 줄 씩 출력***

git config --global -l ***# 현재 사용자 정보 확인***

---
***HEAD는 제일 최신의 commit을 따라 움직인다.***

## **git commit --amend**    →  commit 수정하기

- 이거는 commit 하고나서 바로 직후에만 사용가능함.

## **commit 메시지 수정**

1. commit의 hash값 확인
2. git commit --amend
3. i 눌러서 insert 상태로 만들고 수정하기
4. 수정완료되면 “:wq” 로 편집상태 빠져나오기
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