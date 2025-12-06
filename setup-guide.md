# 📋 Step-by-Step GitHub Setup Guide

Complete guide to upload your toolkit in Github

# 🎯 Prerequisites

- [ ] GitHub account (create at https://github.com/signup)
- [ ] Git installed on your computer
- [ ] Python 3.6+ installed
- [ ] Basic command-line knowledge

---

# 📝 Method 1: GitHub Web Interface (Easiest for Beginners)

# Step 1: Create GitHub Account
1. Go to https://github.com
2. Click "Sign up"
3. Follow the registration process
4. Verify your email

# Step 2: Create New Repository
1. Click the *"+"* icon (top right) → *"New repository"*
2. Fill in details:
   - *Repository name*: `dorker`
   - *Description*: `A comprehensive CLI tool for security research: Google dorking, email enumeration, directory busting, and vulnerability scanning`
   - *Visibility*: Choose "Public" (so everyone can use it)
   - ✅ Check "Add a README file"
   - *License*: Choose "MIT License"
3. Click *"Create repository"*

# Step 3: Upload Files via Web Interface
1. Click *"Add file"* → *"Upload files"*
2. Create these files on your computer first:
   - Save artifact 1 as `security_toolkit.py`
   - Save artifact 2 as `README.md`
   - Save artifact 3 as `requirements.txt`
   - Save artifact 4 as `.gitignore`
   - Save artifact 5 as `CONTRIBUTING.md`
   - Save artifact 6 as `SETUP_GUIDE.md` (this file)
   - Copy the LICENSE file content

3. Drag and drop all files to GitHub
4. Scroll down, add commit message: `Initial commit: Security Toolkit CLI v1.0`
5. Click *"Commit changes"*

# Step 4: Edit README
1. Click on `README.md`
2. Click the pencil icon (Edit)
3. Replace `yourusername` with your actual GitHub username
4. Replace `your.email@example.com` with your email
5. Commit changes

# Step 5: Add Topics/Tags
1. Click *"⚙️ Settings"* (on the right sidebar)
2. In "Topics" section, add:
   - `security`
   - `penetration-testing`
   - `bug-bounty`
   - `google-dorks`
   - `osint`
   - `reconnaissance`
   - `vulnerability-scanner`
   - `ethical-hacking`
3. Save changes

*✅ Done! Your repository is live!*

---

# 💻 Method 2: Git Command Line (Recommended)

# Step 1: Install Git

*Windows:*
```powershell
# Download and install from: https://git-scm.com/download/win
# Or use chocolatey:
choco install git
```

*Mac:*
```bash
# Using Homebrew:
brew install git

# Or download from: https://git-scm.com/download/mac
```

*Linux:*
```bash
# Debian/Ubuntu
sudo apt-get update
sudo apt-get install git

# Fedora
sudo dnf install git

# Arch
sudo pacman -S git
```

# Step 2: Configure Git (First Time Only)
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Verify configuration
git config --list
```

# Step 3: Create Project Directory
```bash
# Create project folder
mkdir security-toolkit-cli
cd security-toolkit-cli

# Create all necessary files
touch security_toolkit.py
touch README.md
touch requirements.txt
touch .gitignore
touch CONTRIBUTING.md
touch LICENSE
```

# Step 4: Add File Contents

Copy and paste the content from each artifact into the corresponding file:

1. *security_toolkit.py* - Copy from Artifact 1
2. *README.md* - Copy from Artifact 2
3. *requirements.txt* - Copy from Artifact 3
4. *gitignore* - Copy from Artifact 4
5. *CONTRIBUTING.md* - Copy from Artifact 5

*LICENSE* (MIT License):
```
MIT License

Copyright (c) 2024 [Your Name]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

# Step 5: Create Repository on GitHub
1. Go to https://github.com/new
2. Repository name: `dorker`
3. Keep it *Public*
4. *DON'T* initialize with README (we already have one)
5. Click "Create repository"

# Step 6: Initialize Git and Push

```bash
# Initialize git repository
git init

# Add all files
git add .

# Check what will be committed
git status

# Commit files
git commit -m "Initial commit: Security Toolkit CLI v1.0"

# Add remote repository (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/thelkotolsantosh/dorker.git

# Rename branch to main (if needed)
git branch -M main

# Push to GitHub
git push -u origin main
```

*If prompted for credentials:*
- Use your GitHub username
- Use a Personal Access Token (not password)
  - Generate token: GitHub → Settings → Developer settings → Personal access tokens → Generate new token
  - Select scopes: `repo` (all)
  - Copy the token and use it as password

# Step 7: Verify Upload
1. Go to https://github.com/YOUR_USERNAME/security-toolkit-cli
2. Refresh the page
3. Verify all files are present

---

# 🔑 Setting Up Personal Access Token (Required for CLI)

Since GitHub no longer accepts passwords for Git operations:

1. Go to GitHub → Click your profile picture → *Settings*
2. Scroll down → Click *Developer settings*
3. Click *Personal access tokens* → *Tokens (classic)*
4. Click *Generate new token (classic)*
5. Give it a name: "Git CLI Access"
6. Select scopes:
   - ✅ *repo* (all)
7. Click *Generate token*
8. *COPY THE TOKEN* (you won't see it again!)
9. Use this token as your password when pushing to GitHub

---

# 🎨 Optional: Making Your Repo Stand Out

# Add Banner/Logo
1. Create a banner image (1280x640px recommended)
2. Upload to repository: Create `assets` folder
3. Add to README: `![Banner](assets/banner.png)`

# Add Badges
Add to top of README:
```markdown
[![Python](https://img.shields.io/badge/python-3.6+-blue.svg)](https://python.org)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/yourusername/security-toolkit-cli.svg)](https://github.com/yourusername/security-toolkit-cli/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/yourusername/security-toolkit-cli.svg)](https://github.com/yourusername/security-toolkit-cli/issues)
```

# Add Screenshots
1. Run the tool and take screenshots
2. Create `screenshots` folder
3. Upload images
4. Add to README:
```markdown
# 📸 Screenshots

![Main Menu](screenshots/main-menu.png)
![Dorking Results](screenshots/dorking.png)
```

# Enable GitHub Discussions
1. Go to repository → *Settings*
2. Scroll to *Features*
3. ✅ Enable *Discussions*

# Add Topics
1. Repository page → Click *⚙️* next to "About"
2. Add topics: `security`, `pentesting`, `bug-bounty`, etc.

---

# 🔄 Updating Your Repository

After making local changes:

```bash
# Check what changed
git status

# Add changes
git add .

# Commit with message
git commit -m "Add new feature: subdomain takeover detection"

# Push to GitHub
git push
```

---

# 🐛 Troubleshooting

# "Permission denied (publickey)"
```bash
# Generate SSH key
ssh-keygen -t ed25519 -C "your.email@example.com"

# Add to GitHub: Settings → SSH and GPG keys → New SSH key
# Copy public key:
cat ~/.ssh/id_ed25519.pub
```

# "Repository not found"
- Check repository URL is correct
- Verify you're logged in with correct account

# "Failed to push"
- Pull latest changes first: `git pull origin main`
- Resolve conflicts if any
- Push again: `git push`

---

# ✅ Final Checklist

Before sharing your repository:

- [ ] All files uploaded successfully
- [ ] README has your username/email (not placeholders)
- [ ] LICENSE has your name
- [ ] Requirements.txt is present
- [ ] .gitignore is configured
- [ ] Repository is Public
- [ ] Topics/tags added
- [ ] Script runs without errors
- [ ] All links in README work

---

# 🌟 Promoting Your Repository

# Share on Social Media
```
🚀 Just released Security Toolkit CLI - A comprehensive tool for:
✅ Google Dorking
✅ Email Enumeration  
✅ Directory Busting
✅ Vulnerability Scanning

Check it out: https://github.com/YOUR_USERNAME/security-toolkit-cli

#bugbounty #infosec #cybersecurity #pentesting
```

# Submit to Lists
- Awesome Security: https://github.com/sbilly/awesome-security
- Awesome Penetration Testing: https://github.com/enaqx/awesome-pentest
- Hacker News: https://news.ycombinator.com

# Blog About It
Write a blog post explaining:
- Why you built it
- How to use it
- Real-world examples
- Future plans

---

# 📞 Need Help?

- GitHub Docs: https://docs.github.com
- Git Tutorial: https://git-scm.com/doc
- Open an issue in the repository

---

*Congratulations!* 🎉 Your dorker is now on GitHub and ready to be used by the community!
