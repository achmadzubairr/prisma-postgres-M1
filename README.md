This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, install dependencies:

```bash
npm install
```

Run, Docker Container with PostgreSQL Database, PgAdmin and Next.js Development Server:

```bash
docker-compose up
```

Run, prisma migration:

```bash
npx prisma migrate dev
```

Run, prisma client generation

```bash
npx prisma generate
```

Run, prisma database seed with dummy user data (from `/prisma/seed.ts`):

```bash
npx prisma db seed --preview-feature
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.
Open [http://localhost:3000/users](http://localhost:3000/users) with your browser to see data from the database or the error for this case.
Open [http://localhost:3000/api/graphql](http://localhost:3000/api/graphql) with your browser to see GraphiQL Playground and the example query

Open [http://localhost:5050](http://localhost:5050) for PgAdmin and login with test data from `docker-compose.yml`
Email: `test@test.com`
Password: `test`

You can inspect the postgreSQL Database from pgAdmin by connecting it.
Steps to inspect on PgAdmin:

1. Login on [http://localhost:5050](http://localhost:5050) with test data above
2. Right click on `Server` inside the PgAdmin Dashboard
3. Under `General` tab type a name
4. Under `Connection` tab type followings:
   - Host name / address: `test-postgres`
   - Port: `5432`
   - Maintenance database: `postgres`
   - Username: `postgres`
   - Password: `postgres`

make sure postgres and next have a same networks
add on next service
```bash
      networks:
         app-tier
```

if you see this error : Error: Command failed with exit code 1: ts-node --eval "
// @ts-ignore

just install this in next container
```bash
npm install ts-node --save-dev
```
```bash
install npm install @prisma/client prisma@latest
```
```bash
npm install typescript@latest
```

update node.js # tdk bisa
```bash
curl -fsSL https://deb.nodesource.com/setup_18.x | bash -
apt-get update
apt-get install -y nodejs
node -v
```
```bash
docker restart test-next
node -v
```
