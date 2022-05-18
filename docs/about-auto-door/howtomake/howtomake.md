# 開き戸自動化プロジェクト

## 開き戸自動化プロジェクトについて

[Rekonstruu Auxtomatan Pordon](https://github.com/Rekonstruu-Auxtomatan-Pordon/Rekonstruu-Auxtomatan-Pordon) 通称「RAP」は開き戸を再構築して、自動化を図るツールを開発するためのプロジェクトです。Raspberry Pi 3台と[C++](https://isocpp.org/)言語にて成り立っています。

### 開き戸自動化プロジェクトのビルド方法

この節では実際に[g++](https://gcc.gnu.org/onlinedocs/gcc-11.3.0/libstdc++/manual/)を使い、本プロジェクトをビルドする方法について解説します。

#### 依存ファイルのインストール

本プロジェクトは、[g++-11](https://packages.debian.org/sid/g++-11),[make](https://packages.debian.org/bullseye/make),[pigpio](https://github.com/joan2937/pigpio)によって成り立っています。
g++は[apt](https://tracker.debian.org/pkg/apt)コマンドで普通にインストールすると古いバージョンが落ちるため、注意してください。

1. gcc-11とg++-11のインストール

    ```shell
    sudo apt install gcc-11 g++-11
    ```

2. build-essentialのインストール

    ```shell
    sudo apt install build-essential
    ```

3. gcc,g++コマンドを代替バージョンに切り替える

    ```shell
    sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-11 80 --slave /usr/bin/g++ g++ /usr/bin/g++-11 --slave /usr/bin/gcov gcov /usr/bin/gcov-11
    sudo update-alternatives --config gcc
    sudo update-alternatives --config g++
    ```

4. gcc,g++のバージョンを確認する

    ```shell
    gcc -v
    g++ -v
    ```

5. gitをインストールする

    ```shell
    sudo apt install git
    ```

以上のステップを踏むことで、ビルドできます。

#### ビルドの方法

では、実際にビルドしてみましょう!

1. gitからファイルをクローンする
    任意のディレクトリへ移動してください。
    そこで、

    ```shell
    git clone --recursive https://github.com/Rekonstruu-Auxtomatan-Pordon/Rekonstruu-Auxtomatan-Pordon.git
    ```

2. srcディレクトリへ移動する

3. ディレクトリ内でmakeコマンドを走らせる

    ```shell
    make all
    ```

4. 生成したファイルを走らせる

### 開き戸自動化プロジェクトの回路の作り方

### 開き戸自動化プロジェクトの3dプリント

### 開き戸自動化プロジェクトのRaspberry Piの配線

## 参考文献

[How to Install GCC Compiler on Ubuntu 22.04 LTS](https://www.linuxcapable.com/how-to-install-gcc-compiler-on-ubuntu-22-04-lts/)
