# myled
ロボットシステム学　課題1で作成したデバイスドライバ
---
# 実装内容
- カップラーメンなどを作る時に使う3分間と5分間のタイマーです
- デバイスファイルに３を書き込むと3分経過後電子ブザーが鳴り、ledが点灯
- ５を書き込むと５分経過後電子ブザーが鳴り、ledが点灯
- ０（ゼロ）を書き込むと音がやみledが消灯
---
# 実験器具
- Raspberry Pi4 Model B
- ブレッドボード
- ジャンパーワイヤ
- 配線コード
- led（赤）
- 電子ブザー
---
# 回路
- プラス側をGPIO25番のピンに接続しています
<img src="https://user-images.githubusercontent.com/72371850/104026586-7ec5af00-5209-11eb-9e8c-f8dcd1c64ace.jpg" width="320px">

--- 
# 実行方法
``` bash
$ git clone https://github.com/taiyokiyohara/myled.git
$ cd myled
$ make
$ sudo insmod myled.ko
$ sudo chmod 666 /dev/myled0 
```
- 3分のタイマーをセット

` echo 3 > /dev/myled0 `

- 5分のタイマーをセット

` echo 5 > /dev/myled0 `

- 停止  
` echo 0 > /dev/myled0 `
---
# 動画
[YouTube](https://youtu.be/eYCgkhfP7zo)

---
