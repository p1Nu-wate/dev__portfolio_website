覚えること！

ーーーgulp編ーーー

初めの1回目にやること！
npm i →node_modulesと書くプラグインを入れる意味！これがないと動かない。。。。

それ以降は
npx gulp →gulpを起動しますよー！という意味

でオッケ！

ーーー作業ファイル編ーーー
src/assetsを編集していきましょ！

img→写真を入れる！
js→適当に書く
sass→sassを書く

それらを編集したら自動でassetというファイルにコンパイルされます！
htmlやcssで相対パスを書くときはassetsじゃなくassetから辿るようにしましょ！

ーーーsass編ーーー
fundationにベース系(htmlやbody、reset.cssなど)
layoutにheaderやfooter
mixinはmixin置き場
pageは各ページのレイアウト、これを追加で書くことが多い
settingは各変数置き場として

上記のように作成しています。

新しくpage(scss)を作るときは
_index-fv.scss
↑のようにアンダーバーをつける！
そのあと一番上に

@use './mixin' as *;
@use './setting' as *;

を書く！(@includeや変数を呼び出せるように)

あとはいつものscssの書き方でおk！

ーーー納品、公開編ーーー
完成してサーバーにあげる時は
作ったhtml
cssファイル(中身はstyle.min.cssだけでおk！)
imgファイル
jsファイル(中身はcommon.jsだけでおk！)
plugin(使ってたら入れるぐらい)