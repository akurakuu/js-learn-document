# 02: ボタンをクリックした回数をJavaScriptでカウントする
HTMLではボタンを作成することができます。HTMLのみだとただの飾り同然ですが、JavaScriptによって意味を持たせることもできます。<br>

```html
<div>
    ボタンを押した回数:<span id="clickcount">0</span><br>
    <button id="button">クリック！</button>
</div>
```
上記のHTMLは、ボタンを押した回数と、押すためのボタンを表示するものです。<br>

JavaScriptでボタンに処理をつけるまでの処理の流れは以下の通りです。
1. HTMLの内、`button`タグを設置し、`id`を設定する
2. JavaScriptで`id`を指定した`button`を取得する。
3. 取得した要素にクリック時に実行する処理を設定する。

## 1, ボタンを設置して、idを設定する
次のように指定します。タグの中に好きな文字を入れることで、ボタンに表示することができます。<br>
```html
<button id="button">クリック！</button>
```

## 2, ボタンを取得する
```javascript
let element = document.getElementById('button');
```

## 3, 取得した要素に文字列を設定する
HTMLの要素に何か変化が起こった時の処理を指定するばあい、`addEventListener`を使用します。<br>
`addEventListener`で、ページのロード時、クリック時、キーボードが入力されたときなど、様々な仕掛けを作成することが可能です。<br>
```javascript
element.addEventListener('click', function() { // 'click'とすることで、クリック時の処理を指定することができます。
    // ここに処理を記述する
});
```

## 補足: 回数のカウント
ボタンをクリックした回数を変数に保存し、表示することで、ボタンをクリックした回数をカウントすることができます。<br>
カウントアップの方法は様々です。
```javascript
let count = 0;

count++; // カウントを1増やす(インクリメント)
count += 1; // カウントを1増やす(加算代入)
count = count + 1; // カウントを1増やす
```