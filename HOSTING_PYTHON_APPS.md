# Hosting Python Web Applications

This guide covers options for hosting Python web applications and linking them from your GitHub Pages blog.

## Quick Decision Guide

**What framework are you using?**
- **Streamlit** → Use Streamlit Cloud (easiest!)
- **Gradio** → Use Hugging Face Spaces (easiest!)
- **Flask/FastAPI/Django** → Use Render or Railway
- **Static HTML/JS** → Can use GitHub Pages

## Option 1: Streamlit Cloud (Best for Streamlit Apps)

### Setup:
1. Push your Python app to a GitHub repository
2. Go to [share.streamlit.io](https://share.streamlit.io)
3. Sign in with GitHub
4. Click "New app"
5. Select your repository and main file
6. Click "Deploy"

### Pros:
- ✅ Completely free
- ✅ Automatic deployments on git push
- ✅ No configuration needed
- ✅ Custom subdomain: `yourapp.streamlit.app`

### Example:
If your app file is `app.py`, Streamlit Cloud will automatically detect it.

## Option 2: Hugging Face Spaces (Best for Gradio Apps)

### Setup:
1. Create account at [huggingface.co](https://huggingface.co)
2. Go to Spaces → Create new Space
3. Choose "Gradio" SDK
4. Upload your code or connect GitHub repo
5. Auto-deploys!

### Pros:
- ✅ Free
- ✅ Great for ML/AI apps
- ✅ Automatic deployments
- ✅ URL: `yourusername-spacename.hf.space`

## Option 3: Render (Best for Flask/FastAPI/Django)

### Setup:
1. Push code to GitHub
2. Go to [render.com](https://render.com)
3. Sign in with GitHub
4. Click "New +" → "Web Service"
5. Connect your repository
6. Set build command: `pip install -r requirements.txt`
7. Set start command: `python app.py` (or `gunicorn app:app` for production)
8. Click "Create Web Service"

### Pros:
- ✅ Free tier available
- ✅ Automatic SSL
- ✅ Custom domain support
- ✅ Auto-deploys on git push

### Requirements:
Create a `requirements.txt` file:
```
streamlit==1.28.0
# or
flask==2.3.0
# or whatever packages you need
```

## Option 4: Railway

### Setup:
1. Go to [railway.app](https://railway.app)
2. Sign in with GitHub
3. Click "New Project" → "Deploy from GitHub repo"
4. Select your repository
5. Railway auto-detects Python and deploys

### Pros:
- ✅ Free tier ($5 credit/month)
- ✅ Very simple setup
- ✅ Auto-deploys

## Linking from Your Blog

Once your app is hosted, add a link to it from your blog:

### Option A: Add to Navigation
Edit `_config.yml` and add:
```yaml
navigation:
  - title: "My App"
    url: "https://yourapp.streamlit.app"
```

### Option B: Create a Page
Create `apps.md`:
```markdown
---
layout: page
title: My Applications
permalink: /apps/
---

Check out my interactive applications:

- [My Python App](https://yourapp.streamlit.app)
```

### Option C: Add to About Page
Edit `about.md` and add links to your hosted apps.

## Example Project Structure

For a Streamlit app:
```
my-python-app/
├── app.py
├── requirements.txt
├── README.md
└── data/  (if needed)
```

`requirements.txt`:
```
streamlit==1.28.0
pandas==2.0.0
# other dependencies
```

`app.py`:
```python
import streamlit as st

st.title("My App")
st.write("Hello, world!")
```

## Which Should You Choose?

- **Streamlit app?** → Streamlit Cloud (no brainer!)
- **Gradio app?** → Hugging Face Spaces
- **Custom Flask/FastAPI?** → Render or Railway
- **Want more control?** → Railway or Render
- **Need database?** → Render (includes PostgreSQL)

## Important Notes

1. **GitHub Pages cannot run Python** - it's static only
2. **Always use `requirements.txt`** - lists all dependencies
3. **Environment variables** - Use platform's env var settings for secrets
4. **File size limits** - Check each platform's limits
5. **Free tiers** - Usually have usage limits, check before deploying

## Quick Start Checklist

- [ ] Push Python app to GitHub
- [ ] Create `requirements.txt` with all dependencies
- [ ] Choose hosting platform (Streamlit Cloud if Streamlit)
- [ ] Deploy app
- [ ] Test the deployed URL
- [ ] Add link to your blog
