# Shopify QR Code Generator - Remix

The Shopify QR Code Generator App is a powerful tool that allows Shopify store owners to generate QR codes for various purposes, including product links, discounts, and more. This application is built using the Remix framework, ensuring a fast and responsive user experience.

This is a template for building a [Shopify app](https://shopify.dev/docs/apps/getting-started) using the [Remix](https://remix.run) framework.

<!-- TODO: Uncomment this after we've started using the template in the CLI -->
<img width="1439" alt="Screenshot 2023-09-27 at 01 38 35" src="https://github.com/richardwaters9049/QRGenerator/assets/119029825/322873c6-59cd-4a53-b66a-752b8237bc42">

<img width="1440" alt="Screenshot 2023-09-27 at 01 38 20" src="https://github.com/richardwaters9049/QRGenerator/assets/119029825/780ac7cc-0d32-4598-b3c7-8db6e86dfb54">

<!-- Rather than cloning this repo, you can use your preferred package manager and the Shopify CLI with [these steps](#installing-the-template). -->

## Quick Start

### Prerequisites

1. You must [download and install Node.js](https://nodejs.org/en/download/) if you don't already have it.
2. You must [create a Shopify partner account](https://partners.shopify.com/signup) if you don’t have one.
3. You must create a store for testing if you don't have one, either a [development store](https://help.shopify.com/en/partners/dashboard/development-stores#create-a-development-store) or a [Shopify Plus sandbox store](https://help.shopify.com/en/partners/dashboard/managing-stores/plus-sandbox-store).

<!-- TODO Make this section about using @shopify/app once it's added to the CLI. -->

### Setup

If you used the CLI to create the template, you can skip this section.

Using yarn:

```shell
yarn install
```

Using npm:

```shell
npm install
```

Using pnpm:

```shell
pnpm install
```

### Local Development

Using yarn:

```shell
yarn dev
```

Using npm:

```shell
npm run dev
```

Using pnpm:

```shell
pnpm run dev
```

Press P to open the URL to your app. Once you click install, you can start development.

Local development is powered by [the Shopify CLI](https://shopify.dev/docs/apps/tools/cli). It logs into your partners account, connects to an app, provides environment variables, updates remote config, creates a tunnel and provides commands to generate extensions.

## Deployment

### Application Storage

This template uses [Prisma](https://www.prisma.io/) to store session data, by default using an [SQLite](https://www.sqlite.org/index.html) database.
The database is defined as a Prisma schema in `prisma/schema.prisma`.

This use of SQLite works in production if your app runs as a single instance.
The database that works best for you depends on the data your app needs and how it is queried.
You can run your database of choice on a server yourself or host it with a SaaS company.
Here’s a short list of databases providers that provide a free tier to get started:

| Database   | Type             | Hosters                                                                                                                                                                                                                               |
| ---------- | ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| MySQL      | SQL              | [Digital Ocean](https://www.digitalocean.com/try/managed-databases-mysql), [Planet Scale](https://planetscale.com/), [Amazon Aurora](https://aws.amazon.com/rds/aurora/), [Google Cloud SQL](https://cloud.google.com/sql/docs/mysql) |
| PostgreSQL | SQL              | [Digital Ocean](https://www.digitalocean.com/try/managed-databases-postgresql), [Amazon Aurora](https://aws.amazon.com/rds/aurora/), [Google Cloud SQL](https://cloud.google.com/sql/docs/postgres)                                   |
| Redis      | Key-value        | [Digital Ocean](https://www.digitalocean.com/try/managed-databases-redis), [Amazon MemoryDB](https://aws.amazon.com/memorydb/)                                                                                                        |
| MongoDB    | NoSQL / Document | [Digital Ocean](https://www.digitalocean.com/try/managed-databases-mongodb), [MongoDB Atlas](https://www.mongodb.com/atlas/database)                                                                                                  |

To use one of these, you can use a different [datasource provider](https://www.prisma.io/docs/reference/api-reference/prisma-schema-reference#datasource) in your `schema.prisma` file, or a different [SessionStorage adapter package](https://github.com/Shopify/shopify-api-js/tree/main/docs/guides/session-storage.md).

### Build

Remix handles building the app for you, by running the command below with the package manager of your choice:

Using yarn:

```shell
yarn build
```

Using npm:

```shell
npm run build
```

Using pnpm:

```shell
pnpm run build
```

## Tech Stack

This template uses [Remix](https://remix.run). The following Shopify tools are also included to ease app development:

- [Shopify App Remix](https://github.com/Shopify/shopify-app-js/blob/main/packages/shopify-app-remix/README.md) provides authentication and methods for interacting with Shopify APIs.
- [Shopify App Bridge](https://shopify.dev/docs/apps/tools/app-bridge) allows your app to seamlessly integrate your app within Shopify's Admin.
- [Polaris React](https://polaris.shopify.com/) is a powerful design system and component library that helps developers build high quality, consistent experiences for Shopify merchants.
- [Webhooks](https://github.com/Shopify/shopify-app-js/tree/main/packages/shopify-app-remix#authenticating-webhook-requests): Callbacks sent by Shopify when certain events occur
- [Polaris](https://polaris.shopify.com/): Design system that enables apps to create Shopify-like experiences

> **Note**: This template runs on JavaScript, but it's fully set up for [TypeScript](https://www.typescriptlang.org/).
> If you want to create your routes using TypeScript, we recommend removing the `noImplicitAny` config from [`tsconfig.json`](/tsconfig.json)

## Resources

- [Remix Docs](https://remix.run/docs/en/v1)
- [Shopify App Remix](https://github.com/Shopify/shopify-app-js/blob/release-candidate/packages/shopify-app-remix/README.md)
- [Introduction to Shopify apps](https://shopify.dev/docs/apps/getting-started)
- [App authentication](https://shopify.dev/docs/apps/auth)
- [Shopify CLI](https://shopify.dev/docs/apps/tools/cli)
- [App extensions](https://shopify.dev/docs/apps/app-extensions/list)
- [Shopify Functions](https://shopify.dev/docs/api/functions)
- [Getting started with internationalizing your app](https://shopify.dev/docs/apps/best-practices/internationalization/getting-started)
