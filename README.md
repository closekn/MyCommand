# MyCommand

ターミナル用自作コマンド

## 目的

コマンドの勉強 & シェルスクリプトの練習

## 使用法

- MyCommandディレクトリにPATHを通す
```.zshrc
export PATH="$PATH:hoge/piyo/MyCommand"
```
- 各コマンドに実行権限がない場合は実行権限を付与する
```
> chmod a+x hoge
```

## コマンド

### mycpp

競プロ用cppファイル作成コマンド
```
> mycpp hoge
```
により、内容が以下の hoge.cpp を作成する。
```cpp:hoge.cpp
#include <bits/stdc++.h>
using namespace std;

int main() {


  return 0;
}
```
引数の数だけ各引数名のcppファイルを作成する。
カレントディレクトリに既に同名cppファイルがある場合は作成しない。

### ipcs-kill

共有メモリ、セマフォ、キューを全消去するためのコマンド<br>
引数はなし。

## 更新

あると良いと思うコマンドを何か思いついたら
