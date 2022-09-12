#https://hub.docker.com/_/python(OS:Debian Linux)
FROM python:3

#コンテナで/codeディレクトリ作成
RUN mkdir /code
#作業ディレクトリ
WORLDIR /code

#requirements.txtをコンテナにコピー
COPY requirements.txt /code


# opencv-devのインストール
RUN apt-get update -y && apt-get install -y libopencv-dev \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*


#vimのインストール
RUN apt-get update -y && apt-get install -y vim

#requirements.txtに書かれているパッケージをインストール
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

