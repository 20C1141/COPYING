# report1
ロボットシステム学　課題

# 概要
講義ビデオを見て著作権やライセンスを考慮し、デバイスドライバを作成する。

# 準備するもの
Raspberry Pi 3 Model B
抵抗（200Ω）×１
発光ダイオード　×１
ブレットボード　×１
ジャンパーワイヤ　×２

# 回路
以下のように接続する。
![image](https://user-images.githubusercontent.com/67887230/146323253-d0888f15-a497-4c7d-9b49-b461fd9e7498.png)
ラズパイのGPIO25と抵抗、LEDとラズパイのGroundを接続する。

# インストール
以下のコマンドをターミナルで実行する。
$ git clone git@github.com:20c1141/report1.git

$ cd report1/

$ make

$ sudo insmod myled.ko

$ sudo chmod 666 /dev/myled0

# 実行方法
LEDを点灯させる
$ echo 1 > /dev/myled0
LEDを消灯させる
$ echo 0 > /dev/myled0

# サンプル動画
https://youtu.be/rFYxb5qziAI

# ライセンス
GNU General Public Lイセンセv2.0
以下のURLから閲覧可能。
https://github.com/SakaTaku2/robosys_report1/blob/3394557b1d9618ffd1dcc6306e8000a87f2b1b60/LICENSE


