# IRCMAP - munin plugin

https://travis-ci.org/koi-chan/munin-ircmap.svg?branch=master

munin で、任意の IRC サーバ・ネットワークの情報を取得するためのプラグイン。

# 使い方

1. 任意のディレクトリにリポジトリをチェックアウトするか、実行ファイルと設定ファイルをダウンロード・配置する。
2. munin のプラグインディレクトリから実行ファイルにシンボリックリンクを張る。
3. munin-node を再起動する。

```bash
cd /opt
sudo git clone https://github.com/koi-chan/munin-ircmap.git
cd munin-ircmap
sudo vi config.rb
sudo bundle install --path vendor/bundle --deployment
cd /etc/munin/plugins
sudo ln -s /opt/munin-ircmap/irc_map .
sudo systemctl reload munin-node
```

# 動作環境

Ruby スクリプトとして実装されているので、Ruby の実行環境が必要です。  
また、ライブラリとして ruby-gems を利用しているため、bundle が使えるようになっている必要があります。

# 開発・動作確認環境

* CentOS 7.1
* Ruby 2.3.1
* irc.cre.jp (IRC サーバ)

# ライセンス

[MIT License](LICENSE)（[日本語](LICENSE.ja)）
