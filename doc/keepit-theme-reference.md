# KeepIt Hugo Theme: Practical Reference

This is a living, actionable reference for building and maintaining your hypnotherapy practice website with the KeepIt Hugo theme. Use this as a cheat sheet for yourself and your AI assistant.

---

## 1. Project Setup

### Install Hugo (extended version recommended)
- [Download Hugo](https://gohugo.io/getting-started/installing/)
- Minimum version: **0.62.0**

### Create a New Site
```bash
hugo new site mysite
cd mysite
git init
git submodule add https://github.com/Fastbyte01/KeepIt.git themes/KeepIt
```

### Basic `config.toml` Example
```toml
baseURL = "https://yourdomain.com/"
theme = "KeepIt"
title = "Dr. Kristof Hypnotherapy"
languageCode = "en"
languageName = "English"
[author]
  name = "Dr. Kristof"
  email = "your@email.com"
[menu]
  [[menu.main]]
    name = "Home"
    url = "/"
    weight = 1
  [[menu.main]]
    name = "About"
    url = "/about/"
    weight = 2
  [[menu.main]]
    name = "Services"
    url = "/services/"
    weight = 3
  [[menu.main]]
    name = "Contact"
    url = "/contact/"
    weight = 4
```

---

## 2. Content Organization
- Blog posts: `content/posts/`
- Pages: `content/about.md`, `content/services.md`, etc.
- Use [page bundles](https://gohugo.io/content-management/page-bundles/) for posts with images/resources.

### Example: Creating a Post
```bash
hugo new posts/benefits-of-hypnotherapy.md
```

---

## 3. Shortcodes & Markdown Extensions

### Custom Style
```markdown
{{< style "text-align:center; color:#2a9d8f;" >}}
Welcome to Dr. Kristof's Hypnotherapy Practice!
{{< /style >}}
```

### Admonitions (Tips, Notes, etc.)
```markdown
{{< admonition tip "Hypnotherapy is safe and effective for stress relief." >}}
```

### Font Awesome Icons
```markdown
:fas fa-brain fa-fw: Hypnotherapy for the mind
```

### Mermaid Diagrams
```markdown
{{< mermaid >}}
graph TD; A[Client] --> B[Hypnotherapy Session];
{{< /mermaid >}}
```

### Music Player
```markdown
{{< music url="/music/relaxing.mp3" name="Relaxing Music" artist="Dr. Kristof" cover="/images/relax.jpg" >}}
```

### Typing Animation
```markdown
{{< typeit >}}Experience deep relaxation...{{< /typeit >}}
```

---

## 4. Customization

### Override Styles
- Create `assets/css/_override.scss` to override theme variables.
- Create `assets/css/_custom.scss` for your own CSS.

#### Example: Change Primary Color
```scss
// assets/css/_override.scss
$primary: #2a9d8f;
```

---

## 5. SEO & Analytics
- Add Google Analytics code in `config.toml`:
  ```toml
  googleAnalytics = "UA-XXXXXXX-X"
  ```
- Set `description`, `images`, and `copyright`.

---

## 6. Multilingual Support
- Add more languages in `config.toml` under `[languages]`.
- Example:
  ```toml
  [languages.en]
    languageName = "English"
    weight = 1
  [languages.ru]
    languageName = "Russian"
    weight = 2
  ```

---

## 7. Deployment
- Build: `hugo`
- Local preview: `hugo serve --disableFastRender`
- Deploy to Netlify, GitHub Pages, Render, etc.

---

## 8. Useful Tips for Hypnotherapy Practice Sites
- Use diagrams to explain therapy processes.
- Highlight important info with admonitions.


---

*Update this doc as you add new features or learn new tricks!* 