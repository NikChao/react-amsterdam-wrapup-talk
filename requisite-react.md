# Requisite react: Kent C Dodds

1. Kent can fix faucets
2. The better you understand your abstractions the better you can use them
3. `youdontneedjquery.com` used as an example

- All abstractions have a cost
- Be mindful of your abstractions, and ask yourself
  - what is the cost
  - what is the benefit

- babel repl jsx will show you:
```jsx
import React from 'react';

let ui

ui = <div id='root'>Hello world</div>

// elementType, props, ...children
ui = React.createElement('div', { id: 'root' }, 'Hello world')
/**
Returns
{
  type: 'div',
  key: null,
  ref: null,
  props: { id: 'root', children: 'Hello world' },
  ...
}
*/
```

*Takeaway:* Play with babel repl to understand what's happening under the hood

If you want to get better at JS, implement lodash, went through hooks impl example

learn your abstractions, read source, don't be afraid of node_modules

### Resources:
- github.com/kentcdodds/requisite-react
