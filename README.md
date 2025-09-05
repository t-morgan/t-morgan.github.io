# Tim Morgan's Quarto Blog

This is my learning-in-public blog, built with [Quarto](https://quarto.org).  
I’m sharing notes from the [fast.ai](https://course.fast.ai) course, side projects, and random ML experiments.

## Quick Start

### 1. Install Quarto
Follow the instructions here: <https://quarto.org/docs/get-started/>

### 2. Clone the repo
```bash
git clone https://github.com/t-morgan/t-morgan.github.io.git
cd t-morgan.github.io
```

### 3. (Optional) Set up a virtual environment
```bash
python3 -m venv .venv
source .venv/bin/activate   # Linux/Mac
# .venv\Scripts\activate    # Windows PowerShell
```

### 4. Preview locally
```bash
quarto preview
```
This site will be available locally with live reload.

## Deployment (GitHub Pages)
This repo is configured for deployment via GitHub Pages.

1. In repo settings on GitHub, go to Pages and set:
    * Source: GitHub Actions

2. Quarto will auto-generate the GitHub Actions workflow on the first deploy:
```bash
quarto publish gh-pages
```

3. After the action completes, the blog will be live at:
https://t-morgan.github.io/<repo-name>/

## Project Structure
```bash
.
├── _quarto.yml      # site config (title, tagline, navbar, theme)
├── index.qmd        # home page with auto-generated post listing
├── about.qmd        # About page
├── posts/           # blog posts (one .qmd per post)
├── styles.css       # optional custom styles
├── .gitignore
└── README.md
```

## Creating a New Post
```bash
quarto create post "My New Post" --dir posts
```
Or create a new `.qmd` under `posts/` with front matter (title, date).