# Action Tracker

A simple meeting action tracker for teams that keep forgetting agreed actions.

## Features

- Add an action with an owner and a due date
- Actions grouped by owner, with a tick box for done
- Open, done and overdue counts; overdue actions are highlighted in red
- Data is saved in the browser's local storage (per browser and device)

## Run locally

Open `index.html` in any browser. No build step or dependencies are needed.

## Deploy to Vercel

1. Sign in to [Vercel](https://vercel.com) and choose **Add New… → Project**.
2. Import the `alexto889/action-tracker` GitHub repository.
3. Leave the framework preset as **Other**; no build command or output directory is needed.
4. Click **Deploy**.

Every push to `main` will redeploy automatically.

## Note

Because data lives in local storage, each person sees only the actions entered in their own browser. A shared team view would need a backend (for example Supabase).
