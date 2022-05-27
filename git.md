
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