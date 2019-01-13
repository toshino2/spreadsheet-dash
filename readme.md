# スプレッドーシート ボタン
スプレッドシートにデータを記録するプログラムです。
## googleフォームを利用します
このプログラムを使うにはgoogleフォームとの連携が必要です。
## googleフォームを作成します。
<img width="812" alt="2019-01-13 15 22 27" src="https://user-images.githubusercontent.com/28776859/51082270-18574480-1747-11e9-8e91-0fca5b20dccc.png">
上記のようなフォームを作成します。
時間は自動で記録されますので項目を追加する必要はありません。
ボタンの名前等を記録するためのテキストフィールドを作成します。他にも情報を載せたい場合は項目をついかすることも可能です。(このプラグラムでは機能として搭載してはいません。)

## フォームから送信先と、inputのname名を取り出す
フォームを完成させたら、フォームの送信ページでフォームの値を入手する必要があります。
デベロッパーツールでフォームのactionの値と、inputのnameの値を取り出してください。

form actionの値
<img width="1084" alt="2019-01-13 15 29 23" src="https://user-images.githubusercontent.com/28776859/51082334-60c33200-1748-11e9-8483-d87ed10116b9.png">

input nameの値
<img width="1070" alt="2019-01-13 15 34 45" src="https://user-images.githubusercontent.com/28776859/51082365-e941d280-1748-11e9-914e-5c6fd9f98887.png">


## 以下の箇所を取得したデータに書き換えてください。
```html
//googleフォーム actionの値を入力してください
var formAction = "https://docs.google.com/forms/d/e/[key]/formResponse";
``` 
上記「formAction」にactionの値を入力

```html
//googleフォーム nameの値を入力してください
data: { "entry.xxxxxx" : field1 },
``` 
上記「entry.xxxxxx」をnameの値に書き換え


