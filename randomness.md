# Randomness

## Generating random integer from *min* ~ *max* values

### Answer

1. Simpliest but not *truely* random, I guess ¯\_(ツ)_/¯
```js
const random = Math.floor(Math.random() * (max - min + 1)) + min;
```

2. Seedable number generator: **Mersenne-Twister**

See gist: https://gist.github.com/banksean/300494

**[TODO]** I've never tried this, find time to inspect the method and add description.
