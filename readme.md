NodeJS API TypeScript Express
-> npm i -D @types/node @types/express prisma typescript tsc-watch ts-node
-> npm i express dotenv pg @prisma/client
create and configure tsconfig.json
-> npx tsc --init
Prisma PostgreSQL Docker
-> docker run --name a-postgres-db -p 5432:5432 -e POSTGRES_PASSWORD=password -d postgres
-> npx prisma init
create models in .prisma file then run
-> npx prisma db push
(optional) open prisma in browser to view your database
-> npx prisma studio
(seeding) after "prisma db push" , a prisma client library generates in your node_modules folder and you can create a seed.ts file in your root/prisma folder next to the schema.prisma where you can instantiate your client and create and execute a function that will insert a user into the database then run
-> npm run seed
build api routes flow in index.ts then run
-> npx prisma migrate dev --name init
rerun npx prisma studio to open up the browser database view and you might need to re-seed again by running npm run seed
(unused) -> npx prisma migrate deploy (I think this migrates changes every time after the first migrate init)
-> npm run build
-> npm run dev
