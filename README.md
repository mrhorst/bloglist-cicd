# Bloglist CI/CD

A Full Stack Open Part 11 project focused on testing and deploying a small full-stack application through GitHub Actions.

The application has an Express and MongoDB backend, a React frontend, authentication, and API tests.

## Pipeline

On pull requests and pushes to `main`, the workflow:

1. Installs the backend and frontend dependencies
2. Builds the React frontend
3. Runs the backend test suite
4. Triggers a Render deployment after a successful push to `main`
5. Creates a patch release tag

Deployment can be skipped by including `#skip` in the commit message.

## Local development

Install both sets of dependencies:

```bash
npm install
npm --prefix frontend install
```

Run the backend in development:

```bash
npm run dev
```

Run the tests and build the frontend:

```bash
npm test
npm run build:frontend
```

The backend expects `MONGODB_URI` and `SECRET` environment variables.

## Course context

This repository contains my work for the CI/CD section of the University of Helsinki's Full Stack Open course. The rest of my course exercises are in [mrhorst/fullstackopen](https://github.com/mrhorst/fullstackopen).
