# Syntax Tricks

## Short-circuiting

1. Initializing values with default value (using OR `||` operator)

```js
/* Ternery form */
const a = something ? something : defaultValue;

/* OR operator short-circuited form */
const a = something || defaultValue;
```

Hint: this means that if `something` is in a `false` state (such as `undefined`, `null`, `0`(number zero), `''` (empty string)), then it will assign the `defaultValue` to the constant `a` instead of `something`

2. Assign value if condition is satisfied (using AND `&&` operator)

Sometimes in React JSX, if we try to use conditional rendering:

```js
class Title extends React.Component {
  render() {
    const { show } = this.props;
    return (
      <div>
        { show ? <h1>Title</h1> : undefined }
      </div>
    );
  }
}
```

You can instead use short-circuited syntax to replace the ternery operator, it means that if `show` is `true`, then return the latter value which is the JSX `<h1>Title</h1>`:

```js
class Title extends React.Component {
  render() {
    const { show } = this.props;
    return (
      <div>
        { show && <h1>Title</h1> }
      </div>
    );
  }
}
```

## Number Range Conditioning

Plain old way is to use the `if...else...` statement:

```js
if (num > 1000) {
  console.log('Huge Number');
} else if (num > 500) {
  console.log('Big Number');
} else if (num > 100) {
  console.log('Medium Number');
} else {
  console.log('Small Number');
}
```

Another way is to use the `switch...case...` statement in another style:

```js
switch (true) {
  case num > 1000: console.log('Huge Number');   break;
  case num > 500:  console.log('Big Number');    break;
  case num > 100:  console.log('Medium Number'); break;
  default:         console.log('Small Number');
}
```

(Personally I don't bother to use the `if...else...` statement, it depends on how you feel to program in this case.)
