FROM node:20
WORKDIR app/
COPY . .
RUN apt update -y
RUN apt install nginx -y
RUN npm install
RUN npm run build
RUN rm -r /var/www/html/*
RUN cp -r dist/* /var/www/html/
CMD ["nginx", "-g", "daemon off;"]
