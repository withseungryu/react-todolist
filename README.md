### TODO LIST 만들어보기  React with Typescript

React의 작업 단위 = Component

Component Tree => Dom Tree (Virtual DOM 사용)

기본적으로 JSX 문법 사용하지만, Typescript를 사용 할 것이기 때문에 TSX문법, 즉 확장자는 tsx가 될 것이다.

데이터가 변하면 다시 render를 호출해서 그려준다.

-  render가 호출되고, 재호출되는 지점을 파악
-  render를 JSX로 표현
-  데이터와 JSX가 합쳐져 하나의 컴포넌트를 이룸.

### 시작

참조 영상 : https://www.youtube.com/watch?v=ODvirqIC09A 

프로젝트 만들기

`yarn create react-app [프로젝트 명] --typescript`

or

`npx create-react-app [프로젝트 명] --typescript`

`yarn start` or `npm start` 를 하면 아래와 같은 기본 페이지를 볼 수 있다.

기본적인 페이지를 없애고 새로운 페이지를 만들어보자

`rm App.css App.test.tsx index.css logo.svg serviceWorker.ts`

하고, 

App.tsx 파일을 아래 예시와 같이 바꿔주고, 

```tsx
import React from 'react';
import logo from './logo.svg';
import './App.css';

function App() {
  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>
          Edit <code>src/App.tsx</code> and save to reload.
        </p>
        <a
          className="App-link"
          href="https://reactjs.org"
          target="_blank"
          rel="noopener noreferrer"
        >
          Learn React
        </a>
      </header>
    </div>
  );
}

export default App;

```

```tsx
import React from 'react';

function App() {
  return (
   <div>Hello World</div>
  );
}

export default App;

```

index.tsx 파일도 아래 예시와 같이 바꿔주자

```tsx
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';
import * as serviceWorker from './serviceWorker';

ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById('root')
);

// If you want your app to work offline and load faster, you can change
// unregister() to register() below. Note this comes with some pitfalls.
// Learn more about service workers: https://bit.ly/CRA-PWA
serviceWorker.unregister();

```

```tsx
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';

ReactDOM.render(
    <App />,

  document.getElementById('root')
);

```

