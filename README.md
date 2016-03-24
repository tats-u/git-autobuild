# Git自動ソースビルダー

##概要
Gitのバージョンを確認して最新版をソースビルドしてインストールするまで自動で行うシェルスクリプトです。

##予めインストールしておくべきもの
- tcsh
- [porg](http://porg.sourceforge.net/)
- その他Gitのソースビルドに必要なもの(各種ライブラリ)

##利用方法
(初回)

```Bash
git clone https://github.com/git/git git
cd git
wget https://raw.githubusercontent.com/tats-u/git-autobuild/make_git
chmod +x make_git
./make_git
```

(2回目以降)
```Bash
cd git
./make_git
```

##大学等のSSHサーバでの利用において
このスクリプトはホスト名に「`.jp`」が入っている場合はサーバモードになります。このモードでは「`./make_git root`」と引数に「`root`」をつけて実行しない場合は一般ユーザとみなし、`~/local/`以下にインストールされます。つけた場合は管理者とみなし、通常通り`/usr/local`以下にインストールされます。また、ホスト名(`hostname -s`の実行結果)が「`ssh`」で、一般ユーザの場合サーバの負担を抑えてインストール作業を行います。

##ライセンス
このソフトは、MITライセンスでライセンスされています。(`LICENSE`参照)
