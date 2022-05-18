# 初めに

こちらの文章は、**492470977eacf262d76e85bbec6ea6a4363c69a4** に基づいて書かれています。内容が古い場合があります。

## ソースコードについて

本プロジェクトでは、C++23を採用しました。理由としては、私がC++の勉強をしたいため、最新版のC++23を選びました。

### main.cppのソースコード

main.cppのソースコードを以下に示します。

``` cpp
#include "headers/stdafx.hpp"

const int FRONT_DOOR_SENSOR 11
const int BACK_DOOR_SENSOR 13

int main()
{
 // 初期化
 if (gpioInitialise() < 0)
 {
  std::cerr << "pigpio初期化失敗!!: " << e.what() << std::endl;
 }
 // GPIOの入力設定 
 if (gpioSetMode(FRONT_DOOR_SENSOR, PI_INPUT) != 0)
 {
  std::cerr << "フロントドアの設定失敗!!: " << e.what() << std::endl;
 }
 if (gpioSetMode(BACK_DOOR_SENSOR, PI_INPUT) != 0)
 {
  std::cerr << "背面ドアの設定失敗!!: " << e.what() << std::endl;
 }
 //メインループ
 while(1){
  
 }
 // pigpioの終了
 gpioTerminate();
    return 0;
}
```

### main.cppの解説

ソースコードの解説です。

1行目では、stdafx.hppをインクルードしています。このヘッダファイルは何かというと、ヘッダファイルをまとめたヘッダファイルとなっています。わざわざまとめた理由は、ヘッダファイルをプリコンパイルするためです。  
3-4行目では、定数として、前のドアセンサ、後ろのドアセンサのGPIOのピン番号を設定しています。C言語ではよくdefine文が使われますが、C++では、型チェックの厳格化のために、このようにconst型名で定数を宣言できます。  
9行目では、pigpioの初期化をしています。初期化をしないと使えません。  
14-18行目では、GPIOピンをインプット設定して、センサからデータを入力できるようにしています。  
27行目は、これがないと、ほかのプログラムでGPIOが使えません...  
