# TodoStart29 — To-Do App

Live demo: <https://todostart29.ccbp.tech>

Streamlined, keyboard-friendly to-do app with offline persistence.

---

## Features
- Add, edit, complete, and delete tasks
- Bulk actions: complete-all / clear-completed
- LocalStorage persistence (works offline)
- Keyboard shortcuts: **Enter** to add, **E** to edit, **⌫** to delete, **Space** to toggle
- Filters: All / Active / Completed
- Accessible: labels, focus states, ARIA where needed
- Responsive, mobile-first layout

## Tech Stack
- **HTML5**, **CSS3**, **JavaScript (ES6+)**
- No frameworks or build step required

## Quick Start
```bash
# 1) Download
git clone <your-repo-url> todostart29
cd todostart29

# 2) Run (any static server works)
# Option A: open index.html directly
# Option B: use a tiny server
python3 -m http.server 8080
# then visit http://localhost:8080
```

## Project Structure
```
.
├─ index.html
├─ css/
│  └─ style.css
├─ js/
│  ├─ app.js          # state & handlers
│  ├─ storage.js      # localStorage helpers
│  └─ dom.js          # rendering & events
└─ assets/
   └─ icons/
```

## Configuration
- LocalStorage key: `todostart29.todos`
- Each task: `{ id: string, title: string, completed: boolean, createdAt: number }`

## Testing (manual)
- Add > refresh page → tasks persist
- Edit title → blur / Enter saves
- Toggle complete → moves between filters
- Clear completed → removes only done items
- Tab through controls → visible focus ring

## Deployment
- **Netlify / Vercel / GitHub Pages**: deploy the root folder as a static site.
- Custom domain already mapped to `ccbp.tech` (live link above).

## Roadmap (push beyond “yet-another todo”)
- Smart capture: parse “Call Sam @ 5pm” → reminder
- Streaks & XP for habit-forming tasks
- Natural-language bulk add (paste a list)
- Offline-first sync with Conflict-Free Replicated Data Types (CRDTs)
- Shareable lists with role-based access
- Tiny service worker for installable PWA

## Contributing
1. Fork → create feature branch → PR
2. Keep JS pure and framework-free
3. Use semantic HTML; run Lighthouse and fix any a11y regressions

## License
MIT © You/Org Name
