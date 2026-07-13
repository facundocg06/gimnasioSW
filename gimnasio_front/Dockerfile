FROM alpine:3.19

WORKDIR /app

COPY dist/ /usr/share/nginx/html/

CMD ["sh", "-c", "echo 'Frontend listo' && tail -f /dev/null"]