# Movie App 2020

# Do it! 클론 코딩 영화 평점 웹서비스

#### 명령어
- node -v 
    - node.js 버전 확인 
- npm -v
    - npm 버전 확인
    - 자바스크리브를 위한 package(module) 관리자
- npm install npx-g 
    - npm으로 npx 전역 설치 
    - npm의 레지스트리의 package 사용 경험을 파악하기 위한 도구 
    - 최신버전에 해당하는 package를 설치하여 실행하고, 실행 이후 해당 package 제거
- git --version 
    - git 버전 확인 
- create-react-app 
    - 페이스북에서 개발한 react 웹 개발용 boilerplate 
    - create-react-app 프로젝트의 구조를 사용 
- npm start 
    - package.json의 scripts에 있는 start 명령어 실행 
- npm install prop-types
    - npm으로 prop-types 설치 
    - props 자료형 검사 도구 
    - 컴포넌트가 전달받은 props의 값 확인
- npm install axios 
    - npm으로 axios 설치
    - HTTP Client 라이브러리로써 비동기 방식으로 HTTP 데이터를 요청해 실행 
    - XMLHttpRequest를 직접적으로 다루지 않고 AJAX 호출 가능
- npm install react-router-dom
    - npm으로 react-router-dom 설치 
    - 화면전환을 도와주는 역할
    - a tag를 사용해 화면을 전환하는 일반적인 웹과는 달리 react-router를 사용해 Link 태그를 통해 화면 전환 
    - 사용자에게 새로고침, 뒤로가기, 즐겨찾기 등의 기능을 제공하기 위해 사용 
- npm install gh-pages 
    - npm으로 gh-pages 설치
    - github 저장소를 이용해 웹 사이트를 무료로 호스팅해주는 서비스 
#### 코드

```sh
<div id="root"></div>
```

```sh
ReactDOM.render(<App />, document.getElementById('root'));
```
- `<App/>`을 `ReactDom.render()`의 첫 번째 인자로 전달하면 `<App/>` 컴포넌트가 반환하는 것들을 그릴 수 있음 

- `ReactDom.render()`의 두 번째 인자는 `<App/>` 컴포넌트가 그려질 위치를 의미 

```sh
import React from 'react';
```
- react가 JSX를 이해하기 위한 import 

```sh
render()
```
- 클래스형 컴포넌트에서 JSX를 반환하기 위해 사용
- 함수형 컴포넌트의 경우 return문으로, 클래스형 컴포넌트의 경우 render() 함수로 JSX 반환 

```sh
setState()
```
- state 객체의 내용 변경 후 render() 자동호출 
- setState() 함수에서 새로운 state 전달 시 state 업데이트
- state 업데이트 이후 render() 함수 자동실행 

```sh
construtor()
```
- 가장 먼저 실행 
- Component를 생성할 때 state를 초기화하거거나 method를 바인딩할 때 사용 
- state 값 초기화 시 setState() 대신 this.state 사용 
- super(props)선언 권고 

```sh
componentDidMount() 
```
- 컴포넌트가 처음 화면에 그려지면(render 호출) 실행되는 함수 
```sh
{ moives : movies } == { moives }
```
- ES6에서는 객체의 키와 대입할 변수의 이름이 같다면 코드 축약 가능 

#### 개념 
- props 
    - 컴포넌트에서 컴포넌트로 전달하는 데이터 
    - 컴포넌트를 효율적으로 재사용할 수 있음 
    - props에 있는 데이터는 문자열인 경우를 제외하면 모두 중괄호{}로 값을 감싸야함 
- key 
    - 리스트 각 원소는 유일한 key props를 가져야 함 
    - 리스트의 원소인 컴포넌트가 서로 다른 존재임을 명시 
- state
    - 동적 데이터를 다룰 때 사용
    - props로는 다룰 수 없음 
    - state가 변경되면 render() 함수를 다시 실행해 변경된 state를 화면에 출력하지만 state를 직접 변경하는 경우에는 render() 함수를 다시 실행하지 않기 때문에 state를 직접 변경할 수 없도록 함 
    - state 변경 시 setState() 함수를 통해 변경해야함
    - setState() 함수로 state 변경 시 변경되지 않은 데이터는 그대로 유지하고 변경된 데이터만 변경하며 새로 생성한 데이터의 경우 업데이트 
