# Base64<br>
HSPでBase64エンコード（デコード）を使えるようにするモジュールです。
数値型変数（配列）、実数型変数（配列）、文字列型変数に対応しています。
<pre>
例：
"abcdefghijklmn123456789"
↓エンコード
"hJ2YkVmZnhWaqtGbt5WMyMDN1YzN4kD="
</pre>

## 使い方
「base64.hsp」を、使用するソースコードと同じフォルダ内に置くか、HSP のインストールディレクトリ下の commonフォルダ内に置いてください。

あとはソースコードの先頭に
<pre>
#include "base64.hsp"
</pre>

と書けばOKです。

## 関数一覧
### エンコード
#### val = b64en(p1, p2)
val = Base64文字列
p1 = 変換元データ
p2 = 変換元文字列のバイト長（省略可）

「encodedt = b64en(dt)」と書くと、「encodedt」変数に「dt」変数の中身をエンコードした文字列を設定します。


### デコード
#### b64de p1, p2
p1 = 変換先データ
p2 = Base64文字列

「b64de decodedt,encodedt」と書くと、「decodedt」変数に「encodedt」変数の中身をデコードした文字列を設定します。
この時設定されるデータ型は「decodedt」変数の型に依存します（数値型配列の場合は数値型配列として設定される）。