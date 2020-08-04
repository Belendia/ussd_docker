FROM nginx:latest
LABEL maintainer="Belendia Serda belendia@gmail.com"

ADD ./nginx/nginx.conf /etc/nginx/nginx.conf

EXPOSE 8999

CMD ["nginx", "-g", "daemon off;"]