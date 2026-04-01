# Vitya's Life

Vitya's Life is a small browser-based sokoban-style puzzle game with an office-themed UI.
The repository now contains the shipped web version only: the game runs from `index.html`, uses static assets from `assets/`, and is served through nginx in Docker.

## Stack

- Static HTML, CSS and vanilla JavaScript
- Asset files in `assets/`
- nginx for serving the game
- Docker and Docker Compose for local run and deployment

## Project Structure

- `index.html` - game UI, gameplay rendering and interaction logic
- `assets/images` - player and box sprites
- `assets/sounds` - background music
- `Dockerfile` - container image definition
- `docker-compose.yml` - runtime configuration
- `nginx.conf` - static file serving rules

## Run Locally

### Option 1: Docker Compose

```bash
docker compose up --build
```

Open:

- `http://localhost:8080`

### Option 2: Static File Server

Any static file server works. For example:

```bash
python -m http.server 8080
```

Then open:

- `http://localhost:8080`

## Controls

- `Enter` or click on the start screen: start game
- `Arrow keys`: move
- `Z`: undo last move
- `R`: reset current board
- `H`: toggle hint bubble

## Deployment

The repository includes a GitHub Actions workflow that:

- validates the static app files
- builds a Docker image
- pushes the image to GHCR
- deploys it with Docker Compose on the target server

## Notes

- The old Python/pygame prototype and redesign reference files were removed to keep the repository aligned with the active web version.
- Browser audio starts only after user interaction because autoplay is restricted by default.
