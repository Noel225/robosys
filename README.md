# デバイスドライバ
2021年度のロボシス課題１のコードを少し変更しました。
# 環境
Ubuntu Server 20.04
# 使用したもの
- ブレッドボード
- Raspberry Pi3 Model B
- LED 5本
- ジャンプワイヤ(オス-メス) 7本
- ジャンプワイヤ(オス-オス) 5本
- 抵抗 180Ω 5本
# ピンの配置について
GPIOは2,14,17,20,25の5カ所です。GNDはどこでもいいです。
（因みにpinoutと打つと、GPIOやGNDの位置が分かります。）
![gazo](https://user-images.githubusercontent.com/92023120/148549805-f329cfae-7e3b-4912-a2ec-6390b1c87caf.jpeg)
![gazo2](https://user-images.githubusercontent.com/92023120/148550502-96d559d2-27ef-40c4-814e-8fe3a09c8758.png)
# インストール
- git clone https://github.com/Noel225/robosys.git
- cd robosys
- make
- sudo insmod myled.ko
- sudo chmod 666 /dev/myled0
# LEDの消灯
echo 0 > /dev/myled0
# LEDの点灯(１つずつ光る)
echo t > /dev/myled0
# LEDの点灯(光る順番が逆になる)
echo h > /dev/myled0
# アンインストール
sudo rmmod myled

# 動画
https://youtu.be/7w-jiCp_I7s

# 参考
sleepを使いたいがどんなヘッダファイルを追加すればよいか分からなかったため、以下の方のリポジトリを参考にしました。
https://github.com/MiyamotoKK/robosys_devicedriver
