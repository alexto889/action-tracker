# Action Tracker

A simple meeting action tracker for teams that keep forgetting agreed actions.

## Features

- Add an action with an owner and a due date
- Actions grouped by owner, with a tick box for done
- Open, done and overdue counts; overdue actions are highlighted in red
- Data is stored in a shared Supabase database, so the whole team sees the same actions

## Run locally

Open `index.html` in any browser. No build step or dependencies are needed.

## Deploy to Vercel

1. Sign in to [Vercel](https://vercel.com) and choose **Add New… → Project**.
2. Import the `alexto889/action-tracker` GitHub repository.
3. Leave the framework preset as **Other**; no build command or output directory is needed.
4. Click **Deploy**.

Every push to `main` will redeploy automatically.

## Note

The app talks to Supabase using the project's publishable key, which is safe to expose in the browser. There is no sign-in, so anyone with the site link can view and edit actions (row-level security policies allow the `anon` role). Add Supabase Auth if you need to restrict access.
