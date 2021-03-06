# グリッドシステムについて

---
このレクチャーでは、Bootstrap4のグリッドシステムについてお話しします。

---
グリッドシステムはページレイアウトを手軽に指定できる機能です。Bootstrap4の要とも言える機能でしょう。このレクチャーではHTMLにおけるグリッドシステムの指定方法を効率的に確認します。具体的にはHTMLへのグリッドシステムの適用を、VSCodeのHTMLリアルタイムプレビュー機能で確認していくことです。

---
前のレクチャーで、「グリッドシステムとはページ全体を横幅12分割で構成する仕組みであること」そして「各コンテンツが何列分の幅を使用するか？を指定すると、ページ全体のレイアウトを自由に組み立てらること」をお話しました。列数の指定も可能ですが、等しい幅に分割すること可能です。まずはその等分割をご紹介しましょう。

---
VSCodeにindex.htmlを開きましょう。bodyタグの直下に .row>.col*3 + タブと入力します。rowクラスを適用したdivタグの中にcolクラスを適用したdivタグを3個作成しました。グリッドシステムを使用する場合は、はじめにrowクラスのdiv要素を作成し、その中にcolクラスのdiv要素を配置します。それから3つの列のdivタグにそれぞれ「ブロックA」「ブロックB」「ブロックC」と表示させましょう。


---
実はこれで3つの領域に等分割されたグリッドシステムになっているのですが、背景が無色なので目で確認することができません。そこで列ごとに違った色をつけてみます。

---
背景色の適用方法はBootstrap4公式ホームページのドキュメント、UtilitiesのColorsの中で紹介されています。今回はこの中から、bg-primary、bg-secondary、bg-success、3つのバックグラウンドカラーを使用します。

---
それでは1つ目のcolの隣にbg-primaryを追加してみましょう。ブロックAが青の背景色に変化しました。同様に2つ目の列にbg-secondary、3つ目の列にbg-successを追加します。ご覧の通り、3色に色付けされたことで等分割されていることがわかるようになりました。

---
今回は3等分の例でお話しましたが、もちろん2等分や4等分のレイアウトも可能です。colのクラスのdivタグを分割する数分並べるだけです。このようにグリッドレイアウトは簡単にブロックを作ることができます。

---
次に「何列分の幅を使用するか」を指定したレイアウトの方法をご紹介します。

---
3等分割したブロックA,B,Cのrow、すなわち行をコピーしてもう一行作成します。それからコピーした行のカラム（列）をブロックAをDに,BをE,CをFに変更します。それから、最初の列のcolクラスをcol-3, 2つ目の列をcol-6に、3つ目の列をcol-3に変更します。このように指定すると12分割を3,6,3で使用するカラムレイアウトを作成することができます。

---
3-6-3に分割した行をもう一行コピーして、今度は2列、ブロックG,Hとして5-7に分割してみましょう。このように思うようなレイアウトが簡単に実現できることがおわかりいただけると思います。

---
これでBootstrap4のグリッドシステムの紹介を終わります。
