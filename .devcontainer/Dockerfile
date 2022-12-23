FROM tensorflow/tensorflow:latest-gpu
#過去バージョンを使う場合(FROM tensorflow/tensorflow:2.8.0-gpu など)
#apt-getコマンドを使用するとでGPG errorが発生するため要検討
#過去のバージョンのインストールに使ったapt-keyと最新のapt-keyが異なるため?

RUN apt-get update && apt-get upgrade -y && apt-get install -y --no-install-recommends \
    git
