# 🏦 Nova Bank — Setup & Deployment Guide

## What's in this project
- `app.py` — the Flask web server
- `templates/` — HTML pages (login, register, dashboard)
- `requirements.txt` — Python packages needed
- `Procfile` — tells Render how to start the app

---

## Step 1 — Run it on your computer first

Open a terminal (Command Prompt on Windows, Terminal on Mac) in this folder and run:

```bash
pip install -r requirements.txt
python app.py
```

Then open your browser and go to: **http://localhost:5000**

---

## Step 2 — Put it on GitHub

1. Go to **github.com** and sign in (or create a free account)
2. Click the **+** button → **New repository**
3. Name it `nova-bank`, make it **Public**, click **Create repository**
4. On the next page, click **uploading an existing file**
5. Drag and drop ALL the files from this folder
6. Click **Commit changes**

---

## Step 3 — Deploy free on Render.com

1. Go to **render.com** and sign up with your GitHub account
2. Click **New +** → **Web Service**
3. Click **Connect** next to your `nova-bank` repo
4. Fill in the settings:
   - **Name**: nova-bank
   - **Runtime**: Python 3
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `gunicorn app:app`
   - **Instance Type**: Free
5. Click **Create Web Service**
6. Wait ~2 minutes for it to build
7. Your site will be live at: `https://nova-bank-xxxx.onrender.com` 🎉

---

## Notes
- The free Render tier sleeps after 15 minutes of inactivity (first load takes ~30 seconds to wake up)
- To add a custom domain later, upgrade to Render's paid plan
- This is a DEMO project — do not use for real financial data
