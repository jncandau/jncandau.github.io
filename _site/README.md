# QEFIR Lab Website

A Jekyll-based static website for the QEFIR Lab (Quantitative Ecology of Forest Insects Research).

## 🌲 Features

- **Clean, nature-inspired design** with forest/ecological color palette
- **Four main sections**: Home, Lab Info, Lab Projects, Publications
- **Responsive layout** for mobile and desktop
- **Easy to update** via Markdown files and YAML data
- **SEO-friendly** with Jekyll SEO plugin

## 🚀 Quick Start

### Option 1: GitHub Pages (Recommended)

1. **Fork or clone this repository**
   ```bash
   git clone https://github.com/yourusername/QEFIR-Lab.git
   ```

2. **Rename the repository** to `yourusername.github.io` (for a user site) or keep any name (for a project site)

3. **Enable GitHub Pages**
   - Go to Settings → Pages
   - Select source branch: `main`
   - Select folder: `/ (root)`
   - Click Save

4. **Customize the content** (see below)

5. Your site will be live at `https://yourusername.github.io`

### Option 2: Local Development

1. **Install Jekyll** (requires Ruby):
   ```bash
   gem install bundler jekyll
   ```

2. **Create a Gemfile** in the root directory:
   ```ruby
   source "https://rubygems.org"
   gem "jekyll", "~> 4.3"
   gem "jekyll-seo-tag"
   gem "jekyll-sitemap"
   ```

3. **Install dependencies**:
   ```bash
   bundle install
   ```

4. **Run locally**:
   ```bash
   bundle exec jekyll serve
   ```

5. Visit `http://localhost:4000`

## 📁 Directory Structure

```
QEFIR-Lab/
├── _config.yml          # Site configuration
├── _layouts/            # Page templates
│   ├── default.html
│   ├── home.html
│   └── page.html
├── _data/
│   └── team.yml         # Team member data
├── assets/
│   ├── css/
│   │   └── main.css     # Styles
│   └── images/          # Images (add your own)
├── index.md             # HOME page
├── lab-info/
│   └── index.md         # LAB INFO page
├── lab-projects/
│   └── index.md         # LAB PROJECTS page
└── publications/
    └── index.md         # PUBLICATIONS page
```

## ✏️ Customization

### 1. Update Site Settings (`_config.yml`)

```yaml
title: "Your Lab Name"
description: "Your research focus"
email: your.email@university.edu
github_username: your-github
twitter_username: your-twitter
```

### 2. Update Pages

Each section has its own `index.md` file:

- **Home** (`index.md`): Edit hero text, research focus areas, and news
- **Lab Info** (`lab-info/index.md`): Update team members, opportunities, values
- **Lab Projects** (`lab-projects/index.md`): Add/remove project cards
- **Publications** (`publications/index.md`): Add your papers

### 3. Add Team Photos

1. Add photos to `assets/images/team/`
2. Update references in `_data/team.yml` or directly in `lab-info/index.md`

### 4. Customize Colors

Edit CSS variables in `assets/css/main.css`:

```css
:root {
  --forest-deep: #1a3c34;    /* Dark green - headers, footer */
  --forest-mid: #2d5a4e;     /* Medium green */
  --lichen: #8fa876;         /* Accent green */
  --moth-amber: #c9a227;     /* Gold accent */
  /* ... */
}
```

### 5. Add Publication PDFs

1. Create `assets/papers/` folder
2. Add PDFs there
3. Link in publications: `[PDF](/assets/papers/yourpaper2024.pdf)`

## 📝 Adding Content

### New Publication

Add to `publications/index.md`:

```html
<li class="publication-item">
  <span class="publication-year">2026</span>
  <h3 class="publication-title">Your paper title</h3>
  <p class="publication-authors">Author A, <strong>Your Name</strong>, Author B</p>
  <p class="publication-journal">Journal Name, volume(issue), pages</p>
  <div class="publication-links">
    <a href="/assets/papers/paper.pdf">PDF</a>
    <a href="https://doi.org/xxx">DOI</a>
  </div>
</li>
```

### New Project

Add to `lab-projects/index.md`:

```html
<div class="card">
  <div class="card-image">🔬</div>
  <div class="card-content">
    <h3><a href="#">Project Title</a></h3>
    <p class="card-meta">2024 – Present | Funded by XYZ</p>
    <p class="card-description">Project description...</p>
    <div class="tags">
      <span class="tag">Tag 1</span>
      <span class="tag">Tag 2</span>
    </div>
  </div>
</div>
```

### New Team Member

Add to the appropriate section in `lab-info/index.md`:

```html
<div class="team-card">
  <div class="team-photo">👩‍🔬</div>
  <h3>Name</h3>
  <p class="team-role">Role</p>
  <p class="team-research">Research interests</p>
</div>
```

## 🎨 Design Notes

The theme uses a **forest-inspired palette** appropriate for ecology research:
- Deep forest greens for headers and accents
- Bark browns for secondary text
- Lichen greens for highlights
- Cream/off-white backgrounds mimicking paper

Typography combines:
- **Libre Baskerville** (serif) for headings — academic, authoritative
- **Source Sans 3** (sans-serif) for body — clean, readable

## 📄 License

Feel free to use and adapt this template for your own academic lab website.

## 🐛 Issues?

If something's not working, check:
1. YAML front matter syntax (spaces, not tabs)
2. File paths are relative
3. GitHub Pages build status in repository settings

---

*Built with Jekyll and designed for academic research labs studying forest ecosystems.*
