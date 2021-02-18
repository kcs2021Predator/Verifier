# Verifier
<img src="https://img.shields.io/badge/-Raspberrypi-C51A4A.svg?logo=raspberrypi&style=plastic"> <img src="https://img.shields.io/badge/-Python-F9DC3E.svg?logo=python&style=flat">  <img src="https://img.shields.io/badge/-Docker-1488C6.svg?logo=docker&style=plastic">

![画像 -20210218-003724-54e67f9a](https://user-images.githubusercontent.com/79233748/108295060-61a5d800-71da-11eb-8d5d-854f1858b0b5.jpeg)
---
# Verifier
RaspberryPi4を使って体温とマスク着用判定を行います。
マスク付けていない場合には赤色LEDが発光しブザーを鳴らします。
付けている場合は緑色LEDが発光しブザーは鳴りません。

実行環境が無ければエラーが出ますので
モジュールの確認をしましょう。

必要モジュール
AMG8833 Webカメラ or RaspberryPiカメラ 
buzeer 色付きLED

コンソールで以下の通りに出ていれば成功しています。
```
\# i2cdetect -r -y 1
     0  1  2  3  4  5  6  7  8  9  a  b  c  d  e  f
00:          -- -- -- -- -- -- -- -- -- -- -- -- --
10: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
20: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
30: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
40: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
50: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
60: -- -- -- -- -- -- -- -- 68 -- -- -- -- -- -- --
70: -- -- -- -- -- -- -- --
```

以上出来たら次はインストールです。
以下のコードをコンソール(時間がかかる事があります。）
```
$ git clone https://github.com/ForexRobotics/mask_camera.git

$ cd mask_camera/docker

$ sudo docker build -t fr/l4t-ml:1.0 .

Q.終了するには？
A.Qキーを押す事で終了できます。


