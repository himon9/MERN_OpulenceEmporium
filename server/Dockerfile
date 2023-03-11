FROM node:18 AS Production

ENV NODE_ENV=Production HOST=0.0.0.0 PORT=1337 APP_KEYS=hg39Ea4S7Q3x1P5d4oskIA==,+Tl4s6PWUJYB8ymHM916CQ==,IEOk0Rzx4ArqXFevJ8o6pg==,gvsx5Wl0PPateqpnbgJ17w== API_TOKEN_SALT=R8iE36xizLw+XmGQdB21Kg== ADMIN_JWT_SECRET=0e3gCxbH2HBRf1hVUb0nIg== TRANSFER_TOKEN_SALT=E8Hc7BxB36hUHAYCOghs2w== DATABASE_CLIENT=sqlite DATABASE_FILENAME=.tmp/data.db JWT_SECRET=lMRBWt7vhKst0JHJGNd6zA== STRIPE_SECRET_KEY=sk_test_51MkLShSB0J90V9Sb0AkcvfiQbbStUQYvYtMhJtF5rPlO4hG9rZI5GBemfQjXEWYpmTRlr0Z1ceQ2tiAgtSjXepzv00LjUOlGIg 

    

WORKDIR /usr/src/server

COPY package.json .
COPY package-lock.json .

RUN npm install 

COPY . .

RUN npm run build

CMD ["sh", "-c", "npm start"]

