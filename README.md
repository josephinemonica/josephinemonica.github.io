# Josephine Monica — personal site

Minimalist personal website for hosting on GitHub Pages (`*.github.io`).

## Files
- `index.html` — homepage with 3 layout variations (Centered / Sidebar / Academic). Use the Tweaks toggle to switch between them, plus theme (Paper / Ivory / Dark) and accent color.
- `blog.html` — writing index, grouped by year.
- `post.html` — single-post reader. Reads a markdown file by slug.
- `posts/` — one `.md` file per post, plus `index.json` as the manifest.
- `styles/base.css` — shared tokens and site chrome.

## Writing a new post
1. Create `posts/YYYY-MM-slug.md` (edit in Obsidian or any editor — just a file and a folder).
2. Add frontmatter at the top:
   ```
   ---
   title: Your post title
   date: 2026-04-19
   ---
   ```
3. Write Markdown below. Headings, lists, links, blockquotes, code, and images all work.
4. Add an entry to `posts/index.json`:
   ```json
   { "slug": "YYYY-MM-slug", "title": "Your post title", "date": "2026-04-19" }
   ```
5. Commit and push. That's it.

## Deploy to GitHub Pages
1. Create a repo named `<your-username>.github.io`.
2. Push these files to `main`.
3. In repo Settings → Pages, set source to `main` / root.
4. Your site will be live at `https://<your-username>.github.io/`.

No build step. Everything is static HTML + vanilla JS.
