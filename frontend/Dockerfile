FROM node:18-alpine

WORKDIR /app

COPY package.json package-lock.json ./
RUN npm ci

COPY . .

RUN npm run build

CMD ["sh", "-c", "mkdir -p /frontend_static/frontend && cp -r /app/build/* /frontend_static/frontend/"]
