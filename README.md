# flask-todo
##FlaskでTodoアプリを作ってみた
・Python＋SQLite
・piで実行
・uWSGIをアプリサーバとし、nginxでWebアクセスさせる
# コマンド類
## piコマンド類
・起動：
```
$cd ~/flasktodo/
$uwsgi --ini flasktodo.ini
```
・停止：
```
$uwsgi --stop /tmp/flasktodo.pid
```
・リロード：
```
$uwsgi --reload /tmp/flasktodo.pid
```

## デーモン化後
起動：
```
$sudo systemctl start flasktodo.service
```

再起動：
```
$sudo systemctl restart flasktodo.service
```

停止：
```
$sudo systemctl stop flasktodo.service
```

常時起動設定：
```
$sudo systemctl enable flasktodo.service
$sudo systemctl disable flasktodo.service    #解除
```
