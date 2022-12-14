# REST API App

Requirements: Node.js + Express.js

## Table of Contents

- [Demo Version](#demo-version)
- [Build and Run](#build-and-run)
- [Run Tests](#run-tests)
- [CI-CD](#ci-cd)
- [References](#references)

## Demo Version

Run locally with `ngrok`:

```bash
npm run tunnel
```

## Build and Run the App

### Locally:

```bash
npm install
npm start
```

### With Docker:

```bash
docker build -t api-rest .
docker run -m 512m --memory-reservation=256m -p 3000:3000 api-rest
```

## Run Tests

```bash
npm test
```

## CI-CD

### GitHub Actions

Tests are configured to run on multiple OS and Node.js versions to make sure the app is compatible across many platforms.

#### Test locally with `act`

```bash
act -j tests
```

### Deployment to Production Branch

If tests are passing, the CI with GitHub Actions pushes the changes to a production branch (`prod`).

## References

### Express.js API documentation:

https://expressjs.com/en/4x/api.html

### Ngrok

https://ngrok.com

### Base dockerfile created with:

https://github.com/vercel/next.js/tree/canary/examples/with-docker

### Test GitHub Actions Locally

https://github.com/nektos/act
