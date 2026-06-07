# Zen Garden

Zen Garden is a full-stack web application that allows users to create, customize, and persist virtual garden layouts.

Users can register accounts, design their own garden plots by placing plants and decorative elements, and return later to continue modifying their layouts. Garden state is stored in PostgreSQL and rendered dynamically through SVG-based visualizations.

---

## Features

- User registration and authentication
- Persistent garden layouts tied to individual accounts
- Add, remove, and modify garden elements
- PostgreSQL-backed data persistence
- Dynamic SVG-based rendering
- Responsive web interface

---

## Tech Stack

### Backend
- Node.js
- Express
- Sequelize ORM
- PostgreSQL

### Frontend
- Handlebars
- JavaScript
- HTML
- CSS

### Authentication
- bcrypt
- express-session
- connect-session-sequelize

### Development Tools
- Nodemon
- dotenv

---

## Architecture

Zen Garden follows an MVC architecture where:

- Models manage garden, user, and plant data
- Controllers process user actions and application logic
- Views render garden layouts and account pages

The database serves as the source of truth for all garden state. User actions update persistent records, which are then transformed into SVG-rendered visualizations.

For a deeper discussion of the application's architecture and design decisions:

➡️ **[System Design Overview](https://github.com/swokamoto/system-design-notes/blob/main/zen-garden.md)**

---

## Running Locally

### Install Dependencies

```bash
npm install
```

### Configure Environment Variables

Create a `.env` file with the required PostgreSQL connection information.

### Seed Database

```bash
npm run seed
```

### Start Development Server

```bash
npm run watch
```

---

## Contributors

- Scott Okamoto
- Crystal Lisi
- Mike Jurek
- Miranda Delapaz
- Samuel Wlodawski

---

## Project Goals

This project was originally developed during a full-stack web development bootcamp as an exploration of:

- Authentication and user ownership
- Relational database design
- State persistence
- Server-rendered web applications
- Dynamic visual rendering

While originally built as a team project, it remains a useful example of modeling structured application state and translating that state into interactive visual output.
