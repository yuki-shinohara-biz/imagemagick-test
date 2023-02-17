FROM ubuntu:latest

# 日本語入力可能にするためにロケールを設定
RUN apt-get update \
    && apt-get install -y locales \
    && locale-gen ja_JP.UTF-8 \
    && echo "export LANG=ja_JP.UTF-8" >> ~/.bashrc

# IPAフォントのインストール
RUN apt-get update &&\
    apt-get install -y wget &&\
    apt-get install -y zip unzip &&\
    apt-get install -y fontconfig

# IPAフォントのインストール
RUN wget https://moji.or.jp/wp-content/ipafont/IPAexfont/IPAexfont00301.zip &&\
  unzip IPAexfont00301.zip && rm IPAexfont00301.zip &&\
  mkdir -p /usr/share/fonts/ipa &&\
  cp IPAexfont00301/*.ttf /usr/share/fonts/ipa &&\
  rm -rf IPAexfont00301/ &&\
  fc-cache -fv

# ImageMagickのインストール
RUN apt update -y \
  && apt-get -y install imagemagick