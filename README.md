# safe-callback

Simple callback wrapper that always causes a function to be "callable." 

## Usage

```js
const safe = require('safe-callback');

function foo(callback) {
  const safe_callback = safe(callback);
  safe_callback();
}

// works!
foo(err => { console.log("bar"); });

// still works!
foo(null);
```