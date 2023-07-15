# 01: JavaScriptで任意の文字列を表示する
JavaScriptではHTMLのDOMを操作して、動的に任意の文字列を表示することができます。<br>
このサンプルでは、JavaScriptで任意の文字列を表示する方法を紹介します。
```html
<div>
    世界の人口は
    <span id="population"></span>
    人です。
</div>
```
上記のHTMLは、人口を表示するというものです。`span`タグに人口を表示することにします。<br>

JavaScriptで文字列を表示させるまでの処理の流れは以下の通りです。
1. HTMLの内、表示させたい文字列を表示する場所に要素を置き、`id`を設定する
2. JavaScriptで`id`を指定した要素を取得する。
3. 取得した要素に文字列を設定する。

## 1, 要素をおいて、idを設定する
次のように指定します。要素の種類は何でも構いませんがサンプルではspanになっています。<br>
```html
<div id="population"></div>
```

## 2, 要素を取得する
JavaScriptで要素を取得するには、`document.getElementById`を使用します。<br>
`document.getElementById`は、`id`を指定して要素を取得することができます。<br>
```javascript
let element = document.getElementById('population');
```

## 3, 取得した要素に文字列を設定する
取得した要素に文字列を設定するには、`innerText`を使用します。<br>
`innerText`は、要素の中身を設定することができます。<br>
```javascript
element.innerText = '1000万人';
```