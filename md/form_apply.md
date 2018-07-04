# フォームの応用

---
このレクチャーでは、Bootstrap4のフォームの応用についてお話しします。

---
前のレクチャーで、Boostrap4の基本について学びました。
HTMLのフォーム要素はinputタグやselectタグで構成されます。
見た目に優れ、操作性のよいフォームを作るために、HTMLのフォーム要素にどのようなBootstrap4のクラスを適用し、どうようなクラスのdiv要素で囲めばよいのかがご理解いただけたと思います。

---
ここでは、習得したBootstrap4の基本の知識を生かして、学習用アプリケーションPMMSのフォーム画面を実装していきたいと思います。

---
まずは、学習用アプリケーションPMMSの画面構成を確認しましょう。Chromeブラウザで完成形の新規会員登録画面を開きます。なぜChromeブラウザで確認するかというと、iPadやiPhoneでの見え方を簡単に確認できるからです。ChromeブラウザでのiPadやiPhone確認については「画面サイズに応じたレイアウト」のレクチャーでご紹介しました。

---
ご覧のとおり、入力フィールドの左にタイトルを配置する画面となっています。タイトルの左となりには「必須」「任意」のバッジを配置しました。この画面はグリッドシステムを使用しています。バッジを含んだタイトルは12列のうち2列、入力フォーム側に残り10列を指定しています。

---
バッジについては、公式ホームページのComponentsのBadgeに記載されています。色やサイズなどが紹介されています。

---
col-sm-2クラスやcol-sm-10クラスを使用していますので、ブレイクポイントは576pxです。つまり、576px以上のときに2列10列の横並びとなり、576px未満の場合はタイトルと入力フィールドは縦に並びます。横幅が375pxのiPhone6/7/8では縦に並びます。横幅が768pxのiPadでは横に並びます。

---
inputタグを使用した入力フィールドにはform-controlクラスを指定することを「Bootstrap4の基本」のレクチェーで学びました。Bootstrap4のクラスを適用しない入力フィールドは、フィールド自体の横幅が狭く、iPhoneのような小さなデバイスでは入力しずらいのですが、Bootstrap4のform-controlクラスの適用でデバイスの横幅いっぱいに広がり、入力しやすくなっています。これもレスポンシブウェブデザインです。

---
それでは、HTMLのコーディングを行なっていきましょう。まずは、グリッドシステムの骨格を作成します。.container>form>.form-group.row*7 とタブキーをタイプして7行のグリッドシステムの骨格を作成します。
それから、formタグの上に、h2タグで「新規会員登録」とタイトルを入れ、その下にhrタグで罫線を入れましょう。

---
それでは初めに、１つ目の氏名を入力する入力フィールドを作っていきます。まずは、labelタグを作ります。form-groupクラスのdivタグの中で label.col-sm-2.col-form-label[for=name]{氏名} とタブをタイプします。labelが作成できました。

---
次に文字列「氏名」の後に　span.badge.badge-pill.badge-danger{必須} とタブをタイプしてバッジを設定します。氏名とバッジの間が接近しすぎなので、&nbsp; でスペースを挿入します。

---
それからlabelタグの後で、.col-sm-10>input.form-control[type=text id=name placeholder=] とタブをタイプします。その後、placeholderに「（例）&nbsp;仙台 次郎」を設定します。

---
次に「読み仮名」の入力フィールドを作成します。「氏名」で追加した部分をコピーし貼り付けましょう。そして「氏名」を「読み仮名」に、idのnameをkanaに、placeholderの「（例）&nbsp;仙台 次郎」を「（例）&nbsp;せんだいじろう」に修正します。

---
次に「英名」の入力フィールドを作成します。「氏名」で追加した部分をコピーし貼り付けましょう。そして「氏名」を「英名」に、idのnameをenameに、placeholderの「（例）&nbsp;仙台 次郎」を「（例）&nbsp;Jiro SENDAI」に修正します。

---
次に「メールアドレス」の入力フィールドを作成します。「氏名」で追加した部分をコピーし貼り付けましょう。そして「氏名」を「メールアドレス」に、idのnameをemailに、placeholderの「（例）&nbsp;仙台 次郎」を「（例）&nbsp;jiro@foo.co.jp」に修正します。inputタグのtypeはtextからemailに修正しましょう。

---
次に「性別」のラジオボタンを作成します。ラジオボタンについてはform-groupクラスはdivタグではなくfieldsetタグを使用します。form-groupクラスを指定したdivタグは削除します。

---
ここではemmetの省略記法を活用します。長いです。fieldset.form-group>.row>legend.col-form-label.col-sm-2.pt-0{性別}+.col-sm-10>(.form-check.form-check-inline>input:radio.form-check-input[name=gender id=]+label.form-check-label[for=])*2 とタブキーをタイプします。+記号は同じレベル（同じ深さ）に異なる要素を作成する記法です。

---
emmetを展開したら、１つ目のlabelに「男」を、2つ目のlabelに「女」を入力します。ラジオボタンのidにはmale femaleを設定しましょう。入力フィールドのように必須バッジもコピーして挿入しましょう。

---
次に「所属部会」のチェックボックスを作成します。form-groupクラスのdivタグの中で 
.col-sm-2{所属部会}>.col-sm-10>(.form-check.form-check-inline>input:checkbox.form-check-input+label.form-check-label[for=])*4 とタブをタイプします。4つのチェックボックスができました。

---
emmetを展開したら、4つのlabelに Java, C/C++, Python, Rubyと入力しましょう。4つのidは java, ccpp, python, ruby としましょう。任意バッヂも作成します。入力フィールドのように必須バッジをコピーして挿入しましょう。それから「必須」を「任意」、badge-danger を badge-success に修正します。

---
最後に新規登録ボタンをを作成します。form-groupクラスのdivタグの中で.col-sm-12>button.btn.btn-primary.float-right[type=button]{新規登録} とタブキーをタイプします。これでボタンができました。

---
これで学習用アプリケーションPMMSの新規会員登録画面のフォームが完成しました。

--

以上で、Bootstrap4のフォームの応用について解説を終わります。



