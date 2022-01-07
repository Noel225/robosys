# デバイスドライバ
2021年度のロボシス課題１のコードを少し変更した。
# 使用したもの
- ブレッドボード
- Raspberry Pi3 Model B
- LED 5本
- ジャンプワイヤ(オス-メス) 7本
- ジャンプワイヤ(オス-オス) 5本
# ピンの配置について
GPIOは2,14,17,20,25の5カ所です。GNDはどこでもいいです。
（因みにpinoutと打つと、GPIOやGNDの位置が分かります。）
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


# 参考
sleepを使いたいがどんなヘッダファイルを追加すればよいか分からなかったため、以下の方のリポジトリを参考にした。
https://github.com/MiyamotoKK/robosys_devicedriver
