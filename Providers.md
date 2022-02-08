src\Providers.tsx

ts `@types/react-redux` 與 `react-redux` 是一組的

@pancakeswap/uikit 會與 styled-components 搭配使用

```js
 "@pancakeswap/uikit": "^0.63.1",
 "@types/styled-components": "^5.1.18",
 "styled-components": "^5.3.3",
```

> Property 'store' is missing in type '{ children: Element; }' but required in type '{ store: Store<any, AnyAction>;

[@reduxjs/toolkit](https://redux-toolkit.js.org/)

`const Providers: React.FC<{ store: Store }> = ({ children, store }) => {`  
```js
import store from './state'
const Providers: React.FC = ({ children }) => {
```

