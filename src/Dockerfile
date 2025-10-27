# ベースイメージ
FROM public.ecr.aws/docker/library/nginx:latest

# curlをインストール (ヘルスチェック用)
USER root
RUN apt-get update && apt-get install -y curl && \
    # クリーンアップ
    apt-get clean && rm -rf /var/lib/apt/lists/*

# カスタムNginx設定ファイル (8080ポート用) をコピー
COPY default.conf /etc/nginx/conf.d/default.conf

# サンプルページの追加
COPY index.html /usr/share/nginx/html/index.html

# 8080ポートを公開
EXPOSE 8080

# Nginxユーザーに戻す
USER nginx