# フォームの基本

---
このレクチャーでは、Bootstrap4のフォームの基本についてお話しします。

---
フォーム画面はユーザに何らかの入力を行ってもらう画面です。エンジニアにとってフォーム画面の作成は切っても切れない関係でしょう。
フォームはテキストボックス、プルダウンメニュー、ボタンなど、構成する部品も多く、どれもよく使われるものだと思います。
Bootstrap4には、それぞれの部品に対するクラスが豊富に用意されています。

---
このレクチャーでは、学習用アプリケーションで使用しない部品も含め、網羅的に学んでいきます。
学習用アプリケーションのフォームについては後のレクチャーで解説していきます。

---
このレクチャーのために、専用のHTMLファイルを作成したいと思います。
学習用アプリケーションPMMSのnew.htmlをコピーして、form.htmlを準備してください。
form.htmlを開くと、このようなシンプルなHTMLになっていると思います。
Bootstrap4の適用でフォームどのように変化するかを体感するため、まずは、headタグ内のlink要素をコメントアウトします。

---
それでは、基本的なフォームを作っていきたいと思います。
bodyタグの直下に h1{フォームの実験} とタブキーをタイプしましょう。
それから、form>input*4 とタブキーをタイプしましょう。inputタグが4つできたことを確認して、2つ目のinputのtypeをemailに、3つ目のtypeをpasswordに、4つ目のtypeをsubmitに変更します。

---
ご覧の通り、3つの入力フィールドと1つの送信ボタンが、横並びで表示されました。
それでは、先ほどコメントアウトした、Bootstrap4のCSSを読み込むlinkタグを元に戻しましょう。
Bootstrap4を有効にしたことで、入力フィールドと送信ボタンが少し大きくなって、見やすくなりました。ここで、入力フィールドの内部をクリックしてフォーカスしてみましょう。今の状態では、入力フィールドの輪郭が「細い」青線に変化することを確認しましょう。

---
今度は、3つの入力フィールドにBootstrap4の form-control クラスを適用してみます。 class="form-control" を追加してみましょう。
ご覧のとおり、入力フィールドが横幅いっぱいに広がりました。よく見ると、角も丸くなっています。
入力フィールド内部をクリックしてみましょう。青い輪郭線がBootstrap4適用前より太くなっています。フォーカスしたことがはっきりわかるようになりました。

---
今度は、送信ボタンにBootstrap4の btn クラスを適用します。 class="btn" を追加してみましょう。ボタンがグレーのフラットなデザインに変化しました。少し大きくなりましたね。

---
次はそれぞれの入力フィールドにラベルを追加しましょう。ラベルは入力フィールドに何を入力するかを伝えるタイトルです。具体的には入力フィールドの上にlabelタグを追加します。また、入力フィールドの下に入力のための補足情報を追加します。具体的には入力フィールドの下にsmallタグを追加します。

---
まずは、labelタグを追加しましょう。labelタグは対応する入力フィールドのidとfor属性で紐付けを行いますので、input タグにid属性を追加します。3つの入力フィールドのidを txt, mail, pw に設定しましょう。

---
そして一番上のinputタグの上で label[for=txt] とタブをタイプします。それからlabel行を2つコピーして、for属性をmail, pw に変更しましょう。そして、3つのlabelタグの中身に「テキスト」「メールアドレス」「パスワード」を設定します。

---
次に、入力フィールドの補足情報を追加します。3つの入力フィールドの下にsmallタグを設定していきます。まずは、1つ目の入力フィールドの下の行で、small{テキストフィールドの説明です} とタブを入力しましょう。それからsmall行を2つコピーして補足情報にそれぞれ「メールアドレスフィールドの説明です」「パスワードフィールドの説明です」に変更しましょう。

---
さらに、ここではプレースホルダを設定します。プレースホルダとは入力フィールドに未入力の状態で表示される「入力されると消えるテキスト」です。具体的には、inputタグのplaceholder属性で設定します。3つの入力フィールドにplaceholderを追加します。そして、smallタグで設定した文言と同じ文言をコピーして設定します。ご覧の通り、入力フィールドの中にグレーで文字列が表示されました。入力フィールドに何か文字を入れてみましょう。プレースホルダの文字が消えることを確認できます。

---
これで入力フィールドのタイトルと補足情報を設定したのですが、ご覧の通り、smallタグとlabelタグの間に改行がなく、分りにくい状態となっています。そこで、1つの入力フィールドに対するlabel, input, smallタグをBootstrap4の form-group クラスを適用したdivタグで囲みたいと思います。

---
実は、このように入力フィールド毎に form-group クラスを適用したdivタグで囲むのがBootstrap4のフォームの基本です。ご覧の通り、適切な改行が行われ、グループ毎の間隔もいい感じにパディングされています。入力フィールドのタイトルをクリックしてみましょう。グルーピングした入力フィールドの枠が青くなりフォーカスされました。labelタグのfor属性とinputタグのid属性で紐付けがうまくいっていることをお分かりいただけると思います。

