# AJACS27

[[講習会のページに戻る>AJACS21]]

&size(24){データベースを探す・検索する・ダウンロードする};
        --
~目次
#contents
        --

## 生命科学データベース横断検索 [#p13874b8]

> http://biosciencedbc.jp/dbsearch/

+【実習１】：iPS細胞の樹立に利用された遺伝子の名前を調べてみましょう
++キーワード''iPS細胞''で検索
++どのカテゴリで絞り込むかがポイントです。遺伝子カテゴリで絞りこむのがベストとは限りません。
#fold(←ヒントはここをクリック。,「文献」カテゴリで絞り込みます)
#fold{{{
←クリックして答えを見る。
Oct3/4、Sox2、c-Myc、Klf4（いわゆる山中４因子）
#br
例えば、山中先生著作の以下の文献にたどりつく（上から１５番目）とわかります。候補遺伝子を絞りこんだ過程も解説されています。
+[[蛋白質核酸酵素:マウス線維芽細胞から誘導多能性幹細胞をつくる[pne_merge]>http://lifesciencedb.jp/dbsearch/Literature/get_pne_cgpdf.php?year=2006&number=5115&file=JYQeKIy1Ms9S7N6tZoUbCw==&search=%22ips%20cell%E3%80%80%E5%B1%B1%E4%B8%AD%22]]
#br
また、「タンパク質」カテゴリのPDBjのエントリにも山中４因子の記述があります。
+[[PDB:1GT0>http://www.pdbj.org/eprots/index_ja.cgi?PDB%3a1GT0]]
```

+【実習２】：今年６月、山中因子のひとつを別の因子に置換することで、iPS細胞の作製効率を上げ、なおかつ腫瘍化リスクを減らせることが発表されました。どの遺伝子をどの遺伝子に置換するのでしょうか。
++キーワード''iPS細胞''で検索
#fold{{{
←クリックして答えを見る。
c-MycをGlis1に置換
#br
以下の文献（”iPS細胞”で検索した結果の上から４番目）がその発表論文の日本語レビューです。
#br
[[転写因子Glis1による体細胞初期化の促進 : ライフサイエンス 新着論文レビュー[first_author]>http://first.lifesciencedb.jp/archives/3079]]
#br
[[ライフサイエンス新着論文レビュー>http://first.lifesciencedb.jp/]](DBCLSが発信）とは：
Nature，Science，Cell などに代表されるトップジャーナルに掲載された日本人を著者とする生命科学分野の論文について，論文の著者自身の執筆による，専門分野の異なる生命科学研究者にむけた日本語によるレビューを，だれでも自由に閲覧・利用できるようWeb上にていち早く無料で公開するものです．
#br
google検索でも答えは得られますが、ポータルサイトやブログ、ニュースが上位にくることが多いのではないでしょうか。
```

+【実習３】:キーワードの日英翻訳機能を確認しましょう
++キーワード''口蹄疫''で検索
++検索結果（スニペット）には、''口蹄疫''以外のワードもハイライトされています。それは何でしょうか？
#fold{{{
←クリックして答えを見る。
’foot and mouth disease’
#br
このように日本語で検索しても英語でのデータベースも同時に翻訳されて検索結果が返ってくるのがこの横断検索の大きな特徴です。反対に、英語キーワードの日本語化も行っています。
```

- 【応用】自分の研究テーマに関係のあるキーワードで検索してみましょう。

- 横断検索と同様の仕組みで[[''TogoProt''>http://lifesciencedb.jp/togoprot/index.php]]という蛋白質関連データベース統合検索も提供されてます。

## 生命科学系データベースカタログ [#p13874b8]

> http://biosciencedbc.jp/dbcatalog/

+【実習】：キーワード''iPS細胞''で検索すると、どのようなデータベースが検索されるでしょうか。

#fold{{{
←クリックして答えを見る。
iPS細胞作成用プラスミドの配布を行っているバイオリソースNPOの[[Addgene>http://www.addgene.org/pgvec1]]が検索されます。
#br
Addgeneのページの[[Search for Plasmidsを「"iPS”」で検索>http://www.addgene.org/pgvec1?identifier=ips&f=c&cmd=searchpl&x=12&y=16]]すると山中４因子が出てきます。
```

# 生命科学系データベースアーカイブ [#q97d7b5e]

> http://dbarchive.biosciencedbc.jp/

+【実習】：[[Atlas (ISH Data Base)>http://dbarchive.biosciencedbc.jp/jp/dicty-atlas/desc.html]]の画像データは、改変や再配布は可能でしょうか。その際の条件は何でしょうか

++[[利用許諾>http://dbarchive.biosciencedbc.jp/jp/dicty-atlas/lic.html]]を見ます。
#fold{{{
←クリックして答えを見る。
改変も再配布も可能です。因みに商用利用もできます。

標準利用許諾（CC-BY-SA）と追加利用許諾に従う必要があります。
```


# 自習教材 [#xfc3ae27]

統合TVやMotDBには動画や過去の講習会資料がありますので、ご活用ください。

##[[統合TVCurated>http://togotv-curated.dbcls.jp/]] [#m0fa36a6]
データベースや解析ツールの使い方だけでなく、DBCLS開発者の学会発表の動画も含まれます。サービス名でキーワード検索してみてください。

##統合TV　http://lifesciencedb.jp/image/small_video_icon.png [#kb04fe87]
使い方の詳細を解説しています。

- [[生命科学データベース横断検索を使い倒す>http://togotv.dbcls.jp/20091008.html]]
- [[TogoProtの使い方～検索と連携～>http://togotv.dbcls.jp/20100706.html]]
- [[生命科学系データベースカタログを使い倒す 2009>http://togotv.dbcls.jp/20090523.html]]
- [[生命科学 学協会 カタログを使い倒す>http://togotv.dbcls.jp/20090612.html]]
- [[生物アイコンを使い倒す2009>http://togotv.dbcls.jp/20090130.html]]

##MotDB [#ba4e6ff9]
過去のAJACSでの横断検索やカタログの使い方の実習資料です。課題に挑戦してみてください。

- [[生命科学横断検索の利用法(2009/11/6)>AJACS14/sk2]]
- [[生命科学横断検索の利用法(2010/7/6)>AJACS20/shoko]]
- [[生物アイコン～生物種画像レポジトリサイトの紹介(2009/11/6)>AJACS14/bando]]

#クレジット [#nfdefcfb]
このページならびにパワーポイント資料は、以下のコンテンツを再利用しました。
- [[統合データベースの利用法：統合データベースプロジェクトのサービスを使い倒す>AJACS21/bono1]]
- [[生命科学横断検索の利用法>AJACS20/shoko]]
