## UDP上の転送プロトコル

QUIC は UDP のユーザースペースに実装された転送プロトコルです。
あなたのネットワークトラフィックを軽く確認してみれば、
QUIC は UDP パケットとして現れることでしょう。

QUIC は UDP のポート番号を利用してマシン上の特定のサーバを識別します。

## うまく動きますか？

エンタープライズのネットワークなどではポート53(DNS に利用されている)以外の
UDP トラフィックを止めるように設定していることがあります。
他にも、制御技術が QUIC の性能を TCP を利用したプロトコルよりも悪くすることがあります。
このような運用者がやるかもしれないことに関する議論には果てがありません。

近いうちでは、すべての QUIC をもとにした転送の用途は、
もう一つの(TCP をもとにした)代替手段に正常に切り替えられる必要があるでしょう。
これに関して、Google のエンジニアは計測では失敗率は1桁台前半のパーセンテージだと
以前に言及しています。

## 良くなりますか？

QUIC がインターネットの世界にとって価値のある追加物だと証明されれば、
人々はそれを使いたいと考え、自分たちのネットワークで機能することを望み、
企業はそれに対する障害について考え直すでしょう。
長年にわたり QUIC の開発は進んでいるので、
QUIC のインターネットでの成功率は上昇しています。
