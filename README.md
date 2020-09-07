# HTTPS Server Example

##### ESP32-WROVER(TTGO Camera)でHTTPS Serverを立ち上げPCとSSL通信をする(開発環境ESP-IDF & Eclipse)
  

少々長いタイトルですが、以前のTTGO T-CameraをESP-IDF & Eclipseで動かすでHTTP Serverを立ち上げPC or スマホからカメラ画像を取得してみました。

今回はそれをHTTPS ServerにしてSSL通信してみます。ただし送受信するデータはカメラ画像ではなく文字データだけなのでESP32-WROVER(TTGO Camera)というタイトルになっています。ESP32-WROVER類なら何でもいいのですが私が持っているのがTTGO Cameraだけなのでこれを使っています。

また"PCと"と限定しているのはSSL通信するにはルート証明書(オレオレ証明書)というものをPCにしか登録を試していないのでPC限定になっています。

最終目的がPCアプリとの通信なのでスマホはとりあえずスルーしています。

・ｍDNS(DNS名：esp32-mdns.local)にも対応しました。  
・POSTリクエストにも対応しました(エコーバック)。

sdkconfig→Example Connection Exampleのmyssidとmypasswordはご自身の環境のSSIDとPasswordを入力してください。

cacert.pemとprivate.pemはTemplateに入っているものなので
https://neocode.jp/2020/09/02/esp32-wroberttgo-camerahttps-serverpcsslesp-idf-eclipse/
を参考に自分自身で作ってみてください。