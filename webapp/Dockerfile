FROM node:20
WORKDIR app/
COPY . .
ARG VITE_API_URL
ENV VITE_API_URL=$VITE_API_URL
RUN apt update -y && apt install nginx -y && npm install && npm run build && rm -r /var/www/html/* && cp -r dist/* /var/www/html/
#RUN apt install nginx -y
#RUN npm install
#RUN npm run build
#RUN rm -r /var/www/html/*
#RUN cp -r dist/* /var/www/html/
CMD ["nginx", "-g", "daemon off;"]
