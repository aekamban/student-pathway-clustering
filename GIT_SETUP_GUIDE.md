# Git Setup and Push Guide

Follow these steps to upload your student-pathway-clustering project to GitHub.

## Prerequisites

1. Make sure you have Git installed: `git --version`
2. Make sure you're logged into GitHub CLI or have your credentials ready
3. Create a new repository on GitHub named `student-pathway-clustering` (do NOT initialize with README, .gitignore, or license)

## Step-by-Step Commands

### 1. Navigate to your project directory
```bash
cd /path/to/student-pathway-clustering
```

### 2. Initialize Git repository
```bash
git init
```

### 3. Add all files to staging
```bash
git add .
```

### 4. Verify what will be committed
```bash
git status
```

You should see:
- README.md
- requirements.txt
- .gitignore
- LICENSE
- notebooks/
- reports/
- dashboards/
- images/
- data/README.md

### 5. Create your first commit
```bash
git commit -m "Initial commit: Add student pathway clustering project with reproducible notebook, README, and dashboard assets"
```

### 6. Add your GitHub repository as remote
Replace `YOUR_GITHUB_USERNAME` with your actual GitHub username:

```bash
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/student-pathway-clustering.git
```

### 7. Rename branch to main (if needed)
```bash
git branch -M main
```

### 8. Push to GitHub
```bash
git push -u origin main
```

## Verification

After pushing, visit your repository at:
`https://github.com/YOUR_GITHUB_USERNAME/student-pathway-clustering`

You should see:
- ✅ README.md displaying with the dashboard image
- ✅ All folders populated with files
- ✅ Clean, professional structure

## Common Issues and Solutions

### Issue: Permission denied (publickey)
**Solution**: Set up SSH keys or use HTTPS with personal access token

### Issue: Repository already exists
**Solution**: If you already created the repo with files, either:
```bash
git pull origin main --allow-unrelated-histories
git push -u origin main
```

OR start fresh:
```bash
# Delete the repo on GitHub and recreate it empty
# Then follow the steps above
```

### Issue: Large files rejected
**Solution**: The .gitignore should prevent this, but if you added large data files:
```bash
git rm --cached data/*.csv
git commit -m "Remove large data files"
git push
```

## Next Steps After Pushing

1. ✅ Verify README displays correctly on GitHub
2. ✅ Check that dashboard image shows up
3. ✅ Test clone and notebook execution from a fresh environment
4. 🔗 Add repository link to your resume/LinkedIn
5. 📧 Share with potential employers!

## Quick Reference

```bash
# Check status
git status

# Add changes
git add .

# Commit changes
git commit -m "Your message"

# Push changes
git push

# Pull latest changes
git pull
```
