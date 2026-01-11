# Blog Repository

This is a Jekyll-based blog repository configured for GitHub Pages.

## Setup Instructions

### 1. Create the GitHub Repository

1. Go to [GitHub](https://github.com) and create a new repository
2. Name it `yourusername.github.io` (replace `yourusername` with your GitHub username) for a user/organization site, OR name it anything you want for a project site
3. **Do NOT** initialize it with a README, .gitignore, or license (we already have these)

### 2. Initialize Git and Push

```bash
cd taor-blog
git init
git add .
git commit -m "Initial blog setup"
git branch -M main
git remote add origin https://github.com/yourusername/your-repo-name.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **Settings**
3. Scroll down to **Pages** section
4. Under **Source**, select **Deploy from a branch**
5. Select **main** branch and **/ (root)** folder
6. Click **Save**

GitHub Pages will automatically build and deploy your site. It may take a few minutes for the first deployment.

### 4. Access Your Blog

- If you named it `yourusername.github.io`: `https://yourusername.github.io`
- If you named it something else: `https://yourusername.github.io/repo-name`

## Local Development

To run the blog locally:

```bash
# Install dependencies (requires Ruby)
bundle install

# Run the Jekyll server
bundle exec jekyll serve
```

Then visit `http://localhost:4000` in your browser.

## Adding New Posts

1. Create a new file in the `_posts` directory
2. Name it: `YYYY-MM-DD-title.md` (e.g., `2025-01-12-my-new-post.md`)
3. Add front matter at the top:

```yaml
---
layout: post
title: "Your Post Title"
date: 2025-01-12
categories: category1 category2
---
```

4. Write your content below the front matter
5. Commit and push to GitHub

## Customization

- Edit `_config.yml` to customize site settings, title, description, etc.
- Edit `about.md` to add information about yourself
- The blog uses the `minima` theme by default. You can customize it or switch themes in `_config.yml`

## Notes

- All your existing blog posts have been converted to Jekyll format and placed in `_posts/`
- You may want to update the dates in the post filenames and front matter to reflect when they were actually written
- Update the author information in `_config.yml` with your details
