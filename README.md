# デバイスドライバ
2021年度のロボシス課題１のコードを少し変更した。

# LEDの消灯
echo 0 > /dev/myled0
# LEDの点灯
echo t > /dev/myled0
# LEDの点灯(光る順番が逆になる)
echo h > /dev/myled0
