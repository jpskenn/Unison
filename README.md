# Unison / ユニゾン とは

![Unison Music style](./assets/readme/DSC_7287.jpg)

ユニゾン（Unison）は、GH60互換の60%ケースに収まる狭ピッチキーボードです。  

ロータリーエンコーダを搭載しシーケンサーやMIDIキーボードとしてDAW連携を想定した”Misicスタイル（ミュージック・スタイル）”と、コンピュータでの作業を想定した”Terminalスタイル（ターミナル・スタイル）”を用意しています。

音楽用とコンピュータ用のふたつのキーボードがひとつになるイメージから、音楽用語のユニゾンが名前の由来です。


## コンセプト

このキーボードのコンセプトや実現したい要件は次の通りです。

- 格好良いシンセサイザー、[OP-1](https://teenage.engineering/products/op-1)へのオマージュ。
- 狭ピッチなキーボードを作ってみたい。
- 狭ピッチなキーボードを使ってみたい。
- 挟ピッチなキーボードに触れる機会を増やしたい。
- ケースのあるキーボードを作りたいが、ケースの設計が大変だから、GH60型のケース対応にしてケース設計をメイン作業に含めない。
- キーキャップの選択肢を広げる。  
    安くて、そこそこ流通しているものが使えると普及しやすい。  
    標準的なキーキャプですべて埋められるレイアウトにしておく。
- 多キー、多ロータリーエンコーダ。

## 特徴

### 挟ピッチ

<!-- TODO　60%との比較写真  -->
<!-- TODO スイッチだけの写真 -->
通常の19.05mmのキーピッチに対して約87%となる、**縦16.4mm × 横16.8mm**のキーピッチを採用しています。

デザインの元となったOP-1と同様に、4行×17列のキーとロータリーエンコーダが60%キーボードのケースに収まるように配置しました。  
また、キーピッチに少し余裕を持たせることで、入手性の良い”[Cherry MX Backlit Low Profile Keycap Set](https://yushakobo.jp/shop/cherry-mx-backlit-low-profile-keycap-set/)”が使用できるようにしています。

16mmピッチ＋α以下の挟ピッチ対応キーキャップが使用できます。  
挟ピッチ対応のキーキャップについては、e3w2q氏の記事”[狹ピッチ対応キーキャップを求めて](https://e3w2q.github.io/10/)”が大変参考になります。

<!-- TODO　ロープロキャップ写真 -->
<!-- TODO YKNキャップ写真 -->


### 独自の物理配列

以前設計した60%キーボードの[Jones](https://github.com/jpskenn/Jones)と同じく、2行目と3行目のずれをなくし、ロースタッガードとオルソリニアを組み合わせたキー配列を採用しています。  

アルファ部が左右対称になることで、肘、手首、指先が直線上に並んだ自然なポジションで打鍵できるなどのメリットがあります。  
詳しくは[Jones：キーレイアウト](https://github.com/jpskenn/Jones#キーレイアウト)を参照してください。

また、この配列を採用したことで、白鍵と黒鍵のずれをうまく表現できました。


### ふたつのレイアウト・スタイル

シーケンサーやMIDIキーボードとしてDAW連携を想定した”Misicスタイル”と、コンピュータでの作業を想定した”Terminalスタイル”の2種類が選べます。

#### Musicスタイル（ミュージック・スタイル）
<!-- TODO写真 -->

DAW連携を想定したMisicスタイルは、上部に5個のロータリーエンコーダと4個のスイッチを配置した、4行×17列のレイアウトです。

[![layout: Unison Music style](./assets/readme/layout_music_style.png)Keyboard Layout Editor: Unison Music style](http://www.keyboard-layout-editor.com/#/gists/866c93c6eb4c580be0cf582207fa1836)


キーボードファームウェア[QMK](https://github.com/qmk/qmk_firmware)の機能によってシーケンサーとMIDIキーボードが使用でき、USB接続のMIDIデバイスとしてDAWと連携させることができます。  
もちろん、通常のコンピュータ用キーボードとしても使用できます。

シーケンサーは8トラック、32ステップあり、MIDIチャンネル1に固定されています。  
音源側（DAWなど）でチャンネル1にドラムセットを割り当てて使用するのが基本です。

MIDIキーボードは24鍵の鍵盤で演奏でき、ロータリーエンコーダを使ってベロシティやトランスポーズのコントロールやオクターブの上げ下げなどがおこなえます。

シーケンサーとMIDIキーボードは、それぞれ単独でも、両方を同時にでも使用できます。  
MIDIキーボードのチャンネルを変更することで、チャンネル1でシーケンサーを再生しながら、別チャンネルに割り当てた音源が演奏できます。

参考：シーケンサーとMIDIキーボードを同時に使用するデモンストレーション動画  
[![](http://img.youtube.com/vi/_A8NaXlWKeE/0.jpg)](http://www.youtube.com/watch?v=_A8NaXlWKeE "QMK Sequencer & MIDI keyboard")  
[QMK Sequencer & MIDI keyboard](http://www.youtube.com/watch?v=_A8NaXlWKeE)



#### Terminalスタイル（ターミナル・スタイル）
<!-- TODO写真 -->
コンピュータでの作業を想定したTerminalスタイルは、数字行を含めた5行×17列のレイアウトです。

[![layout: Unison Music style](./assets/readme/layout_terminal_style.png)Keyboard Layout Editor: Unison Terminal style ](http://www.keyboard-layout-editor.com/#/gists/f8cf33730eca47e1e9039568cd3ca72c)

60%キーボードにテンキーを組み合わせたようなレイアウトで、挟ピッチによって手をホームポジションから大きく動かさずに入力することができ、コンピュータでの作業を快適におこなえます。  

最下行に配置した1.5uと2uのModキーの配置は、好みに応じていくつかのバリエーションから選択でき、全て1uにすることもできます。

テンキーは、肩を開いたホームポジションとなる中央への配置がおすすめですが、左や右に配置することもできます。  

また、スピーカーを搭載することで、特定のキー操作でメロディーを鳴らしたり、ピコピコという電子音とともにキー入力することもできます。  
音楽モードをONにすればキーボードを鍵盤に見立てて演奏することもでき、ちょっとしたハーモニーも楽しめます。


## ビルドガイド

- [v04](https://github.com/jpskenn/Unison/blob/main/docs/BuildGuide_v04_JA.md)

## ギャラリー
![](./assets/readme/IMG_2669.jpeg)  
Musicスタイル  
60% プラスチックケース ホワイト, Cherry MX Backlit Low Profile Keycap Set

![](./assets/readme/DSC_7352.jpg)  
Musicスタイル, サイドビュー  
60% プラスチックケース ホワイト, Cherry MX Backlit Low Profile Keycap Set

![](./assets/readme/IMG_2684.jpeg)  
Terminalスタイル, アンダーグローLED追加  
60% プラスチックケース クリア, YKNキーキャップセット(MX/ChocV2スイッチ 16x16mmキーピッチ用) v1.2

![](./assets/readme/IMG_2626.jpeg)  
Terminalスタイル, アンダーグローLED追加  
60% プラスチックケース クリア, Cherry MX Backlit Low Profile Keycap Set

![](./assets/readme/IMG_2392.jpeg)  
60%キーボードとの比較, 上：Jones, 下：Unison
## 製作歴

### v05（開発中）

組み立てやすさの向上。  
細部の調整。
### v04

v03の不具合修正、各部調整などをおこなった、*ほぼ*完成版。  
ロータリーエンコーダを搭載せず、数字キーを含めた5行レイアウトのTerminalスタイルに対応。

簡易ケースレスなボトムプレートを用意したが、組み立てに難ありでボツ。

![v04](./assets/readme/IMG_2626.jpeg)
### v03

初期動作版。

各部のサイズ調整をおこない、一通りの組み立てができ、動作も確認できた。  
キーピッチは縦16.4mm × 横16.8mmで確定。

LED光をマスクするミドルプレートや、アクリルのトッププレートも作成し、製品としての見た目もできあがってきた。  

![v03](./assets/readme/DSC_7274.jpeg)

### v02

v01発注後、縦16mmピッチで基板データを仮に作成したもの。

キーピッチに余裕がないため、ボツ。

### v01

挟ピッチキーボードの試作として、Jonesの設計をベースに開発を開始。  
部品を手はんだするつもりで基板を発注したが、MCUのフットプリント間違いで組み立てられなかったたため、モックアップとして使用。

現在よりもピッチをつめた、5行×17列にロータリーエンコーダの1列を合わせたレイアウトで、縦のピッチは16mm未満。  
キーキャップの干渉具合や、ロータリーエンコーダの配置など、各部の寸法チェックをおこなった。

![v01](./assets/readme/IMG_2311.jpeg)
### v01以前

OP-1のスタイルに惚れ、60%キーボードの[Jones](https://github.com/jpskenn/Jones)に多数のロータリーエンコーダを搭載したバリエーションとして開発をスタート。

![befre v01](./assets/readme/before_v01.png)