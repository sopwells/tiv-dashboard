# The Intelligent View - Jekyll Blog

A clean, minimal blog for daily tech and investment insights.

## Quick Start Guide

### Initial Setup (One-time, ~15 minutes)

1. **Install Prerequisites**
   - Install Git: https://git-scm.com/downloads
   - Install Ruby: https://www.ruby-lang.org/en/downloads/
   - Install Jekyll: `gem install jekyll bundler`

2. **Create GitHub Repository**
   - Go to GitHub.com and create a new repository called `tivframework.com`
   - Keep it public (required for free GitHub Pages)

3. **Upload Your Blog**
   ```bash
   cd tiv-jekyll-blog
   git init
   git add .
   git commit -m "Initial blog setup"
   git remote add origin https://github.com/YOUR-USERNAME/tivframework.com.git
   git push -u origin main
   ```

4. **Enable GitHub Pages**
   - Go to your repository Settings → Pages
   - Source: Deploy from branch `main`
   - Folder: `/ (root)`
   - Click Save
   - Your site will be live at `https://YOUR-USERNAME.github.io/tivframework.com` in ~1 minute

5. **Connect Custom Domain (Optional)**
   - In GitHub Pages settings, add custom domain: `tivframework.com`
   - In your domain registrar, point your domain to GitHub:
     - Add A records pointing to: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
     - Or add CNAME record: `YOUR-USERNAME.github.io`

### Daily Posting Workflow (~2 minutes)

1. **Create New Article File**
   - Name format: `_posts/YYYY-MM-DD-your-article-title.md`
   - Example: `_posts/2026-02-09-ai-regulation-update.md`

2. **Use This Template**
   ```markdown
   ---
   layout: post
   title: "Your Article Title Here"
   date: 2026-02-09
   category: "AI"  # or "Markets", "UK Finance", "Tech", etc.
   summary: "Your one-paragraph summary here describing the key insight."
   commentary: "Your quick take or opinion in one sentence."
   visualization: "/assets/images/your-chart.png"  # or leave as "" if pending
   ---

   Your longer commentary goes here. This is the main body of your article.
   
   You can write multiple paragraphs with more detail and analysis.
   ```

3. **Add Visualization (if you have one)**
   - Save your chart/graph image to `assets/images/`
   - Reference it in the `visualization:` field above

4. **Publish**
   ```bash
   git add .
   git commit -m "New article: Your Title"
   git push
   ```
   - Site updates automatically in ~30 seconds!

### Example Daily Workflow

```bash
# Morning: Create your article
cd tiv-jekyll-blog
code _posts/2026-02-09-my-new-article.md  # Opens in VS Code, or use any text editor

# Add your visualization if ready
# Save to: assets/images/my-chart.png

# Publish
git add .
git commit -m "Article: My New Article Title"
git push

# Done! Live in 30 seconds.
```

## File Structure

```
tiv-jekyll-blog/
├── _config.yml          # Site settings (email, title, etc.)
├── _layouts/            # Page templates (don't touch these)
├── _posts/              # Your articles go here!
│   └── 2026-02-09-article-name.md
├── assets/
│   ├── css/            # Styling (don't touch)
│   └── images/         # Your visualization images go here
│       ├── tiv-logo.jpg
│       └── your-charts.png
└── index.html          # Homepage (don't touch)
```

## Tips

- **Article filenames** must start with date: `YYYY-MM-DD-title.md`
- **Categories** can be anything: "AI", "Markets", "Tech", "Regulation", etc.
- **Visualizations** are optional - leave the field empty (`visualization: ""`) if pending
- **Commit messages** help you track what you posted: `git commit -m "Article: UK loses tech unicorn"`

## Testing Locally (Optional)

Before pushing, you can preview locally:

```bash
cd tiv-jekyll-blog
bundle exec jekyll serve
```

Visit `http://localhost:4000` in your browser.

## Troubleshooting

- **"Page not found"**: Wait 1-2 minutes after pushing, GitHub needs to rebuild
- **Images not showing**: Check the path starts with `/assets/images/`
- **Old article still showing**: Clear browser cache or try incognito mode

## Need Help?

Email: sophiegeorginawells@gmail.com
