# fibonacci sequence
規則

  F0 = 0
  
  F1 = 1
  
  Fn = Fn-1 + Fn-2 (fn 表費氏數列的第 n 項的值）

Javascript:

```js
const fibonacci = (len, init = 1) => {
    return Array.from({length: len - 2}).reduce(
        (prevVal, elem, index) => {
            return [
                ...prevVal,
                prevVal[index + 1] + prevVal[index]
            ];
        },
        [init, init + 1]
    );
};

for (const [index, elem] of fibonacci(10).entries()) {
    console.log(`第${index}個月,兔子有${elem}對`);
}
```
[JS Bin Demo](http://jsbin.com/momalu/edit?js,console)
## 參考資源
[費式數列](http://openhome.cc/Gossip/AlgorithmGossip/FibonacciNumber.htm)

[好神的費式數列](http://blog.xuite.net/windyku0601/wretch/97914546)

[費式數列 PDF](http://www.shs.edu.tw/works/essay/2008/03/2008032822231396.pdf)


