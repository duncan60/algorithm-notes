# hanoi tower
規則
 - 先把 n-1 個盤全部移到 「暫存柱」
 - 再把 第 n 個盤 移動到 「目標柱」
 - 最後，把放在「暫存柱」的所有盤全部移到「目標柱」

Javascript:

```js
const hanoi = (n, a, b, c) => {
    if(n === 1) {
        return [{from: a, to: c }];
    }
    return [
        ...hanoi(n - 1, a, c, b),
        ...hanoi(1, a, b, c),
        ...hanoi(n - 1, b, a, c)
    ];
};
    

for (const [index, elem] of hanoi(3, 'A', 'B', 'C').entries()) {
    console.log('盤從 ' + elem.from + ' 移至 ' + elem.to);
}
```
[JS Bin Demo](http://jsbin.com/sotoki/edit?js,console)
## 參考資源
[河內塔](http://openhome.cc/Gossip/AlgorithmGossip/HanoiTower.htm)

[河內塔-遞迴](http://finalfrank.pixnet.net/blog/post/18372611)
