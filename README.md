##########コンテナ起動の手順##################################################################

#以下自分のworkspace内で実行していく
$ cd
$ cd (worlspace-name)

#最初に実行するコマンド
docker-compose run python-django-opencv  django-admin.py startproject composeexample .

#コンテナ二つを起動するコマンド
docker-compose up -d

#起動されたコンテナの確認
docker-compose ps                       

#ファイル所有権の変更
sudo chown -R $USER:$USER .





###以下はメモ###
#１つずつコンテナ起動
docker-compose run db-sqlite3
docker-compose run python-django-opencv
