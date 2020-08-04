FROM nginx:latest
LABEL maintainer="Belendia Serda belendia@gmail.com"

ADD ./nginx/nginx.conf /etc/nginx/nginx.conf
COPY ./ussd-fe/build /usr/share/nginx/html
COPY ./ussd-be/staticfiles /usr/share/nginx/html/static/staticfiles

EXPOSE 8999

CMD ["nginx", "-g", "daemon off;"]