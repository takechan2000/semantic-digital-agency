# sematic-digital-agency
RDF description of Digital Agency Organization

## ソース
- https://www.digital.go.jp/about/member　にある組織図を organization ontology を使って記述してみました。
- また、https://www.digital.go.jp/about/member　から幹事の方々を紐づけました。
- ネットワーク図の生成は神崎さんのツールを使わせてもらっています。 　https://www.kanzaki.com/works/2009/pub/graph-draw
-- 全部のネットワーク graph-draw.png
-- 組織と役職だけの可視化： typed-graph.png

## 課題
- 監督系統はreportToという関係で下位から上位の役職へつないだ。ただし、横に伸びる役職関係をどうかくかで困った。今回は横の役職は上位の役職へのreportToとした。下位の役職から横に伸びた役職への　reportTO関係も必要か？
- 組織としてはグループまでとした。グループの中に箱はなんだかわからなかった。組織にようにみえるところもあるし、そうでもないところもあるし。
- 幹事名簿には組織図にない、分野統括という役職がある。
- 人名は今回はリテラルとしたが、本当はリソースであるべき。
