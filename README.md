# AIPB Navigator

A searchable guide to Julian Goldie's AI Profit Boardroom Skool community classrooms. Find which module covers the topic you need.

## Deploy to GitHub Pages

```bash
# 1. Create repo and push
cd ~/aipb-navigator
git init
git add .
git commit -m "Initial commit: AIPB Navigator"
gh repo create aipb-navigator --public --source=. --push

# 2. Enable GitHub Pages (serves from main branch root)
gh api repos/{owner}/aipb-navigator/pages -X POST -f source.branch=main -f source.path=/

# 3. Your site will be live at:
# https://{your-username}.github.io/aipb-navigator/
```

## Updating Content

All classroom data lives in the `DATA` array inside `index.html`. To add or update a classroom, edit that array. Each entry has:

- `title` - Classroom name
- `category` - One of: course, classroom, framework, resource, locked
- `description` - What's inside and what topics it covers
- `topics` - Array of searchable keywords

## Features

- Full-text search across titles, descriptions, and topic tags
- Category filters (Courses, Classrooms, Frameworks, Resources, Locked)
- Search result highlighting
- Relevance-ranked results
- Mobile responsive
- Single HTML file, no build step, no dependencies
