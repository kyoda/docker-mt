# Docker for Movable Type

webのdocker imageはcentos7です。

# Note

+ utf8mb4設定時の"The maximum column size is 767 bytes."
  - mysql 5.7にしmy.cnfで対応
+ volumesの権限
  - 起動後にapache権限に変更
  - docker-compose exec mt-web chown apache. -R /var/www/html /var/www/cgi-bin
+ exit 1でmt-dbが停止している場合は、db_logに書き込み権限が必要かもしれない
  - chmod 777 db_log
