# Public Wall Application - Database Setup

## SQL Schema

Run this SQL command in your Neon PostgreSQL database to create the messages table:

```sql
CREATE TABLE messages (
  id SERIAL PRIMARY KEY,
  content TEXT NOT NULL,
  created_at TIMESTAMP DEFAULT NOW()
);
```

## Database Configuration

Your DATABASE_URL is already configured in the `.env` file. Make sure you have run the SQL command above in your Neon database console before starting the application.

## Running the Application

1. Make sure the database table is created (run the SQL above in Neon console)
2. Start the development server:
   ```bash
   npm run dev
   ```
3. Open http://localhost:3000 in your browser

## Features

- ✅ Anonymous posting (no authentication required)
- ✅ Real-time updates every 2 seconds via polling
- ✅ Clean, modern UI with Tailwind CSS
- ✅ Timestamps for each message
- ✅ Auto-scroll to newest messages
- ✅ PostgreSQL database via Neon
