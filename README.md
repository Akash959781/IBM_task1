# IBM_task1

# Library Management API

A simple RESTful API for managing a library (books, authors, lending operations) built with Node.js, Express and MongoDB (Mongoose).

This repository provides the server-side code (entry point: `index.js`) and organizes models and routes under the `models/` and `routes/` directories.

## Features
- CRUD for library resources (e.g. books)
- Built with Express and Mongoose
- Environment-driven configuration via `.env`
- Scripts for running (production and development)

## Getting started

Prerequisites
- Node.js (v16+ recommended)
- npm
- A MongoDB instance (local or cloud)

Clone the repo
```bash
git clone https://github.com/Akash959781/IBM_task1.git
cd IBM_task1
```

Install dependencies
```bash
npm install
```

Create a `.env` file in the project root with at least:
```
MONGODB_URI=<your-mongodb-connection-string>
PORT=3000
```

Run the server
- Production:
```bash
npm start
```
- Development (auto-reload with nodemon):
```bash
npm run dev
```

## Available npm scripts
- `start` — run `node index.js`
- `dev` — run `nodemon index.js` (requires `nodemon`)

These scripts are defined in `package.json`.

## Project structure
- `index.js` — application entry point
- `models/` — Mongoose models (data schemas)
- `routes/` — Express route handlers / API endpoints
- `package.json` / `package-lock.json` — project metadata and dependencies
- `README.md` — this file

## Environment variables
- `MONGODB_URI` — MongoDB connection URI
- `PORT` — port the server listens on (default often 3000)

Adjust/add variables as required by the code in `index.js`.

## API (example)
The exact endpoints depend on the route files, but a typical set for a library API looks like:

- List books
  - GET /api/books
- Get a book by id
  - GET /api/books/:id
- Create a new book
  - POST /api/books
  - Body (example):
    ```json
    {
      "title": "The Great Book",
      "author": "Author Name",
      "isbn": "1234567890",
      "publishedDate": "2020-01-01",
      "copiesAvailable": 3
    }
    ```
- Update a book
  - PUT /api/books/:id
- Delete a book
  - DELETE /api/books/:id

Check the files inside `routes/` and `models/` for the actual route names and request/response shapes.

## Contributing
Contributions are welcome. Typical workflow:
1. Fork the repository
2. Create a feature branch
3. Make changes and add tests if applicable
4. Open a pull request describing your changes

## Troubleshooting
- MongoDB connection errors: verify `MONGODB_URI` and network access
- Port in use: change `PORT` in `.env`
- Missing dependencies: run `npm install`

## License
This project is provided as-is. Add a license of your choice to `LICENSE` if you wish to make licensing explicit.

## Contact
For questions or help, open an issue in the repository or contact the maintainer.

```
