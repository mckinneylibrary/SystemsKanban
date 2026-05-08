# McKinney Public Library — Systems & Technology Kanban

A lightweight, self-contained project management board for tracking the Library Systems & Technology team's 6-month roadmap. Built as a single HTML file — no frameworks, no build steps, no server required.

**Live board → [mckinneylibrary.github.io/SystemsKanban](https://mckinneylibrary.github.io/SystemsKanban/)**

---

## About This Project

This board was created to support the Library Systems & Technology team during the first six months of new leadership. It translates a structured discovery-to-stabilization roadmap into 50 actionable tasks, organized across ten functional areas and tracked through a four-column Kanban workflow. 

---

## Features

- **Drag-and-drop** cards between columns (Backlog → To Do → In Progress → Done)
- **Click any card** to open a detail panel with three tabs:
  - **View** — at-a-glance summary of the card's title, area, priority, target month, and current column
  - **Edit** — modify the title, area, priority, target month, or column directly; delete a card
  - **Notes** — add timestamped status notes to track progress, blockers, or observations; notes record which column the card was in when written
- **Filter by area** using the chip bar at the top of the board
- **Search** tasks by keyword
- **Persistent state** — all card positions, edits, and notes are saved to browser `localStorage` and survive page refreshes
- **Reset Board** button to restore all defaults (with confirmation prompt)
- **Add Task** button on every column to create new cards on the fly

---

## Functional Areas

| Color | Area | Description |
|---|---|---|
| 🟢 | Public Computing | Computer lab management, print allocation, LPT:One / Libki, Hall Library laptops |
| 🔵 | Documentation | System ownership, onboarding checklists, troubleshooting resources, workflow docs |
| 🟡 | Data & Analytics | Metabase, attendance tracking, Power BI, ticketing systems |
| 🔴 | Digital Services | OPAC, LibCal, cloudLibrary, book lockers, Omeka, vendor contacts |
| 🟣 | Aspen App | ByWater partnership, push notifications, SMS reduction, patron troubleshooting |
| 🔵 | AMH | Holds processing, warranty, maintenance tracking, replacement planning |
| 🟠 | Team Dev | 1:1s, cross-training, subject matter experts, leadership expectations |
| 🟢 | Innovation | Empower Hour, AI sandbox, professional development time |
| 🩷 | Hall Library | Staffing distribution, dual-location operations, shared knowledge |
| 🟡 | Robotics | Catalog integration, dialogue flow, wayfinding |

---

## How to Use

**Opening the board**
Navigate to the live URL above, or open `index.html` directly in any modern browser. No installation or internet connection is required once the file is loaded (fonts are pulled from Google Fonts on first load).

**Moving a card**
Drag any card and drop it onto a different column, or open the card and use the **Edit** tab → **Column** selector.

**Editing a card**
Click any card to open the detail panel, then select the **Edit** tab. You can update the title, area, priority, target month, and column. Changes are saved automatically when you click **Save changes**.

**Adding a status note**
Click a card, go to the **Notes** tab, type your update, and click **Add Note** or press **⌘↵** (Mac) / **Ctrl↵** (Windows). Each note is stamped with the date, time, and the column the card was in when the note was written — giving you a chronological history of each item's progress.

**Filtering**
Click any area chip in the filter bar to narrow the board to that area. Click **All** to reset.

**Searching**
Type in the search box in the header to filter cards by keyword in real time.

---

## Data Persistence

All board state is stored in your browser's `localStorage` under the key `mckinney_kanban_v2`. This means:

- State is **per-browser and per-device** — changes made in Chrome on one computer will not appear in Firefox or on another machine.
- The board is intended as a **single-user personal tracking tool**. If multiple people need to view the same board state, consider exporting to a shared platform (see notes below).
- To clear all saved data and restore the original 50-item board, click **Reset Board** in the top-right corner.

---

## Project Structure

```
SystemsKanban/
└── index.html        # The entire application — HTML, CSS, and JavaScript in one file
└── README.md         # This file
```

There are no dependencies to install, no package.json, and no build process. The application is entirely self-contained in `index.html`.

---

## Deployment

This project is hosted via **GitHub Pages**. Any commit to the `main` branch will automatically redeploy the live site within a few minutes.

To deploy your own copy:

1. Fork this repository
2. Go to **Settings → Pages**
3. Set source to **Deploy from a branch**, branch `main`, folder `/ (root)`
4. Your board will be available at `https://[your-username].github.io/SystemsKanban/`

> **Note:** GitHub Pages requires a public repository on free GitHub accounts. The HTML source will be publicly visible at the repository URL even if the live site URL is shared privately. For access-restricted hosting, consider [Netlify](https://netlify.com) with site password protection.

---

## Background

This board was developed in May 2026 as part of a strategic planning conversation between the Ed Veal the Library Systems Manager and Spencer Smith the Library Director at McKinney Public Library. It is based on the **Library Systems Leadership – First 6 Months** roadmap and covers the period from onboarding through the opening of the Roy and Helen Hall Memorial Library. 

This is intended to expand and grow over time. 


---

*McKinney Public Library · Systems & Technology Team · McKinney, Texas*
