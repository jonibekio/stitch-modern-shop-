# Stitch Modern Shop

> A Django e-commerce backend prototype with a partial storefront integration. This repository is not currently a complete, production-ready online shop.

## Overview

The codebase contains Django applications for catalog, accounts, cart, orders and related storefront workflows. The repository also contains a large checked-in Python virtual environment and a frontend gitlink whose source is not present in this checkout. Review those repository contents before attempting a full local setup.

## Current capabilities

- Django backend with product and account-related application modules.
- Cart and order data models and API routes.
- Docker and Compose configuration for local services.
- A small backend test suite; several tests are placeholders and do not establish end-to-end behavior.

Payment processing is not connected to a payment provider. The current code records application state and must not be treated as handling real payments. The frontend source is not available in this repository checkout.

## Technology

Python, Django, Django REST Framework, PostgreSQL-oriented configuration, Docker and Docker Compose. Confirm exact dependency versions in the backend requirements file.

## Architecture and layout

The backend is organized into Django apps for the shop's domains. Compose files describe local service orchestration. A frontend gitlink is present, but its submodule metadata/source is incomplete, so the UI cannot be reconstructed from this repository alone.

## Setup

1. Clone the repository and inspect its submodule status and Docker configuration.
2. Create a virtual environment and install dependencies from the backend requirements file.
3. Configure a local environment file using non-production values. Do not reuse credentials committed in repository history.
4. Start the configured database and application services, then apply Django migrations.

Exact commands and required variables depend on the checked-in Compose and settings files; verify them before running. The checked-in environment file contains credential material and should be treated as exposed.

## Configuration and API

The Django settings and Compose configuration define environment-dependent database and application settings. There is no reliable, verified API reference in the current repository documentation; inspect URL configuration and schema output in a local development instance before integrating clients.

## Data and tests

The backend uses Django models and a local SQLite database is tracked in the repository. The available tests include placeholders and do not verify checkout or payment workflows. No test results are claimed here.

## Deployment and security

Deployment is not documented as a validated production process. Before deployment, remove exposed credentials from active configuration, rotate any real values that have appeared in Git history, use secret storage, disable debug mode, configure allowed hosts, and implement provider-verified payment callbacks. Do not deploy this prototype for real transactions.

## Screenshots

No verified screenshots are available in this repository.

## Future work

- Restore and document the frontend source and its submodule metadata.
- Add reproducible dependency and environment setup.
- Replace local development defaults and remove generated artifacts from version control.
- Implement and test real payment-provider verification before enabling checkout.
- Add meaningful API and integration tests.
