# 환경세팅 연습용 - 리액트와 스프링부트 함께 쓰기
[참고사이트](https://www.youtube.com/watch?v=1sw8UTWC8kc)

> 개발환경

IDE <br />
IntelliJ Community, Visual Studio Code

개발언어<br />
Java, JavaScript

프레임워크<br />
Spring Boot, React

---

## 1. IntelliJ 설치

[다운로드사이트](https://www.jetbrains.com/idea/)

[참고사이트](https://how-can-i.tistory.com/127)

<br />

<img width="682" alt="intelliJ 다운로드1" src="https://github.com/YoonHan0/java-study/assets/87405950/4eb2d5e1-8197-4100-8b08-be84fd899eb7">
<img width="450" alt="2" src="https://github.com/YoonHan0/java-study/assets/87405950/e9d4c705-2e58-4828-8f4e-945978072cae">

<br />
<br />
<br />

IntelliJ 설치 후, 실행을 했을 때 <br />
"응용프로그램이 응답할 수 없습니다." 라고 출력되면서 실행이 되질 않았는데 여러 방법들을 시도해 봤지만.. <br />
재부팅으로 해결이 되었다.

<img width="790" alt="3" src="https://github.com/YoonHan0/java-study/assets/87405950/dce562ee-fd76-4ea6-8310-434553774ad0">

<br />
<br />

## 2. Spring Initializr를 통한 프로젝트 생성

[프로젝트 생성 사이트](https://start.spring.io/)

<img width="622" alt="springboot 설정1" src="https://github.com/YoonHan0/java-study/assets/87405950/9e24e984-16fa-4ee2-9e9b-e82b51756543">

<br />
<br />
<br />

- dependencies 추가

<img width="564" alt="springboot2" src="https://github.com/YoonHan0/java-study/assets/87405950/3c8b81fc-d8a8-46c4-9c73-c3d3b11ae0b3">

<br />
<br />

## 3. IntelliJ 설정

File > settings > "gradle" 검색 <br />
IntelliJ IDEA 로 수정

<img width="1191" alt="springboot설정3" src="https://github.com/YoonHan0/java-study/assets/87405950/336d4858-c781-4320-af00-75eaa62e085d">

<br />
<br />
<br />

- main Application 실행

src > main > java > ExamApplication.java 실행

<img width="1351" alt="springboot 실행1" src="https://github.com/YoonHan0/java-study/assets/87405950/422ba3f3-23fc-49b2-a2fa-505b64660179">


<br />
<br />
<br />

- localhost:8080 확인

<img width="569" alt="springboot 실행2" src="https://github.com/YoonHan0/java-study/assets/87405950/969a9b5f-625b-43a3-baf3-0e58f5820143">

<br />
<br />

## 4. React 프로젝트 생성

``` shell
cd src/main
npx create-react-app front  # front: 프로젝트명
```

<img width="709" alt="springboot 실행3" src="https://github.com/YoonHan0/java-study/assets/87405950/d12c4d55-f53f-47cb-814a-df5a54fcb38b">


<br />
<br />
<br />

- localhost:3000 확인

``` shell
# 현재 path: src/main
cd front
npm start  # 프론트 프로젝트 실행
```

<img width="944" alt="react 실행1" src="https://github.com/YoonHan0/java-study/assets/87405950/2d2770b7-6e5f-4909-9551-7a6ae20504e2">

<br />
<br />
<br />

- proxy 설정

React 는 port 3000번이고, <br />
SpringBoot 는 port가 8080 이기때문에

연결하기 위해서 proxy를 추가해 주어야한다.

<img width="955" alt="proxy설정1" src="https://github.com/YoonHan0/java-study/assets/87405950/d0a2dfbe-1b69-44fb-a55e-a6c72f9de0e5">

<br />
<br />
<br />

- build.gradle 수정

[복사할 코드](https://developer-rooney.tistory.com/190)

1. 위 링크에서 코드를 복사한 후, build.gradle 파일에 코드 붙여넣기
2. 재빌드
   - 우측 gradle 아이콘 클릭
   - exam > Tasks > build > build(톱니바퀴) 더블 클릭

<img width="944" alt="build" src="https://github.com/YoonHan0/java-study/assets/87405950/de073363-23df-4c69-b4c2-a24f5c1e2817">

<br />
<br />
<br />

- build 후 main application 실행

main application 위치로 이동한 후, 실행

<img width="952" alt="build후 application 실행" src="https://github.com/YoonHan0/java-study/assets/87405950/836a053d-031f-4f89-b64d-90facabb0bef">

<br />
<br />
<br />

- `localhost:8080` 으로 접근했을 때 react 코드로 실행되는 화면이 나오는지 확인

<img width="924" alt="8080 확인" src="https://github.com/YoonHan0/java-study/assets/87405950/d37dbb3d-0db8-45bc-993d-20db84fefb53">
