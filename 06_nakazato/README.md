# 「Sequence Read Archive(SRA)の活用術：その統計と検索」


<div class="jumpmenu"><a href="#navigator">&uarr;</a></div><h3 id="content_1_1"><a id="z296afbf" href="http://MotDB.DBCLS.jp/?AJACS27%2Fthecla#z296afbf" title="z296afbf">_</a> はじめに  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>Sequence Read Archive (SRA) は、次世代シーケンサーによるデータを集めたデータベースです。</li>
<li>今回はデータ解析はやりません
<ul class="list2" style="padding-left:16px;margin-left:16px"><li><a href="http://www.ddbj.nig.ac.jp/ddbjing/24dl.html" rel="nofollow">第24回 DDBJing 講習会 in 東京</a>などご覧ください</li></ul></li></ul>

<div class="jumpmenu"><a href="#navigator">&uarr;</a></div><h3 id="content_1_2"><a id="vb0a8f56" href="http://MotDB.DBCLS.jp/?AJACS27%2Fthecla#vb0a8f56" title="vb0a8f56">_</a> 次世代シーケンサー (NGS) とは  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>そもそも言葉が
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>新型シーケンサー</li>
<li>次世代シーケンサー</li>
<li>New-generation Sequencing (NGS)</li>
<li>Next-generation Sequencing (NGS)</li>
<li>他にmassively parallel DNA sequencing とか...</li></ul></li></ul>

<div class="jumpmenu"><a href="#navigator">&uarr;</a></div><h3 id="content_1_3"><a id="maedadd4" href="http://MotDB.DBCLS.jp/?AJACS27%2Fthecla#maedadd4" title="maedadd4">_</a> 何が新型／次世代なのか?  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>90年代
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>ゲル板で</li>
<li>ポリアクリルアミドゲル電気泳動 + 蛍光標識ダイデオキシヌクレオチド
<div class="img_margin" style="text-align:left"><a href="http://bunseiserver.pharm.hokudai.ac.jp/img/seuencer-monitar.jpg" title="seuencer-monitar.jpg"><img src="http://bunseiserver.pharm.hokudai.ac.jp/img/seuencer-monitar.jpg" alt="seuencer-monitar.jpg" title="seuencer-monitar.jpg" /></a></div>

<a href="http://bunseiserver.pharm.hokudai.ac.jp/gihou/sequence.html" rel="nofollow">DNAシーケンス解析（北大・薬・分子生物）より</a></li>
<li><a href="http://ja.wikipedia.org/wiki/DNA%E3%82%B7%E3%83%BC%E3%82%AF%E3%82%A8%E3%83%B3%E3%82%B7%E3%83%B3%E3%82%B0#.E6.A4.9C.E5.87.BA" rel="nofollow">DNAシークエンシング - Wikipedia -- 検出</a>も参照</li></ul></li></ul>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>00年代
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>キャピラリ
<div class="img_margin" style="text-align:left"><a href="http://MotDB.DBCLS.jp/?plugin=attach&amp;refer=AJACS27%2Fthecla&amp;openfile=66414.jpg" title="66414.jpg"><img src="http://MotDB.DBCLS.jp/?plugin=ref&amp;page=AJACS27%2Fthecla&amp;src=66414.jpg" alt="66414.jpg" title="66414.jpg" width="600" height="489" /></a></div>

<a href="http://www.appliedbiosystems.jp/website/jp/product/modelpage.jsp?MODELCD=50768&amp;MODELPGCD=66447" rel="nofollow">ABI PRISM&#174; 3100-Avant Genetic Analyzerより</a></li></ul></li></ul>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>10年代
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>NGSの登場
<div class="img_margin" style="text-align:left"><a href="http://www.hssnet.co.jp/images/2/2_3_10_3_sample05.gif" title="2_3_10_3_sample05.gif"><img src="http://www.hssnet.co.jp/images/2/2_3_10_3_sample05.gif" alt="2_3_10_3_sample05.gif" title="2_3_10_3_sample05.gif" /></a></div>

<a href="http://www.hssnet.co.jp/2/2_3_10_1.html" rel="nofollow">次世代シーケンス解析サービス：概要・原理 | 北海道システム・サイエンス株式会社</a>より</li>
<li>Sanger法（dideoxy法）→ パイロシーケンシング</li>
<li>超並列</li>
<li>どんなの?
<div class="img_margin" style="text-align:left"><a href="http://g86.dbcls.jp/~togoriv/wp-content/uploads/2011/04/GenomeSequencer1_sm.png" title="GenomeSequencer1_sm.png"><img src="http://g86.dbcls.jp/~togoriv/wp-content/uploads/2011/04/GenomeSequencer1_sm.png" alt="GenomeSequencer1_sm.png" title="GenomeSequencer1_sm.png" /></a></div>

