# web:dev

chart 數據要有值 port要3000 url: `http://localhost:3000`  

## Debug

> `web:dev: - error Failed to load next.config.mjs, see more info here https://nextjs.org/docs/messages/next-config-error`

apps/web/next.config.mjs

```js
// import { withWebSecurityHeaders } from '@pancakeswap/next-config/withWebSecurityHeaders'

export default withBundleAnalyzer(
  // withVanillaExtract(withSentryConfig(withAxiom(withWebSecurityHeaders(config)), sentryWebpackPluginOptions)),
  withVanillaExtract(withSentryConfig(withAxiom(config), sentryWebpackPluginOptions)),
)
```


## Menu

web/src/components/Menu/config/config.ts
