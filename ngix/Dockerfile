FROM nginx:latest

COPY nginx.conf D:\DevOps_CloudComputing\ngix\nginx.conf

RUN command --name some-nginx -v /some/content:/usr/share/nginx/html:ro -d amd64/nginx


FROM amd64/nginx
COPY static-html-directory D:\DevOps_CloudComputing\ngix\html


RUN command --name some-nginx -d some-content-nginx


RUN command --name some-nginx -d -p 8080:80 some-content-nginx

RUN command --rm --entrypoint=cat amd64/nginx /etc/nginx/nginx.conf > /host/path/nginx.conf