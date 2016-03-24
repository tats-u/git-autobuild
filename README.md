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

##ライセンス
このソフトは、MITライセンスでライセンスされています。(`LICENSE`参照)
