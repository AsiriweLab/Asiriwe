# Academic Personal Website

A clean, modern academic website built with Jekyll for GitHub Pages.

## Quick Start - Deploy to GitHub Pages

### Step 1: Create GitHub Repository
1. Go to [github.com](https://github.com) and create a new repository
2. Name it `username.github.io` (replace `username` with your GitHub username) for a user site, or any name for a project site

### Step 2: Upload Files
1. Upload all contents of this `website_claude` folder to your repository
2. Or use git:
   ```bash
   cd website_claude
   git init
   git add .
   git commit -m "Initial website"
   git branch -M main
   git remote add origin https://github.com/username/username.github.io.git
   git push -u origin main
   ```

### Step 3: Enable GitHub Pages
1. Go to your repository on GitHub
2. Click **Settings** → **Pages**
3. Under "Source", select **Deploy from a branch**
4. Select **main** branch and **/ (root)** folder
5. Click **Save**

Your site will be live at `https://username.github.io` within a few minutes!

---

## Customizing Your Website

### Basic Configuration
Edit `_config.yml` to update:
- Your name and title
- University/affiliation
- Email and office location
- Research areas
- Social/academic profile links

### Adding Content

#### Publications (`_data/publications.yml`)
```yaml
- title: "Your Paper Title"
  authors: "Your Name, Co-Author"
  venue: "Conference/Journal Name"
  year: 2024
  pdf: "/assets/papers/paper.pdf"
  doi: "10.1000/xxxxx"
  code: "https://github.com/..."
```

#### Courses (`_data/courses.yml`)
```yaml
- code: "CS 101"
  name: "Course Name"
  semester: "Fall 2024"
  level: "Undergraduate"
  description: "Course description..."
  current: true
```

#### News (`_data/news.yml`)
```yaml
- date: "Dec 2024"
  content: "Paper accepted at Conference X!"
```

#### Projects (`_data/projects.yml`)
```yaml
- title: "Project Title"
  status: "Ongoing"
  funding: "Funding Source"
  description: "Project description..."
```

#### Students (`_data/students.yml`)
```yaml
- name: "Student Name"
  degree: "Ph.D."
  topic: "Research Topic"
```

### Profile Photo
Replace `assets/images/profile.jpg` with your photo (recommended: 400x400px, square).

### CV PDF
Add your CV as `assets/cv.pdf`.

### Editing Pages
Each page is a Markdown file in the root:
- `index.md` - Home page / About
- `research.md` - Research interests and projects
- `publications.md` - Publications list
- `teaching.md` - Courses and teaching
- `cv.md` - Curriculum Vitae
- `contact.md` - Contact information

---

## Features

- **Dark/Light Theme Toggle** - Respects system preference, remembers user choice
- **Responsive Design** - Works on desktop, tablet, and mobile
- **Easy Content Management** - Update YAML files, no coding required
- **SEO Friendly** - Proper meta tags and semantic HTML
- **Fast Loading** - Minimal dependencies, optimized CSS
- **Accessible** - Semantic markup and proper contrast

---

## File Structure

```
website_claude/
├── _config.yml          # Site configuration
├── _layouts/
│   └── default.html     # Main layout template
├── _includes/
│   ├── header.html      # Navigation header
│   └── footer.html      # Page footer
├── _data/
│   ├── publications.yml # Publications list
│   ├── courses.yml      # Courses list
│   ├── news.yml         # News items
│   ├── projects.yml     # Research projects
│   └── students.yml     # Student list
├── assets/
│   ├── css/
│   │   └── style.css    # All styles
│   ├── js/
│   │   └── theme.js     # Theme toggle
│   └── images/          # Images folder
├── index.md             # Home page
├── research.md          # Research page
├── publications.md      # Publications page
├── teaching.md          # Teaching page
├── cv.md                # CV page
├── contact.md           # Contact page
├── Gemfile              # Ruby dependencies
└── README.md            # This file
```

---

## Local Development (Optional)

To preview locally before pushing:

```bash
# Install Ruby and Bundler first, then:
bundle install
bundle exec jekyll serve
```

Visit `http://localhost:4000` in your browser.

---

## Troubleshooting

**Site not updating?**
- GitHub Pages may take 1-2 minutes to rebuild
- Check Actions tab for build errors
- Clear browser cache

**Styles look wrong?**
- If using a project site (not `username.github.io`), update `baseurl` in `_config.yml` to `/repo-name`

**Images not loading?**
- Ensure paths start with `/assets/...`
- Check file extensions match exactly

---

## License

Free to use and modify for your personal academic website.
