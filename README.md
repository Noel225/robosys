# デバイスドライバ
2021年度のロボシス課題１のコードを少し変更した。

# ピンの配置について
GPIOは2,14,17,20,25の5カ所です。GNDはどこでもいいです。
（因みにpinoutと打つと、GPIOやGNDの位置が分かります。）
# LEDの消灯
echo 0 > /dev/myled0
# LEDの点灯
echo t > /dev/myled0
# LEDの点灯(光る順番が逆になる)
echo h > /dev/myled0
