FROM node:20
WORKDIR app/
COPY . .
RUN apt update -y && npm install && npx prisma generate && npm run build
#RUN npm install
#RUN npx prisma generate
#RUN npx prisma db push
#RUN npm run build
CMD [" sh","node build/index.js"]

