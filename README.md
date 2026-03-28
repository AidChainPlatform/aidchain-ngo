# AidChain NGO

AidChain NGO is the web portal used by NGO operators to manage campaigns, beneficiaries, vendors, market flows, and operational reporting inside the AidChain platform.

This repository is published as a clean portfolio snapshot. Project provenance is documented in [PROVENANCE.md](./PROVENANCE.md).

## What This App Does

- authenticates NGO users against the AidChain API
- displays campaign, beneficiary, and vendor management views
- supports market and cash-for-work workflows
- surfaces transaction and operational views for NGO teams
- provides account, support, and settings sections for tenant-level management

## Platform Position

```text
AidChain NGO (Nuxt web app)
          |
          v
       AidChain API
          |
          v
   AidChain Blockchain
```

## Tech Stack

- Nuxt 2
- Vue 2
- Vuex
- Axios
- Bootstrap / BootstrapVue
- Element UI
- Jest
- ESLint / Prettier

## Key Pages and Domains

The `pages/` directory includes working areas such as:

- `dashboard/`
- `projects/`
- `beneficiaries/`
- `vendors/`
- `market/`
- `cash-for-work/`
- `settings/`
- `account/`
- `support/`
- `sign-up/`

## Repository Layout

```text
pages/          route-based views
components/     reusable UI and domain components
store/          Vuex state management
middleware/     route guards and auth checks
plugins/        client plugins
assets/         styles and bundled assets
static/         static files
public/         public assets
api/            API integration helpers
utils/          shared utilities
```

## Prerequisites

- Node.js 16+ recommended for Nuxt 2 compatibility
- npm or yarn

## Installation

```bash
npm install
```

## Environment Setup

Create a local environment file before running the app.

Example:

```bash
BASE_URL=http://localhost:3000/v1
NUXT_PORT=3002
PAYSTACK_KEY=
GOOGLE_API=
RECAPTCHA_SITE_KEY=
```

The published snapshot excludes runtime `.env` files.

## Development

```bash
npm run dev
```

## Production Build

```bash
npm run build
npm run start
```

## Quality Checks

```bash
npm test
npm run lint
npm run lintfix
```

## Docker

The repo includes Docker assets for local or deployment packaging.

```bash
docker-compose up --build
```

## Integration Notes

This app relies on the AidChain API for authentication and all business data. In a full local stack, run it together with:

- `AidChainPlatform/aid-api`
- `AidChainPlatform/aidchain-blockchain`

## Notes

- The frontend reflects a multi-workflow NGO portal rather than a single dashboard screen.
- The published org repository is a clean snapshot without prior git history.
