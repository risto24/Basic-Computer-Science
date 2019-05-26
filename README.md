![](./pics/laptop.jpg)
# Basic Computer Science
<br>

* [5大機能について](#section1)
* [演算機能](#section2)
* [記憶機能](#section3)

<a id="section1" href="#section1"></a>
<br>
<br>

##5大機能について

コンピューターはハードウェアと呼ばれるパーツによって構成されている

パーツは大きく分けて以下の5種類に機能分けされている

* 入力 (input)
* 出力 (output)
* 記憶 (memory)
* 演算 (Calculation)
* 制御 (Control)

それぞれがお互いに協力しあってユーザーの求める処理を行なう

<br>

## <a id="section2" href="#section2">演算機能</a>

5大機能を動かしているのがパソコンの脳と呼ばれるCPUである

CPUは中央演算処理装置と呼ばれ **演算** と **制御** の機能を担っています

### CPU：中央演算処理装置

CPU（セントラル・プロセッシング・ユニット）と呼ばれ、ユーザーの命令（入力）を処理し、求められた結果を演算処理にて（出力）する

パソコン起動時、一番最初に電流が流されて動き出すパーツであり、PUは制御（入力・記憶・出力）処理を行い別のパーツを起動させる

<br>

## <a id="section3" href="#section3">記憶機能</a>

SRAM・DRAMと呼ばれる記憶機能を担っているパーツのことである

### SRAM（Static Random Access Memory）：主記憶装置

**キャッシュメモリ** と呼ばれる

* データ読み込み時間がDRAMに比べて早い
* 構造が複雑である為、容量あたりのコストが高価
* 消費電力が低い

記憶部にフリップフロップ回路を用いており、リフレッシュ動作が不要であることから、DRAMより高速である

主に、高速な情報の出し入れが可能な点を生かしたキャッシュメモリでの使用や、低消費電力を生かした携帯型機器での使用など、比較的データ量の少ない用途によく用いられる。

低消費電力の例として、SRAMに小さな電池を内蔵あるいは外部に配置することで、主電源が供給されない間も記憶情報を保持する仕組みの不揮発メモリ（NVRAM, コンピュータの時計やBIOS設定情報の保持など）が挙げられる

情報を維持するために定期的に情報を読み出し、再度書き込みをする必要（リフレッシュ）が必要ないことからスタティック（＝静的）RAMと呼ばれるようになった



### DRAM（Dynamic Random Access Memory）：主記憶装置

**メインメモリ** と呼ばれる

* データ読み込み時間がSRAMに比べて遅い
* 構造が単縦である為、容量あたりのコストが低価
* 省電力が高い

コンデンサーに電荷を蓄える事でデータを記憶している為、時間経過による自然放電によりデータが消えてしまうことから、情報を維持するために定期的に情報を読み出し、再度書き込みをする必要がある(リフレッシュ)ことからダイナミック（＝動的）RAMと呼ばれるようになった

<br>

### CPUと記憶装置の間における動作方式

#### ライトバック

* 記憶処理が高速
* SRAMとDRAMの情報整合性の担保が取れない

CPUが記憶装置にデータを書き込む際、一時的にSRAMにデータを書き込み、処理の空き時間ができた際にSRAMからDRAMに書き込む方式

#### ライトスルー

* 記憶処理が低速である
* SRAMの利点を活かすことが出来ない
* SRAMとDRAMとの間でのデータが常に一致する

CPUがDRAMにデータを書き込むと同時に、SRAMにも同じ内容を書き込む方式

#### メモリインターリーブ

ブロック分けされた複数のDRAMに対して同時・並行的にアクセスすることでデータ転送速度を向上する方法

複数のメモリバンク（ブロック分けされたメモリ）に渡って連続したアドレスを交互に割り振っておき、あるデータへのアクセスで生じた遅延時間の間に次のアドレスへアクセス要求を発信する

サーバーやワークステーションなどの高い性能が要求されるシステムで用いられる場合が多いが、最近では一般ユーザー向けのPCでもメモリインターリーブが採用されている

メモリインターリーブ方式における、メモリの増設は同じ容量で同じ種類のメモリモジュールを用意しなくてはならない

<br>

**DRAMはSRAMに比べて大量のデータを保存することが出来るが、容量を越えるとデータは破損してしまう為、主記憶装置は補助記憶装置にデータを保存する**

<br>

### SSD（Solid State Drive）：補助記憶装置

* 衝撃に強く、発熱、消費電力が少ない
* 読み書きの速度が非常に速い
* 作動音がない
* HDDよりサイズが小さく、軽い
* 容量に対するコストが高価

SSDは半導体素子メモリを使ったドライブ（記憶媒体）のことを指す<br>
上記の特徴を始め、消費電力が少なくバッテリーの持ちがよく発熱も少なくて済むことから、ノートPCに適しており近年のでは比較的多く採用されている

ただし、SSDに用いられている「フラッシュメモリ」のデータを記録する最小単位であるセルが徐々に劣化を起こし、およそ1千～1万回程度の書き込みと消去で寿命を迎える為、毎日頻繁に大量のデータを書き換える場合などはHDDを選択するのが賢明である

### HDD（Hard Disc Drive）

* 消費電力が大きい
* 衝撃に弱い
* 容量に対するコストが低価

HDDはデータやプログラムなどを電磁的に読み書きする記憶装置<br>
中にデータを記録する磁性体が塗られた円盤（プラッタ）が複数枚入っており、磁気ヘッドで書き込み・読み出しをする仕組みである<br>
HDDに大きな衝撃が加わると、プラッタとヘッドが強く接触し、プラッターの表面に薄くコーティングされている磁性体に傷が付き、その一部がプラッターから剥がれ落ちると **不良セクタ** と呼ばれる状態になり、破損やデータ消失や動作不良を引き起こす

ただし、HDDは不良セクタが存在しても動き続ける為、状態は悪循環化してしまう<br>
HDDは定期的に検査を実施し不良セクタが多く存在した場合は交換するのが妥当である



