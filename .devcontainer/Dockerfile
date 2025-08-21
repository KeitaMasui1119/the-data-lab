FROM python:3.13-slim

# 必要なパッケージと日本語フォントをインストール
RUN apt-get update && apt-get install -y \
    git curl build-essential libglib2.0-0 libxext6 libsm6 libxrender1 \
    fonts-ipafont-gothic \
    && rm -rf /var/lib/apt/lists/*

# 作業ディレクトリを作成
WORKDIR /workspace

# Python依存ライブラリをインストール
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
