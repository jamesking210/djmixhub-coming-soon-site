# DJMIXHUB.com Coming Soon Page

Simple dark neon teaser site for **DJMIXHUB.com** using your logo and a lightweight Docker setup.

## Files
- `index.html`
- `styles.css`
- `assets/logo.jpg`
- `Dockerfile`
- `docker-compose.yml`

## Run with Docker Compose
```bash
docker compose up -d --build
```

Then open:
```text
http://YOUR-SERVER-IP:8086
```

## Run with plain Docker
```bash
docker build -t djmixhub-coming-soon .
docker run -d --name djmixhub-coming-soon -p 8086:80 --restart unless-stopped djmixhub-coming-soon
```

## GitHub deploy flow
1. Upload these files to a new or existing GitHub repo.
2. Clone the repo on your server.
3. Run:
```bash
docker compose up -d --build
```

## Notes
- The site is a simple static page served by `nginx:alpine`.
- External port is **8086**.
- Replace `assets/logo.jpg` any time if you update the logo later.
