# WorkAround App

[![Netlify Status](https://api.netlify.com/api/v1/badges/d4dead3a-cb33-46f8-a1f2-6ad5c183aa99/deploy-status)](https://app.netlify.com/sites/app-workaround/deploys)
![Tests](https://github.com/WorkAroundHQ/app/actions/workflows/automated-tests.yml/badge.svg)
[![MPL-2.0 License](https://img.shields.io/badge/License-MPL--2.0-ffffff)](https://github.com/WorkAroundHQ/app/blob/main/LICENSE)
[![WorkAroundHQ](https://img.shields.io/twitter/follow/workaroundhq?label=Follow)](https://twitter.com/workaroundhq)

The WorkAround application is a platform for digital nomads who call the world their home. With WorkAround, digital nomads can pick their next ideal destination and connect with the community there.

## Run Locally

1. Clone repository:

```zsh
git clone git@github.com:WorkAroundHQ/app.git
```

2. Change directory:

```zsh
cd app
```

3. Install packages:

```zsh
yarn
```

3. Add values to `.env` file (see [`sample.env`](https://github.com/WorkAroundHQ/app/blob/main/sample.env))

4. Start development server:

```zsh
yarn start
```

## Automated Testing

Run automated tests:

> These tests also get executed with GitHub Actions on PRs onto `main`!

```zsh
yarn test
```

Run cypress tests:

1. Add values to `cypress.env.json` (see [`sample.cypress.env.json`](https://github.com/WorkAroundHQ/app/blob/main/sample.cypress.env.json))

2. Start development server:

```zsh
yarn start
```

3. Start cypress:

```zsh
yarn cy
```

4. Start test in Cypress app.

## Deployment

The deployment process is simple:

- Every push on `main` triggers a build on Netlify
- Every open pull request with target `main`, creates a deploy preview on Netlify

## Architecture

![WorkAround-Architecture](https://user-images.githubusercontent.com/28442090/141678851-3a1a180d-dc42-4088-9eaa-1dfde476df6e.jpg)

### Frontend

WorkAround is a Single Page Application developed with [`ReactJs`](https://reactjs.org) and [`SCSS`](https://sass-lang.com) as a CSS preprocessor.

### Hosting

WorkAround ist hosted on [`Netlify's`](https://www.netlify.com) CDN to provide fast loading times for users around the globe.

### Backend

[`Supabase`](https://supabase.io) provides three different services:
- Database
- Authentication / Authorization
- Storage

These services can be accessed via different REST endpoints, dynamically created by Supabase.

## Security Measures

Have a look on our [Security](https://github.com/WorkAroundHQ/app/blob/main/SECURITY.md) Measures.

## Feedback

If you have any feedback, please reach out to us [@WorkAroundHQ](https://twitter.com/workaroundhq)

## Authors

[@mrcgrhrdt](https://www.github.com/mrcgrhrdt)

## License

[Mozilla Public License Version 2.0](https://github.com/WorkAroundHQ/app/blob/main/LICENSE)

Made with ❤️ and ☕️
