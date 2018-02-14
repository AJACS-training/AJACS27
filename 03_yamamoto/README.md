# AJACS27

[AJACS27](http://MotDB.DBCLS.jp/?AJACS27 "AJACS27 (2263d)")

* * *

目次

*   [文献情報関連サービスの活用法](#xc0530c3)
    *   [Allie (アリー) を使って略語の使い方を検索](#m2fb05ff)
        *   [試してみる。](#m8586e43)
    *   [inMeXes (インメクセズ) を使って文献中の英語表現を検索](#v51d4f81)
        *   [試してみる。](#w53c946f)
    *   [TogoDoc / TogoDocClient (統合ドック) を使って文献情報を管理](#ba08edcd)

* * *

### [_](http://MotDB.DBCLS.jp/?AJACS27%2Fyayamamo#xc0530c3 "xc0530c3") 文献情報関連サービスの活用法

山本泰智

*   [発表スライド](http://www.slideshare.net/yayamamo/ajacs27-togo-docinmexesallie)

[↑](#navigator)

### [_](http://MotDB.DBCLS.jp/?AJACS27%2Fyayamamo#m2fb05ff "m2fb05ff") Allie (アリー) を使って略語の使い方を検索

*   [http://allie.dbcls.jp/](http://allie.dbcls.jp/)

生命科学分野の文献では略語が多用されます。Allieはその展開形を文献情報や共起略語(同じ文献情報に出現する他の略語)などと共に検索します。

同じ略語で異なる展開形が存在する事例(多義性を持つ略語)や、一つの展開形に対して複数の略語が存在する事例(各略語は互いに類義語の関係にある)があるため、文献中に展開形なしに略語のみで出現していると、読者を混乱させることになります。

Allieでは略語を入力すると、その展開形の一覧を、それが出現する文献情報や共起略語とともに表示するので、略語の意味を知るための一助となります。

[↑](#navigator)

#### [_](http://MotDB.DBCLS.jp/?AJACS27%2Fyayamamo#m8586e43 "m8586e43") 試してみる。

*   SPF
*   ER
*   CT

それぞれ展開形の候補リストや、各候補について、その意味で主に使われている研究分野や同じ文献で出現する共起略語を確認する。

また、Allieのサイトから、Allieで検索可能なすべての略語と展開形、およびそれらが出現するPubMed[?](http://MotDB.DBCLS.jp/?cmd=edit&page=PubMed&refer=AJACS27%2Fyayamamo) IDのデータベースをフリーでダウンロード出来るようになっています。

[↑](#navigator)

### [_](http://MotDB.DBCLS.jp/?AJACS27%2Fyayamamo#v51d4f81 "v51d4f81") inMeXes[?](http://MotDB.DBCLS.jp/?cmd=edit&page=MeXes&refer=AJACS27%2Fyayamamo) (インメクセズ) を使って文献中の英語表現を検索

*   [http://docman.dbcls.jp/im/](http://docman.dbcls.jp/im/)

英語非ネイティブ研究者が英作文中によく出くわすだろう問題として、前置詞の使い分けや馴染みの無い単語の綴りなどがあると思います。

inMeXes[?](http://MotDB.DBCLS.jp/?cmd=edit&page=MeXes&refer=AJACS27%2Fyayamamo)を利用することで、より簡単に、実際の生命科学系論文で使われている用例を検索出来ます。

[↑](#navigator)

#### [_](http://MotDB.DBCLS.jp/?AJACS27%2Fyayamamo#w53c946f "w53c946f") 試してみる。

*   information に続く前置詞。
*   in conjunction に続く前置詞。
*   in regard に続く前置詞。

検索結果を他の利用者とURL(パーマリンク)を介して共有出来ます。

*   例: [http://docman.dbcls.jp/im/?q=is%20associated%20&d=50&o=incl&a=LSDconc](http://docman.dbcls.jp/im/?q=is%20associated%20&d=50&o=incl&a=LSDconc)

[↑](#navigator)

### [_](http://MotDB.DBCLS.jp/?AJACS27%2Fyayamamo#ba08edcd "ba08edcd") TogoDoc[?](http://MotDB.DBCLS.jp/?cmd=edit&page=TogoDoc&refer=AJACS27%2Fyayamamo) / TogoDocClient[?](http://MotDB.DBCLS.jp/?cmd=edit&page=TogoDocClient&refer=AJACS27%2Fyayamamo) (統合ドック) を使って文献情報を管理

電子ジャーナルの発達で多くの論文がPDF形式で全文を読めるようになりましたが、読後のファイルの管理はおろそかになりがちです。 その一方で、自信の研究あるいは興味のある分野に関連の深い論文の発表件数は年々増加をし続け、効率的に見つけることが困難になって来ていると考えられます。 そこで、既にPCのディスクに保存されている論文情報を抽出し、それに基づいた文献の検索が出来れば、それは利用者にとって興味のある文献を効率的に得る協力な手段となり得るでしょう。

TogoDocClient[?](http://MotDB.DBCLS.jp/?cmd=edit&page=TogoDocClient&refer=AJACS27%2Fyayamamo)は各利用者のPCにインストールして利用するソフトウェアで、TogoDoc[?](http://MotDB.DBCLS.jp/?cmd=edit&page=TogoDoc&refer=AJACS27%2Fyayamamo)はDBCLSのサーバーにあるウェブサービスです。 両者は互いに連携し、上記の問題に取り組むシステムを実現しています。TogoDocClient[?](http://MotDB.DBCLS.jp/?cmd=edit&page=TogoDocClient&refer=AJACS27%2Fyayamamo)は指定されたフォルダにあるPDF形式のファイルを全て解析し、タイトルや著者名などの書誌情報を抽出します。 得られた結果はTogoDoc[?](http://MotDB.DBCLS.jp/?cmd=edit&page=TogoDoc&refer=AJACS27%2Fyayamamo)に送信され、続いて、それに基づき、最新のMEDLINE所蔵文献情報から関連性の高い順に提示します。

また、PCに保存されているPDF形式ファイル名を予め指定した形式に一括変換出来ます。

*   [TogoDoc](http://docman.dbcls.jp/pubmed_recom)
*   [TogoDocClient](http://tdc.cb.k.u-tokyo.ac.jp/)
*   [情報交換用twitter](http://twitter.com/togodoc)

推薦機能を利用するにはオープンIDが必要になります。 DBCLSの提供するオープンIDを利用すると、サインインの処理を簡略化出来ます。 アカウントの作成は[こちら](https://openid.dbcls.jp/account/signup)から可能です。

<
