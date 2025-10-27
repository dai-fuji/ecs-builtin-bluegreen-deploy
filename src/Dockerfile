FROM public.ecr.aws/nginx/nginx:latest

# ★★★ コピー先を nginx.conf 本体に変更 ★★★
COPY src/nginx.conf /etc/nginx/nginx.conf

COPY src/ /usr/share/nginx/html/

# ★★★ Nginxのlistenポートと合わせる ★★★
EXPOSE 8080

CMD ["nginx", "-g", "daemon off;"]