# study.nomad.reactjs-masterclass

## Create-React-App 프로젝트 생성

- Create-React-App 프로젝트를 먼저 만들고 TypeScript 를 나중에 추가하면 여러 에러가 발생되어 Create-React-App 프로젝트를 만들때 TypeScript 타입으로 지정하여 생성함.
- npx create-react-app my-app --template typescript
- 프로젝트내 불필요한 파일 삭제
- github repository 연동 (git init 할 필요없음)
  - git add
  - git commit
  - git remote add origin https://github.com/heejun/study.nomad.reactjs-masterclass.git
  - git branch -M main
  - git push -u origin main
- styled-components 설치
  - npm i --save-dev @types/styled-components
  - npm i styled-components

## VSCode Extentions

- [vscode-styled-components](https://marketplace.visualstudio.com/items?itemName=styled-components.vscode-styled-components)

## 3.2 Typing the Props

- TypeScript 에서는 component 와 styled-componet 에 props 을 전달할때 interface 를 사용하여 반드시 타입을 명시한다.

## 3.2 Optional Props

- ? 를 사용하면 optional type 이 되는데, 아래와 같은 방식으로 디폴트 값을 지정할 수 있다.
  - 함수 파라미터에 디폴트를 지정하는 방식 (이건 타입스크립트 문법이 아닌 ES6 문법)
  - ?? 연산자를 사용하는 방법

```
interface CircleProps {
  bgColor: string;
  borderColor?: string;
  text?: string;
}

function Circle({ bgColor, borderColor, text = "default text" }: CircleProps) {
  return (
    <Container bgColor={bgColor} borderColor={borderColor ?? bgColor}>
      {text}
    </Container>
  );
}
```

## 4.2 BrowserRouter

- install react router dom 6.4
  - npm i react-router-dom@6.4

# 5 CRYPTO TRACKER

- https://api.coinpaprika.com/
- https://tanstack.com/query/latest
- npm i @tanstack/react-query

## 5.1 Styles

- Reset CSS

  - https://github.com/zacanger/styled-reset/blob/master/src/index.ts

- Google Fonts

  - https://fonts.google.com

- Flat UI Color
  - https://flatuicolors.com/palette/gb

## 5.4 Route States

- https://cryptoicon-api.pages.dev/

## 5.6 Data Types

- VSCode 단축키
  Ctrl(Command)+D: 같은 문자열 선택
  Shift+Alt(Option)+i: 선택한 모든 문자열에 가장 우측 끝으로 포커싱
  Ctrl(Command)+Shift+오른쪽 화살표: 현재 선택한 문자열을 기준으로 우측 끝까지 문자열 선택

- 니꼬쌤 인터페이스 타입 정의
  https://github.com/nomadcoders/react-masterclass/commit/98646c226c0d2176a535dc43f4714099d2b9f1a8

- 노마드코더 코딩 인생 꿀템 VSC 단축키 5분 정리해드림
  https://www.youtube.com/watch?v=Wn7j5dfbJF4

- JSON데이터를 타입스크립트 타입으로 빠르게 변환시켜주는 사이트
  https://app.quicktype.io/?l=ts

## 5.7 Nested Routes part One

- https://ui.dev/react-router-nested-routes/

## 5.9 React Query part One

- "react-query" 대신 "@tanstack/react-query" 사용

## 5.10 React Query part Two

- npm i -D @tanstack/react-query-devtools

## 5.13 Price Chart part Two

- https://apexcharts.com/
- npm install --save react-apexcharts apexcharts

## 5.15 Final Touches

- React Helmet
  - head 내용 변경시 사용
  - https://www.npmjs.com/package/react-helmet
  - npm i react-helmet
  - npm i --save-dev @types/react-helmet

## 7.7

- npm i gh-pages
- npm run build
- [package.json] "homepage": "https://heejun.github.io/study.nomad.reactjs-masterclass"
- npm run deploy
- 이렇게 해도 계속 404 에러페이지가 나와서 확인결과 github repository를 public 으로 설정해야 함
- github 설정 참고: https://www.youtube.com/watch?v=7wzuievFjrk

# 6 STATE MANAGEMENT

## 6.2 Introduction to Recoil

- https://recoiljs.org/ko/
- npm install recoil
- useRecoilState
- useSetRecoilState
