# Golf Booking Interface

A clean, responsive front-end for browsing golf courses and booking tee times. This lightweight project demonstrates an intuitive UI, search/filter functionality, and a simple booking flow — suitable as a prototype, demo, or starting point for a more complete booking system.

## Table of contents

- [Demo](#demo)
- [Features](#features)
- [Tech stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Development](#development)
- [Project structure](#project-structure)
- [Customization](#customization)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Demo

Open `index.html` in your browser to see the interface. For a local server (recommended for ES module/assets), run a simple static server (examples below).

## Features

- Golf course listing with details (name, location, rating, photos)
- Search and filters (location, price, amenities)
- Tee time browsing and simple booking flow (front-end only)
- Responsive layout for desktop and mobile
- Clean, extendable HTML/CSS/JS codebase for prototyping

## Tech stack

- HTML5
- CSS3 (vanilla)
- JavaScript (vanilla ES6+)

## Installation

No build tools are required — this is a static front-end. You can run it in two ways:

1) Quick (open file):

	- Double-click `index.html` or open it from your browser: File → Open File → select `index.html`.

2) Recommended (static server) — serves assets and avoids CORS/module issues:

- With Python 3 (works on Windows PowerShell):

```powershell
# from the project folder
python -m http.server 8000
# then open http://localhost:8000
```

- With Node.js (http-server):

```powershell
npx http-server -c-1 . -p 8000
# then open http://localhost:8000
```

## Usage

- Browse the list of golf courses on the home page.
- Use the search box and filters to narrow results by location, price, or amenities.
- Click a course to view details and available tee times.
- Select a tee time and follow the booking form to simulate a reservation (note: this project contains front-end booking flow only — no backend persistence).

## Development

- Recommended: open repository in VS Code and use the Live Server extension for hot reload.
- Keep JavaScript modular and separate UI concerns from data logic when extending the app.

Quick checklist for common tasks:

- Run a local server (see Installation).
- Edit `style.css` for styling changes.
- Edit `script.js` to change data handling, add new filters, or connect to a backend API.

## Project structure

- `index.html` — main entry file and layout
- `style.css` — project styles
- `script.js` — client-side logic: search, filter, and booking flows
- `README.md` — this file

If you add assets (images, icons), place them in an `assets/` folder and reference them from `index.html` or CSS.

## Customization

- To connect to a real backend, change `script.js` to fetch course and tee-time data from your API instead of static objects. Suggested contract:

- GET /courses -> returns array of course objects { id, name, location, price, amenities, images, rating }
- GET /courses/:id/teetimes -> returns available tee times for a course
- POST /bookings -> accepts booking payload and returns confirmation

## Contributing

Contributions are welcome. Keep changes small and focused. Suggested steps:

1. Fork the repository
2. Create a feature branch
3. Open a PR with a clear description

If you add JavaScript features, include basic manual testing steps in the PR description.

## License

This project is provided under the MIT License. See the `LICENSE` file for details.

## Contact

If you have questions or want improvements, open an issue or contact the project owner.

