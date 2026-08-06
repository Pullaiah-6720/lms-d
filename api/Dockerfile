FROM node:20
WORKDIR app/
COPY . .
RUN apt update -y
RUN npm install
RUN npx prisma generate
RUN npx prisma db push
RUN npm run build
CMD ["node", "build/index.js"]

