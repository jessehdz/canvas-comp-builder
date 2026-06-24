# Canvas Component Builder
**Seattle Colleges eLearning**

A free, browser-based tool that lets faculty build accessible, Canvas-ready HTML components without writing a single line of code. Fill out a form, pick a style and color theme, click Build — then copy the generated code directly into Canvas.

🔗 **[Open the Builder](https://jessehdz.github.io/canvas-comp-builder/)**

---

## What It Does

Faculty choose what they want to build, fill in their content, select a layout and color palette, and receive Canvas-ready inline HTML they can paste directly into any Canvas page via the HTML editor (`</>` button).

### Components

| Component | Description |
|---|---|
| **Course Homepage** | Navigation buttons linking to Canvas sections + office hours bar |
| **Announcement** | Styled notice or update with tag, headline, message, and footer |
| **Module Intro** | Week header, learning objectives, and optional this-week checklist |
| **Discussion Prompt** | Prompt header, guiding questions, and reply requirements |
| **Syllabus Banner** | Course header with instructor info and quick-stat boxes |
| **Section Divider** | Label to visually separate sections on any Canvas page |

### Homepage Layout Options

| Layout | Description | Canvas Editor Safe? |
|---|---|---|
| Stacked buttons | Full-width single-column buttons | Visual editor safe |
| Card grid — no header | Solid-color cards, centered, fixed width | HTML editor only |
| Card grid — with header | Dark header band + card grid below | HTML editor only |

### Color Themes

11 WCAG AA-verified palettes — all text/background combinations tested at ≥ 4.5:1 contrast ratio:

Ocean · Sand · Forest · Plum · Terra · Slate · Night · Rose · Sage · Charcoal · Indigo

---

## Privacy & Data

**This tool saves nothing.**

- No server, no database, no account required
- All form input lives only in your browser tab — nothing is transmitted anywhere
- Closing the tab clears everything
- No external scripts, no cookies, no tracking of any kind
- FERPA safe — the form only asks for course-level information (title, meeting time, office hours). No student data is ever entered or processed.

You can verify this by opening your browser's Network tab in Developer Tools while using the builder — you will see zero outbound requests from the form.

---

## Intellectual Property

**You own everything this tool generates.**

The HTML code produced by this builder is yours to use, modify, copy, and distribute however you like. Seattle Colleges eLearning makes no intellectual property claim on the output. The templates are provided as a free resource for Seattle Colleges faculty and staff with no license restrictions.

---

## Accessibility

All generated code is built to meet **WCAG 2.2 AA** standards:

- Every navigation link includes a descriptive `aria-label`
- Decorative elements use `aria-hidden="true"`
- Semantic HTML throughout: `<h1>`, `<nav>`, `<header>`, `<aside>`, `role="main"`
- All 11 built-in color palettes pass 4.5:1 contrast for body text and 3:1 for large text and UI elements

> **Note:** The builder provides an accessible structure. Instructors are responsible for the accessibility of content they add — including alt text for images and captions for embedded video.

---

## How to Use

### Pasting Code Into Canvas

1. Go to your Canvas course → **Pages** → **+ Page**
2. Name the page (e.g. "Course Home")
3. In the Rich Content Editor toolbar, click the **`</>`** button (bottom right, or under the `···` menu)
4. Delete any existing content in the HTML view
5. Paste your generated code
6. Click **Save & Publish**

### Setting as Your Course Home Page

1. Go to **Pages** → find your page → click the **⋮** three-dot menu → **"Use as Front Page"**
2. Go to your course **Home** → click **"Choose Home Page"** on the right → select **"Pages Front Page"**

### Important: Layout Levels and the Visual Editor

Once you paste a layout template (Card grid layouts), only ever edit it through the `</>` HTML editor button. The Canvas visual editor does not understand flex-based layouts and will collapse the design if you save through it.

**Stacked buttons** are the only layout you can safely edit in Canvas's normal visual editor after pasting.

---

## Updating the Tool

When a new version of the builder is released, the URL stays the same — just refresh the page. Any code you've already pasted into Canvas keeps working regardless of updates to this tool.

---

## FAQ

The builder includes a built-in **How to Use** tab (right panel) with 7 sections and 20+ answers covering:

- Getting Started
- Using the Builder
- Adding Links
- Customizing After Pasting
- Accessibility
- Sharing & Hosting
- Privacy, Data & Intellectual Property

---

## Feedback & Support

Found a bug? Have a feature request? Use the links in the footer of the builder, or contact us directly:

📧 [elearning@seattlecolleges.edu](mailto:elearning@seattlecolleges.edu)

Please include:
- Which component you were building
- What happened vs. what you expected
- Your browser and operating system

---

## For Developers

This is a single self-contained HTML file with no external dependencies, no build process, and no package manager.

**Stack:**
- Vanilla HTML, CSS, and JavaScript — no frameworks
- All styles are inline in the `<style>` block (not used in Canvas output — the generated HTML uses only inline `style=""` attributes to survive Canvas's HTML sanitizer)
- CSS custom properties (`var(--ink)`, etc.) power the light/dark mode toggle
- The code generator runs entirely in the browser via string construction in JavaScript

**To run locally:** Just open `index.html` in any browser. No server required.

**To update and redeploy:**
1. Edit `index.html` locally
2. Go to your GitHub repo → click `index.html` → pencil icon → paste updated content → Commit
3. GitHub Pages auto-deploys within ~60 seconds

**File size:** ~92KB (single file, no assets)

---

## License

Free to use, modify, and distribute. No license restrictions.

Built by Seattle Colleges eLearning · [elearning@seattlecolleges.edu](mailto:elearning@seattlecolleges.edu)
