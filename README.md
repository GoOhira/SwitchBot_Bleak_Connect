# BleakによるSwitchBotとの通信(Windows10)
Window10でのSwitchBotとのBLE通信の方法を記述します。言語はpython
とはいえSwitchBotのための特別な仕様があるわけではなく、Bleakを使用してSwitchBotに接続して命令を送信しているだけです
# 要件
* OS Windows10
* python 3.7.6
* bleak 0.7.1
* Bluetooth_Dongle 5.0

# 初期設定
Window10がBlueTooth通信ができる状態である必要があります。Bluetoothドングルを使用する場合、以下URLからドライバをダウンロードしてください。
### https://www.dropbox.com/s/vcvemz9rwr711rl/5.zip?dll=0

以下のpipコマンドを実行してbleakライブラリを取得します

    pip install bleak

[Discover.py]を実行し、周辺のBluetooth機器、つまりSwitchBotを探します。見つかった場合にはSwitchBotのMacアドレスが表示されます。それを基に[Bleak_Connect_SwitchBot.py]の中の[address]の値を書き換えてください

    
    address = " " #各自のSwitchBotのMacアドレスに書き換える

