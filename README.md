# Robosys2020_DeviceDriver
ロボットシステム学の課題演習にて作成したプログラム

# 概要
もともとは講義内で作成したデバイスドライバを改造したものです

12月に入り、某百均店にて売られていた飾り物のクリスマスツリーを電飾したものです

# 動作環境
ハードウェア

・Raspberry Pi 4 Model B

ソフトウェア(OS)

・Ubuntu 20.04 
# 使用したもの
・Raspberry Pi 4 Model B　×1

・装飾するクリスマスツリー　×1

・ブレッドボード　×1

・LED (赤、黄、緑)　各色×3

・抵抗(330Ω)　×9

・リード線　×18
　(LEDの延長用)

・オス-メスジャンパー線　×5
　(Raspberry Pi ４との接続用)
 
 ※配線をしやすくするためにGPIO×3、GND×2としていたが、配線が上手い方は4本(GPIO×3,GND×1)でも大丈夫です

# 回路について
この回路では各色に1つのGPIOを割り当てています

3つのLED(同色)を並列につなげています

# ビルド方法
以下の手順で操作を行ってください

・インストール手順

`$ git clone https://github.com/NSOrange/Robosys2020_DeviceDriver.git`

`$ cd myled`

`$ make`

`$ sudo insmod myled.ko`

`$ sudo chmod 666 /dev/myled0`

・実行手順

`$ echo 1~3のうちの任意の数値 > /dev/myled0`

・終了する際に

`$ sudo rmmod myled`

# 実行について
・現在３つの発光パターンがあり、そのモード選択を1～3の数値で行ってます

・このプログラムではGPIOの使用しているピンもなんとなくクリスマスを連想させる番号を使ってます

　必要があれば25行目の{}内の3つ数値を任意のGPIOの番号に変えてください

・部屋を暗くして楽しんでください！

# 実際の動作
以下のURLより動画を視聴できます

https://www.youtube.com/watch?v=BrEtdw6s65M

# ライセンス
このリポジトリには以下のライセンスが付与されています

GNU General Public License v3.0

