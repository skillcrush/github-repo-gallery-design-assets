# GitHub Repo Gallery: Style Tile

A quick-reference guide to the colors, type, and reusable UI patterns. Share this with Claude when prompting for new components.

---

## Color Palette

| Swatch | Name | Hex | Used For |
| :---- | :---- | :---- | :---- |
| 🟪 | Deep Purple | `#483978` | Page title banner background, profile section background, primary button fill, small accent circle in the top corner tab, search input, search icon |
| 🟪 | Deep Purple (hover) | `#2f2550` | "View Repo" button hover state |
| 🟪 | Soft Lavender | `#9b8dc9` | Divider line under profile stats |
| 🟧 | Coral | `#f7614A` | repo card border, repo card title text |
| 🟧 | Bright Coral | `#f86d58` | GitHub icon color |
| 🟨 | Pale Yellow | `#fbf9de` | Page background |
| ⬜ | White | `#fff` | Card and section backgrounds, button text |
| ⬛ | Body Text | `#333` | Default body text |
| ⬜ | Neutral Grey | `grey` | Badge tab background |
| ⬜ | Border Grey | `#ccc` | "Back to Repo" button hover border |

---

## Typography

**Headings:** Oswald, weight 500, uppercase
**Body copy:** Open Sans, weights 400 (regular) and 700 (bold)

| Element | Font | Size | Notes |
| :---- | :---- | :---- | :---- |
| h1 | Oswald, 500 | `56px` |
| h2 | Default |
| h3 | Oswald, 500 | `20px` |
| Normal text | Open Sans, 400/700 | `18px` |

Fonts are loaded from Google Fonts:
```
Open Sans: wght@400;700
Oswald: wght@500
```

Icons come from Font Awesome Pro 5.10.0 ('fa-github-alt' and 'fa-search').
<link rel="stylesheet" href="https://pro.fontawesome.com/releases/v5.10.0/css/all.css"
    integrity="sha384-AYmEC3Yw5cVb3ZcuHtOA93w35dYTsvhLPVnYs9eStHfGJvOvKxVfELGroGkvsg+p" crossorigin="anonymous" />
---

## Content Reference (Copy-Paste Placeholders)

This project pulls all of its content live from the GitHub API rather than typing it into the HTML by hand. Since you won't wire up any JavaScript yet, use the text below as placeholder content so your shell already reads like the finished page once the data is fetched in.

### Profile Section

| Label | Sample Data |
| :---- | :---- |
| Avatar | Included in img directory of style assets |
| Name | Tauri StClaire |
| Bio | Hello! I am a responsive coder who loves Javascript React! HTML5 CSS3 FTP Web Hosting Git Version Control JSX ES6 |
| Location | San Diego, California |
| Number of public repos | 118 |

### Repo Gallery List (card titles only)

- gen-ai-recipe-chatbot
- 105-turn_back_time-2
- wordpress-nutrition-blog
- national-park-tour-planner
- study-buddy-with-ui
- study-buddy

### Repo Detail View (shown after a card is clicked)

Clicking a card swaps the gallery for a detail view with its own labeled data. A real example, so you can see the pattern and use this text to build your repo-detail view:

**Placeholder Text**

| Label | Sample Data |
| :---- | :---- |
| Name | gen-ai-recipe-chatbot |
| Description | ChefBoost Gen AI app made with LangChain, Supabase, and pgvector |
| Default Branch | main |
| Languages | Python, JavaScript, CSS, HTML, PLpgSQL |
| Link text | View Repo on GitHub! |

## Core UI Components

---

### Breakpoints

| Breakpoint | Device |
| :---- | :---- |
| Default | Mobile
| `min-width: 700px` | Tablet
| `min-width: 1200px` | Desktop

---

### Badge + Circle
A small decorative tab that sits above the page header.

```css
.badge {
    height: 80px;
    width: 50px;
    background-color: grey;
    z-index: 98;
    margin-bottom: -35px;
    margin-top: 10px;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
}

.circle {
    width: 20px;
    height: 20px;
    background-color: #483978;
    border-radius: 100%;
    z-index: 99;
    align-self: center;
    margin-top: auto;
    margin-bottom: 8px;
}
```
**Markup:**
```html
<div class="badge">
    <div class="circle"></div>
</div>
```