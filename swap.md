# Swap

packages/uikit/src/components/Chart/PairPriceChart.tsx

```
import LineChartLoader from "./LineChartLoaderSVG";
{!chartCreated && <LineChartLoader />}
<div style={{ flex: 1, maxWidth: "100%" }} ref={chartRef} id="swap-line-chart" {...rest} />
```

uikit/src/components/Chart/index.ts  
`export * from "./PairPriceChart";`

apps/web/src/views/Swap/components/Chart/BasicChart.tsx

```
import { useFetchPairPricesV3 } from 'state/swap/hooks'
  const { data: pairPrices = [] } = useFetchPairPricesV3({
    token0Address,
    token1Address,
    timeWindow,
    currentSwapPrice,
  })

 <ButtonMenu activeIndex={timeWindow} onItemClick={setTimeWindow} scale="sm">
    <ButtonMenuItem>{t('24H')}</ButtonMenuItem>
    <ButtonMenuItem>{t('1W')}</ButtonMenuItem>
    <ButtonMenuItem>{t('1M')}</ButtonMenuItem>
    <ButtonMenuItem>{t('1Y')}</ButtonMenuItem>
  </ButtonMenu>
</Box>

       <SwapLineChart
          data={pairPrices}
```

Swap/components/Chart/PriceChart.tsx

````js
import BasicChart from './BasicChart'
      <BasicChart
        token0Address={token0Address}
        token1Address={token1Address}
````


web/src/views/Swap/components/Chart/PriceChartContainer.tsx

```
  const token0Address = inputCurrency?.wrapped.address?.toLocaleLowerCase()
  const token1Address = outputCurrency?.wrapped.address?.toLocaleLowerCase()

    <PriceChart
      token0Address={isPairReversed ? token1Address : token0Address}
      token1Address={isPairReversed ? token0Address : token1Address}
      inputCurrency={isPairReversed ? outputCurrency : inputCurrency}
```


apps/web/src/views/Swap/index.tsx

```
import PriceChartContainer from './components/Chart/PriceChartContainer'
import { currencyId } from 'utils/currencyId'

  const {
    [Field.INPUT]: { currencyId: inputCurrencyId },
    [Field.OUTPUT]: { currencyId: outputCurrencyId },
  } = useSwapState()

          <PriceChartContainer
            inputCurrencyId={inputCurrencyId}
            inputCurrency={currencies[Field.INPUT]}
```


apps/web/src/utils/currencyId.ts

```js
export function currencyId(currency: Currency): string {
  if (currency?.isNative) return currency.symbol?.toUpperCase()
```
