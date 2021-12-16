# COPYING
ロボットシステム学　課題

# 概要
ロボットシステム学第7，8回の講義動画を見てデバイスドライバを作成し、同講義第9回のビデオを見て著作権やライセンスに配慮する。

適当なディレクトリにmyled.cを作る。

MakeFileという名前のファイルを作る。（後処理の手順を書いたファイル）

myledに動画を見ながら書き足す。

動作確認。（下記の実行方法）

githubでリポジトリを作成。

作成したリポジトリをUbuntuにcloneしてmyled.cとMakeFileを移動。

# 動作環境
Ubuntu 18.04 LTS

Raspberry Pi 3 Model B

# 準備するもの
抵抗（200Ω）×１

発光ダイオード　×１

ブレットボード　×１

ジャンパーワイヤ　×２

# 回路
以下のように接続する。
![image](https://user-images.githubusercontent.com/67887230/146323253-d0888f15-a497-4c7d-9b49-b461fd9e7498.png)
ラズパイのGPIO25と抵抗、LEDとラズパイのGroundを接続する。

回路図は以下のようになる。

![スクリーンショット 2021-12-16 190848](https://user-images.githubusercontent.com/67887230/146351771-d644fe15-d6be-4559-a69b-0cdc157f06d8.png)



# インストール
以下のコマンドをターミナルで実行する。

$ git clone https://github.com/20C1141/COPYING.git

$ cd COPYING/

$ make

$ sudo insmod myled.ko

$ sudo chmod 666 /dev/myled0

# 実行方法
LEDを点灯させる

$ echo 1 > /dev/myled0

LEDを消灯させる

$ echo 0 > /dev/myled0

# 後処理

$ sudo rmmod myled

$ make clean

# サンプル動画
https://youtu.be/rFYxb5qziAI


# ライセンス
GNU General Public Licensev2.0
以下のURLから閲覧可能。
https://github.com/SakaTaku2/robosys_report1/blob/3394557b1d9618ffd1dcc6306e8000a87f2b1b60/LICENSE


