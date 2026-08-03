# Class Project (HTML + CSS only, no JS needed)

A class website where each of the 20 students owns **one page** and edits
nothing else. Built to practice: fork → branch → commit → push → pull
request → review → merge.

## Files

```
index.html              → home page + directory grid (owner edits this)
css/style.css            → shared styling for the whole site (owner edits this)
students/2303108.html    → that student's page
students/2303109.html    → that student's page
students/110.html        → that student's page
...
students/133.html        → that student's page
```

Each file is named after that student's PRN.

## Why one file per student

With 20 people, editing a single shared page at the same time causes merge
conflicts. Giving everyone their own file means two students almost never
touch the same lines, so pull requests merge cleanly.

## Setup (repo owner, once)

```
git init
git remote add origin <repo_url>
git push -u origin main
```

Add all 20 classmates as collaborators: GitHub → Settings → Collaborators.

## What each student does

```
git clone https://github.com/<owner-username>/<repository_name>.git
cd <repository_name>
git checkout -b feature/2303108        (use your own PRN)
```

Open **only your own file**, e.g. `students/2303108.html`, and edit:
- Your name and role
- The "About Me" paragraph
- The "What I'm Working On" paragraph
- Your links (GitHub, LinkedIn, portfolio)

You can also change your card's avatar initials and the text under your
name on the directory grid in `index.html` — but touch only your own
`<a class="directory-card">` block, not anyone else's.

```
git add .
git commit -m "Added 2303108 profile"
git push origin feature/2303108
```

Then on GitHub: **Compare & pull request** → describe what you changed →
submit. Once a teammate reviews and approves it, the owner merges it into
`main`.

## Tip to avoid conflicts

Before creating your branch, pull the latest `main` first:

```
git checkout main
git pull origin main
git checkout -b feature/2303108
```

This way you're always branching from the newest version of the site.

## No JavaScript required

- The mobile menu uses a pure-CSS checkbox trick.
- Dark mode follows the visitor's system setting automatically via
  `prefers-color-scheme` in CSS — nothing to wire up.

Everything a student needs to touch is plain HTML and CSS.
