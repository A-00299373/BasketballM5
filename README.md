# BasketballM5

A small FastAPI app that uses the **balldontlie** basketball API to show:
- an index page with quick links,
- a table of NBA players,
- game results for a given season,
- and average team scoring + win % for a season.

The app renders HTML with **Jinja2** templates and serves a logo from `/static`.

---

## ✨ Features

- **Players list** — server-side filtered list of players (limited to 25–100 rows).
- **Season games** — winner/margin per game for a given season.
- **Team averages** — average points/game and win percentage per team for a season.
- **Simple UI** — clean tables built with Jinja templates.

---

## 🗺️ Routes

| Method | Path                        | Description                                  | Template            |
|-------:|-----------------------------|----------------------------------------------|---------------------|
| GET    | `/`                         | Welcome page + links                         | `templates/index.html` |
| GET    | `/allplayers?count=100`     | Players list (25 ≤ `count` ≤ 100)            | `templates/players.html` |
| GET    | `/games/{season}`           | Game results for a season (e.g. `2018`)      | `templates/games.html` |
| GET    | `/team-averages/{season}`   | Avg points & win % per team for a season     | `templates/team_averages.html` |

> The app also mounts static files at `/static` (e.g. `/static/HomeLogo.png`).

---

## 🧱 Tech Stack

- **Python** (FastAPI)
- **Jinja2** templates
- **requests** (direct HTTP calls)
- **balldontlie** Python client (for the players endpoint)
- **Uvicorn** ASGI server

---

## 📁 Project Structure