<div class="img_margin" style="text-align:left"><a href="http://g86.dbcls.jp/~togoriv/wp-content/uploads/2011/04/genomesequencer2_sm.png" title="genomesequencer2_sm.png"><img src="http://g86.dbcls.jp/~togoriv/wp-content/uploads/2011/04/genomesequencer2_sm.png" alt="genomesequencer2_sm.png" title="genomesequencer2_sm.png" /></a></div>

<div class="img_margin" style="text-align:left"><a href="http://g86.dbcls.jp/~togoriv/wp-content/uploads/2011/05/Genomesequencer3_sm1.png" title="Genomesequencer3_sm1.png"><img src="http://g86.dbcls.jp/~togoriv/wp-content/uploads/2011/05/Genomesequencer3_sm1.png" alt="Genomesequencer3_sm1.png" title="Genomesequencer3_sm1.png" /></a></div>

<ul class="list3" style="padding-left:16px;margin-left:16px"><li>Togo picture gallery ( <a href="http://g86.dbcls.jp/~togoriv/" rel="nofollow">http://g86.dbcls.jp/~togoriv/</a> ) より
<div class="img_margin" style="text-align:left"><a href="http://creativecommons.jp/wp/wp-content/uploads/2009/10/by.png" title="by.png"><img src="http://creativecommons.jp/wp/wp-content/uploads/2009/10/by.png" alt="by.png" title="by.png" /></a></div>

&#169; 2011 DBCLS Licensed under CC 表示 2.1 日本
←クレジットをいれれば、転載・改変・再利用 OK</li></ul></li></ul></li></ul>

<div class="jumpmenu"><a href="#navigator">&uarr;</a></div><h3 id="content_1_4"><a id="a5364707" href="http://MotDB.DBCLS.jp/?AJACS27%2Fthecla#a5364707" title="a5364707">_</a> SRAとは  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>NGSのデータのレポジトリサイトです</li>
<li>SRA = Sequence Read Archive
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>昔は「Short Read Archive」だったが、shortでなくなってきたので</li></ul></li>
<li>誰（どこ）が集めているのか?
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>NCBI（米）: <a href="http://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?" rel="nofollow">SRA</a></li>
<li>EBI（欧）: <a href="http://www.ebi.ac.uk/ena/home" rel="nofollow">ENA</a> (European Nucleotide Archive)</li>
<li>DDBJ（日）: <a href="http://trace.ddbj.nig.ac.jp/dra/index.shtml" rel="nofollow">DRA</a> (DDBJ Sequnece Read Archive)</li>
<li>3局でデータの交換をしている
<ul class="list3" style="padding-left:16px;margin-left:16px"><li>DDBJを見に行ったとして、入っているのは日本だけ、ということはない、ということです。</li>
<li>（ただ、個人情報にからむものは、実際の配列データはしかるべきところにしかないものがあるとかないとか）</li></ul></li></ul></li></ul>

<div class="jumpmenu"><a href="#navigator">&uarr;</a></div><h4 id="content_1_5"><a id="sf7df990" href="http://MotDB.DBCLS.jp/?AJACS27%2Fthecla#sf7df990" title="sf7df990">_</a> NCBI SRAやめます事件(11/2/16 現地時間)  </h4>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://www.ncbi.nlm.nih.gov/About/news/16feb2011" rel="nofollow">NCBI To Discontinue Sequence Read Archive and Peptidome</a>
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>予算がなくなったのでやめます</li>
<li>解析結果は受け付けます
<ul class="list3" style="padding-left:16px;margin-left:16px"><li>RNA-Seq, ChIP-Seq, and epigenomic data that are submitted to GEO</li>
<li>Genomic and Transcriptomic assemblies that are submitted to <span class="noexists">GenBank<a href="http://MotDB.DBCLS.jp/?cmd=edit&amp;page=GenBank&amp;refer=AJACS27%2Fthecla">?</a></span></li>
<li>16S ribosomal RNA data associated with metagenomics that are submitted to <span class="noexists">GenBank<a href="http://MotDB.DBCLS.jp/?cmd=edit&amp;page=GenBank&amp;refer=AJACS27%2Fthecla">?</a></span></li></ul></li>
<li>EBI、DDBJは直後に続けます宣言
<ul class="list3" style="padding-left:16px;margin-left:16px"><li><a href="http://www.ebi.ac.uk/ena/SRA_announcement_Feb_2011.pdf" rel="nofollow">EMBL-EBI will continue to support the Sequence Read Archive for raw data (PDF)</a></li>
<li><a href="http://www.ddbj.nig.ac.jp/whatsnew/2011/DRA20110222.html" rel="nofollow">DDBJ will continue Sequence Raw Data Archiving</a></li></ul></li></ul></li>
<li>NCBI SRA（一応）続けられます宣言(11/5/9)
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>（とりあえず）<a href="http://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?view=history" rel="nofollow">SRA Archive is still in service. (List of all News, Events and Notifications)</a></li></ul></li></ul>

<div class="jumpmenu"><a href="#navigator">&uarr;</a></div><h3 id="content_1_6"><a id="q0c94951" href="http://MotDB.DBCLS.jp/?AJACS27%2Fthecla#q0c94951" title="q0c94951">_</a> NGSデータの規模  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>【実習】どのくらいのデータ量になるか考えてみましょう
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>ゲル板：750 (base/lane) × 48/4 lanes</li>
<li>キャピラリ：500 (base/lane) × 96 lane</li>
<li>次世代： 36 (base/seq) × 40M seq/run
<a name="plugin_fold_anchor1"></a>
<div class="plugin_fold_title_plus" onclick="return plugin_fold_onclick(this,event,'plugin_fold_anchor1')"><p>←こたえはここをクリック</p>
</div>
<div class="plugin_fold_body"><p>9kbase、48kbase、1.44Gbase</p>
</div></li>
<li>↑これらの数字は規模感をつかむだけなので、ざっくりな数字になっています（1 runにかかる時間は比較してないですし）</li>
<li>↑これらの数字は「塩基数」であって、シーケンサの出力である「画像データ」のデータサイズでないことに注意！</li>
<li>そして、その画像データはSRAには登録されていない</li></ul></li>
<li>[参考] 各シーケンサの性能比較
<ul class="list2" style="padding-left:16px;margin-left:16px"><li><a href="http://bit.ly/ngsspecbydritoshi" rel="nofollow">http://bit.ly/ngsspecbydritoshi</a> （二階堂さん@理研）</li>
<li><a href="http://dbcls.rois.ac.jp/~kawano/ng.html" rel="nofollow">http://dbcls.rois.ac.jp/~kawano/ng.html</a> （河野さん@DBCLS）</li></ul></li></ul>

<div class="jumpmenu"><a href="#navigator">&uarr;</a></div><h3 id="content_1_7"><a id="o7b298cc" href="http://MotDB.DBCLS.jp/?AJACS27%2Fthecla#o7b298cc" title="o7b298cc">_</a> 【実習】DRASearchを使ってみる（ <a href="http://trace.ddbj.nig.ac.jp/DRASearch/" rel="nofollow">http://trace.ddbj.nig.ac.jp/DRASearch/</a> ）  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>こういうときはNCBIと思いがちですが、データ転送量が多い + インターフェースきれい なのでDDBJを使いましょう
<ul class="list2" style="padding-left:16px;margin-left:16px"><li><a href="http://trace.ddbj.nig.ac.jp/DRASearch/" rel="nofollow">http://trace.ddbj.nig.ac.jp/DRASearch/</a> にアクセス</li>
<li>Keyword に興味のある語を入れてみましょう（例：variation）</li>
<li>Filtered by の document type で絞り込み：Study</li>
<li>Filtered by の organism で絞り込み：Homo sapiens</li>
<li>ACCESSION の SRP...... をクリック → 詳細が</li>
<li>画面右の Navigation にあるFASTQやSRALiteからデータがダウンロード可能</li></ul></li>
<li>DDBJにあるドキュメント見てみる
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>データ構造（StudyとかExpとかRunとか）
<div class="img_margin" style="text-align:left"><a href="http://MotDB.DBCLS.jp/?plugin=attach&amp;refer=AJACS27%2Fthecla&amp;openfile=dra.meta.halfsize.png" title="dra.meta.halfsize.png"><img src="http://MotDB.DBCLS.jp/?plugin=ref&amp;page=AJACS27%2Fthecla&amp;src=dra.meta.halfsize.png" alt="dra.meta.halfsize.png" title="dra.meta.halfsize.png" width="514" height="568" /></a></div>

<a href="http://trace.ddbj.nig.ac.jp/dra/documentation.shtml" rel="nofollow">DDBJ Sequence Read Archive - Document - Metadata</a>より</li></ul></li></ul>

<div class="jumpmenu"><a href="#navigator">&uarr;</a></div><h3 id="content_1_8"><a id="r9d815cb" href="http://MotDB.DBCLS.jp/?AJACS27%2Fthecla#r9d815cb" title="r9d815cb">_</a> 統計情報から検索する (SRAs： <a href="http://sra.dbcls.jp/" rel="nofollow">http://sra.dbcls.jp/</a> )  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>まずは普通に全部表示：まずは見てみる → by Studies
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>最初は新着順です</li>
<li>【実習】収載されているもので大規模にデータを出しているプロジェクトは何でしょう? → Exps や Runs をクリックして sortしてみる</li></ul></li>
<li>目的別
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>【実習】興味のある「目的」をクリックしてどんなプロジェクトがあるか見てみましょう</li></ul></li>
<li>Platform別
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>【実習】興味のある「Platform」をクリックして、（以下同）</li></ul></li>
<li>生物種別
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>【実習】興味のある「生物種」をクリックして、（以下同）</li></ul></li></ul>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>データの増加具合を確認
<ul class="list2" style="padding-left:16px;margin-left:16px"><li><a href="http://sra.dbcls.jp/index.1107140402.html" rel="nofollow">現在</a> (7/8 更新)</li>
<li><a href="http://sra.dbcls.jp/index.1107090402.html" rel="nofollow">1週間前</a>(7/1 更新)</li>
<li><a href="http://sra.dbcls.jp/index.1106150402.html" rel="nofollow">1ヶ月前</a>(6/3 更新)</li>
<li><a href="http://sra.dbcls.jp/index.1105150402.html" rel="nofollow">2ヶ月前</a>(5/13 更新)</li>
<li><a href="http://sra.dbcls.jp/index.1104150402.html" rel="nofollow">3ヶ月前</a>(4/7 更新)</li>
<li><a href="http://sra.dbcls.jp/index.1101150402.html" rel="nofollow">半年前</a>(12/30 更新)</li></ul></li></ul>
<a name="plugin_fold_anchor2"></a>
<div class="plugin_fold_title_plus" onclick="return plugin_fold_onclick(this,event,'plugin_fold_anchor2')"><p>Study数の変化</p>
</div>
<div class="plugin_fold_body"><p>Total: 4380 → 5660 → 6042 → 6102 → 6537 → 6578</p>
</div>
<ul class="list2" style="padding-left:32px;margin-left:32px"><li>グラフにしてみた
<ul class="list3" style="padding-left:16px;margin-left:16px"><li><a href="http://sra.dbcls.jp/sra.stat.html" rel="nofollow">Study別（Totalあり）</a></li>
<li><a href="http://sra.dbcls.jp/sra.stat.2.html" rel="nofollow">Study別（Totalなし）</a></li></ul></li></ul>

<div class="jumpmenu"><a href="#navigator">&uarr;</a></div><h3 id="content_1_9"><a id="ie158519" href="http://MotDB.DBCLS.jp/?AJACS27%2Fthecla#ie158519" title="ie158519">_</a> 文献から検索する  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>SRAs の文献リスト： <a href="http://sra.dbcls.jp/cgi-bin/publication.cgi" rel="nofollow">http://sra.dbcls.jp/cgi-bin/publication.cgi</a>
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>NGS関連文献とそこで言及されているNGSデータのリスト</li>
<li>目的/Platform/生物種で絞り込み可能</li></ul></li>
<li>鎖鋸（kusarinoko）：<a href="http://g86.dbcls.jp/kusarinoko" rel="nofollow">http://g86.dbcls.jp/kusarinoko</a>
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>目的：「使える」データをさがす</li>
<li>文献として成果が出ているSRAデータセットをさがしてデータの内容とともに俯瞰する</li>
<li>生物種、目的に制限あり</li>
<li>【実習】鎖鋸をつかってみる：hypoxia で検索
<ul class="list3" style="padding-left:16px;margin-left:16px"><li>この場合、データが汚い（よくある）：SRAsのリストでExperimentを比較 <a href="http://sra.dbcls.jp/cgi-bin/experimentlist.cgi?rp=SRP000403&amp;limit=20" rel="nofollow">http://sra.dbcls.jp/cgi-bin/experimentlist.cgi?rp=SRP000403&amp;limit=20</a></li></ul></li></ul></li></ul>

<div class="jumpmenu"><a href="#navigator">&uarr;</a></div><h3 id="content_1_10"><a id="yf06d685" href="http://MotDB.DBCLS.jp/?AJACS27%2Fthecla#yf06d685" title="yf06d685"><span class="sanchor">_</span></a> 今後  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>混沌としておりますが、バージョンアップなどしてこなれていく + 整理される（はず）</li></ul>
<hr class="full_hr" />
<p><a href="http://MotDB.DBCLS.jp/?AJACS27" title="AJACS27 (2400d)">AJACS本郷9</a> &gt; 「Sequence Read Archive(SRA)の活用術：その統計と検索」</p>
