# Playwright Setup i Pokretanje

Playwright E2E testovi nalaze se u zasebnom projektu:

[`PricalicaE2E`](/c:/Users/Andrej/Desktop/Pricalica%202026/PricalicaE2E)

## Glavne datoteke

- konfiguracija: [playwright.config.js](/c:/Users/Andrej/Desktop/Pricalica%202026/PricalicaE2E/playwright.config.js)
- testovi: [app.spec.js](/c:/Users/Andrej/Desktop/Pricalica%202026/PricalicaE2E/tests/e2e/app.spec.js)
- Docker setup: [docker-compose.e2e.yml](/c:/Users/Andrej/Desktop/Pricalica%202026/PricalicaE2E/docker-compose.e2e.yml)

## Instalacija

Iz mape `PricalicaE2E`:

```bash
npm install
npx playwright install
```

## Lokalno pokretanje

Ako su API i web app već pokrenuti:

```bash
npm run test:e2e
```

Ako želiš vidjeti browser:

```bash
npm run test:e2e:headed
```

Ako želiš Playwright UI:

```bash
npm run test:e2e:ui
```

## Pokretanje u Dockeru

Iz mape `PricalicaE2E`:

```bash
docker compose -f docker-compose.e2e.yml up --build --abort-on-container-exit playwright
```

Gašenje:

```bash
docker compose -f docker-compose.e2e.yml down -v
```

## Što testovi pokrivaju

- prijavu korisnika
- pretragu knjiga
- otvaranje detalja knjige
- uređivanje korisnika u admin dijelu
- brisanje korisnika uz potvrdu dijaloga
- prikaz greške ako API vrati problem
