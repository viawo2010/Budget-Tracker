

Readme · MD
# 💰 Budget Tracker
 
A single-file web app for tracking income and expenses, with a live balance and a spending breakdown by category.
 
<!--
📸 Add a screenshot or GIF here before sharing this project!
Open budget-tracker.html in your browser, add a few transactions, then take a screenshot
(or record a short screen capture for a GIF) and drop the image in this folder.
Then replace this comment with something like:
![Budget Tracker screenshot](screenshot.png)
-->
 
## Try It
 
Open [`budget-tracker.html`](./budget-tracker.html) in any browser — no install, no server, no account.
 
## Quick Start
 
1. Download `budget-tracker.html`
2. Double-click it — it opens directly in your browser
3. Start adding transactions
That's it. One file, zero setup.
 
## Features
 
- Add income or expense transactions with a description, amount, and category
- Live-updating totals for income, expenses, and current balance
- Scrollable transaction list with one-click delete
- Pie chart showing spending broken down by category
- Data is saved automatically in your browser (`localStorage`) — it's still there the next time you open the file
## How to Run It Locally (for editing)
 
No build tools or dependencies required — it's plain HTML/CSS/JS in one file.
 
- **Language/tools needed:** just a text editor (e.g. [VS Code](https://code.visualstudio.com/)) and any modern browser
- **To edit:** open `budget-tracker.html` in your editor and change the code
- **To preview changes:** save the file, then refresh the browser tab — or use VS Code's "Live Server" extension to auto-refresh on save
- **No environment variables, no `npm install`, nothing to configure**
## How It Works
 
The whole app lives in one HTML file to keep it dead simple to share and run:
 
- **HTML** defines the structure — the add-transaction form, the transaction list, the summary cards.
- **CSS** handles the dark-themed layout and styling, all scoped with CSS custom properties (`--accent`, `--income`, `--expense`, etc.) so colors are easy to retheme from one place.
- **JavaScript** manages state as a plain array of transaction objects. Every add/delete re-renders the summary, the list, and the chart from that single source of truth, rather than patching the DOM in multiple places — simpler to reason about at this scale, even though it re-renders more than strictly necessary.
- The **pie chart** is drawn by hand on an HTML `<canvas>` using basic trigonometry (`arc()` calls with computed angles) rather than a charting library, to keep the project dependency-free.
- **Persistence** is just `localStorage.setItem`/`getItem` with the transactions array as JSON — no backend needed since everything runs in the browser.
## Project Status
 
Work in progress — being built and learned step by step.
 
 


