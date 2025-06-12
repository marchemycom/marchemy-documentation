# 📚 Project Documentation

This repository contains the source code for the project documentation built with [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

## 🚀 Getting Started

We use [`uv`](https://github.com/astral-sh/uv) for dependency management.

### 1. Install dependencies

```bash
uv sync --frozen
```
This installs all required packages based on the pyproject.toml and uv.lock files.

### 2. Start the development server
`mkdocs serve`

Open http://localhost:8000 in your browser to see the documentation live with hot-reload.

### 📁 Project Structure
```.
├── docs/                   # Markdown source files  
│   ├── index.md            # Main landing page (homepage)  
│   ├── assets              # images, favicons, etc.
│   └── styleeshets         # styles overrides
├── mkdocs.yml              # MkDocs configuration file  
├── pyproject.toml          # Project metadata and dependencies  
├── uv.lock                 # Frozen dependency versions (used by uv)  
└── README.md               # This file  
```

### ✅ Deployment
All changes merged to the main branch are automatically deployed to production (e.g. via GitHub Pages or CI pipeline).

# ➕ How to Add a New Page to the Documentation

To add a new page to the documentation site, follow these steps:

### 1. Create a new Markdown file
Create a .md file in the docs/ directory, for example:

```
touch docs/my-new-page.md
```
## and add your content using Markdown syntax

### 2. Add the page to the navigation
Open mkdocs.yml and add your new file to the nav section. For example:

```yaml
nav:
  - Home: index.md
  - Getting Started: getting-started.md
  - My New Page: my-new-page.md  # <-- Add this line
```
You can also nest pages in sections:

```yaml
nav:
  - Home: index.md
  - Guides:
      - Getting Started: getting-started.md
      - My New Page: my-new-page.md
```
