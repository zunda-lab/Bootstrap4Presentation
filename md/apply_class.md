# Bootstrap4のクラス適用

---
このレクチャーでは、Bootstrap4のクラス適用についてお話しします。

---
Bootstrap4を読み込んだHTMLでは、HTMLタグにクラスを適用することで書式を指定する仕組みになっています。

---
imgタグにクラスを適用する例をご紹介します。まずは、index.htmlにimg+Tabをタイプしてimgタグを追加します。それからsrc属性に画像ファイルを指定しましょう。画像が表示されました。

---
このimgタグのクラスにBootstrap4のクラスを適用してみます。class属性を追加して、rounded-circleクラスを指定します。ご覧の通り、画像が円形、長方形画像なので楕円形に切り抜いて表示されました。

---
Bootstrap4のクラス適用をもうひとつ紹介します。画像の上に、クラス属性付きのdivタグを追加しましょう。まずは、Hello worldのH1タグを削除します。

---
次に .jumbotron>h1{Hello World} を入力します。これはEmmetの省略記法で「divタグにclass属性を追加してjumbotronを指定する。その子要素としてHello Worldを表示するh1タグを追加する」という意味です。先頭がドットで始まっていますが、divタグが省略されていると思ってください。ドットはクラス、シャープはid属性といったCSSのセレクタに準じています。

---
Tabキーを入力しましょう。ご覧のようにdivタグとその中にh1タグが展開されました。一方、HTMLリアルタイムプレビューを見ると画像の上に、周囲を囲ってタイトルのように表示する書式が表示されています。これはjumbotronといわれるBootstrap4のコンポーネントのひとつです。jumbotronは後のレクチャーで詳しく解説します。

---
jumbotronを指定したクラスにもう１つBootstrap4のクラスを適用してみましょう。jumbotronの後ろにスペースをひとつ挿入し text-centerと入力してください。ご覧の通りHello Worldがセンタリングされました。text-centerは文字を中央揃えで配置する書式です。このように１つのclass属性に複数の書式指定を適用できます。

---
Bootstrap4には多くの書式設定が準備されています。このレクチャーで全てを紹介することができませんので、Bootstarp4の公式ページでの参照方法をご紹介します。

---
公式ページの上部、Documentationリンクをクリックします。表示されたページの左のメニューをご覧ください。Layout, Content, Components, Utilitiesとならんでいます。Contentをクリックすると文字の体裁や画像、テーブルなどの書式設定が紹介されています。Typographyの中にtext-centerが紹介されています。

---
Componentsをクリックすると、多くのコンポーネントが紹介されています。jumbotronはこの中で紹介されています。

---
Utilitiesをクリックして、その中のBordersを見ていると一番下に画像を楕円形に切り抜いたrounded-circleが紹介されています。

---
公式ページでは、classに何を指定すれば、どのように変化するのかが、多くの例で記載されています。HTMLの例と適用後の表示が掲載されていますので、英語が苦手でも理解することができます。色々な書式の存在を理解すればBootstrap4を理解したい気持ちが高まると思います。

---
最後に、このレクチャーで追加したHTML部分を削除します。

---
これでBootstrap4のクラス適用の紹介を終わります。
