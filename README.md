# Action Tracker

A simple meeting action tracker for teams that keep forgetting agreed actions.

## Features

- Add an action with an owner and a due date
- Actions grouped by owner, with a tick box for done
- Open, done and overdue counts; overdue actions are highlighted in red
- Data is stored in a shared Supabase database, so the whole team sees the same actions
- Sign in and sign out with a username and password (Supabase Auth; passwords are stored hashed in `auth.users`)
- Admins can add and remove users and set their initial password; everyone can change their own password

## Run locally

Open `index.html` in any browser. No build step or dependencies are needed.

## Deploy to Vercel

1. Sign in to [Vercel](https://vercel.com) and choose **Add New… → Project**.
2. Import the `alexto889/action-tracker` GitHub repository.
3. Leave the framework preset as **Other**; no build command or output directory is needed.
4. Click **Deploy**.

Every push to `main` will redeploy automatically.

## Users and security

- Sign-in uses Supabase Auth. A username such as `alex` maps to the email `alex@actiontracker.example` (a reserved example domain; no email is ever sent).
- The `profiles` table links to `auth.users` and holds each person's username, display name and role (`admin` or `member`).
- Only admins can add or remove users, through the `create_app_user` and `delete_app_user` database functions.
- Row-level security means only signed-in users can read or change actions.
- The starter accounts `alex` (admin), `dan` and `marcus` were created with the initial password `password`. **Everyone should change it on first sign-in.**
- The publishable key in `index.html` is safe to expose in the browser; never put a secret or service-role key in this repository.
