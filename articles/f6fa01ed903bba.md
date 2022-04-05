---
title: "【JavaScript】関数まとめ"
emoji: "📘"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["JavaScript"]
published: false
---

# はじめに
JavaScriptの関数について学習した際の備忘録になります。

# 関数宣言の方法
JavaScriptにおける関数は
1. 関数名
2. 引数
3. 処理内容

の3つの部分からなる。
関数の定義の方法は、
1. 関数宣言
2. 関数式
3. アロー関数

の3種類が存在する。

## 関数宣言
次のような形で記述される。
```js
function 関数名(引数のリスト) {
    処理内容;
};
```
具体的には
```js
function increment(n) {
    return n+1;
};
console.log(increment(1));
```

## 関数式
```js
const 変数 = function (引数のリスト) {
    処理内容;
};
```

具体的には
```js
const increment = function(n) {
    return n + 1;
};
console.log(increment(1));
```

## アロー関数
```js
const 関数名 => (引数のリスト) => {
    処理内容;
};
```
具体的には、
```js
const increment = (n) => {
    return n + 1;
};
```