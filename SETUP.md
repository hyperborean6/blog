# Git Setup Instructions

If you're getting the error "Source RefSpec Main does not match any", follow these steps:

## Step 1: Make sure you're in the blog directory
```bash
cd C:\Users\cagney\Desktop\taor-blog
```

## Step 2: Initialize git (if not already done)
```bash
git init
```

## Step 3: Add all files
```bash
git add .
```

## Step 4: Make your first commit
```bash
git commit -m "Initial blog setup"
```

## Step 5: Rename branch to main (lowercase!)
```bash
git branch -M main
```

## Step 6: Add your remote repository
Replace `yourusername` and `your-repo-name` with your actual GitHub username and repository name:
```bash
git remote add origin https://github.com/yourusername/your-repo-name.git
```

## Step 7: Push to main (lowercase!)
```bash
git push -u origin main
```

**Important:** Make sure you use lowercase `main` not `Main` or `MAIN`. Git is case-sensitive on Windows for branch names.

If you already added a remote with the wrong case, remove it first:
```bash
git remote remove origin
```
Then add it again with the correct URL.
