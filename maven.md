## maven 설정하기
spring boot를 사용하여 자바 개발하다보면 필수 적으로 maven을 사용하게 된다. 
그래서 먼저 maven 설정에 대해 간단하게 알아보도록 한다.

### maven 자장소
메이븐 저장소는 사용자 홈 디렉토리에 보이지 않는 숨겨진 디렉토리 이다.
'.'으로 시작한다.

#### linux, mac os
linux나 mac os의 경우 사용자 홈 디렉토리에 위치한다.
cd ~/.m2
```
~/.m2
```

settings.xml

```
mvn clean
```
빌드 결과(target) 디렉토리를 삭제한다.

maven은 pom.xml 파일이 프로젝트 파일이다

디렉토리 구조가 정해져 있다.

src/main/java
src/main/resources

src/test/java
src/test/resources

