# CrewLoop
Lightweight field service CRM (quotes → jobs → invoices) with web and mobile apps. Built with Next.js, Express, Prisma, and PostgreSQL.  Optional “About” fields  Website: (add later after deploy) Topics: crm, field-service, scheduling, invoices, nextjs, react, express, nodejs, prisma, postgresql, react-native, expo
CrewLoop
Lightweight field service CRM for small teams. Quotes → Jobs → Invoices, simple scheduling, and mobile-ready.

Features

Customers & properties
Quotes → Jobs → Invoices
Scheduling and job status
Basic JWT auth
Web (Next.js) + Mobile (Expo)
Tech stack

Web: Next.js, React, Tailwind
API: Node.js, Express, Prisma
DB: PostgreSQL
Mobile: React Native (Expo)
Quick start (local)

API
cd server
cp .env.example .env
docker compose up -d
npm i
npx prisma migrate dev --name init
npm run dev
Health: http://localhost:4000/health
Seed
POST /auth/register { "accountName":"Demo Co","email":"owner@example.com","password":"password" }
Web
cd ../web
echo "NEXT_PUBLIC_API=http://localhost:4000" > .env.local
npm i
npm run dev
Open http://localhost:3000 → Open App
Mobile (optional)
cd ../mobile
npm i
npx expo start
Set API base in mobile/App.js (10.0.2.2 for Android emulator)
Environment variables

server/.env
DATABASE_URL=postgresql://postgres:postgres@localhost:5432/crewloop?schema=public
JWT_SECRET=your_random_string
web/.env.local
NEXT_PUBLIC_API=http://localhost:4000
Deploy (summary)

API: Render/Fly/Heroku (set DATABASE_URL, JWT_SECRET)
Web: Vercel (set NEXT_PUBLIC_API to API URL)
Mobile: point base URL to API domain
Roadmap

Stripe payment links, Twilio SMS
Recurring jobs, route optimization
RBAC, reporting
License

MIT (or your choice)
Regenerate
Copy
Good response
Bad response
