
리덕스에서 비동기 처리

그냥 setTimeout을 이용해서 5초 뒤에 dispatdch를 해도 괜찮지만, 
만약 처리해야 하는 dispatch가 여러개라면, 처음에 실행된 것을 기준으로 5초 이후에 실행되어 마지막에 실행된건 화면에 보이지 않을 수도 있다. 

따라서 reducers에 id를 전달하여 실행 여부를 판별해야 한다. 이런 로직을 구현하려면 시간차를 고려한 별도의 함수가 필요하며, id 부여 함수에 dispatch 함수를 인자로 전달해야 한다(의존성 주입). store를 직접 참조하는 의존성 있는 함수로 정의하면 테스트가 어려워진다. 

대표적으로 사용하는 미들웨어가 redux-thunk, redux-saga 



---

Typescript + Redux

https://www.toptal.com/react/react-hooks-typescript-example

https://davevanhoorn.com/2020/01/converting-a-react-function-component-to-typescript/