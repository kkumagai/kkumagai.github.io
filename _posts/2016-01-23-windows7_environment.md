---
layout: post
title: "会社PC更新時に行ったWindows7環境構築メモ"
category: blog
published: true
---

先日会社PCを変更し、久しぶりにWindows環境を再構築したのでメモ。

# キーボード配列入替え系
入社一年目からAutoHotKeyを使っており、あっという間にこれなしでは生きられない体に。特に、Win + IJKLを方向キーにするのは右手をほとんど動かさずに方向キー操作が完了するのでおすすめ。
あと、CapsLockをそのまま使っている人は、頭がどうかしてるんじゃないかと思う。

- [AutoHotkey](https://autohotkey.com)
    - Win + IJKL を方向キーに
        -これをやるとWin + L 入力時にエラーになるので、[レジストリをいじってWin + L をつぶす](http://www.howtogeek.com/howto/windows-vista/disableenable-lock-workstation-functionality-windows)
    - Win + N/M を Backspace/Deleteに
    - Win + H/: を Home/Endに
    - Win + A を右クリックに
    - F1キーを無効にする
- [CapsLockをCtrlに](http://www.forest.impress.co.jp/library/software/changekey/download_10668.html)
- Ctrl+SpaceをIMEのON/OFFに（Google日本語入力より設定）

# ソフトインストール

コンサル会社って仕事柄いろいろなソフトをインストールできるのがいいところです。就職先をきめたときも会社PCへのインストールが制限されていないことを確認してから入社しました。そうじゃない会社には転職できないなー。

## ブラウザ: Chrome
定番

## IME: Google日本語入力
IMEは、標準インストールのMicrosoft
IMEでいいかなと思って2,3日使ってみたけれど、変換・圧縮が圧倒的にイケておらずすぐに耐えられなくなってGoogle日本語入力をインストールしました。

## ファイラ: [cFiler](https://sites.google.com/site/craftware/cfiler)
中学生のころからあふのヘビーユーザーで２画面ファイラー万歳です。
黒い背景を扱っているとクライアントをビビらせる効果も。

## 圧縮解凍: [Lhaz](http://chitora.com/lhaz.html)
解答せずにフォルダの中身を閲覧できるので気に入っています。

## テキストエディタ: [Sublime Text3](http://www.sublimetext.com/3)
何度かAtomもいいなーと思いつつも結局こちらに。(以前自宅Macで使おうとして偉い重くなったので敬遠してしまいました。)なんだかんだ前のPCではSublime2 と Sublime3が併存してしまっていたので、3に一本化を完了。

こちらを見ながら設定。 [[tips][Sublime Text] Sublime Text 3をインストールしたらまずやること](undefined)
    - Convert to UTF8
    - trailing spaces

## メモ: [Boostnote公式サイト](https://b00st.io/jp/)
年明けあたりから急に話題になっているソフト。[プログラマのための"和製"メモ帳Boostnoteをつかってみた！設定法や使用法についての記載あり！ - プログラミング向上雑記](http://niisi.hatenablog.jp/entry/2016/01/12/220000)

仕事柄、議事メモとか資料作成の骨子をどうしようかな？とメモを取る機会は結構あり、Evernoteにはじまり、SimplenoteやResophnoteなど、いろいろなメモアプリを試してみたけど、これはというものがなく結局いつもSublimeTextに戻ってましたが、PC交換してから使い始めたBoostnoteは圧倒的にしっくり来ているので定番化しそう。

## スクリーンショット: [Light Cutter](http://www.vector.co.jp/soft/win95/art/se261807.html)
メールでいろいろやり取りする場合にサッとスクリーンショットもつけてメールを送ることが多い。

## Python環境: [anaconda](https://www.continuum.io/downloads)
最初はビッグデータ関連の分析で使い始めましたが、最近は大概の分析をiPython notebook(Jupyter)で行うことが多いです。

コンサルというとEXCELをめっちゃ使いこなして徹夜で分析！というイメージがありますが、ロジックをプログラムとして書いていくPythonやRでの分析と比べて、操作を手作業で行うEXCELは、ミスも多く、後で計算ロジックの確認・修正コストがめちゃくちゃ大きいためできれば使いたくありません。(DBからのデータ抽出→分析作業→グラフ表など結果を作成
するまでの作業が一気通貫でできるので非常に便利。

あと、一度作ったコードを使いまわせるようにしておくと、使えば使うほど生産性が上がっていい感じ。Excelだと入社１年目にショートカット覚えて作業が早くなって以降、作業スピードは大幅には上がらないのでは？という疑いがあります。

- [現代のエンジニアのための強力なメモ帳 Jupyter notebookのすゝめ - クックパッド開発者ブログ](http://techlife.cookpad.com/entry/write-once-share-anywhare)
- [The IPython Notebook — IPython](http://ipython.org/notebook.html)

グラフ作成パッケージのmatpotlibの日本語設定ではまった。こちらのページの解決方法がわかりやすかったです。

- [【matplotlib】日本語の設定 - keisukeのブログ](http://kaisk.hatenadiary.com/entry/2015/02/15/215831)

## Gitクライアント: [TortoiseGit](https://tortoisegit.org/)

Pythonを使うことが多くなったので、最近は別場所で働くチームと分析結果をGitで管理できるようになりました。

## VPN: [vpnux client](https://www.plum-systems.co.jp/vpnux-client/)

AWS上の分析基盤にアクセスする際につかってます。
