FROM tensorflow/tensorflow:latest-gpu
#過去バージョンを使う場合(FROM tensorflow/tensorflow:2.8.0-gpu など)
#apt-getコマンドを使用するとでGPG errorが発生するため要検討
#過去のバージョンのインストールに使ったapt-keyと最新のapt-keyが異なるため?

RUN apt-get update && apt-get upgrade -y && apt-get install -y --no-install-recommends \
    git 

# scikit-learnの利用時に必要
RUN apt-get update && apt-get upgrade -y && apt-get install -y --no-install-recommends \
    libglib2.0-0 libsm6 libxrender1 libxext6 libgl1-mesa-dev

COPY ./requirements.txt ./
RUN pip3 install --no-cache-dir install --upgrade pip
RUN pip3 --disable-pip-version-check --no-cache-dir install --user -r ./requirements.txt
RUN rm ./requirements.txt