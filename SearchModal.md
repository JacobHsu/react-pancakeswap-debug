> TypeError: Cannot read properties of undefined (reading 'background')

push../node_modules/@pancakeswap/uikit/dist/index.esm.js.Modal
var theme = _a.theme;
> 4403 |     return theme.modal.background;

src\Providers.tsx

```js
import { light } from 'npm-react-uikit' // '@pancakeswap/uikit'
```

pancake-toolkit\packages\pancake-uikit\src\theme\light.ts

```js
import { light as lightModal } from "../widgets/Modal/theme";
const lightTheme: DefaultTheme = {
  modal: lightModal,
```

src\widgets\Modal\theme.ts

```js
export const light: ModalTheme = {
  background: lightColors.backgroundAlt,
};
```
