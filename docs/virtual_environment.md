# 仮想環境のすゝめ

## Why 仮想環境？
- １つの仮想開発環境に、一つのPythonと必要なパッケージがインストール可能。
- それによりプロジェクトごとに開発環境を作ることが可能。
- ディレクトリを削除すれば開発環境を削除可能。
- PC内にあるローカルのPythonにパッケージをインストールしないため、競合や不具合なども起きにくい。

いわゆる、環境が壊れるのを防ぐためですね。

「え、Anaconda版とPython公式版を混ぜなければ壊れないんじゃないの！？」

と思うかもしれません。
その認識は間違いではありません。
が、様々なライブラリやツールを使用する際、ライブラリ（あるいはパッケージ）のバージョンが指定されることがあります。

さて、**一つの環境でいろんなことをし、たくさんのライブラリをごちゃごちゃにしたら何が起こるでしょう...**  
恐ろしいですね、首都高速でエンドレス玉突き事故が起きているようなものです。  

そういうことを防ぐためにも、仮想環境を使ってやっていくのがおすすめです。  
まぁ、執筆者は学外でやってる活動もあって、環境破壊しないようにしてるだけなので。

（これは強制ではありません、興味があればやってみてください。）

!!! note
    環境を破壊してしまうと、環境を作り直す必要があります。大変めんどくさいですね。
    「環境をぶっ壊～す」を防ぐために、仮想環境を使ってやっていきましょう。
    え、さっき強制じゃないって言ったじゃんって？さぁ、なんのことやら。

## 仮想環境の種類
仮想環境には、いくつか種類があります。ピックアップしましょう。

- venv
- virtualenv
- conda

### venv
Python3.3から標準で付属している仮想環境です。  
Python3.3以降のバージョンであれば、`venv`コマンドで仮想環境を作成できます。

### virtualenv
Python2.7以前のバージョンで使用されていた仮想環境です。  
Python3.3以降のバージョンでも使用可能ですが、`venv`の方が標準で付属しているので、`venv`を使うことをおすすめします。

### conda
Anacondaに付属している仮想環境です。  
Anacondaをインストールすると、`conda`コマンドで仮想環境を作成できます。

てな感じで、最初から仮想環境が作れるようになってたりします。
なお、venvとvirtualenvはPythonの標準ライブラリではないので、pipでインストールする必要があります。

あと、venv+Poetryという組み合わせもあります。ガッチガチに環境を固めたい人はこちらを使うと良いでしょう。

### どれを使えばいいの？
**どれでもいいです。**
ただ、Anacondaを使っている人はcondaを使うと良いでしょう。  
僕は宗教（派閥）上の理由でvenvを使っています。

### まとめ
- venv
    - Python3.3以降のバージョンで使用可能
    - Pythonの標準ライブラリではないので、pipでインストールする必要がある
    - Poetryと組み合わせることで、環境をガッチガチに固めることができる
- virtualenv
    - Python2.7以前のバージョンで使用可能
    - Python3.3以降のバージョンでも使用可能
    - Pythonの標準ライブラリではないので、pipでインストールする必要がある
- conda
    - Anacondaに付属している
    - Anacondaをインストールすると、`conda`コマンドで仮想環境を作成できる
