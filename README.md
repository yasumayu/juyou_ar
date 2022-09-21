### コンテナ起動の手順

1.最初に実行するコマンド (docker-compose.yamlの存在するディレクトリで行う) 
docker-compose run python-django-opencv  django-admin.py startproject composeexample .

2.コンテナ二つを起動するコマンド  
docker-compose up -d

3.起動されたコンテナの確認  
docker-compose ps                       
![ps](https://user-images.githubusercontent.com/84883605/191478555-62ed3f78-d462-4dd7-919a-51fa2422e075.png)



<その他>

・１つずつコンテナ起動  
docker-compose run db-sqlite3  
docker-compose run python-django-opencv

・ファイル所有権の変更  
sudo chown -R $USER:$USER .

