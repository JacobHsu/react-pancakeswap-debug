> TypeError: Cannot destructure property 'isInitialized' of 'Object(...)(...)' as it is undefined.

state\profile\hooks.ts

```js
export const useProfile = () => {
  const { isInitialized, isLoading, data, hasRegistered }: ProfileState = useSelector((state: State) => state.profile)
  return { profile: data, hasProfile: isInitialized && hasRegistered, isInitialized, isLoading }
}
```

state\index.ts

```js
const PERSISTED_KEYS: string[] = ['user', 'profile'];
const store = configureStore({
  devTools: process.env.NODE_ENV !== 'production',
  reducer: {
    profile: profileReducer,
```
