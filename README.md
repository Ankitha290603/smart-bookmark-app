# Smart Bookmark App

Smart Bookmark is a full-stack web application that allows users to save and manage bookmarks securely. Users sign in with Google, and each user can only view and manage their own bookmarks.

## Features
- Google OAuth authentication
- Add and delete bookmarks (title + URL)
- User-specific private data (Row Level Security)
- Real-time updates
- Responsive UI

## Tech Stack
- Next.js (TypeScript, App Router)
- Supabase (PostgreSQL, Auth, Realtime)
- Tailwind CSS
- Deployed on Vercel

## Live Demo
https://your-vercel-url.vercel.app

## How to Run Locally

### 1. Clone the repository
```bash
git clone https://github.com/Ankitha290603/smart-bookmark-app.git
cd smart-bookmark-app

2. Install dependencies
npm install
npm run dev

3. Environment Setup

Create a .env.local file in the project root:

NEXT_PUBLIC_SUPABASE_URL=your_supabase_project_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key

4. Open the app

Visit: http://localhost:3000

Supabase Setup (Steps)

Create a Supabase project

Create a bookmarks table with columns:
id, created_at, user_id, title, url

Enable Row Level Security (RLS)

Add policies:

Select: auth.uid() = user_id

Insert: auth.uid() = user_id

Delete: auth.uid() = user_id

Enable Google OAuth provider

Add redirect URLs for local and production

Author

Ankitha
