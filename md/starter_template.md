# Bootstrap4の基本的な雛形

---
このレクチャーでは、Bootstrap4の基本的な雛形についてお話しします。

---
Bootstrap4の基本的な雛形は、Bootstrap4の公式ページに掲載されています。
Google で　Bootstrap4 を検索し、Bootstrap4の公式ページを表示させましょう。

---
ブラウザを立ち上げて、Googleのキーワードに「Bootstrap4」と入力して検索します。ヒットしたBootstrap4の公式ページにジャンプしましょう。

---
Bootstrap4の公式ページが表示されたら「Get Started」ボタンをクリックします。表示されたページを少し下にスクロールして「Starter template」のセクションを表示させてください。

---
ここに表示されたHTMLが、Bootstrap4の基本的な雛形です。CopyボタンをクリックしてHTMLをクリップボードに記憶させます。

---
次に、VSCodeでHTMLリアルタイムプレビューを表示させます。VSCodeを起動したら、index.htmlを開いてください。それから表示メニューのコマンドパレットを選択します。コマンドパレットが表示されたら、Show side と入力し、表示された Show side preview を選択します。そうすると、編集エリア内にVSCodeの内部エディタが起動されます。

---
それでは、学習用アプリケーションのフォルダに作成済みのindex.htmlに、Bootstrap4の基本的な雛形を貼り付けましょう。VSCodeでindex.htmlを開いて、既に入力されてあるHTMLを全て削除しましょう。それから、クリップボードからBootstrap4の雛形を貼り付けます。

---
雛形を貼り付けると、HTMLリアルタイムプレビューに「Hello, world!」と表示されます。このままだとBootstrap4が適用されているのがわからないので、雛形のCSS部分であるlinkタグをコメントアウトしましょう。

---
VSCodeで該当の行を選択して、Ctrl-/(MacではCommand-/)をタイプするとコメントアウトされます。

そうすると、表示された文字が通常のHTMLのフォントで表示されます。

もう一度Ctrl-/でコメントアウトを外しましょう。

文字が標準より少し大きくなっていることがわかります。ここではこの違いでBootstrap4が適用されていると感じていただければと思います。

この後のレクチャーでBootstrap4独自のクラスを適用させる実験をしますので、そちらでさらにBootstarp4の適用を感じていただきます。

---
貼り付けた雛形のCSSやJavaScriptはCDNを参照するようになっているので、これをnpmでインストールしたローカルのCSSやJavaScriptを参照するように変更します。

---
VSCodeでlinkとタブをタイプして、src属性にnpmでインストールしたbootstrap.min.cssを指定します。CDNのlink行は不要なので削除しましょう。

---
同じく、JavaScriptもnpmでインストールしたBootstrap4, JQueryやPopper.jsに変更します。script:srcとタブをタイプし、src属性にnpmでインストールしたjquery.min.jsを指定します。

同様にpopper.min.jsやbootstrap.min.jsもローカルのjsファイルを参照するように作成しましょう。

3行完成したらCDNのscript行は不要なので削除しましょう。

---
これで、Bootstrap4の基本的な雛形に関する解説は終わりです。



