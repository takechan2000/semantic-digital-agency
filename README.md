# semantic-digital-agency
RDF description of Digital Agency Organization

## ソース
- 組織図: https://www.digital.go.jp/about
- 幹事名簿: https://www.digital.go.jp/about/member
- ネットワーク図の生成は神崎さんのツールを使わせてもらっています。 　https://www.kanzaki.com/works/2009/pub/graph-draw
  - 全部のネットワーク graph-draw.png
  - 組織と役職だけの可視化： typed-graph.png

## 作業と課題
- organization ontology を使って記述してみました。
- 監督系統はreportToという関係で下位から上位の役職へつないだ。ただし、横に伸びる役職関係をどうかくかで困った。今回は横の役職は上位の役職へのreportToとした。下位の役職から横に伸びた役職への　reportTO関係も必要か？
- 組織としてはグループとその一つ下までとした。その中にある箱はなんだかわからなかった。組織にようにみえるところもあるし、そうでもないところもあるし。
- 幹事名簿には組織図にない、分野統括という役職がある。
- 人名は今回はリテラルとしたが、本当はリソースであるべき。

## Version 2を追加
2を追加したファイル名のもの。
- 変更点：
  - 人をリソース化。人にはIDがいないので、適当にnpa:...でつくる。
  - org:heldByでなく、逆向きのorg:holdを使う。
  - 外むきリンクをいれる。wikidataと日本語DBpedia。人（除官僚）とデジタル庁、デジタル大臣。なお、日本語DBpediaは更新がまだないので、デジタル庁とはまだない。
- 効果
  - typed-graph2.pngで人まで表示されるようになった。
  - 将来、官僚名簿IDがあれば、人IDはそれに置き換えるべき。

## Version 3を追加
3を付記したフィアル。
- 変更点：
  - 2021/10/4発足の内閣による政務人事を反映。
  - org:holdsとorg:postInでスペルミスを訂正。
  - 外部リンクなしのバージョン(digital-agency-organization3.ttl)とありのバージョン(digital-agency-organization3link.ttl)に分ける。
