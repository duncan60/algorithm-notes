# pascal Triangle

規則

rC0 = 1

rCn = rCn-1 * (r - n + 1) / n


Javascript:

```js
const combi = (r, n) => {
    if(n == 0) {
        return 1;
    } else {
        return combi(r, n - 1) * (r - n + 1) / n;
    }
}

const pascalTriangle = (height) => {
    return Array.from({length: height}, (val, r) => {
         return Array.from({length: r + 1}, (val, n) => combi(r, n));
    });
}

pascalTriangle(8).map((item) => {
    console.log(item);
});
```
[JS Bin Demo](https://jsbin.com/yasacag/edit?js,console)
