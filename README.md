# ros2_ws/src/mypkg
* robosys2023_ros2
# 概要
[![test](https://github.com/erisu-Y/robosys2023/actions/workflows/test.yml/badge.svg)](https://github.com/erisu-Y/ros2_robosys/actions)

* ロボットシステム学の講義内で、ros2環境におけるプロセス間通信を学び、  
  ロボットシステムへの理解を深めるためのリポジトリである。
* ロボットシステム学　第2回目の課題提出用。
* ros2 foxy環境下での使用を想定。

## ダウンロード
`$ git clone https://github.com/erisu-Y/ros2_robosys.git`

## テスト環境
* Ubuntu20.04
* ros2 foxy
* Python3

## ノード&トピック概要
### ノード
#### talker
* 実行後に変数nを1ずつ増やして数字をカウントして、トピック/countupを通じて送信する。
* 今回のメッセージの型は16ビット符号つき整数である。

#### listener
* 実行後にトピック/countupよりもらったメッセージ内容を表示する。

### トピック
#### countup
* talkerより受け取った変数をlistenerに送信する。

## 実行手順&インストール方法概要
### <注意>ros2 foxy環境下で実行することが前提である。
1.上記のダウンロードの項目に記載されている`git clone`コマンドを用いて、このリポジトリを`ros2_ws/src`の下にコピーする。  
2.`cd ~/ros2_ws/`コマンドを用いてros2_wsディレクトリに移動し`colcon build`を行う。  
3.1つ目の端末で`ros2 run mypkg talker`を用いてtalkerを実行する。  
4.2つ目の端末で`ros2 run mypkg listener`を用いてlistenerを実行する。  
5.満足のいくまで数字をカウントしたら`Ctrl+C`を用いて終了する。  
## ライセンス
* このソフトウェアパッケージは、3条項BSDライセンスの下、再配布および使用が許可されます。  
* このパッケージのコードは、下記のスライド(CC-BY-SA 4.0 by Ryuichi Ueda)のものを、本人の許可を得て、いくつか変更点を加え、自身の著作としたものです。  
[ryuichiueda/my_slides/robosys2023/lesson4.md](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)  
©　2023 Yuto Okuda
