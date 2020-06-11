# MyCommand

ターミナル用自作コマンド

## 目的

コマンドの勉強 & シェルスクリプトの練習

## 使用法

- MyCommandディレクトリにPATHを通す

```zsh
export PATH="$PATH:hoge/piyo/MyCommand"
```

- 各コマンドに実行権限がない場合は実行権限を付与する

```zsh
> chmod a+x hoge
```

## コマンド

### mycpp

競プロ用cppファイル作成コマンド

```zsh
> mycpp hoge
```

により、内容が以下の hoge.cpp を作成する。

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {


  return 0;
}
```

引数の数だけ各引数名のcppファイルを作成する。
カレントディレクトリに既に同名cppファイルがある場合は作成しない。

### mygo

競プロ用goファイル作成コマンド  
操作はmycppと同様  
内容が以下のgoファイルを作成する。

```go
package main

import (
  "bufio"
  "fmt"
  "os"
  "strconv"
)

var sc = bufio.NewScanner(os.Stdin)
var wtr = bufio.NewWriter(os.Stdout)

func nextInt() int {
  sc.Scan()
  i, e := strconv.Atoi(sc.Text())
  if e != nil {
    panic(e)
  }
  return i
}

func nextLine() string {
  sc.Scan()
  return sc.Text()
}

func main() {
  //sc.Split(bufio.ScanWords)
}
```

### md4thesis

論文まとめ用のマークダウンファイル作成コマンド
引数に論文タイトル(空白無し)を用いる。

```sh
> md4thesis title
```

により、内容が以下の title.md を作成する。

```md
# $title

## Info

- Author
- Source
- Year of pPublication

[link]()

## Summary

### What research

### Better than previous research

### Core Technologies & Methods

### Verification/Experiment methods

### Future research

### My thoughts

### Relations

## Special note
```

### ipcs-kill

共有メモリ、セマフォ、キューを全消去するためのコマンド  
引数はなし。

## 更新

あると良いと思うコマンドを何か思いついたら
