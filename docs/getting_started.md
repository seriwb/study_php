# For Mac

### Apacheのあれこれ

- 起動
      sudo apachectl start
  起動したらhttp://localhost/  にアクセス

- 停止
      sudo apachectl stop
PHPの設定をする場合は、Apacheを止めておく。

- ドキュメントルート
      /Library/WebServer/Documents

- PHPの作業フォルダをwebappsにシンボリックリンク
      ln -s リンクさせたいフォルダのパス シンボリックリンクを置きたい場所
      sudo ln -s /Users/xxxxx/git/study_php/src/php /Library/WebServer/Documents

#### httpd.conf

- デフォルトの場所
      /etc/apache2/httpd.conf

- PHPをApacheから利用可能にする
      LoadModule php5_module libexec/apache2/libphp5.so

- index.phpを省略可能にする
      DirectoryIndex index.html index.php
