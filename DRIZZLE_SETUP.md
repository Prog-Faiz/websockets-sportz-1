# Drizzle + Neon (node-postgres) setup (JavaScript)

## What I added

- `drizzle.config.js` — Drizzle Kit config (uses `process.env.DATABASE_URL`).
- `src/schema.js` — Database schema (demo `demo_users` table).
- `src/db.js` — Drizzle client using `node-postgres` (`pg`) and exported `pool` and `db`.
- `src/db_demo.js` — Demo script that performs a full CRUD lifecycle.
- `.env` — Template file (fill `DATABASE_URL` here; do not commit real credentials).
- Added scripts to `package.json`: `db:generate`, `db:migrate`, `db:crud`.
- Added `/drizzle` to `.gitignore`.

## Next steps (run locally)

1. Add your Neon connection string to `.env` (set `DATABASE_URL`).
2. Install dependencies (if not already done):

   npm install

   (Or explicitly: `npm install drizzle-orm pg dotenv` and `npm install -D drizzle-kit`)

3. Generate the initial migration (creates files under `./drizzle`):

   npm run db:generate

4. Apply the migration to your Neon database:

   npm run db:migrate

5. Run the CRUD demo:

   npm run db:crud

If anything fails, paste the error here and I'll help troubleshoot.
