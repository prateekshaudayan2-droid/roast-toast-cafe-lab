# Roast Toast Coast Cafe: Troubleshoot Your Code Lab

A small café website used in the IBM SkillsBuild lab "Troubleshoot Your Code Using IBM Bob". The page has a welcome message, a tagline, a background image, and an **Our Menu** button that shows and hides the menu items.

## Files

| File | Purpose |
|------|---------|
| `Menu.html` | The corrected website (HTML, CSS and JavaScript in one file) |
| `requirements.txt` | Notes on what is needed to run the page |
| `README.md` | This file |

## How to run

1. Download `Menu.html`.
2. Double-click it to open it in a web browser (Edge, Chrome or Firefox).
3. Click **Our Menu** to show the menu items. Click it again to hide them.

An internet connection is needed to load the background image and the Bogart web font.

## Bugs found and fixed

1. **Missing closing parenthesis (CSS syntax error).**
   In the `.image-container` rule, `background-image: url('...';` had no closing `)`.
   The browser ignored all the CSS after that line, so the page showed black text on a black background and no image.
   Fix: add the `)` after the URL.

2. **Wrong class name in JavaScript (functional error).**
   `toggleMenuItems()` used `document.querySelector('.menu-item')`, but the list's class is `menu-items`.
   The selector returned nothing, so clicking **Our Menu** caused an error and the menu never opened.
   Fix: change the selector to `.menu-items`.

## Other observation

The CSS targets `header h1` and `header p`, but the page has no `<header>` element (it uses `<div class="header-container">`), so those rules never apply. This was left unchanged because the default dark text is readable on the wheat background.