---
ここで次の説明のために、画面を整理します。プレースホルダとsmallタグの補足情報は冗長なので、smallタグを全て削除します。

---
次のステップに進みます。
ここまで、inputタグのバリエーションを学習しましたので、これからはinputタグ以外のフォーム要素についてみてみたいと思います。

---
まずはtextareaです。form-groupクラスのdivタグ全体をコピーしてtextareaを作ってみます。textareaのidはmemoとします。labelのfor属性と紐付けをしましょう。タイトルは備考として、プレースホルダには「備考の説明です」と入力しましょう。textareaの完成です。

---
次に、プルダウンメニューとリストボックスです。いずれもselectタグとoptionタグで構成されますが、size属性で複数行見えるようにしたselectがリストボックスです。

---
select.form-control[id=pulldown]>option*3 とタブを入力しましょう。optionの表示文言をピン, ポン, パンとします。それから form-group クラスのdivタグで囲み、labelタグでタイトルを設定しましょう。タイトルは「プルダウンメニュー」とします。上部の入力フィールドとデザインが統一されたプルダウンメニューができました。

---
次はリストボックスを作成します。プルダウンメニューのdivタグを丸ごとコピーし、idをlistboxに修正します。タイトルはリストボックスと修正します。それからselectにsize属性を追加し数字の3を指定します。これでリストボックスが完成です。

---
あと2つのフォーム部品を紹介します。チェックボックスとラジオボタンです。

---
まずはチェックボックスです。好きな食べ物というチェックボックスを考えます。「寿司」「ラーメン」「カレー」というチェックボックスを作っていきます。(label>input[type=checkbox id=])*3 とタブをタイプしてcheckboxのパターンを3つ作ります。idはそれぞれ sushi, ramen, curry とします。

---
checkboxをlabelで囲みました。囲った理由は寿司やラーメンの文字列をクリックしたときも、チェックボックスをON/OFFされたいためです。Bootstrap4ではcheckboxを囲ったlabelをさらにform-checkクラスのdivクラスで囲みます。div.form-check とタブをタイプして、3箇所にコピーしましょう。

---
さらに、checkboxを囲むlabelにはform-check-labelクラスを適用します。それからcheckboxのinputタグにはform-check-inpuクラスを適用します。

---
最後に3つのチェックボックスを囲むように、form-groupクラスを適用したdivタグを作成します。divタグの上にlabelタグで「好きな食べ物」といれましょう。これでBootstrap4のチェックボックスの基本形が完成です。

---
いま、チェックボックスは縦に3つ並んでいます。チェックボックスは縦に並べると右のスペースが無駄になるため、横に並べるチェックボックスが多いと思います。Bootstrap4ではform-checkクラスのdivタグにform-check-inlineクラスを追加することで横に並べることができます。横に並びました。

---
それでは、次に、チェックボックスをコピーしてラジオボタンを作ってみましょう。inputタグのtype属性をcheckboxからradioに修正します。タイトルは「連絡手段」に変更します。選択子は「電子メール」「電話」「郵便」に修正しましょう。それから3つのinputタグに共通のname属性を設定し、１つしか選択できないようにします。

---
フォームの部品が揃ったので、コントロールのサイズ指定についてお話します。入力フィールドは form-control クラスを適用することで、比較的余裕を広くとったスタイルで表示されます。もう少し小さくしたい、あるは、もう少し大きくしたいというときは、form-controlクラスと併せて、form-control-sm あるいは form-control-lg クラスを適用します。

---
それでは、3つの入力フィールドとテキストエリア、そしてプルダウンメニューとリストボックスのform-controlにform-control-lgクラスをプラスしてみましょう。大きくなったことがはっきりとわかりますね。入力される文字も大きくなりました。form-control-lgをform-control-smに置換してみましょう。すっきりコンパクトになりました。

---
送信ボタンの大きさや色を変えてみましょう。大きさはbtnクラスに加えてbtn-lgやbtn-smクラスを指定します。色はbtn-primaryやbtn-dangerなどを指定します。ここで全ての色をご紹介できないのでBootstrap4の公式ホームページを紹介してこのレクチェーを終わりたいと思います。

---
ボタンについては、公式ホームページのComponentsのButtonsに記載されています。色やサイズ、入力不可にする方法などが紹介されています。

---
フォームについては、公式ホームページのComponentsのFormsに記載されています。入力不可にするreadonly属性やグリッドレイアウトを使用したフォームのレイアウトなどが紹介されています。グリッドレイアウトとフォームの併用は学習用アプリケーションPMMSで採用していますので、この後のレクチャーで紹介します。

---

以上で、Bootstrap4のフォームの基本について解説を終わります。
