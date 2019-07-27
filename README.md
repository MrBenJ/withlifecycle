# with-lifecycle-func

### Add a before and after logic to _any_ function

* Zero Dependencies
* Minimum Node version: `v8.x.x`
* Written in pure JS

## Installation
`npm install --save with-lifecycle-func`

## Usage and example
```js
const withLifecycle = require('with-lifecycle-func');

const sayHelloTo = friend => {
  console.log(`Hello ${friend}!`);
};

const before = () => {
  console.log('Looking for friend...');
  console.log('Seeing friend...');
  console.log('Contemplating existence of friend...');
  console.log('Notice friend!');
  console.log('Frantically approach friend with interpretive dance!');
};

const after = () => {
  console.log('Friend has been sucessfully greeted!');
  console.log('Return to take a nice nap.');
}

const findAndSayHelloTo = withLifecycle({
  before,
  after
})(sayHelloTo);

findAndSayHelloTo('Alex');
  // 'Looking for friend...'
  // 'Seeing friend...'
  // 'Contemplating existence of friend...'
  // 'Notice friend!'
  // 'Frantically approach friend with interpretive dance!
  // 'Hello Alex!
  // 'Friend has been sucessfully greeted!'
  // 'Return to take a nice nap.'
```

## Params and stuff



## More Super serious examples
