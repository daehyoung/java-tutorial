
## git 이란
소스 버전 관리(형상관리) 툴 이다.

svn, cvs, git등 다양한 버전관리 툴이 존재하는데 현재 가장 많이 사용되는 버전 관리 툴은 git이다.

###
버전의 변경 히스토리를 가지고 있다.

### git 설치
git 다운로드 설치한다.

### 초기화
git init 

### 원격 저장소 확인
git remote -v

### 원격 저장소 추가
git remote add https://github.com/daehyoung/spring-cloud-stream.git

### 소스코드 다운로드
git clone https://github.com/daehyoung/spring-cloud-stream.git

### 현재 상태
git status

### 현재 변경 사항 추가
git add .

### 커밋 변경사항 기록
git commit -m "변경 사항 설명"

### 원격 저장소 전송
git push origin master


### 특정 버전으로 작업하기
git checkout  ${hash}

git checkout 1f8cfd0e913273f44999b3931b19ff4d62e6790d


### 초기버전 작업 
git checkout 28fcb8e0f6c4e947ba65882483bc7f77fda039c3


### 마지막 버전 작업
git checkout 32aec69bbf1c6458708b33985afb706b8de039d3



## 커밋 stage에 추가 
- 쇼핑 카트에 아이템을 추가하듯이 커밋 할 목록에 파일을 추가한다.
git add <file>

git commit -m "변경 내용 기록"


## 커밋 stage에서 제거
- 쇼핑 카트에서 아이템을 제거하듯이 커밋 할 목록에서 파일을 제외한다.
git restore --staged <file>


## 변경사항을 버리고 이전 버전으로 되돌리기
- 현재 변경 사항을 버리고 이전 상태로 되돌리기
git restore  --worktree <file>
git restore --staged --worktree <file>

## 다시체크아웃 하기
git checkout -- CONTRIBUTING.md



## log
git log


## 작업중인 버전 확인
git worktree list


## 상태
Committed, Modified, Staged

- Modified(수정됨) - worktree
- Staged(커밋 대상) 
- Committed(로컬 리포지토리에 저장됨)


## 설정 보기
git config --list

## 도움말 보기
git help

## 버전 시스템에 파일 추가 
git status
Untracked files




## 변경사항 보기
git diff --staged


## 파일 삭제 및 버전 관리시스템에서 제거

git rm <target>


## 파일 이름 변경하기
git mv <source> <target>



git log --grep test
git log --committer daehyoung
git reflog


## 이전 커밋 수정
git add <file>
git commit --amend

## staged 파일 전체 비우기
git reset HEAD 

## staged 파일 하나만 비우기
git reset HEAD <file>


## 삭제하지 않고 버전관리 시스템에서만 제거
git update-index --skip-worktree  <file>

## 이전 커밋 수정
git add <file>
git commit --amend

## staged 파일 전체 비우기
git reset HEAD 

## staged 파일 하나만 비우기
git reset HEAD <file>


## 내 로컬의 변경 리스트 보기  
git ls-files --modified

## skip worktree 목록 보기 
git ls-files -v . | grep ^S

## 특정 파일 skip worktree 에 포함시키기 
git update-index --skip-worktree <file>

## 현재 로컬 변경 리스트에 있는거 전부 skip worktree 에 포함시키기
git update-index --skip-worktree $(git ls-files --modified)

## 특정 파일 skip worktree 에서 되돌리기
git update-index --no-skip-worktree <file>

## 모든 파일 skip worktree 에서 되돌리기
git ls-files -v | grep -i ^S | cut -c 3- | tr '\012' '\000' | xargs -0 git update-index --no-skip-worktree

