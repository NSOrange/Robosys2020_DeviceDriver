# Robosys2020_DeviceDriver
ロボットシステム学の課題演習にて作成したプログラム

# 概要
もともとは講義内で作成したデバイスドライバを改良したものです

12月に入り、某百均店にて売られていた飾り物のクリスマスツリーを電飾したものです

# 使用したもの
・Raspberry Pi 4 Model B

・ブレッドボード

・オス-メスジャンパー線　×5
　(Raspberry Pi ４との接続用)

・リード線　×18
　(LEDの延長用)

・LED (赤、黄、緑)　各色×3

・抵抗(330Ω)　×9

・装飾するクリスマスツリー
以下が装飾前の物の写真です

# ビルド方法
以下の手順で操作を行ってください

$ git clone https://github.com/NSOrange/Robosys2020_DeviceDriver.git

$ cd myled

$ make

$ sudo insmod myled.ko

$ sudo chmod 666 /dev/myled0

$ echo 1~3のうちの任意の数値 > /dev/myled0

終了する際に

$ sudo rmmod myled

# 実行について
現在３つの発光パターンがあり、そのモード選択を1～3の数値で行ってます

GPIOの使用しているピンもなんとなくクリスマスを連想させるものを使ってます

部屋を暗くして楽しんでください！

# 実際の動作
以下のURLより動画を視聴できます

https://www.youtube.com/watch?v=BrEtdw6s65M

# ライセンス
このリポジトリには以下のライセンスが付与されています

GNU General Public License v3.0

