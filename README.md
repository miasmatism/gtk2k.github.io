# gtk2k.github.io
WebSocketBridgeHMDPositionSensorVRDevice を追加したWebVR Boilerplateサンプルページです。WebVR Boilerplate本来のWebVR対応、キーボード/マウス操作対応、Cardboard対応と、今回追加したWebSocketブリッジデバイス対応の動作確認用です。
IE11はビデオテクスチャーに対応しておらず、Firefoxはビデオテクスチャーに対応しているのですがものすごく重くなり、OperaやVivaldiはOcuBriが現在サポートしていないため、実質Chromeのみ対応という状況となっています。
* [test.html](http://gtk2k.github.io/test.html) PCでは4000x2000(mp4またはwebm)、モバイルでは1920x960(mp4)にビデオソースを切り替えるページです。
* [test_mp4.html](http://gtk2k.github.io/test_mp4.html) PC用:4000x2000でコーデックがh264の動画に限定したページです。
* [test_vp8.html](http://gtk2k.github.io/test_vp8.html) PC用:4000x2000でコーデックがVP8の動画に限定したページです。
* [test_vp9.html](http://gtk2k.github.io/test_vp9.html) PC用:4000x2000でコーデックがVP9の動画に限定したページです。

##動作確認方法
以下の各種ブラウザーからページにアクセスして画面の下中央にあるWebVRアイコンをクリックするとそれぞれの動作確認が行えます。
キーボード/マウス操作はPCからページにアクセスした時点でキーボードやマウスでの操作ができます。
* WebVR: ChromeのWebVRビルド版
* Cardbard: Chrome for Android
* WebSocketブリッジ([OcuBri](https://github.com/gtk2k/OcuBri)): PC用Chromeの安定版でアクセスし、[OcuBri](https://github.com/gtk2k/OcuBri)を実行した後でアイコンをクリックしてください。

##問題点
私のマシン環境が多分に影響していると思いますが以下の問題点があります。
* Oculus Riftでのフレームレートがよくありません。Firefoxではビデオテクスチャー自体フレームレートがよくありません。
* mp4においてはalert()を実行したりすると再生が止まってしまいます。
* ループ再生するよう設定しているのですが、これもまたmp4では１回目の再生終了時点で止まってしまいます。

###私のマシン環境
- MacBook Pro: Mid 2012 Model A1398 EMC 2512
- CPU: i7-3615QM 2.3GHz
- Memory: 8GB
- GPU: GeForce GT 650M (Driver ver: 350.12)
- OS: Windows 8.1(Boot Camp)
