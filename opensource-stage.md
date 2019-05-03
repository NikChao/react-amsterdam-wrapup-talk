# React Async

- Built around promises - handing all states
- deals with cancelling/aborting requests
- defer execution of promises

```jsx
<Async promiseFn={fetchPokemon}>
  <Async.Fulfilled>
    {data => <p>{data}</p>}
  </Async.Fulfilled>
</Async>
```

```jsx
const { data } = useAsync({ promiseFn: fetchPokemon })
```

# microjob
```js
import { job } from  'microjob';

job((function () {
  // runs as worker thread
  // sync and async
  // TS Support
})())
```


# URQL

- graphql client
- react first
- extensibility

- debugging
- cache
`yarn add urql`