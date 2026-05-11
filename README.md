
# The C++ Grind

Anyone can use this to learn how to code — not just C++. The projects, roadmap, and build challenges are language-agnostic at the concept level. Every project here works as a blueprint you can implement in any language. The C++ code is the reference; the patterns are universal.

This repo is intentionally simple — plain HTML/CSS/JS — so the content is easy to edit and the site ships on GitHub Pages with no build step.

## The two repos

| Repo | What it is |
|------|-----------|
| **[TheCppGrind](https://github.com/Cooper-Bugg/TheCppGrind)** | This site — HTML, CSS, JS, articles, and data. The learning journal. |
| **[Start-Learning-Cpp](https://github.com/Cooper-Bugg/Start-Learning-Cpp)** | The project repo — all 43 C++ projects, hand-typed and documented. Use them as references when building your own version in any language. |

## What's in here

- **Intro**: start here — what the site is, who it's for, how to use it.
- **Roadmap**: a phase-based path through core C++ topics, resources mapped to each phase.
- **Articles**: chapter-by-chapter notes following Roberts' *Programming Abstractions in C++*, written as I learn.
- **Projects**: 43 projects from CLI tools to systems programming, each tied to specific concepts.
- **Games**: C++ Wordle and a daily code challenge.
- **References / Resources**: quick lookup + curated links.

## Tech stack

- **HTML** pages under `index.html` and `pages/`
- **CSS** in `css/main.css` (design tokens via CSS variables)
- **JS** in `js/main.js` (nav, theme toggle, local progress state)
- **Icons** via Google Material Symbols Rounded (loaded from Google Fonts)
- **Data** in `site-data.json` (resource lists, metadata)

## Theme (dark + light)

The site is **dark mode by default**.

There's also a light theme that keeps the same accent palette but uses a cool off-white background.

- The toggle lives next to the site title in the header.
- User preference is saved in `localStorage` under `theme` (`dark` or `light`).
- If there's no saved preference, it follows the OS setting (`prefers-color-scheme`).

Theme values are controlled via CSS variables in `css/main.css`:

- `:root` = dark theme tokens
- `[data-theme="light"]` = light theme overrides

## Progress tracking

Some pages use clickable progress markers (elements with the `.progress-check` class). Their state is stored locally in the browser:

- Key format: `progress:<path>:<index>`
- Storage: `localStorage`

No analytics and no server-side tracking.

## Project layout

```text
.
├── index.html
├── pages/              # top-level site pages (intro, roadmap, articles, …)
├── articles/           # chapter notes (static html)
├── css/
│   └── main.css
├── js/
│   └── main.js
├── images/
├── documentation/
└── site-data.json
```

## Notes

- This site is a learning journal, not a copy of LearnCpp/Roberts/other resources.
- The C++ projects live in [Start-Learning-Cpp](https://github.com/Cooper-Bugg/Start-Learning-Cpp) — check that repo for runnable code.
