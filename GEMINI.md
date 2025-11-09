# Design Rule
- Khi user nhắc đến shadcn hay frontend hay design hay ui, thì hãy vào ./src/components/ui để đọc trước (vì đây là baseui không phải radix). Chỉ được sử dụng component đã có sẵn trong ./src/components/ui. CẤM CÀI THÊM UI MỚI, thiếu gì thì nói
- User đã chạy `bun dev` ở port 3000, cấm chạy lại
- KHÔNG ĐƯỢC PHÉP SỬA HAY WRITE BẤT KÌ FILE NÀO NẾU USER CHƯA YÊU CẦU

4/11/2025

---
id: overview
title: TanStack Start Overview
---

> [!NOTE]
> TanStack Start is currently in the **Release Candidate** stage! This means it is considered feature-complete and its API is considered stable.
> **This does not mean it is bug-free or without issues, which is why we invite you to try it out and provide feedback!**
> The road to v1 will likely be a quick one, so don't wait too long to try it out!

TanStack Start is a full-stack React framework powered by TanStack Router. It provides a full-document SSR, streaming, server functions, bundling, and more. Thanks to [Vite](https://vite.dev/), it's ready to develop and deploy to any hosting provider or runtime you want!

## Dependencies

TanStack Start is built on two key technologies:

- **[TanStack Router](https://tanstack.com/router)**: A type-safe router for building web applications with advanced features like nested routing, search params, and data loading
- **[Vite](https://vite.dev/)**: A modern build tool that provides fast development with hot module replacement and optimized production builds

## Should I use TanStack Start or just TanStack Router?

90% of any framework usually comes down to the router, and TanStack Start is no different. **TanStack Start relies 100% on TanStack Router for its routing system.** In addition to TanStack Router's amazing features, Start enables even more powerful features:

- **Full-document SSR** - Server-side rendering for better performance and SEO
- **Streaming** - Progressive page loading for improved user experience
- **Server Routes & API Routes** - Build backend endpoints alongside your frontend
- **Server Functions** - Type-safe RPCs between client and server
- **Middleware & Context** - Powerful request/response handling and data injection
- **Full-Stack Bundling** - Optimized builds for both client and server code
- **Universal Deployment** - Deploy to any Vite-compatible hosting provider
- **End-to-End Type Safety** - Full TypeScript support across the entire stack

That said, if you **know with certainty** that you will not need any of the above features, then you may want to consider using TanStack Router alone, which is still a powerful and type-safe SPA routing upgrade over other routers and frameworks.

## Are there limitations?

The only relevant limitation is that TanStack Start does not currently support React Server Components, **but we are actively working on integration and expect to support them in the near future.**

Otherwise, TanStack Start provides the same capability as other full-stack frameworks like Next.js, Remix, etc, with even more features and a more powerful developer experience.

## How is TanStack Start funded?

TanStack is 100% open source, free to use, and always will be. It is built and maintained by an extremely talented and dedicated community of developers and software engineers. TanStack.com (also open source) is owned by TanStack LLC, a privately held company, 100% bootstrapped and self-funded. We are not venture-backed and have never sought investors. To support the development of TanStack Start and other TanStack libraries, TanStack.com partners with [these amazing companies](https://tanstack.com/partners?status=active&libraries=%5B%22start%22%5D) who offer both financial support and resources to help us continue to build the best possible developer experience for the web community:

<iframe src="https://tanstack.com/partners-embed" style="aspect-ratio: 1/2; width: 100%;"></iframe>

## Ready to get started?

Go to the next page to learn how to install TanStack Start and create your first app!
---
id: getting-started
title: Getting Started
---

## Migrate an existing project from another framework

- [Start a new project from scratch](#start-a-new-project-from-scratch) to quickly learn how Start works (see below)
- Refer to a migration guide for your specific framework:
  - [Next.js](../migrate-from-next-js)
  - Remix 2 / React Router 7 "Framework Mode" (coming soon!)

## Start a new project from scratch

Choose one of the following options to start building a _new_ TanStack Start project:

- [TanStack Start CLI](../quick-start) - Just run `npm create @tanstack/start@latest`. Local, fast, and optionally customizable
- [TanStack Builder](#) (coming soon!) - A visual interface to configure new TanStack projects with a few clicks
- [Quick Start Examples](../quick-start) Download or clone one of our official examples
- [Build a project from scratch](../build-from-scratch) - A guide to building a TanStack Start project line-by-line, file-by-file.

## Next Steps

Unless you chose to build a project from scratch, you can now move on to the [Routing](../guide/routing) guide to learn how to use TanStack Start!
---
id: quick-start
title: Quick Start
---

## Impatient?

The fastest way to get a Start project up and running is with the cli. Just run

```
pnpm create @tanstack/start@latest
```

or

```
npm create @tanstack/start@latest
```

depending on your package manage of choice. You'll be prompted to add things like Tailwind, eslint, and a ton of other options.

You can also clone and run the [Basic](https://github.com/TanStack/router/tree/main/examples/react/start-basic) example right away with the following commands:

```bash
npx gitpick TanStack/router/tree/main/examples/react/start-basic start-basic
cd start-basic
npm install
npm run dev
```

If you'd like to use a different example, you can replace `start-basic` above with the slug of the example you'd like to use from the list below.

Once you've cloned the example you want, head back to the [Routing](../guide/routing) guide to learn how to use TanStack Start!

## Examples

TanStack Start has load of examples to get you started. Pick one of the examples below to get started!

- [Basic](https://github.com/TanStack/router/tree/main/examples/react/start-basic) (start-basic)
- [Basic + Auth](https://github.com/TanStack/router/tree/main/examples/react/start-basic-auth) (start-basic-auth)
- [Counter](https://github.com/TanStack/router/tree/main/examples/react/start-counter) (start-counter)
- [Basic + React Query](https://github.com/TanStack/router/tree/main/examples/react/start-basic-react-query) (start-basic-react-query)
- [Clerk Auth](https://github.com/TanStack/router/tree/main/examples/react/start-clerk-basic) (start-clerk-basic)
- [Convex + Trellaux](https://github.com/TanStack/router/tree/main/examples/react/start-convex-trellaux) (start-convex-trellaux)
- [Supabase](https://github.com/TanStack/router/tree/main/examples/react/start-supabase-basic) (start-supabase-basic)
- [Trellaux](https://github.com/TanStack/router/tree/main/examples/react/start-trellaux) (start-trellaux)
- [WorkOS](https://github.com/TanStack/router/tree/main/examples/react/start-workos) (start-workos)
- [Material UI](https://github.com/TanStack/router/tree/main/examples/react/start-material-ui) (start-material-ui)

### Stackblitz

Each example above has an embedded stackblitz preview to find the one that feels like a good starting point

### Quick Deploy

To quickly deploy an example, click the **Deploy to Netlify** button on an example's page to both clone and deploy the example to Netlify.

### Manual Deploy

To manually clone and deploy the example to anywhere else you'd like, use the following commands replacing `EXAMPLE_SLUG` with the slug of the example you'd like to use from above:

```bash
npx gitpick TanStack/router/tree/main/examples/react/EXAMPLE_SLUG my-new-project
cd my-new-project
npm install
npm run dev
```

Once you've clone or deployed an example, head back to the [Routing](../guide/routing) guide to learn how to use TanStack Start!

## Other Router Examples

While not Start-specific examples, these may help you understand more about how TanStack Router works:

- [Quickstart (file-based)](https://github.com/TanStack/router/tree/main/examples/react/quickstart-file-based)
- [Basic (file-based)](https://github.com/TanStack/router/tree/main/examples/react/basic-file-based)
- [Kitchen Sink (file-based)](https://github.com/TanStack/router/tree/main/examples/react/kitchen-sink-file-based)
- [Kitchen Sink + React Query (file-based)](https://github.com/TanStack/router/tree/main/examples/react/kitchen-sink-react-query-file-based)
- [Location Masking](https://github.com/TanStack/router/tree/main/examples/react/location-masking)
- [Authenticated Routes](https://github.com/TanStack/router/tree/main/examples/react/authenticated-routes)
- [Scroll Restoration](https://github.com/TanStack/router/tree/main/examples/react/scroll-restoration)
- [Deferred Data](https://github.com/TanStack/router/tree/main/examples/react/deferred-data)
- [Navigation Blocking](https://github.com/TanStack/router/tree/main/examples/react/navigation-blocking)
- [View Transitions](https://github.com/TanStack/router/tree/main/examples/react/view-transitions)
- [With tRPC](https://github.com/TanStack/router/tree/main/examples/react/with-trpc)
- [With tRPC + React Query](https://github.com/TanStack/router/tree/main/examples/react/with-trpc-react-query)
---
id: build-from-scratch
title: Build a Project from Scratch
---

> [!NOTE]
> If you chose to quick start with an example or cloned project, you can skip this guide and move on to the [Routing](../guide/routing) guide.

_So you want to build a TanStack Start project from scratch?_

This guide will help you build a **very** basic TanStack Start web application. Together, we will use TanStack Start to:

- Serve an index page
- Display a counter
- Increment the counter on the server and client

[Here is what that will look like](https://stackblitz.com/github/tanstack/router/tree/main/examples/react/start-counter)

Let's create a new project directory and initialize it.

```shell
mkdir myApp
cd myApp
npm init -y
```

> [!NOTE] > We use `npm` in all of these examples, but you can use your package manager of choice instead.

## TypeScript Configuration

We highly recommend using TypeScript with TanStack Start. Create a `tsconfig.json` file with at least the following settings:

```json
{
  "compilerOptions": {
    "jsx": "react-jsx",
    "moduleResolution": "Bundler",
    "module": "ESNext",
    "target": "ES2022",
    "skipLibCheck": true,
    "strictNullChecks": true
  }
}
```

> [!NOTE] > Enabling `verbatimModuleSyntax` can result in server bundles leaking into client bundles. It is recommended to keep this option disabled.

## Install Dependencies

TanStack Start is powered by [Vite](https://vite.dev/) and [TanStack Router](https://tanstack.com/router) and requires them as dependencies.

To install them, run:

```shell
npm i @tanstack/react-start @tanstack/react-router
```

We also need vite as a devDependency:

```shell
npm i -D vite
```

You'll also need React:

```shell
npm i react react-dom
```

As well as React's Vite plugin:

```shell
npm i -D @vitejs/plugin-react
```

Alternatively, you can also use `@vitejs/plugin-react-oxc` or `@vitejs/plugin-react-swc`.

and some TypeScript:

```shell
npm i -D typescript @types/react @types/react-dom @types/node vite-tsconfig-paths
```

## Update Configuration Files

We'll then update our `package.json` to use Vite's CLI and set `"type": "module"`:

```json
{
  // ...
  "type": "module",
  "scripts": {
    "dev": "vite dev",
    "build": "vite build"
  }
}
```

Then configure TanStack Start's Vite plugin in `vite.config.ts`:

```ts
// vite.config.ts
import { defineConfig } from 'vite'
import tsConfigPaths from 'vite-tsconfig-paths'
import { tanstackStart } from '@tanstack/react-start/plugin/vite'
import viteReact from '@vitejs/plugin-react'

export default defineConfig({
  server: {
    port: 3000,
  },
  plugins: [
    tsConfigPaths(),
    tanstackStart(),
    // react's vite plugin must come after start's vite plugin
    viteReact(),
  ],
})
```

## Add the Basic Templating

There are 2 required files for TanStack Start usage:

1. The router configuration
2. The root of your application

Once configuration is done, we'll have a file tree that looks like the following:

```
.
├── src/
│   ├── routes/
│   │   └── `__root.tsx`
│   ├── `router.tsx`
│   ├── `routeTree.gen.ts`
├── `vite.config.ts`
├── `package.json`
└── `tsconfig.json`
```

## The Router Configuration

This is the file that will dictate the behavior of TanStack Router used within Start. Here, you can configure everything
from the default [preloading functionality](/router/latest/docs/framework/react/guide/preloading) to [caching staleness](/router/latest/docs/framework/react/guide/data-loading).

> [!NOTE]
> You won't have a `routeTree.gen.ts` file yet. This file will be generated when you run TanStack Start for the first time.

```tsx
// src/router.tsx
import { createRouter } from '@tanstack/react-router'
import { routeTree } from './routeTree.gen'

export function getRouter() {
  const router = createRouter({
    routeTree,
    scrollRestoration: true,
  })

  return router
}
```

## The Root of Your Application

Finally, we need to create the root of our application. This is the entry point for all other routes. The code in this file will wrap all other routes in the application.

```tsx
// src/routes/__root.tsx
/// <reference types="vite/client" />
import type { ReactNode } from 'react'
import {
  Outlet,
  createRootRoute,
  HeadContent,
  Scripts,
} from '@tanstack/react-router'

export const Route = createRootRoute({
  head: () => ({
    meta: [
      {
        charSet: 'utf-8',
      },
      {
        name: 'viewport',
        content: 'width=device-width, initial-scale=1',
      },
      {
        title: 'TanStack Start Starter',
      },
    ],
  }),
  component: RootComponent,
})

function RootComponent() {
  return (
    <RootDocument>
      <Outlet />
    </RootDocument>
  )
}

function RootDocument({ children }: Readonly<{ children: ReactNode }>) {
  return (
    <html>
      <head>
        <HeadContent />
      </head>
      <body>
        {children}
        <Scripts />
      </body>
    </html>
  )
}
```

## Writing Your First Route

Now that we have the basic templating setup, we can write our first route. This is done by creating a new file in the `src/routes` directory.

```tsx
// src/routes/index.tsx
import * as fs from 'node:fs'
import { createFileRoute, useRouter } from '@tanstack/react-router'
import { createServerFn } from '@tanstack/react-start'

const filePath = 'count.txt'

async function readCount() {
  return parseInt(
    await fs.promises.readFile(filePath, 'utf-8').catch(() => '0'),
  )
}

const getCount = createServerFn({
  method: 'GET',
}).handler(() => {
  return readCount()
})

const updateCount = createServerFn({ method: 'POST' })
  .inputValidator((d: number) => d)
  .handler(async ({ data }) => {
    const count = await readCount()
    await fs.promises.writeFile(filePath, `${count + data}`)
  })

export const Route = createFileRoute('/')({
  component: Home,
  loader: async () => await getCount(),
})

function Home() {
  const router = useRouter()
  const state = Route.useLoaderData()

  return (
    <button
      type="button"
      onClick={() => {
        updateCount({ data: 1 }).then(() => {
          router.invalidate()
        })
      }}
    >
      Add 1 to {state}?
    </button>
  )
}
```

That's it! 🤯 You've now set up a TanStack Start project and written your first route. 🎉

You can now run `npm run dev` to start your server and navigate to `http://localhost:3000` to see your route in action.

You want to deploy your application? Check out the [hosting guide](../guide/hosting.md).
---
id: migrate-from-next-js
title: Migrate from Next.js
---

This guide provides a step-by-step process to migrate a project from the Next.js App Router to **TanStack Start**. We respect the powerful features of Next.js and aim to make this transition as smooth as possible.

## Step-by-Step (Basics)

This step-by-step guide provides an overview of how to migrate your Next.js App Router project to TanStack Start. The goal is to help you understand the basic steps involved in the migration process so you can adapt them to your specific project needs.

### Prerequisites

Before we begin, this guide assumes your project structure looks like this:

```txt
├── next.config.ts
├── package.json
├── postcss.config.mjs
├── public
│   ├── file.svg
│   ├── globe.svg
│   ├── next.svg
│   ├── vercel.svg
│   └── window.svg
├── README.md
├── src
│   └── app
│       ├── favicon.ico
│       ├── globals.css
│       ├── layout.tsx
│       └── page.tsx
└── tsconfig.json
```

Alternatively, you can follow along by cloning the following [starter template](https://github.com/nrjdalal/awesome-templates/tree/main/next.js-apps/next.js-start):

```sh
npx gitpick nrjdalal/awesome-templates/tree/main/next.js-apps/next.js-start next.js-start-er
```

This structure is a basic Next.js application using the App Router, which we will migrate to TanStack Start.

### 1. Remove Next.js

First, uninstall Next.js and remove related configuration files:

```sh
npm uninstall @tailwindcss/postcss next
rm postcss.config.* next.config.*
```

### 2. Install Required Dependencies

TanStack Start leverages [Vite](https://vite.dev) and TanStack Router:

```sh
npm i @tanstack/react-router @tanstack/react-start
```

For Tailwind CSS and resolving imports using path aliases:

```sh
npm i -D vite @vitejs/plugin-react @tailwindcss/vite tailwindcss vite-tsconfig-paths
```

### 3. Update Project Configuration

Now that you've installed the necessary dependencies, update your project configuration files to work with TanStack Start.

- `package.json`

```json
{
  "type": "module",
  "scripts": {
    "dev": "vite dev",
    "build": "vite build",
    "start": "node .output/server/index.mjs"
  }
}
```

- `vite.config.ts`

```ts
// vite.config.ts
import { defineConfig } from 'vite'
import { tanstackStart } from '@tanstack/react-start/plugin/vite'
import viteReact from '@vitejs/plugin-react'
import tsconfigPaths from 'vite-tsconfig-paths'
import tailwindcss from '@tailwindcss/vite'

export default defineConfig({
  server: {
    port: 3000,
  },
  plugins: [
    tailwindcss(),
    // Enables Vite to resolve imports using path aliases.
    tsconfigPaths(),
    tanstackStart({
      srcDirectory: 'src', // This is the default
      router: {
        // Specifies the directory TanStack Router uses for your routes.
        routesDirectory: 'app', // Defaults to "routes", relative to srcDirectory
      },
    }),
    viteReact(),
  ],
})
```

By default, `routesDirectory` is set to `routes`. To maintain consistency with Next.js App Router conventions, you can set it to `app` instead.

### 4. Adapt the Root Layout

> TanStack Start uses a routing approach similar to Remix, with some changes to support nested structures and special features using tokens. Learn more about it at [Routing Concepts](/router/latest/docs/framework/react/routing/routing-concepts) guide.

Instead of `layout.tsx`, create a file named `__root.tsx` in the `src/app` directory. This file will serve as the root layout for your application.

- `src/app/layout.tsx` to `src/app/__root.tsx`

```tsx
- import type { Metadata } from "next" // [!code --]
import {
  Outlet,
  createRootRoute,
  HeadContent,
  Scripts,
} from "@tanstack/react-router"
import appCss from "./globals.css?url"

- export const metadata: Metadata = { // [!code --]
-   title: "Create Next App", // [!code --]
-   description: "Generated by create next app", // [!code --]
- } // [!code --]
export const Route = createRootRoute({
  head: () => ({
    meta: [
      { charSet: "utf-8" },
      {
        name: "viewport",
        content: "width=device-width, initial-scale=1",
      },
      { title: "TanStack Start Starter" }
    ],
    links: [
      {
        rel: 'stylesheet',
        href: appCss,
      },
    ],
  }),
  component: RootLayout,
})

- export default function RootLayout({ // [!code --]
-   children, // [!code --]
- }: Readonly<{ // [!code --]
-   children: React.ReactNode // [!code --]
- }>) { // [!code --]
-   return ( // [!code --]
-     <html lang="en"> // [!code --]
-       <body>{children}</body> // [!code --]
-     </html> // [!code --]
-   ) // [!code --]
- } // [!code --]
function RootLayout() {
  return (
    <html lang="en">
      <head>
        <HeadContent />
      </head>
      <body>
        <Outlet />
        <Scripts />
      </body>
    </html>
  )
}
```

### 5. Adapt the Home Page

Instead of `page.tsx`, create an `index.tsx` file for the `/` route.

- `src/app/page.tsx` to `src/app/index.tsx`

```tsx
+ import { createFileRoute } from '@tanstack/react-router' // [!code ++]

- export default function Home() { // [!code --]
+ export const Route = createFileRoute('/')({ // [!code ++]
+   component: Home, // [!code ++]
+ }) // [!code ++]

+ function Home() { // [!code ++]
  return (
    <main className="min-h-dvh w-screen flex items-center justify-center flex-col gap-y-4 p-4">
      <img
        className="max-w-sm w-full"
        src="https://raw.githubusercontent.com/TanStack/tanstack.com/main/public/images/logos/splash-dark.png"
        alt="TanStack Logo"
      />
      <h1>
        <span className="line-through">Next.js</span> TanStack Start
      </h1>
      <a
        className="bg-foreground text-background rounded-full px-4 py-1 hover:opacity-90"
        href="https://tanstack.com/start/latest"
        target="_blank"
      >
        Docs
      </a>
    </main>
  )
}
```

### 6. Are we migrated yet?

Before you can run the development server, you need to create a file that will define the behavior of TanStack Router within TanStack Start.

- `src/router.tsx`

```tsx
import { createRouter } from '@tanstack/react-router'
import { routeTree } from './routeTree.gen'

export function getRouter() {
  const router = createRouter({
    routeTree,
    scrollRestoration: true,
  })

  return router
}
```

> 🧠 Here you can configure everything from the default [preloading functionality](/router/latest/docs/framework/react/guide/preloading) to [caching staleness](/router/latest/docs/framework/react/guide/data-loading).

Don't worry if you see some TypeScript errors at this point; the next step will resolve them.

### 7. Verify the Migration

Run the development server:

```sh
npm run dev
```

Then, visit `http://localhost:3000`. You should see the TanStack Start welcome page with its logo and a documentation link.

> If you encounter issues, review the steps above and ensure that file names and paths match exactly. For a reference implementation, see the [post-migration repository](https://github.com/nrjdalal/next-to-start).

## Next Steps (Advanced)

Now that you have migrated the basic structure of your Next.js application to TanStack Start, you can explore more advanced features and concepts.

### Routing Concepts

| Route Example                  | Next.js                            | TanStack Start            |
| ------------------------------ | ---------------------------------- | ------------------------- |
| Root Layout                    | `src/app/layout.tsx`               | `src/app/__root.tsx`      |
| `/` (Home Page)                | `src/app/page.tsx`                 | `src/app/index.tsx`       |
| `/posts` (Static Route)        | `src/app/posts/page.tsx`           | `src/app/posts.tsx`       |
| `/posts/[slug]` (Dynamic)      | `src/app/posts/[slug]/page.tsx`    | `src/app/posts/$slug.tsx` |
| `/posts/[...slug]` (Catch-All) | `src/app/posts/[...slug]/page.tsx` | `src/app/posts/$.tsx`     |
| `/api/endpoint` (API Route)    | `src/app/api/endpoint/route.ts`    | `src/app/api/endpoint.ts` |

Learn more about the [Routing Concepts](/router/latest/docs/framework/react/routing/routing-concepts).

### Dynamic and Catch-All Routes

Retrieving dynamic route parameters in TanStack Start is straightforward.

```tsx
- export default async function Page({ // [!code --]
-   params, // [!code --]
- }: { // [!code --]
-   params: Promise<{ slug: string }> // [!code --]
- }) { // [!code --]
+ export const Route = createFileRoute('/app/posts/$slug')({ // [!code ++]
+   component: Page, // [!code ++]
+ }) // [!code ++]

+ function Page() { // [!code ++]
-   const { slug } = await params // [!code --]
+   const { slug } = Route.useParams() // [!code ++]
  return <div>My Post: {slug}</div>
}
```

> Note: If you've made a catch-all route (like `src/app/posts/$.tsx`), you can access the parameters via `const { _splat } = Route.useParams()`.

Similarly, you can access `searchParams` using `const { page, filter, sort } = Route.useSearch()`.

Learn more about the [Dynamic and Catch-All Routes](/router/latest/docs/framework/react/routing/routing-concepts#dynamic-route-segments).

### Links

```tsx
- import Link from "next/link" // [!code --]
+ import { Link } from "@tanstack/react-router" // [!code ++]

function Component() {
-   return <Link href="/dashboard">Dashboard</Link> // [!code --]
+   return <Link to="/dashboard">Dashboard</Link> // [!code ++]
}
```

Learn more about the [Links](/router/latest/docs/framework/react/guide/navigation#link-component).

### Images

Next.js uses the `next/image` component for optimized images. In TanStack Start, you can use the package called [Unpic](https://unpic.pics/) for similar functionality
and almost a drop-in replacement.

```tsx
import Image from 'next/image' // [!code --]
import { Image } from '@unpic/react' // [!code ++]
function Component() {
  return (
    <Image
      src="/path/to/image.jpg"
      alt="Description"
      width="600" // [!code --]
      height="400" // [!code --]
      width={600} // [!code ++]
      height={400} // [!code ++]
    />
  )
}
```

### Server ~Actions~ Functions

```tsx
- 'use server' // [!code --]
+ import { createServerFn } from "@tanstack/react-start" // [!code ++]

- export const create = async () => { // [!code --]
+ export const create = createServerFn().handler(async () => { // [!code ++]
  return true
- } // [!code --]
+ }) // [!code ++]
```

Learn more about the [Server Functions](../guide/server-functions).

### Server Routes ~Handlers~

```ts
- export async function GET() { // [!code --]
+ export const Route = createFileRoute('/api/hello')({ // [!code ++]
+  server: { // [!code ++]
+     handlers: { // [!code ++]
+       GET: async () => { // [!code ++]
+         return Response.json("Hello, World!")
+       } // [!code ++]
+    } // [!code ++]
+  } // [!code ++]
+ }) // [!code ++]
```

Learn more about the [Server Routes](../guide/server-routes).

### Fonts

```tsx
- import { Inter } from "next/font/google" // [!code --]

- const inter = Inter({ // [!code --]
-   subsets: ["latin"], // [!code --]
-   display: "swap", // [!code --]
- }) // [!code --]

- export default function Page() { // [!code --]
-   return <p className={inter.className}>Font Sans</p> // [!code --]
- } // [!code --]
```

Instead of `next/font`, use Tailwind CSS’s CSS-first approach. Install fonts (for example, from [Fontsource](https://github.com/fontsource/fontsource)):

```sh
npm i -D @fontsource-variable/dm-sans @fontsource-variable/jetbrains-mono
```

Add the following to `src/app/globals.css`:

```css
@import 'tailwindcss';

@import '@fontsource-variable/dm-sans'; /* [!code ++] */
@import '@fontsource-variable/jetbrains-mono'; /* [!code ++] */

@theme inline {
  --font-sans: 'DM Sans Variable', sans-serif; /* [!code ++] */
  --font-mono: 'JetBrains Mono Variable', monospace; /* [!code ++] */
  /* ... */
}

/* ... */
```

### Fetching Data

```tsx
- export default async function Page() { // [!code --]
+ export const Route = createFileRoute('/')({ // [!code ++]
+   component: Page, // [!code ++]
+   loader: async () => { // [!code ++]
+     const res = await fetch('https://api.vercel.app/blog') // [!code ++]
+     return res.json() // [!code ++]
+   }, // [!code ++]
+ }) // [!code ++]

+ function Page() { // [!code ++]
-   const data = await fetch('https://api.vercel.app/blog') // [!code --]
-   const posts = await data.json() // [!code --]
+   const posts = Route.useLoaderData() // [!code ++]

  return (
    <ul>
      {posts.map((post) => (
        <li key={post.id}>{post.title}</li>
      ))}
    </ul>
  )
}
```
---
id: routing
title: Routing
---

TanStack Start is built on top of TanStack Router, so all of the features of TanStack Router are available to you.

> [!NOTE]
> We highly recommend reading the [TanStack Router documentation](/router/latest/docs/framework/react/overview) to learn more about the features and capabilities of TanStack Router. What you learn here is more of a high-level overview of TanStack Router and how it works in Start.

## The Router

The `router.tsx` file is the file that will dictate the behavior of TanStack Router used within Start. It's located in the `src` directory of your project.

```
src/
├── router.tsx
```

Here, you can configure everything from the default [preloading functionality](/router/latest/docs/framework/react/guide/preloading) to [caching staleness](/router/latest/docs/framework/react/guide/data-loading).

```tsx
// src/router.tsx
import { createRouter } from '@tanstack/react-router'
import { routeTree } from './routeTree.gen'

// You must export a getRouter function that
// returns a new router instance each time
export function getRouter() {
  const router = createRouter({
    routeTree,
    scrollRestoration: true,
  })

  return router
}
```

## File-Based Routing

Start uses TanStack Router's file-based routing approach to ensure proper code-splitting and advanced type-safety.

You can find your routes in the `src/routes` directory.

```
src/
├── routes <-- This is where you put your routes
│   ├── __root.tsx
│   ├── index.tsx
│   ├── about.tsx
│   ├── posts.tsx
│   ├── posts/$postId.tsx
```

## The Root Route

The root route is the top-most route in the entire tree and encapsulates all other routes as children. It's found in the `src/routes/__root.tsx` file and must be named `__root.tsx`.

```
src/
├── routes
│   ├── __root.tsx <-- The root route
```

- It has no path and is **always** matched
- Its `component` is **always** rendered
- This is where you render your document shell, e.g. `<html>`, `<body>`, etc.
- Because it is **always rendered**, it is the perfect place to construct your application shell and take care of any global logic

```tsx
// src/routes/__root.tsx
import {
  Outlet,
  createRootRoute,
  HeadContent,
  Scripts,
} from '@tanstack/react-router'
import type { ReactNode } from 'react'

export const Route = createRootRoute({
  head: () => ({
    meta: [
      {
        charSet: 'utf-8',
      },
      {
        name: 'viewport',
        content: 'width=device-width, initial-scale=1',
      },
      {
        title: 'TanStack Start Starter',
      },
    ],
  }),
  component: RootComponent,
})

function RootComponent() {
  return (
    <RootDocument>
      <Outlet />
    </RootDocument>
  )
}

function RootDocument({ children }: Readonly<{ children: ReactNode }>) {
  return (
    <html>
      <head>
        <HeadContent />
      </head>
      <body>
        {children}
        <Scripts />
      </body>
    </html>
  )
}
```

Notice the `Scripts` component at the bottom of the `<body>` tag. This is used to load all of the client-side JavaScript for the application and should always be included for proper functionality.

## The HeadContent Component

The `HeadContent` component is used to render the head, title, meta, link, and head-related script tags of the document.

It should be **rendered in the `<head>` tag of your root route's layout.**

## The Outlet Component

The `Outlet` component is used to render the next potentially matching child route. `<Outlet />` doesn't take any props and can be rendered anywhere within a route's component tree. If there is no matching child route, `<Outlet />` will render `null`.

## The Scripts Component

The `Scripts` component is used to render the body scripts of the document.

It should be **rendered in the `<body>` tag of your root route's layout.**

## Route Tree Generation

You may notice a `routeTree.gen.ts` file in your project.

```
src/
├── routeTree.gen.ts <-- The generated route tree file
```

This file is automatically generated when you run TanStack Start (via `npm run dev` or `npm run start`). This file contains the generated route tree and a handful of TS utilities that make TanStack Start's type-safety extremely fast and fully inferred.

**You may gitignore this file, since it is a build artifact.**

## Nested Routing

TanStack Router uses nested routing to match the URL with the correct component tree to render.

For example, given the following routes:

```
routes/
├── __root.tsx <-- Renders the <Root> component
├── posts.tsx <-- Renders the <Posts> component
├── posts.$postId.tsx <-- Renders the <Post> component
```

And the URL: `/posts/123`

The component tree would look like this:

```
<Root>
  <Posts>
    <Post />
  </Posts>
</Root>
```

## Types of Routes

There are a few different types of routes that you can create in your project.

- Index Routes - Matched when the URL is exactly the same as the route's path
- Dynamic/Wildcard/Splat Routes - Dynamically capture part or all of the URL path into a variable to use in your application

There are also a few different utility route types that you can use to group and organize your routes

- Pathless Layout Routes (Apply layout or logic to a group of routes without nesting them in a path)
- Non-Nested Routes (Un-nest a route from its parents and render its own component tree)
- Grouped Routes (Group routes together in a directory simply for organization, without affecting the path hierarchy)

## Route Tree Configuration

The route tree is configured in the `src/routes` directory.

## Creating File Routes

To create a route, create a new file that corresponds to the path of the route you want to create. For example:

| Path             | Filename            | Type           |
| ---------------- | ------------------- | -------------- |
| `/`              | `index.tsx`         | Index Route    |
| `/about`         | `about.tsx`         | Static Route   |
|                  | `posts.tsx`         | "Layout" Route |
| `/posts/`        | `posts/index.tsx`   | Index Route    |
| `/posts/:postId` | `posts/$postId.tsx` | Dynamic Route  |
| `/rest/*`        | `rest/$.tsx`        | Wildcard Route |

## Defining Routes

To define a route, use the `createFileRoute` function to export the route as the `Route` variable.

For example, to handle the `/posts/:postId` route, you would create a file named `posts/$postId.tsx` here:

```
src/
├── routes
│   ├── posts/$postId.tsx
```

Then, define the route like this:

```tsx
// src/routes/posts/$postId.tsx
import { createFileRoute } from '@tanstack/react-router'

export const Route = createFileRoute('/posts/$postId')({
  component: PostComponent,
})
```

> [!NOTE]
> The path string passed to `createFileRoute` is **automatically written and managed by the router for you via the TanStack Router Bundler Plugin or Router CLI.** So, as you create new routes, move routes around or rename routes, the path will be updated for you automatically.

## This is just the "start"

This has been just a high-level overview of how to configure routes using TanStack Router. For more detailed information, please refer to the [TanStack Router documentation](/router/latest/docs/framework/react/routing/file-based-routing).
---
id: execution-model
title: Execution Model
---

Understanding where code runs is fundamental to building TanStack Start applications. This guide explains TanStack Start's execution model and how to control where your code executes.

## Core Principle: Isomorphic by Default

**All code in TanStack Start is isomorphic by default** - it runs and is included in both server and client bundles unless explicitly constrained.

```tsx
// ✅ This runs on BOTH server and client
function formatPrice(price: number) {
  return new Intl.NumberFormat('en-US', {
    style: 'currency',
    currency: 'USD',
  }).format(price)
}

// ✅ Route loaders are ISOMORPHIC
export const Route = createFileRoute('/products')({
  loader: async () => {
    // This runs on server during SSR AND on client during navigation
    const response = await fetch('/api/products')
    return response.json()
  },
})
```

> **Critical Understanding**: Route `loader`s are isomorphic - they run on both server and client, not just the server.

## The Execution Boundary

TanStack Start applications run in two environments:

### Server Environment

- **Node.js runtime** with access to file system, databases, environment variables
- **During SSR** - Initial page renders on server
- **API requests** - Server functions execute server-side
- **Build time** - Static generation and pre-rendering

### Client Environment

- **Browser runtime** with access to DOM, localStorage, user interactions
- **After hydration** - Client takes over after initial server render
- **Navigation** - Route loaders run client-side during navigation
- **User interactions** - Event handlers, form submissions, etc.

## Execution Control APIs

### Server-Only Execution

| API                      | Use Case                  | Client Behavior           |
| ------------------------ | ------------------------- | ------------------------- |
| `createServerFn()`       | RPC calls, data mutations | Network request to server |
| `createServerOnlyFn(fn)` | Utility functions         | Throws error              |

```tsx
import { createServerFn, createServerOnlyFn } from '@tanstack/react-start'

// RPC: Server execution, callable from client
const updateUser = createServerFn({ method: 'POST' })
  .inputValidator((data: UserData) => data)
  .handler(async ({ data }) => {
    // Only runs on server, but client can call it
    return await db.users.update(data)
  })

// Utility: Server-only, client crashes if called
const getEnvVar = createServerOnlyFn(() => process.env.DATABASE_URL)
```

### Client-Only Execution

| API                      | Use Case                        | Server Behavior  |
| ------------------------ | ------------------------------- | ---------------- |
| `createClientOnlyFn(fn)` | Browser utilities               | Throws error     |
| `<ClientOnly>`           | Components needing browser APIs | Renders fallback |

```tsx
import { createClientOnlyFn } from '@tanstack/react-start'
import { ClientOnly } from '@tanstack/react-router'

// Utility: Client-only, server crashes if called
const saveToStorage = createClientOnlyFn((key: string, value: any) => {
  localStorage.setItem(key, JSON.stringify(value))
})

// Component: Only renders children after hydration
function Analytics() {
  return (
    <ClientOnly fallback={null}>
      <GoogleAnalyticsScript />
    </ClientOnly>
  )
}
```

### Environment-Specific Implementations

```tsx
import { createIsomorphicFn } from '@tanstack/react-start'

// Different implementation per environment
const getDeviceInfo = createIsomorphicFn()
  .server(() => ({ type: 'server', platform: process.platform }))
  .client(() => ({ type: 'client', userAgent: navigator.userAgent }))
```

## Architectural Patterns

### Progressive Enhancement

Build components that work without JavaScript and enhance with client-side functionality:

```tsx
function SearchForm() {
  const [query, setQuery] = useState('')

  return (
    <form action="/search" method="get">
      <input
        name="q"
        value={query}
        onChange={(e) => setQuery(e.target.value)}
      />
      <ClientOnly fallback={<button type="submit">Search</button>}>
        <SearchButton onSearch={() => search(query)} />
      </ClientOnly>
    </form>
  )
}
```

### Environment-Aware Storage

```tsx
const storage = createIsomorphicFn()
  .server((key: string) => {
    // Server: File-based cache
    const fs = require('node:fs')
    return JSON.parse(fs.readFileSync('.cache', 'utf-8'))[key]
  })
  .client((key: string) => {
    // Client: localStorage
    return JSON.parse(localStorage.getItem(key) || 'null')
  })
```

### RPC vs Direct Function Calls

Understanding when to use server functions vs server-only functions:

```tsx
// createServerFn: RPC pattern - server execution, client callable
const fetchUser = createServerFn().handler(async () => await db.users.find())

// Usage from client component:
const user = await fetchUser() // ✅ Network request

// createServerOnlyFn: Crashes if called from client
const getSecret = createServerOnlyFn(() => process.env.SECRET)

// Usage from client:
const secret = getSecret() // ❌ Throws error
```

## Common Anti-Patterns

### Environment Variable Exposure

```tsx
// ❌ Exposes to client bundle
const apiKey = process.env.SECRET_KEY

// ✅ Server-only access
const apiKey = createServerOnlyFn(() => process.env.SECRET_KEY)
```

### Incorrect Loader Assumptions

```tsx
// ❌ Assuming loader is server-only
export const Route = createFileRoute('/users')({
  loader: () => {
    // This runs on BOTH server and client!
    const secret = process.env.SECRET // Exposed to client
    return fetch(`/api/users?key=${secret}`)
  },
})

// ✅ Use server function for server-only operations
const getUsersSecurely = createServerFn().handler(() => {
  const secret = process.env.SECRET // Server-only
  return fetch(`/api/users?key=${secret}`)
})

export const Route = createFileRoute('/users')({
  loader: () => getUsersSecurely(), // Isomorphic call to server function
})
```

### Hydration Mismatches

```tsx
// ❌ Different content server vs client
function CurrentTime() {
  return <div>{new Date().toLocaleString()}</div>
}

// ✅ Consistent rendering
function CurrentTime() {
  const [time, setTime] = useState<string>()

  useEffect(() => {
    setTime(new Date().toLocaleString())
  }, [])

  return <div>{time || 'Loading...'}</div>
}
```

## Manual vs API-Driven Environment Detection

```tsx
// Manual: You handle the logic
function logMessage(msg: string) {
  if (typeof window === 'undefined') {
    console.log(`[SERVER]: ${msg}`)
  } else {
    console.log(`[CLIENT]: ${msg}`)
  }
}

// API: Framework handles it
const logMessage = createIsomorphicFn()
  .server((msg) => console.log(`[SERVER]: ${msg}`))
  .client((msg) => console.log(`[CLIENT]: ${msg}`))
```

## Architecture Decision Framework

**Choose Server-Only when:**

- Accessing sensitive data (environment variables, secrets)
- File system operations
- Database connections
- External API keys

**Choose Client-Only when:**

- DOM manipulation
- Browser APIs (localStorage, geolocation)
- User interaction handling
- Analytics/tracking

**Choose Isomorphic when:**

- Data formatting/transformation
- Business logic
- Shared utilities
- Route loaders (they're isomorphic by nature)

## Security Considerations

### Bundle Analysis

Always verify server-only code isn't included in client bundles:

```bash
# Analyze client bundle
npm run build
# Check dist/client for any server-only imports
```

### Environment Variable Strategy

- **Client-exposed**: Use `VITE_` prefix for client-accessible variables
- **Server-only**: Access via `createServerOnlyFn()` or `createServerFn()`
- **Never expose**: Database URLs, API keys, secrets

### Error Boundaries

Handle server/client execution errors gracefully:

```tsx
function ErrorBoundary({ children }: { children: React.ReactNode }) {
  return (
    <ErrorBoundaryComponent
      fallback={<div>Something went wrong</div>}
      onError={(error) => {
        if (typeof window === 'undefined') {
          console.error('[SERVER ERROR]:', error)
        } else {
          console.error('[CLIENT ERROR]:', error)
        }
      }}
    >
      {children}
    </ErrorBoundaryComponent>
  )
}
```

Understanding TanStack Start's execution model is crucial for building secure, performant, and maintainable applications. The isomorphic-by-default approach provides flexibility while the execution control APIs give you precise control when needed.
---
id: code-execution-patterns
title: Code Execution Patterns
---

This guide covers patterns for controlling where code runs in your TanStack Start application - server-only, client-only, or isomorphic (both environments). For foundational concepts, see the [Execution Model](../execution-model.md) guide.

## Quick Start

Set up execution boundaries in your TanStack Start application:

```tsx
import {
  createServerFn,
  createServerOnlyFn,
  createClientOnlyFn,
  createIsomorphicFn,
} from '@tanstack/react-start'

// Server function (RPC call)
const getUsers = createServerFn().handler(async () => {
  return await db.users.findMany()
})

// Server-only utility (crashes on client)
const getSecret = createServerOnlyFn(() => process.env.API_SECRET)

// Client-only utility (crashes on server)
const saveToStorage = createClientOnlyFn((data: any) => {
  localStorage.setItem('data', JSON.stringify(data))
})

// Different implementations per environment
const logger = createIsomorphicFn()
  .server((msg) => console.log(`[SERVER]: ${msg}`))
  .client((msg) => console.log(`[CLIENT]: ${msg}`))
```

## Implementation Patterns

### Progressive Enhancement

```tsx
// Component works without JS, enhanced with JS
function SearchForm() {
  const [query, setQuery] = useState('')

  return (
    <form action="/search" method="get">
      <input
        name="q"
        value={query}
        onChange={(e) => setQuery(e.target.value)}
      />
      <ClientOnly fallback={<button type="submit">Search</button>}>
        <SearchButton onSearch={() => search(query)} />
      </ClientOnly>
    </form>
  )
}
```

### Environment-Aware Storage

```tsx
const storage = createIsomorphicFn()
  .server((key: string) => {
    // Server: File-based cache
    const fs = require('node:fs')
    return JSON.parse(fs.readFileSync('.cache', 'utf-8'))[key]
  })
  .client((key: string) => {
    // Client: localStorage
    return JSON.parse(localStorage.getItem(key) || 'null')
  })
```

## Common Problems

### Environment Variable Exposure

```tsx
// ❌ Exposes to client bundle
const apiKey = process.env.SECRET_KEY

// ✅ Server-only access
const apiKey = createServerOnlyFn(() => process.env.SECRET_KEY)
```

### Incorrect Loader Assumptions

```tsx
// ❌ Assuming loader is server-only
export const Route = createFileRoute('/users')({
  loader: () => {
    // This runs on BOTH server and client!
    const secret = process.env.SECRET // Exposed to client
    return fetch(`/api/users?key=${secret}`)
  },
})

// ✅ Use server function for server-only operations
const getUsersSecurely = createServerFn().handler(() => {
  const secret = process.env.SECRET // Server-only
  return fetch(`/api/users?key=${secret}`)
})

export const Route = createFileRoute('/users')({
  loader: () => getUsersSecurely(), // Isomorphic call to server function
})
```

### Hydration Mismatches

```tsx
// ❌ Different content server vs client
function CurrentTime() {
  return <div>{new Date().toLocaleString()}</div>
}

// ✅ Consistent rendering
function CurrentTime() {
  const [time, setTime] = useState<string>()

  useEffect(() => {
    setTime(new Date().toLocaleString())
  }, [])

  return <div>{time || 'Loading...'}</div>
}
```

## Production Checklist

- [ ] **Bundle Analysis**: Verify server-only code isn't in client bundle
- [ ] **Environment Variables**: Ensure secrets use `createServerOnlyFn()` or `createServerFn()`
- [ ] **Loader Logic**: Remember loaders are isomorphic, not server-only
- [ ] **ClientOnly Fallbacks**: Provide appropriate fallbacks to prevent layout shift
- [ ] **Error Boundaries**: Handle server/client execution errors gracefully

## Related Resources

- [Execution Model](../execution-model.md) - Core concepts and architectural patterns
- [Server Functions](../server-functions.md) - Deep dive into server function patterns
- [Environment Variables](../environment-variables.md) - Secure environment variable handling
- [Middleware](../middleware.md) - Server function middleware patterns
---
id: environment-variables
title: Environment Variables
---

Learn how to securely configure and use environment variables in your TanStack Start application across different contexts (server functions, client code, and build processes).

## Quick Start

TanStack Start automatically loads `.env` files and makes variables available in both server and client contexts with proper security boundaries.

```bash
# .env
DATABASE_URL=postgresql://user:pass@localhost:5432/mydb
VITE_APP_NAME=My TanStack Start App
```

```typescript
// Server function - can access any environment variable
const getUser = createServerFn().handler(async () => {
  const db = await connect(process.env.DATABASE_URL) // ✅ Server-only
  return db.user.findFirst()
})

// Client component - only VITE_ prefixed variables
export function AppHeader() {
  return <h1>{import.meta.env.VITE_APP_NAME}</h1> // ✅ Client-safe
}
```

## Environment Variable Contexts

### Server-Side Context (Server Functions & API Routes)

Server functions can access **any** environment variable using `process.env`:

```typescript
import { createServerFn } from '@tanstack/react-start'

// Database connection (server-only)
const connectToDatabase = createServerFn().handler(async () => {
  const connectionString = process.env.DATABASE_URL // No prefix needed
  const apiKey = process.env.EXTERNAL_API_SECRET // Stays on server

  // These variables are never exposed to the client
  return await database.connect(connectionString)
})

// Authentication (server-only)
const authenticateUser = createServerFn()
  .inputValidator(z.object({ token: z.string() }))
  .handler(async ({ data }) => {
    const jwtSecret = process.env.JWT_SECRET // Server-only
    return jwt.verify(data.token, jwtSecret)
  })
```

### Client-Side Context (Components & Client Code)

Client code can only access variables with the `VITE_` prefix:

```typescript
// Client configuration
export function ApiProvider({ children }: { children: React.ReactNode }) {
  const apiUrl = import.meta.env.VITE_API_URL     // ✅ Public
  const apiKey = import.meta.env.VITE_PUBLIC_KEY  // ✅ Public

  // This would be undefined (security feature):
  // const secret = import.meta.env.DATABASE_URL   // ❌ Undefined

  return (
    <ApiContext.Provider value={{ apiUrl, apiKey }}>
      {children}
    </ApiContext.Provider>
  )
}

// Feature flags
export function FeatureGatedComponent() {
  const enableNewFeature = import.meta.env.VITE_ENABLE_NEW_FEATURE === 'true'

  if (!enableNewFeature) return null

  return <NewFeature />
}
```

## Environment File Setup

### File Hierarchy (Loaded in Order)

TanStack Start automatically loads environment files in this order:

```
.env.local          # Local overrides (add to .gitignore)
.env.production     # Production-specific variables
.env.development    # Development-specific variables
.env                # Default variables (commit to git)
```

### Example Setup

**.env** (committed to repository):

```bash
# Public configuration
VITE_APP_NAME=My TanStack Start App
VITE_API_URL=https://api.example.com
VITE_SENTRY_DSN=https://...

# Server configuration templates
DATABASE_URL=postgresql://localhost:5432/myapp_dev
REDIS_URL=redis://localhost:6379
```

**.env.local** (add to .gitignore):

```bash
# Override for local development
DATABASE_URL=postgresql://user:password@localhost:5432/myapp_local
STRIPE_SECRET_KEY=sk_test_...
JWT_SECRET=your-local-secret
```

**.env.production**:

```bash
# Production overrides
VITE_API_URL=https://api.myapp.com
DATABASE_POOL_SIZE=20
```

## Common Patterns

### Database Configuration

```typescript
// src/lib/database.ts
import { createServerFn } from '@tanstack/react-start'

const getDatabaseConnection = createServerFn().handler(async () => {
  const config = {
    url: process.env.DATABASE_URL,
    maxConnections: parseInt(process.env.DB_MAX_CONNECTIONS || '10'),
    ssl: process.env.NODE_ENV === 'production',
  }

  return createConnection(config)
})
```

### Authentication Provider Setup

```typescript
// src/lib/auth.ts (Server)
export const authConfig = {
  secret: process.env.AUTH_SECRET,
  providers: {
    auth0: {
      domain: process.env.AUTH0_DOMAIN,
      clientId: process.env.AUTH0_CLIENT_ID,
      clientSecret: process.env.AUTH0_CLIENT_SECRET, // Server-only
    }
  }
}

// src/components/AuthProvider.tsx (Client)
export function AuthProvider({ children }: { children: React.ReactNode }) {
  return (
    <Auth0Provider
      domain={import.meta.env.VITE_AUTH0_DOMAIN}
      clientId={import.meta.env.VITE_AUTH0_CLIENT_ID}
      // No client secret here - it stays on the server
    >
      {children}
    </Auth0Provider>
  )
}
```

### External API Integration

```typescript
// src/lib/external-api.ts
import { createServerFn } from '@tanstack/react-start'

// Server-side API calls (can use secret keys)
const fetchUserData = createServerFn()
  .inputValidator(z.object({ userId: z.string() }))
  .handler(async ({ data }) => {
    const response = await fetch(
      `${process.env.EXTERNAL_API_URL}/users/${data.userId}`,
      {
        headers: {
          Authorization: `Bearer ${process.env.EXTERNAL_API_SECRET}`,
          'Content-Type': 'application/json',
        },
      },
    )

    return response.json()
  })

// Client-side API calls (public endpoints only)
export function usePublicData() {
  const apiUrl = import.meta.env.VITE_PUBLIC_API_URL

  return useQuery({
    queryKey: ['public-data'],
    queryFn: () => fetch(`${apiUrl}/public/stats`).then((r) => r.json()),
  })
}
```

### Feature Flags and Configuration

```typescript
// src/config/features.ts
export const featureFlags = {
  enableNewDashboard: import.meta.env.VITE_ENABLE_NEW_DASHBOARD === 'true',
  enableAnalytics: import.meta.env.VITE_ENABLE_ANALYTICS === 'true',
  debugMode: import.meta.env.VITE_DEBUG_MODE === 'true',
}

// Usage in components
export function Dashboard() {
  if (featureFlags.enableNewDashboard) {
    return <NewDashboard />
  }

  return <LegacyDashboard />
}
```

## Type Safety

### TypeScript Declarations

Create `src/env.d.ts` to add type safety:

```typescript
/// <reference types="vite/client" />

interface ImportMetaEnv {
  // Client-side environment variables
  readonly VITE_APP_NAME: string
  readonly VITE_API_URL: string
  readonly VITE_AUTH0_DOMAIN: string
  readonly VITE_AUTH0_CLIENT_ID: string
  readonly VITE_SENTRY_DSN?: string
  readonly VITE_ENABLE_NEW_DASHBOARD?: string
}

interface ImportMeta {
  readonly env: ImportMetaEnv
}

// Server-side environment variables
declare global {
  namespace NodeJS {
    interface ProcessEnv {
      readonly DATABASE_URL: string
      readonly REDIS_URL: string
      readonly JWT_SECRET: string
      readonly AUTH0_CLIENT_SECRET: string
      readonly STRIPE_SECRET_KEY: string
      readonly NODE_ENV: 'development' | 'production' | 'test'
    }
  }
}

export {}
```

### Runtime Validation

Use Zod for runtime validation of environment variables:

```typescript
// src/config/env.ts
import { z } from 'zod'

const envSchema = z.object({
  DATABASE_URL: z.string().url(),
  JWT_SECRET: z.string().min(32),
  NODE_ENV: z.enum(['development', 'production', 'test']),
})

const clientEnvSchema = z.object({
  VITE_APP_NAME: z.string(),
  VITE_API_URL: z.string().url(),
  VITE_AUTH0_DOMAIN: z.string(),
  VITE_AUTH0_CLIENT_ID: z.string(),
})

// Validate server environment
export const serverEnv = envSchema.parse(process.env)

// Validate client environment
export const clientEnv = clientEnvSchema.parse(import.meta.env)
```

## Security Best Practices

### 1. Never Expose Secrets to Client

```typescript
// ❌ WRONG - Secret exposed to client bundle
const config = {
  apiKey: import.meta.env.VITE_SECRET_API_KEY, // This will be in your JS bundle!
}

// ✅ CORRECT - Keep secrets on server
const getApiData = createServerFn().handler(async () => {
  const response = await fetch(apiUrl, {
    headers: { Authorization: `Bearer ${process.env.SECRET_API_KEY}` },
  })
  return response.json()
})
```

### 2. Use Appropriate Prefixes

```bash
# ✅ Server-only (no prefix)
DATABASE_URL=postgresql://...
JWT_SECRET=super-secret-key
STRIPE_SECRET_KEY=sk_live_...

# ✅ Client-safe (VITE_ prefix)
VITE_APP_NAME=My App
VITE_API_URL=https://api.example.com
VITE_SENTRY_DSN=https://...
```

### 3. Validate Required Variables

```typescript
// src/config/validation.ts
const requiredServerEnv = ['DATABASE_URL', 'JWT_SECRET'] as const

const requiredClientEnv = ['VITE_APP_NAME', 'VITE_API_URL'] as const

// Validate on server startup
for (const key of requiredServerEnv) {
  if (!process.env[key]) {
    throw new Error(`Missing required environment variable: ${key}`)
  }
}

// Validate client environment at build time
for (const key of requiredClientEnv) {
  if (!import.meta.env[key]) {
    throw new Error(`Missing required environment variable: ${key}`)
  }
}
```

## Production Checklist

- [ ] All sensitive variables are server-only (no `VITE_` prefix)
- [ ] Client variables use `VITE_` prefix
- [ ] `.env.local` is in `.gitignore`
- [ ] Production environment variables are configured on hosting platform
- [ ] Required environment variables are validated at startup
- [ ] No hardcoded secrets in source code
- [ ] Database URLs use connection pooling in production
- [ ] API keys are rotated regularly

## Common Problems

### Environment Variable is Undefined

**Problem**: `import.meta.env.MY_VARIABLE` returns `undefined`

**Solutions**:

1. **Add correct prefix**: Use `VITE_` prefix (e.g. `VITE_MY_VARIABLE`)
2. **Restart development server** after adding new variables
3. **Check file location**: `.env` file must be in project root
4. **Verify bundler configuration**: Ensure variables are properly injected

**Example**:

```bash
# ❌ Won't work in client code
API_KEY=abc123

# ✅ Works in client code
VITE_API_KEY=abc123

# ❌ Won't bundle the variable (assuming it is not set in the environment of the build)
npm run build

# ✅ Works in client code and will bundle the variable for production
VITE_API_KEY=abc123 npm run build
```

### Runtime Client Environment Variables in Production

**Problem**: If `VITE_` variables are replaced at bundle time only, how to make runtime variables available on the client?

**Solutions**:

Pass variables from the server down to the client:

```tsx
const getRuntimeVar = createServerFn({ method: 'GET' }).handler(() => {
  return process.env.MY_RUNTIME_VAR // notice `process.env` on the server, and no `VITE_` prefix
})

export const Route = createFileRoute('/')({
  loader: async () => {
    const foo = await getRuntimeVar()
    return { foo }
  },
  component: RouteComponent,
})

function RouteComponent() {
  const { foo } = Route.useLoaderData()
  // ... use your variable however you want
}
```

### Variable Not Updating

**Problem**: Environment variable changes aren't reflected

**Solutions**:

1. Restart development server
2. Check if you're modifying the correct `.env` file
3. Verify file hierarchy (`.env.local` overrides `.env`)

### TypeScript Errors

**Problem**: `Property 'VITE_MY_VAR' does not exist on type 'ImportMetaEnv'`

**Solution**: Add to `src/env.d.ts`:

```typescript
interface ImportMetaEnv {
  readonly VITE_MY_VAR: string
}
```

### Security: Secret Exposed to Client

**Problem**: Sensitive data appearing in client bundle

**Solutions**:

1. Remove `VITE_` prefix from sensitive variables
2. Move sensitive operations to server functions
3. Use build tools to verify no secrets in client bundle

### Build Errors in Production

**Problem**: Missing environment variables in production build

**Solutions**:

1. Configure variables on hosting platform
2. Validate required variables at build time
3. Use deployment-specific `.env` files

## Related Resources

- [Code Execution Patterns](../code-execution-patterns.md) - Learn about server vs client code execution
- [Server Functions](../server-functions.md) - Learn more about server-side code
- [Hosting](../hosting.md) - Platform-specific environment variable configuration
- [Vite Environment Variables](https://vitejs.dev/guide/env-and-mode.html) - Official Vite documentation
---
id: server-functions
title: Server Functions
---

## What are Server Functions?

Server functions let you define server-only logic that can be called from anywhere in your application - loaders, components, hooks, or other server functions. They run on the server but can be invoked from client code seamlessly.

```tsx
import { createServerFn } from '@tanstack/react-start'

export const getServerTime = createServerFn().handler(async () => {
  // This runs only on the server
  return new Date().toISOString()
})

// Call from anywhere - components, loaders, hooks, etc.
const time = await getServerTime()
```

Server functions provide server capabilities (database access, environment variables, file system) while maintaining type safety across the network boundary.

## Basic Usage

Server functions are created with `createServerFn()` and can specify HTTP method:

```tsx
import { createServerFn } from '@tanstack/react-start'

// GET request (default)
export const getData = createServerFn().handler(async () => {
  return { message: 'Hello from server!' }
})

// POST request
export const saveData = createServerFn({ method: 'POST' }).handler(async () => {
  // Server-only logic
  return { success: true }
})
```

## Where to Call Server Functions

Call server functions from:

- **Route loaders** - Perfect for data fetching
- **Components** - Use with `useServerFn()` hook
- **Other server functions** - Compose server logic
- **Event handlers** - Handle form submissions, clicks, etc.

```tsx
// In a route loader
export const Route = createFileRoute('/posts')({
  loader: () => getPosts(),
})

// In a component
function PostList() {
  const getPosts = useServerFn(getServerPosts)

  const { data } = useQuery({
    queryKey: ['posts'],
    queryFn: () => getPosts(),
  })
}
```

## Parameters & Validation

Server functions accept a single `data` parameter. Since they cross the network boundary, validation ensures type safety and runtime correctness.

### Basic Parameters

```tsx
import { createServerFn } from '@tanstack/react-start'

export const greetUser = createServerFn({ method: 'GET' })
  .inputValidator((data: { name: string }) => data)
  .handler(async ({ data }) => {
    return `Hello, ${data.name}!`
  })

await greetUser({ data: { name: 'John' } })
```

### Validation with Zod

For robust validation, use schema libraries like Zod:

```tsx
import { createServerFn } from '@tanstack/react-start'
import { z } from 'zod'

const UserSchema = z.object({
  name: z.string().min(1),
  age: z.number().min(0),
})

export const createUser = createServerFn({ method: 'POST' })
  .inputValidator(UserSchema)
  .handler(async ({ data }) => {
    // data is fully typed and validated
    return `Created user: ${data.name}, age ${data.age}`
  })
```

### Form Data

Handle form submissions with FormData:

```tsx
export const submitForm = createServerFn({ method: 'POST' })
  .inputValidator((data) => {
    if (!(data instanceof FormData)) {
      throw new Error('Expected FormData')
    }

    return {
      name: data.get('name')?.toString() || '',
      email: data.get('email')?.toString() || '',
    }
  })
  .handler(async ({ data }) => {
    // Process form data
    return { success: true }
  })
```

## Error Handling & Redirects

Server functions can throw errors, redirects, and not-found responses that are handled automatically when called from route lifecycles or components using `useServerFn()`.

### Basic Errors

```tsx
import { createServerFn } from '@tanstack/react-start'

export const riskyFunction = createServerFn().handler(async () => {
  if (Math.random() > 0.5) {
    throw new Error('Something went wrong!')
  }
  return { success: true }
})

// Errors are serialized to the client
try {
  await riskyFunction()
} catch (error) {
  console.log(error.message) // "Something went wrong!"
}
```

### Redirects

Use redirects for authentication, navigation, etc:

```tsx
import { createServerFn } from '@tanstack/react-start'
import { redirect } from '@tanstack/react-router'

export const requireAuth = createServerFn().handler(async () => {
  const user = await getCurrentUser()

  if (!user) {
    throw redirect({ to: '/login' })
  }

  return user
})
```

### Not Found

Throw not-found errors for missing resources:

```tsx
import { createServerFn } from '@tanstack/react-start'
import { notFound } from '@tanstack/react-router'

export const getPost = createServerFn()
  .inputValidator((data: { id: string }) => data)
  .handler(async ({ data }) => {
    const post = await db.findPost(data.id)

    if (!post) {
      throw notFound()
    }

    return post
  })
```

## Advanced Topics

For more advanced server function patterns and features, see these dedicated guides:

### Server Context & Request Handling

Access request headers, cookies, and response customization:

- `getRequest()` - Access the full request object
- `getRequestHeader()` - Read specific headers
- `setResponseHeader()` - Set custom response headers
- `setResponseStatus()` - Custom status codes

### Streaming

Stream typed data from server functions to the client. See the [Streaming Data from Server Functions guide](../streaming-data-from-server-functions).

### Raw Responses

Return `Response` objects binary data, or custom content types.

### Progressive Enhancement

Use server functions without JavaScript by leveraging the `.url` property with HTML forms.

### Middleware

Compose server functions with middleware for authentication, logging, and shared logic. See the [Middleware guide](../middleware.md).

### Static Server Functions

Cache server function results at build time for static generation. See [Static Server Functions](../static-server-functions).

### Request Cancellation

Handle request cancellation with `AbortSignal` for long-running operations.

### Function ID generation for production build

Server functions are addressed by a generated, stable function ID under the hood. These IDs are embedded into the client/SSR builds and used by the server to locate and import the correct module at runtime.

By default, IDs are SHA256 hashes of the same seed to keep bundles compact and avoid leaking file paths.
If two server functions end up with the same ID (including when using a custom generator), the system de-duplicates by appending an incrementing suffix like `_1`, `_2`, etc.

Customization:

You can customize function ID generation for the production build by providing a `generateFunctionId` function when configuring the TanStack Start Vite plugin.

Prefer deterministic inputs (filename + functionName) so IDs remain stable between builds.

Please note that this customization is **experimental** und subject to change.

Example:

```ts
// vite.config.ts
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'
import { tanstackStart } from '@tanstack/react-start/plugin/vite'

export default defineConfig({
  plugins: [
    tanstackStart({
      serverFns: {
        generateFunctionId: ({ filename, functionName }) => {
          // Return a custom ID string. If you return undefined, the default is used.
          return crypto
            .createHash('sha1')
            .update(`${filename}--${functionName}`)
            .digest('hex')
          return undefined
        },
      },
    }),
    react(),
  ],
})
```

---

> **Note**: Server functions use a compilation process that extracts server code from client bundles while maintaining seamless calling patterns. On the client, calls become `fetch` requests to the server.
---
id: static-server-functions
title: Static Server Functions
---

> [!WARNING]
> Static Server Functions are experimental!

## What are Static Server Functions?

Static server functions are server functions that are executed at build time and cached as static assets when using prerendering/static-generation. They can be set to "static" mode by applying the `staticFunctionMiddleware` middleware to `createServerFn`:

```tsx
import { createServerFn } from '@tanstack/react-start'
import { staticFunctionMiddleware } from '@tanstack/start-static-server-functions'

const myServerFn = createServerFn({ method: 'GET' })
  .middleware([staticFunctionMiddleware])
  .handler(async () => {
    return 'Hello, world!'
  })
```

Ensure that `staticFunctionMiddleware` is the final middleware!

This pattern goes as follows:

- Build-time
  - During build-time prerendering, a server function with `staticFunctionMiddleware` is executed
  - The result is cached with your build output as a static JSON file under a derived key (function ID + params/payload hash)
  - The result is returned as normal during prerendering/static-generation and used to prerender the page
- Runtime
  - Initially, the prerendered page's html is served and the server function data is embedded in the html
  - When the client mounts, the embedded server function data is hydrated
  - For future client-side invocations, the server function is replaced with a fetch call to the static JSON file
---
id: environment-functions
title: Environment Functions
---

## What Are Environment Functions?

Environment functions are utilities designed to define and control function execution based on the runtime environment—whether the code is running on the client or the server. These utilities help ensure that environment-specific logic is executed safely and intentionally, preventing runtime errors and improving maintainability in fullstack or isomorphic applications.

Start provides three core environment functions:

- `createIsomorphicFn`: Compose a single function that adapts to both client and server environments.
- `createServerOnlyFn`: Create a function that can only run on the server.
- `createClientOnlyFn`: Create a function that can only run on the client.

---

## Isomorphic Functions

Use `createIsomorphicFn()` to define functions that behave differently depending on whether they are called on the client or the server. This is useful for safely sharing logic across environments while delegating environment-specific behavior to appropriate handlers.

### Complete Implementation

```tsx
import { createIsomorphicFn } from '@tanstack/react-start'

const getEnv = createIsomorphicFn()
  .server(() => 'server')
  .client(() => 'client')

const env = getEnv()
// ℹ️ On the **server**, it returns `'server'`.
// ℹ️ On the **client**, it returns `'client'`.
```

### Partial Implementation (Server)

Here is an example of `createIsomorphicFn()` with only server implementation:

```tsx
import { createIsomorphicFn } from '@tanstack/react-start'

const serverImplementationOnly = createIsomorphicFn().server(() => 'server')

const server = serverImplementationOnly()
// ℹ️ On the **server**, it returns `'server'`.
// ℹ️ On the **client**, it is no-op (returns `undefined`)
```

### Partial Implementation (Client)

Here is an example of `createIsomorphicFn()` with only client implementation:

```tsx
import { createIsomorphicFn } from '@tanstack/react-start'

const clientImplementationOnly = createIsomorphicFn().client(() => 'client')

const client = clientImplementationOnly()
// ℹ️ On the **server**, it is no-op (returns `undefined`)
// ℹ️ On the **client**, it returns `'client'`.
```

### No Implementation

Here is an example of `createIsomorphicFn()` without any environment specific implementation:

```tsx
import { createIsomorphicFn } from '@tanstack/react-start'

const noImplementation = createIsomorphicFn()

const noop = noImplementation()
// ℹ️ On both **client** and **server**, it is no-op (returns `undefined`)
```

#### What is a no-op?

A no-op (short for "no operation") is a function that does nothing when executed - it simply returns `undefined` without performing any operations.

```tsx
// basic no-op implementation
function noop() {}
```

---

## `env`Only Functions

The `createServerOnlyFn` and `createClientOnlyFn` helpers enforce strict environment-bound execution. They ensure the returned function is only callable in the correct runtime context. If misused, they throw descriptive runtime errors to prevent unintentional logic execution.

### `createServerOnlyFn`

```tsx
import { createServerOnlyFn } from '@tanstack/react-start'

const foo = createServerOnlyFn(() => 'bar')

foo() // ✅ On server: returns "bar"
// ❌ On client: throws "createServerOnlyFn() functions can only be called on the server!"
```

### `createClientOnlyFn`

```tsx
import { createClientOnlyFn } from '@tanstack/react-start'

const foo = createClientOnlyFn(() => 'bar')

foo() // ✅ On client: returns "bar"
// ❌ On server: throws "createClientOnlyFn() functions can only be called on the client!"
```

> [!NOTE]
> These functions are useful for API access, filesystem reads, using browser APIs, or other operations that are invalid or insecure outside their intended environment.

## Tree Shaking

Environment functions are tree-shaken based on the environment for each bundle produced.

Functions created using `createIsomorphicFn()` are tree-shaken. All codes inside `.client()` are not included in server bundle, and vice-versa.

On the server, functions created using `createClientOnlyFn()` are replaced with a function that throws an `Error` on the server. The reverse is true for `createServerOnlyFn` functions on the client.
---
id: middleware
title: Middleware
---

## What is Middleware?

Middleware allows you to customize the behavior of both server routes like GET/POST/etc (including requests to SSR your application) and server functions created with `createServerFn`. Middleware is composable and can even depend on other middleware to create a chain of operations that are executed hierarchically and in order.

### What kinds of things can I do with Middleware?

- **Authentication**: Verify a user's identity before executing a server function.
- **Authorization**: Check if a user has the necessary permissions to execute a server function.
- **Logging**: Log requests, responses, and errors.
- **CSP**: Configure Content Security Policy and other security measures.
- **Observability**: Collect metrics, traces, and logs.
- **Provide Context**: Attach data to the request object for use in other middleware or server functions.
- **Error Handling**: Handle errors in a consistent way.
- And many more! The possibilities are up to you!

## Middleware Types

There are two types of middleware: **request middleware** and **server function middleware**.

- **Request middleware** is used to customize the behavior of any server request that passes through it, including server functions.
- **Server function middleware** is used to customize the behavior of server functions specifically.

> [!NOTE]
> Server function middleware is a subset of request middleware that has extra functionality specifically for server functions like being able to validate input data or perform client-side logic both before and after the server function is executed.

### Key Differences

| Feature           | Request Middleware               | Server Function Middleware |
| ----------------- | -------------------------------- | -------------------------- |
| Scope             | All server requests              | Server functions only      |
| Methods           | `.server()`                      | `.client()`, `.server()`   |
| Input Validation  | No                               | Yes (`.inputValidator()`)  |
| Client-side Logic | No                               | Yes                        |
| Dependencies      | Can depend on request middleware | Can depend on both types   |

> [!NOTE]
> Request middleware cannot depend on server function middleware, but server function middleware can depend on request middleware.

## Core Concepts

### Middleware Composition

All middleware is composable, which means that one middleware can depend on another middleware.

```tsx
import { createMiddleware } from '@tanstack/react-start'

const loggingMiddleware = createMiddleware().server(() => {
  //...
})

const authMiddleware = createMiddleware()
  .middleware([loggingMiddleware])
  .server(() => {
    //...
  })
```

### Progressing the Middleware Chain

Middleware is next-able, which means that you must call the `next` function in the `.server` method (and/or `.client` method if you are creating a server function middleware) to execute the next middleware in the chain. This allows you to:

- Short circuit the middleware chain and return early
- Pass data to the next middleware
- Access the result of the next middleware
- Pass context to the wrapping middleware

```tsx
import { createMiddleware } from '@tanstack/react-start'

const loggingMiddleware = createMiddleware().server(async ({ next }) => {
  const result = await next() // <-- This will execute the next middleware in the chain
  return result
})
```

## Request Middleware

Request middleware is used to customize the behavior of any server request that passes through it, including server routes, SSR and server functions.

To create a request middleware, call the `createMiddleware` function. You may call this function with the `type` property set to 'request', but this is the default value so you can omit it if you'd like.

```tsx
import { createMiddleware } from '@tanstack/react-start'

const loggingMiddleware = createMiddleware().server(() => {
  //...
})
```

### Available Methods

Request middleware has the following methods:

- `middleware`: Add a middleware to the chain.
- `server`: Define server-side logic that the middleware will execute before any nested middleware and ultimately a server function, and also provide the result to the next middleware.

### The `.server` method

The `.server` method is used to define server-side logic that the middleware will execute before any nested middleware, and also provide the result to the next middleware. It receives the `next` method and other things like context and the request object:

```tsx
import { createMiddleware } from '@tanstack/react-start'

const loggingMiddleware = createMiddleware().server(
  ({ next, context, request }) => {
    return next()
  },
)
```

To quickly visualize this handshake, here is a diagram:

```mermaid
sequenceDiagram
  HTTP ->> Middleware.server: Request
  Middleware.server ->> Middleware.server: next()
  Middleware.server ->> ServerFn: payload
  ServerFn ->> Middleware.server: result
  Middleware.server ->> Middleware.server: return
  Middleware.server ->> HTTP: Response

  box Server
  participant Middleware.server
  participant ServerFn
  end
```

### Using Request Middleware with Server Routes

You can use request middleware with server routes in two ways:

#### All Server Route Methods

To have a server route use middleware for all methods, pass a middleware array to the `middleware` property of the method builder object.

```tsx
import { createMiddleware } from '@tanstack/react-start'

const loggingMiddleware = createMiddleware().server(() => {
  //...
})

export const Route = createFileRoute('/foo')({
  server: {
    middleware: [loggingMiddleware],
    handlers: {
      GET: () => {
        //...
      },
      POST: () => {
        //...
      },
    },
  },
})
```

#### Specific Server Route Methods

You can pass middleware to specific server route methods by using the `createHandlers` utility and passing a middleware array to the `middleware` property of the method object.

```tsx
const loggingMiddleware = createMiddleware().server(() => {
  //...
})

export const Route = createFileRoute('/foo')({
  server: {
    handlers: ({ createHandlers }) =>
      createHandlers({
        GET: {
          middleware: [loggingMiddleware],
          handler: () => {
            //...
          },
        },
      }),
  },
})
```

## Server Function Middleware

Server function middleware is a **subset** of request middleware that has extra functionality specifically for server functions like being able to validate input data or perform client-side logic both before and after the server function is executed.

To create a server function middleware, call the `createMiddleware` function with the `type` property set to 'function'.

```tsx
import { createMiddleware } from '@tanstack/react-start'

const loggingMiddleware = createMiddleware({ type: 'function' })
  .client(() => {
    //...
  })
  .server(() => {
    //...
  })
```

### Available Methods

Server function middleware has the following methods:

- `middleware`: Add a middleware to the chain.
- `inputValidator`: Modify the data object before it is passed to this middleware and any nested middleware and eventually the server function.
- `client`: Define client-side logic that the middleware will execute on the client before (and after) the server function calls into the server to execute the function.
- `server`: Define server-side logic that the middleware will execute on the server before (and after) the server function is executed.

> [!NOTE]
> If you are (hopefully) using TypeScript, the order of these methods is enforced by the type system to ensure maximum inference and type safety.

### The `.client` method

The `.client` method is used to define client-side logic that the middleware will wrap the execution and result of the RPC call to the server.

```tsx
import { createMiddleware } from '@tanstack/react-start'

const loggingMiddleware = createMiddleware({ type: 'function' }).client(
  async ({ next, context, request }) => {
    const result = await next() // <-- This will execute the next middleware in the chain and eventually, the RPC to the server
    return result
  },
)
```

### The `.inputValidator` method

The `inputValidator` method is used to modify the data object before it is passed to this middleware, nested middleware, and ultimately the server function. This method should receive a function that takes the data object and returns a validated (and optionally modified) data object. It's common to use a validation library like `zod` to do this.

```tsx
import { createMiddleware } from '@tanstack/react-start'
import { zodValidator } from '@tanstack/zod-adapter'
import { z } from 'zod'

const mySchema = z.object({
  workspaceId: z.string(),
})

const workspaceMiddleware = createMiddleware({ type: 'function' })
  .inputValidator(zodValidator(mySchema))
  .server(({ next, data }) => {
    console.log('Workspace ID:', data.workspaceId)
    return next()
  })
```

### Using Server Function Middleware

To have a middleware wrap a specific server function, you can pass a middleware array to the `middleware` property of the `createServerFn` function.

```tsx
import { createServerFn } from '@tanstack/react-start'
import { loggingMiddleware } from './middleware'

const fn = createServerFn()
  .middleware([loggingMiddleware])
  .handler(async () => {
    //...
  })
```

To quickly visualize this handshake, here is a diagram:

```mermaid
sequenceDiagram
  ServerFn (client) ->> Middleware.client: payload
  Middleware.client ->> Middleware.client: next()
  Middleware.client ->> Middleware.server: Request
  Middleware.server ->> Middleware.server: next()
  Middleware.server ->> ServerFn: payload
  ServerFn ->> Middleware.server: result
  Middleware.server ->> Middleware.server: return
  Middleware.server ->> Middleware.client: Response
  Middleware.client ->> Middleware.client: return
  Middleware.client ->> ServerFn (client): result

  box Client
  participant ServerFn (client)
  participant Middleware.client
  end

  box Server
  participant Middleware.server
  participant ServerFn
  end
```

## Context Management

### Providing Context via `next`

The `next` function can be optionally called with an object that has a `context` property with an object value. Whatever properties you pass to this `context` value will be merged into the parent `context` and provided to the next middleware.

```tsx
import { createMiddleware } from '@tanstack/react-start'

const awesomeMiddleware = createMiddleware({ type: 'function' }).server(
  ({ next }) => {
    return next({
      context: {
        isAwesome: Math.random() > 0.5,
      },
    })
  },
)

const loggingMiddleware = createMiddleware({ type: 'function' })
  .middleware([awesomeMiddleware])
  .server(async ({ next, context }) => {
    console.log('Is awesome?', context.isAwesome)
    return next()
  })
```

### Sending Client Context to the Server

**Client context is NOT sent to the server by default since this could end up unintentionally sending large payloads to the server.** If you need to send client context to the server, you must call the `next` function with a `sendContext` property and object to transmit any data to the server. Any properties passed to `sendContext` will be merged, serialized and sent to the server along with the data and will be available on the normal context object of any nested server middleware.

```tsx
const requestLogger = createMiddleware({ type: 'function' })
  .client(async ({ next, context }) => {
    return next({
      sendContext: {
        // Send the workspace ID to the server
        workspaceId: context.workspaceId,
      },
    })
  })
  .server(async ({ next, data, context }) => {
    // Woah! We have the workspace ID from the client!
    console.log('Workspace ID:', context.workspaceId)
    return next()
  })
```

#### Client-Sent Context Security

You may have noticed that in the example above that while client-sent context is type-safe, it is is not required to be validated at runtime. If you pass dynamic user-generated data via context, that could pose a security concern, so **if you are sending dynamic data from the client to the server via context, you should validate it in the server-side middleware before using it.**

```tsx
import { zodValidator } from '@tanstack/zod-adapter'
import { z } from 'zod'

const requestLogger = createMiddleware({ type: 'function' })
  .client(async ({ next, context }) => {
    return next({
      sendContext: {
        workspaceId: context.workspaceId,
      },
    })
  })
  .server(async ({ next, data, context }) => {
    // Validate the workspace ID before using it
    const workspaceId = zodValidator(z.number()).parse(context.workspaceId)
    console.log('Workspace ID:', workspaceId)
    return next()
  })
```

### Sending Server Context to the Client

Similar to sending client context to the server, you can also send server context to the client by calling the `next` function with a `sendContext` property and object to transmit any data to the client. Any properties passed to `sendContext` will be merged, serialized and sent to the client along with the response and will be available on the normal context object of any nested client middleware. The returned object of calling `next` in `client` contains the context sent from server to the client and is type-safe.

> [!WARNING]
> The return type of `next` in `client` can only be inferred from middleware known in the current middleware chain. Therefore the most accurate return type of `next` is in middleware at the end of the middleware chain

```tsx
const serverTimer = createMiddleware({ type: 'function' }).server(
  async ({ next }) => {
    return next({
      sendContext: {
        // Send the current time to the client
        timeFromServer: new Date(),
      },
    })
  },
)

const requestLogger = createMiddleware({ type: 'function' })
  .middleware([serverTimer])
  .client(async ({ next }) => {
    const result = await next()
    // Woah! We have the time from the server!
    console.log('Time from the server:', result.context.timeFromServer)

    return result
  })
```

## Global Middleware

Global middleware runs automatically for every request in your application. This is useful for functionality like authentication, logging, and monitoring that should apply to all requests.

### Global Request Middleware

To have a middleware run for **every request handled by Start**, you can create a middleware and return it as `requestMiddleware` in the `createStart` function in your `src/start.ts` file:

```tsx
// src/start.ts
import { createStart } from '@tanstack/react-start'

const myGlobalMiddleware = createMiddleware().server(() => {
  //...
})

export const startInstance = createStart(() => {
  return {
    requestMiddleware: [myGlobalMiddleware],
  }
})
```

> [!NOTE]
> Global **request** middleware runs before **every request, including server routes, SSR and server functions**.

### Global Server Function Middleware

To have a middleware run for **every server function in your application**, you can create a middleware and return it to the `createStart` function as `functionMiddleware` in your `src/start.ts` file:

```tsx
// src/start.ts
import { createStart } from '@tanstack/react-start'
import { loggingMiddleware } from './middleware'

export const startInstance = createStart(() => {
  return {
    functionMiddleware: [loggingMiddleware],
  }
})
```

### Global Middleware Type Safety

Global middleware types are inherently **detached** from server functions themselves. This means that if a global middleware supplies additional context to server functions or other server function specific middleware, the types will not be automatically passed through to the server function or other server function specific middleware.

To solve this, add the global middleware you are trying to reference to the server function's middleware array. **The global middleware will be deduped to a single entry (the global instance), and your server function will receive the correct types.**

```tsx
import { authMiddleware } from './authMiddleware'

const fn = createServerFn()
  .middleware([authMiddleware])
  .handler(async ({ context }) => {
    console.log(context.user) // <-- Now this will be typed!
    // ...
  })
```

### Middleware Execution Order

Middleware is executed dependency-first, starting with global middleware, followed by server function middleware. The following example will log in this order:

- `globalMiddleware1`
- `globalMiddleware2`
- `a`
- `b`
- `c`
- `d`
- `fn`

```tsx
const globalMiddleware1 = createMiddleware({ type: 'function' }).server(
  async ({ next }) => {
    console.log('globalMiddleware1')
    return next()
  },
)

const globalMiddleware2 = createMiddleware({ type: 'function' }).server(
  async ({ next }) => {
    console.log('globalMiddleware2')
    return next()
  },
)

const a = createMiddleware({ type: 'function' }).server(async ({ next }) => {
  console.log('a')
  return next()
})

const b = createMiddleware({ type: 'function' })
  .middleware([a])
  .server(async ({ next }) => {
    console.log('b')
    return next()
  })

const c = createMiddleware({ type: 'function' })
  .middleware()
  .server(async ({ next }) => {
    console.log('c')
    return next()
  })

const d = createMiddleware({ type: 'function' })
  .middleware([b, c])
  .server(async () => {
    console.log('d')
  })

const fn = createServerFn()
  .middleware([d])
  .server(async () => {
    console.log('fn')
  })
```

## Request and Response Modification

### Reading/Modifying the Server Response

Middleware that uses the `server` method executes in the same context as server functions, so you can follow the exact same [Server Function Context Utilities](../server-functions.md#server-function-context) to read and modify anything about the request headers, status codes, etc.

### Modifying the Client Request

Middleware that uses the `client` method executes in a **completely different client-side context** than server functions, so you can't use the same utilities to read and modify the request. However, you can still modify the request returning additional properties when calling the `next` function. Currently supported properties are:

- `headers`: An object containing headers to be added to the request.

Here's an example of adding an `Authorization` header any request using this middleware:

```tsx
import { getToken } from 'my-auth-library'

const authMiddleware = createMiddleware({ type: 'function' }).client(
  async ({ next }) => {
    return next({
      headers: {
        Authorization: `Bearer ${getToken()}`,
      },
    })
  },
)
```

## Environment and Performance

### Environment Tree Shaking

Middleware functionality is tree-shaken based on the environment for each bundle produced.

- On the server, nothing is tree-shaken, so all code used in middleware will be included in the server bundle.
- On the client, all server-specific code is removed from the client bundle. This means any code used in the `server` method is always removed from the client bundle. `data` validation code will also be removed.

---
[

## Error Boundaries (React Start)

](https://tanstack.com/start/latest/docs/framework/react/guide/error-boundaries#error-boundaries-react-start)

TanStack Start uses TanStack Router's route-level error boundaries.

- Set a default for all routes via the router
- Override per-route with errorComponent

[

### Configure a default

](https://tanstack.com/start/latest/docs/framework/react/guide/error-boundaries#configure-a-default)

tsx

```
// src/router.tsx
import { createRouter, ErrorComponent } from '@tanstack/react-router'
import { routeTree } from './routeTree.gen'

export function getRouter() {
  const router = createRouter({
    routeTree,
    // Shown when an error bubbles to the router
    defaultErrorComponent: ({ error, reset }) => (
      <ErrorComponent error={error} />
    ),
  })
  return router
}
```

[

### Per-route override

](https://tanstack.com/start/latest/docs/framework/react/guide/error-boundaries#per-route-override)

tsx

```
// src/routes/posts.$postId.tsx
import { createFileRoute, ErrorComponent } from '@tanstack/react-router'
import type { ErrorComponentProps } from '@tanstack/react-router'

function PostError({ error, reset }: ErrorComponentProps) {
  return <ErrorComponent error={error} />
}

export const Route = createFileRoute('/posts/$postId')({
  component: PostComponent,
  errorComponent: PostError,
})
```

Notes:

- ErrorComponent is a simple built-in UI you can replace.
- Call reset() to retry rendering the route after fixing state.
- Use beforeLoad/loader to throw errors that will be caught.

---
id: server-routes
title: Server Routes
---

Server routes are a powerful feature of TanStack Start that allow you to create server-side endpoints in your application and are useful for handling raw HTTP requests, form submissions, user authentication, and much more.

Server routes can be defined in your `./src/routes` directory of your project **right alongside your TanStack Router routes** and are automatically handled by the TanStack Start server.

Here's what a simple server route looks like:

```ts
// routes/hello.ts
import { createFileRoute } from '@tanstack/react-router'

export const Route = createFileRoute('/hello')({
  server: {
    handlers: {
      GET: async ({ request }) => {
        return new Response('Hello, World!')
      },
    },
  },
})
```

## Server Routes and App Routes

Because server routes can be defined in the same directory as your app routes, you can even use the same file for both!

```tsx
// routes/hello.tsx
import { createFileRoute } from '@tanstack/react-router'

export const Route = createFileRoute('/hello')({
  server: {
    handlers: {
      POST: async ({ request }) => {
        const body = await request.json()
        return new Response(JSON.stringify({ message: `Hello, ${body.name}!` }))
      },
    },
  },
  component: HelloComponent,
})

function HelloComponent() {
  const [reply, setReply] = useState('')

  return (
    <div>
      <button
        onClick={() => {
          fetch('/hello', {
            method: 'POST',
            headers: {
              'Content-Type': 'application/json',
            },
            body: JSON.stringify({ name: 'Tanner' }),
          })
            .then((res) => res.json())
            .then((data) => setReply(data.message))
        }}
      >
        Say Hello
      </button>
    </div>
  )
}
```

## File Route Conventions

Server routes in TanStack Start follow the same file-based routing conventions as TanStack Router. This means that each file in your `routes` directory with a `server` property in the `createFileRoute` call will be treated as an API route. Here are a few examples:

- `/routes/users.ts` will create an API route at `/users`
- `/routes/users.index.ts` will **also** create an API route at `/users` (but will error if duplicate methods are defined)
- `/routes/users/$id.ts` will create an API route at `/users/$id`
- `/routes/users/$id/posts.ts` will create an API route at `/users/$id/posts`
- `/routes/users.$id.posts.ts` will create an API route at `/users/$id/posts`
- `/routes/api/file/$.ts` will create an API route at `/api/file/$`
- `/routes/my-script[.]js.ts` will create an API route at `/my-script.js`

## Unique Route Paths

Each route can only have a single handler file associated with it. So, if you have a file named `routes/users.ts` which'd equal the request path of `/users`, you cannot have other files that'd also resolve to the same route. For example, the following files would all resolve to the same route and would error:

- `/routes/users.index.ts`
- `/routes/users.ts`
- `/routes/users/index.ts`

## Escaped Matching

Just as with normal routes, server routes can match on escaped characters. For example, a file named `routes/users[.]json.ts` will create an API route at `/users.json`.

## Pathless Layout Routes and Break-out Routes

Because of the unified routing system, pathless layout routes and break-out routes are supported for similar functionality around server route middleware.

- Pathless layout routes can be used to add middleware to a group of routes
- Break-out routes can be used to "break out" of parent middleware

## Nested Directories vs File-names

In the examples above, you may have noticed that the file naming conventions are flexible and allow you to mix and match directories and file names. This is intentional and allows you to organize your Server routes in a way that makes sense for your application. You can read more about this in the [TanStack Router File-based Routing Guide](/router/latest/docs/framework/react/routing/file-based-routing#s-or-s).

## Handling Server Route Requests

Server route requests are handled by Start automatically by default or by Start's `createStartHandler` in your custom `src/server.ts` entry point file.

The start handler is responsible for matching an incoming request to a server route and executing the appropriate middleware and handler.

If you need to customize the server handler, you can do so by creating a custom handler and then passing the event to the start handler. See [The Server Entry Point](../server-entry-point).

## Defining a Server Route

Server routes are created by adding a `server` property to your `createFileRoute` call. The `server` property contains:

- `handlers` - Either an object mapping HTTP methods to handler functions, or a function that receives `createHandlers` for more advanced use cases
- `middleware` - Optional route-level middleware array that applies to all handlers

```ts
// routes/hello.ts
import { createFileRoute } from '@tanstack/react-router'

export const Route = createFileRoute('/hello')({
  server: {
    handlers: {
      GET: async ({ request }) => {
        return new Response('Hello, World! from ' + request.url)
      },
    },
  },
})
```

## Defining Server Route Handlers

You can define handlers in two ways:

- **Simple handlers**: Provide handler functions directly in a handlers object
- **Handlers with middleware**: Use the `createHandlers` function to define handlers with middleware

### Simple handlers

For simple use cases, you can provide handler functions directly in a handlers object.

```ts
// routes/hello.ts
import { createFileRoute } from '@tanstack/react-router'

export const Route = createFileRoute('/hello')({
  server: {
    handlers: {
      GET: async ({ request }) => {
        return new Response('Hello, World! from ' + request.url)
      },
    },
  },
})
```

### Adding middleware to specific handlers

For more complex use cases, you can add middleware to specific handlers. This requires using the `createHandlers` function:

```tsx
// routes/hello.ts
import { createFileRoute } from '@tanstack/react-router'

export const Route = createFileRoute('/hello')({
  server: {
    handlers: ({ createHandlers }) =>
      createHandlers({
        GET: {
          middleware: [loggerMiddleware],
          handler: async ({ request }) => {
            return new Response('Hello, World! from ' + request.url)
          },
        },
      }),
  },
})
```

### Adding middleware to all handlers

You can also add middleware that applies to all handlers in a route by using the `middleware` property at the server level:

```tsx
// routes/hello.ts
import { createFileRoute } from '@tanstack/react-router'

export const Route = createFileRoute('/hello')({
  server: {
    middleware: [authMiddleware, loggerMiddleware], // Applies to all handlers
    handlers: {
      GET: async ({ request }) => {
        return new Response('Hello, World! from ' + request.url)
      },
      POST: async ({ request }) => {
        const body = await request.json()
        return new Response(`Hello, ${body.name}!`)
      },
    },
  },
})
```

### Combining route-level and handler-specific middleware

You can combine both approaches - route-level middleware will run first, followed by handler-specific middleware:

```tsx
// routes/hello.ts
import { createFileRoute } from '@tanstack/react-router'

export const Route = createFileRoute('/hello')({
  server: {
    middleware: [authMiddleware], // Runs first for all handlers
    handlers: ({ createHandlers }) =>
      createHandlers({
        GET: async ({ request }) => {
          return new Response('Hello, World!')
        },
        POST: {
          middleware: [validationMiddleware], // Runs after authMiddleware, only for POST
          handler: async ({ request }) => {
            const body = await request.json()
            return new Response(`Hello, ${body.name}!`)
          },
        },
      }),
  },
})
```

## Handler Context

Each HTTP method handler receives an object with the following properties:

- `request`: The incoming request object. You can read more about the `Request` object in the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/API/Request).
- `params`: An object containing the dynamic path parameters of the route. For example, if the route path is `/users/$id`, and the request is made to `/users/123`, then `params` will be `{ id: '123' }`. We'll cover dynamic path parameters and wildcard parameters later in this guide.
- `context`: An object containing the context of the request. This is useful for passing data between middleware.

Once you've processed the request, you can return a `Response` object or `Promise<Response>` or even use any of the helpers from `@tanstack/react-start` to manipulate the response.

## Dynamic Path Params

Server routes support dynamic path parameters in the same way as TanStack Router. For example, a file named `routes/users/$id.ts` will create an API route at `/users/$id` that accepts a dynamic `id` parameter.

```ts
// routes/users/$id.ts
import { createFileRoute } from '@tanstack/react-router'

export const Route = createFileRoute('/users/$id')({
  server: {
    handlers: {
      GET: async ({ params }) => {
        const { id } = params
        return new Response(`User ID: ${id}`)
      },
    },
  },
})

// Visit /users/123 to see the response
// User ID: 123
```

You can also have multiple dynamic path parameters in a single route. For example, a file named `routes/users/$id/posts/$postId.ts` will create an API route at `/users/$id/posts/$postId` that accepts two dynamic parameters.

```ts
// routes/users/$id/posts/$postId.ts
import { createFileRoute } from '@tanstack/react-router'

export const Route = createFileRoute('/users/$id/posts/$postId')({
  server: {
    handlers: {
      GET: async ({ params }) => {
        const { id, postId } = params
        return new Response(`User ID: ${id}, Post ID: ${postId}`)
      },
    },
  },
})

// Visit /users/123/posts/456 to see the response
// User ID: 123, Post ID: 456
```

## Wildcard/Splat Param

Server routes also support wildcard parameters at the end of the path, which are denoted by a `$` followed by nothing. For example, a file named `routes/file/$.ts` will create an API route at `/file/$` that accepts a wildcard parameter.

```ts
// routes/file/$.ts
import { createFileRoute } from '@tanstack/react-router'

export const Route = createFileRoute('/file/$')({
  server: {
    handlers: {
      GET: async ({ params }) => {
        const { _splat } = params
        return new Response(`File: ${_splat}`)
      },
    },
  },
})

// Visit /file/hello.txt to see the response
// File: hello.txt
```

## Handling requests with a body

To handle POST requests,you can add a `POST` handler to the route object. The handler will receive the request object as the first argument, and you can access the request body using the `request.json()` method.

```ts
// routes/hello.ts
import { createFileRoute } from '@tanstack/react-router'

export const Route = createFileRoute('/hello')({
  server: {
    handlers: {
      POST: async ({ request }) => {
        const body = await request.json()
        return new Response(`Hello, ${body.name}!`)
      },
    },
  },
})

// Send a POST request to /hello with a JSON body like { "name": "Tanner" }
// Hello, Tanner!
```

This also applies to other HTTP methods like `PUT`, `PATCH`, and `DELETE`. You can add handlers for these methods in the route object and access the request body using the appropriate method.

It's important to remember that the `request.json()` method returns a `Promise` that resolves to the parsed JSON body of the request. You need to `await` the result to access the body.

This is a common pattern for handling POST requests in Server routes/ You can also use other methods like `request.text()` or `request.formData()` to access the body of the request.

## Responding with JSON

When returning JSON using a Response object, this is a common pattern:

```ts
// routes/hello.ts
import { createFileRoute } from '@tanstack/react-router'

export const Route = createFileRoute('/hello')({
  server: {
    handlers: {
      GET: async ({ request }) => {
        return new Response(JSON.stringify({ message: 'Hello, World!' }), {
          headers: {
            'Content-Type': 'application/json',
          },
        })
      },
    },
  },
})

// Visit /hello to see the response
// {"message":"Hello, World!"}
```

## Using the `json` helper function

Or you can use the `json` helper function to automatically set the `Content-Type` header to `application/json` and serialize the JSON object for you.

```ts
// routes/hello.ts
import { createFileRoute } from '@tanstack/react-router'
import { json } from '@tanstack/react-start'

export const Route = createFileRoute('/hello')({
  server: {
    handlers: {
      GET: async ({ request }) => {
        return json({ message: 'Hello, World!' })
      },
    },
  },
})

// Visit /hello to see the response
// {"message":"Hello, World!"}
```

## Responding with a status code

You can set the status code of the response by passing it as a property of the second argument to the `Response` constructor

```ts
// routes/hello.ts
import { createFileRoute } from '@tanstack/react-router'
import { json } from '@tanstack/react-start'

export const Route = createFileRoute('/hello')({
  server: {
    handlers: {
      GET: async ({ request, params }) => {
        const user = await findUser(params.id)
        if (!user) {
          return new Response('User not found', {
            status: 404,
          })
        }
        return json(user)
      },
    },
  },
})
```

In this example, we're returning a `404` status code if the user is not found. You can set any valid HTTP status code using this method.

## Setting headers in the response

Sometimes you may need to set headers in the response. You can do this by passing an object as the second argument to the `Response` constructor.

```ts
// routes/hello.ts
import { createFileRoute } from '@tanstack/react-router'
export const Route = createFileRoute('/hello')({
  server: {
    handlers: {
      GET: async ({ request }) => {
        return new Response('Hello, World!', {
          headers: {
            'Content-Type': 'text/plain',
          },
        })
      },
    },
  },
})
// Visit /hello to see the response
// Hello, World!
```
---
id: hydration-errors
title: Hydration Errors
---

### Why it happens

- **Mismatch**: Server HTML differs from client render during hydration
- **Common causes**: `Intl` (locale/time zone), `Date.now()`, random IDs, responsive-only logic, feature flags, user prefs

### Strategy 1 — Make server and client match

- **Pick a deterministic locale/time zone on the server** and use the same on the client
- **Source of truth**: cookie (preferred) or `Accept-Language` header
- **Compute once on the server** and hydrate as initial state

```tsx
// src/start.ts
import { createStart, createMiddleware } from '@tanstack/react-start'
import {
  getRequestHeader,
  getCookie,
  setCookie,
} from '@tanstack/react-start/server'

const localeTzMiddleware = createMiddleware().server(async ({ next }) => {
  const header = getRequestHeader('accept-language')
  const headerLocale = header?.split(',')[0] || 'en-US'
  const cookieLocale = getCookie('locale')
  const cookieTz = getCookie('tz') // set by client later (see Strategy 2)

  const locale = cookieLocale || headerLocale
  const timeZone = cookieTz || 'UTC' // deterministic until client sends tz

  // Persist locale for subsequent requests (optional)
  setCookie('locale', locale, { path: '/', maxAge: 60 * 60 * 24 * 365 })

  return next({ context: { locale, timeZone } })
})

export const startInstance = createStart(() => ({
  requestMiddleware: [localeTzMiddleware],
}))
```

```tsx
// src/routes/index.tsx (example)
import * as React from 'react'
import { createFileRoute } from '@tanstack/react-router'
import { createServerFn } from '@tanstack/react-start'
import { getCookie } from '@tanstack/react-start/server'

export const getServerNow = createServerFn().handler(async () => {
  const locale = getCookie('locale') || 'en-US'
  const timeZone = getCookie('tz') || 'UTC'
  return new Intl.DateTimeFormat(locale, {
    dateStyle: 'medium',
    timeStyle: 'short',
    timeZone,
  }).format(new Date())
})

export const Route = createFileRoute('/')({
  loader: () => getServerNow(),
  component: () => {
    const serverNow = Route.useLoaderData() as string
    return <time dateTime={serverNow}>{serverNow}</time>
  },
})
```

### Strategy 2 — Let the client tell you its environment

- On first visit, set a cookie with the client time zone; SSR uses `UTC` until then
- Do this without risking mismatches

```tsx
import * as React from 'react'
import { ClientOnly } from '@tanstack/react-router'

function SetTimeZoneCookie() {
  React.useEffect(() => {
    const tz = Intl.DateTimeFormat().resolvedOptions().timeZone
    document.cookie = `tz=${tz}; path=/; max-age=31536000`
  }, [])
  return null
}

export function AppBoot() {
  return (
    <ClientOnly fallback={null}>
      <SetTimeZoneCookie />
    </ClientOnly>
  )
}
```

### Strategy 3 — Make it client-only

- Wrap unstable UI in `<ClientOnly>` to avoid SSR and mismatches

```tsx
import { ClientOnly } from '@tanstack/react-router'
;<ClientOnly fallback={<span>—</span>}>
  <RelativeTime ts={someTs} />
</ClientOnly>
```

### Strategy 4 — Disable or limit SSR for the route

- Use Selective SSR to avoid rendering the component on the server

```tsx
export const Route = createFileRoute('/unstable')({
  ssr: 'data-only', // or false
  component: () => <ExpensiveViz />,
})
```

### Strategy 5 — Last resort suppression

- For small, known-different nodes, you can use React’s `suppressHydrationWarning`

```tsx
<time suppressHydrationWarning>{new Date().toLocaleString()}</time>
```

### Checklist

- **Deterministic inputs**: locale, time zone, feature flags
- **Prefer cookies** for client context; fallback to `Accept-Language`
- **Use `<ClientOnly>`** for inherently dynamic UI
- **Use Selective SSR** when server HTML cannot be stable
- **Avoid blind suppression**; use `suppressHydrationWarning` sparingly

See also: [Execution Model](../execution-model.md), [Code Execution Patterns](../code-execution-patterns.md), [Selective SSR](../selective-ssr.md), [Server Functions](../server-functions.md)
---
id: selective-ssr
title: Selective Server-Side Rendering (SSR)
---

## What is Selective SSR?

In TanStack Start, routes matching the initial request are rendered on the server by default. This means `beforeLoad` and `loader` are executed on the server, followed by rendering the route components. The resulting HTML is sent to the client, which hydrates the markup into a fully interactive application.

However, there are cases where you might want to disable SSR for certain routes or all routes, such as:

- When `beforeLoad` or `loader` requires browser-only APIs (e.g., `localStorage`).
- When the route component depends on browser-only APIs (e.g., `canvas`).

TanStack Start's Selective SSR feature lets you configure:

- Which routes should execute `beforeLoad` or `loader` on the server.
- Which route components should be rendered on the server.

## How does this compare to SPA mode?

TanStack Start's [SPA mode](../spa-mode) completely disables server-side execution of `beforeLoad` and `loader`, as well as server-side rendering of route components. Selective SSR allows you to configure server-side handling on a per-route basis, either statically or dynamically.

## Configuration

You can control how a route is handled during the initial server request using the `ssr` property. If this property is not set, it defaults to `true`. You can change this default using the `defaultSsr` option in `createStart`:

```tsx
// src/start.ts
import { createStart } from '@tanstack/react-start'

export const startInstance = createStart(() => ({
  // Disable SSR by default
  defaultSsr: false,
}))
```

### `ssr: true`

This is the default behavior unless otherwise configured. On the initial request, it will:

- Run `beforeLoad` on the server and send the resulting context to the client.
- Run `loader` on the server and send the loader data to the client.
- Render the component on the server and send the HTML markup to the client.

```tsx
// src/routes/posts/$postId.tsx
export const Route = createFileRoute('/posts/$postId')({
  ssr: true,
  beforeLoad: () => {
    console.log('Executes on the server during the initial request')
    console.log('Executes on the client for subsequent navigation')
  },
  loader: () => {
    console.log('Executes on the server during the initial request')
    console.log('Executes on the client for subsequent navigation')
  },
  component: () => <div>This component is rendered on the server</div>,
})
```

### `ssr: false`

This disables server-side:

- Execution of the route's `beforeLoad` and `loader`.
- Rendering of the route component.

```tsx
// src/routes/posts/$postId.tsx
export const Route = createFileRoute('/posts/$postId')({
  ssr: false,
  beforeLoad: () => {
    console.log('Executes on the client during hydration')
  },
  loader: () => {
    console.log('Executes on the client during hydration')
  },
  component: () => <div>This component is rendered on the client</div>,
})
```

### `ssr: 'data-only'`

This hybrid option will:

- Run `beforeLoad` on the server and send the resulting context to the client.
- Run `loader` on the server and send the loader data to the client.
- Disable server-side rendering of the route component.

```tsx
// src/routes/posts/$postId.tsx
export const Route = createFileRoute('/posts/$postId')({
  ssr: 'data-only',
  beforeLoad: () => {
    console.log('Executes on the server during the initial request')
    console.log('Executes on the client for subsequent navigation')
  },
  loader: () => {
    console.log('Executes on the server during the initial request')
    console.log('Executes on the client for subsequent navigation')
  },
  component: () => <div>This component is rendered on the client</div>,
})
```

### Functional Form

For more flexibility, you can use the functional form of the `ssr` property to decide at runtime whether to SSR a route:

```tsx
// src/routes/docs/$docType/$docId.tsx
export const Route = createFileRoute('/docs/$docType/$docId')({
  validateSearch: z.object({ details: z.boolean().optional() }),
  ssr: ({ params, search }) => {
    if (params.status === 'success' && params.value.docType === 'sheet') {
      return false
    }
    if (search.status === 'success' && search.value.details) {
      return 'data-only'
    }
  },
  beforeLoad: () => {
    console.log('Executes on the server depending on the result of ssr()')
  },
  loader: () => {
    console.log('Executes on the server depending on the result of ssr()')
  },
  component: () => <div>This component is rendered on the client</div>,
})
```

The `ssr` function runs only on the server during the initial request and is stripped from the client bundle.

`search` and `params` are passed in after validation as a discriminated union:

```tsx
params:
    | { status: 'success'; value: Expand<ResolveAllParamsFromParent<TParentRoute, TParams>> }
    | { status: 'error'; error: unknown }
search:
    | { status: 'success'; value: Expand<ResolveFullSearchSchema<TParentRoute, TSearchValidator>> }
    | { status: 'error'; error: unknown }
```

If validation fails, `status` will be `error` and `error` will contain the failure details. Otherwise, `status` will be `success` and `value` will contain the validated data.

### Inheritance

At runtime, a child route inherits the Selective SSR configuration of its parent. However, the inherited value can only be changed to be more restrictive (i.e. `true` to `data-only` or `false` and `data-only` to `false`). For example:

```tsx
root { ssr: undefined }
  posts { ssr: false }
     $postId { ssr: true }
```

- `root` defaults to `ssr: true`.
- `posts` explicitly sets `ssr: false`, so neither `beforeLoad` nor `loader` will run on the server, and the route component won't be rendered on the server.
- `$postId` sets `ssr: true`, but inherits `ssr: false` from its parent. Because the inherited value can only be changed to be more restrictive, `ssr: true` has no effect and the inherited `ssr: false` will remain.

Another example:

```tsx
root { ssr: undefined }
  posts { ssr: 'data-only' }
     $postId { ssr: true }
       details { ssr: false }
```

- `root` defaults to `ssr: true`.
- `posts` sets `ssr: 'data-only'`, so `beforeLoad` and `loader` run on the server, but the route component isn't rendered on the server.
- `$postId` sets `ssr: true`, but inherits `ssr: 'data-only'` from its parent.
- `details` sets `ssr: false`, so neither `beforeLoad` nor `loader` will run on the server, and the route component won't be rendered on the server. Here the inherited value is changed to be more restrictive, and therefore, the `ssr: false` will override the inherited value.

## Fallback Rendering

For the first route with `ssr: false` or `ssr: 'data-only'`, the server will render the route's `pendingComponent` as a fallback. If `pendingComponent` isn't configured, the `defaultPendingComponent` will be rendered. If neither is configured, no fallback will be rendered.

On the client during hydration, this fallback will be displayed for at least `minPendingMs` (or `defaultPendingMinMs` if not configured), even if the route doesn't have `beforeLoad` or `loader` defined.

## How to disable SSR of the root route?

You can disable server side rendering of the root route component, however the `<html>` shell still needs to be rendered on the server. This shell is configured via the `shellComponent` property and takes a single property `children`. The `shellComponent` is always SSRed and is wrapping around the root `component`, the root `errorComponent` or the root `notFound` component respectively.

A minimal setup of a root route with disabled SSR for the route component looks like this:

```tsx
import * as React from 'react'

import {
  HeadContent,
  Outlet,
  Scripts,
  createRootRoute,
} from '@tanstack/react-router'

export const Route = createRootRoute({
  shellComponent: RootShell,
  component: RootComponent,
  errorComponent: () => <div>Error</div>,
  notFoundComponent: () => <div>Not found</div>,
  ssr: false, // or `defaultSsr: false` on the router
})

function RootShell({ children }: { children: React.ReactNode }) {
  return (
    <html>
      <head>
        <HeadContent />
      </head>
      <body>
        {children}
        <Scripts />
      </body>
    </html>
  )
}

function RootComponent() {
  return (
    <div>
      <h1>This component will be rendered on the client</h1>
      <Outlet />
    </div>
  )
}
```
---
id: spa-mode
title: SPA mode
---

## What the heck is SPA mode?

For applications that do not require SSR for either SEO, crawlers, or performance reasons, it may be desirable to ship static HTML to your users containing the "shell" of your application (or even prerendered HTML for specific routes) that contain the necessary `html`, `head`, and `body` tags to bootstrap your application only on the client.

## Why use Start without SSR?

**No SSR doesn't mean giving up server-side features!** SPA modes actually pair very nicely with server-side features like server functions and/or server routes or even other external APIs. It **simply means that the initial document will not contain the fully rendered HTML of your application until it has been rendered on the client using JavaScript**.

## Benefits of SPA mode

- **Easier to deploy** - A CDN that can serve static assets is all you need.
- **Cheaper** to host - CDNs are cheap compared to Lambda functions or long-running processes.
- **Client-side Only is simpler** - No SSR means less to go wrong with hydration, rendering, and routing.

## Caveats of SPA mode

- **Slower time to full content** - Time to full content is longer since all JS must download and execute before anything below the shell can be rendered.
- **Less SEO friendly** - Robots, crawlers and link unfurlers _may_ have a harder time indexing your application unless they are configured to execute JS and your application can render within a reasonable amount of time.

## How does it work?

After enabling the SPA mode, running a Start build will have an additional prerendering step afterwards to generate the shell. This is done by:

- **Prerendering** your application's **root route only**
- Where your application would normally render your matched routes, your router's configured **pending fallback component is rendered instead**.
- The resulting HTML is stored to a static HTML page called `/_shell.html` (configurable)
- Default rewrites are configured to redirect all 404 requests to the SPA mode shell

> [!NOTE]
> Other routes may also be prerendered and it is recommended to prerender as much as you can in SPA mode, but this is not required for SPA mode to work.

## Configuring SPA mode

To configure SPA mode, there are a few options you can add to your Start plugin's options:

```tsx
// vite.config.ts
export default defineConfig({
  plugins: [
    tanstackStart({
      spa: {
        enabled: true,
      },
    }),
  ],
})
```

## Use Necessary Redirects

Deploying a purely client-side SPA to a host or CDN often requires the use of redirects to ensure that urls are properly rewritten to the SPA shell. The goal of any deployment should include these priorities in this order:

1. Ensure that static assets will always be served if they exist, e.g. /about.html. This is usually the default behavior for most CDNs
2. (Optional) Allow-list specific subpaths to be routed through to any dynamic server handlers, e.g. /api/\*\* (More on this below)
3. Ensure that all 404 requests are rewritten to the SPA shell, e.g. a catch-all redirect to /\_shell.html (or if you have configured your shell output path to be something custom, use that instead)

## Basic Redirects Example

Let's use Netlify's `_redirects` file to rewrite all 404 requests to the SPA shell.

```
# Catch all other 404 requests and rewrite them to the SPA shell
/* /_shell.html 200
```

## Allowing Server Functions and Server Routes

Again, using Netlify's `_redirects` file, we can allow-list specific subpaths to be routed through to the server.

```
# Allow requests to /_serverFn/* to be routed through to the server (If you have configured your server function base path to be something other than /_serverFn, use that instead)
/_serverFn/* /_serverFn/:splat 200

# Allow any requests to /api/* to be routed through to the server (Server routes can be created at any path, so you must ensure that any server routes you want to use are under this path, or simply add additional redirects for each server route base you want to expose)
/api/* /api/:splat 200

# Catch all other 404 requests and rewrite them to the SPA shell
/* /_shell.html 200
```

## Shell Mask Path

The default pathname used to generate the SPA shell is `/`. We call this the **shell mask path**. Since matched routes are not included, the pathname used to generate the shell is mostly irrelevant, but it's still configurable.

> [!NOTE]
> It's recommended to keep the default value of `/` as the shell mask path.

```tsx
// vite.config.ts
export default defineConfig({
  plugins: [
    tanstackStart({
      spa: {
        maskPath: '/app',
      },
    }),
  ],
})
```

## Prerendering Options

The prerender option is used to configure the prerendering behavior of the SPA shell, and accepts the same prerender options as found in our prerendering guide.

**By default, the following `prerender` options are set:**

- `outputPath`: `/_shell.html`
- `crawlLinks`: `false`
- `retryCount`: `0`

This means that by default, the shell will not be crawled for links to follow for additional prerendering, and will not retry prerendering fails.

You can always override these options by providing your own prerender options:

```tsx
// vite.config.ts
export default defineConfig({
  plugins: [
    tanstackStart({
      spa: {
        prerender: {
          outputPath: '/custom-shell',
          crawlLinks: true,
          retryCount: 3,
        },
      },
    }),
  ],
})
```

## Customized rendering in SPA mode

Customizing the HTML output of the SPA shell can be useful if you want to:

- Provide generic head tags for SPA routes
- Provide a custom pending fallback component
- Change literally anything about the shell's HTML, CSS, and JS

To make this process simple, an `isShell()` function can be found on the `router` instance:

```tsx
// src/routes/root.tsx
export default function Root() {
  const isShell = useRouter().isShell()

  if (isShell) console.log('Rendering the shell!')
}
```

You can use this boolean to conditionally render different UI based on whether the current route is a shell or not, but keep in mind that after hydrating the shell, the router will immediately navigate to the first route and `isShell()` will return `false`. **This could produce flashes of unstyled content if not handled properly.**

## Dynamic Data in your Shell

Since the shell is prerendered using the SSR build of your application, any `loader`s, or server-specific functionality defined on your **Root Route** will run during the prerendering process and the data will be included in the shell.

This means that you can use dynamic data in your shell by using a `loader` or server-specific functionality.

```tsx
// src/routes/__root.tsx

export const RootRoute = createRootRoute({
  loader: async () => {
    return {
      name: 'Tanner',
    }
  },
  component: Root,
})

export default function Root() {
  const { name } = useLoaderData()

  return (
    <html>
      <body>
        <h1>Hello, {name}!</h1>
        <Outlet />
      </body>
    </html>
  )
}
```
---
id: static-prerendering
title: Static Prerendering
---

Static prerendering is the process of generating static HTML files for your application. This can be useful for either improving the performance of your application, as it allows you to serve pre-rendered HTML files to users without having to generate them on the fly or for deploying static sites to platforms that do not support server-side rendering.

## Prerendering

TanStack Start can prerender your application to static HTML files, which can then be served to users without having to generate them on the fly. To prerender your application, you can add the `prerender` option to your tanstackStart configuration in `vite.config.ts` file:

```ts
// vite.config.ts

import { tanstackStart } from '@tanstack/react-start/plugin/vite'
import viteReact from '@vitejs/plugin-react'

export default defineConfig({
  plugins: [
    tanstackStart({
      prerender: {
        // Enable prerendering
        enabled: true,

        // Enable if you need pages to be at `/page/index.html` instead of `/page.html`
        autoSubfolderIndex: true,

        // If disabled, only the root path or the paths defined in the pages config will be prerendered
        autoStaticPathsDiscovery: true,

        // How many prerender jobs to run at once
        concurrency: 14,

        // Whether to extract links from the HTML and prerender them also
        crawlLinks: true,

        // Filter function takes the page object and returns whether it should prerender
        filter: ({ path }) => !path.startsWith('/do-not-render-me'),

        // Number of times to retry a failed prerender job
        retryCount: 2,

        // Delay between retries in milliseconds
        retryDelay: 1000,

        // Maximum number of redirects to follow during prerendering
        maxRedirects: 5,

        // Fail if an error occurs during prerendering
        failOnError: true,

        // Callback when page is successfully rendered
        onSuccess: ({ page }) => {
          console.log(`Rendered ${page.path}!`)
        },
      },
      // Optional configuration for specific pages
      // Note: When autoStaticPathsDiscovery is enabled (default), discovered static
      // routes will be merged with the pages specified below
      pages: [
        {
          path: '/my-page',
          prerender: { enabled: true, outputPath: '/my-page/index.html' },
        },
      ],
    }),
    viteReact(),
  ],
})
```

## Automatic Static Route Discovery

All static paths will be automatically discovered and seamlessly merged with the specified `pages` config

Routes are excluded from automatic discovery in the following cases:

- Routes with path parameters (e.g., `/users/$userId`) since they require specific parameter values
- Layout routes (prefixed with `_`) since they don't render standalone pages
- Routes without components (e.g., API routes)

Note: Dynamic routes can still be prerendered if they are linked from other pages when `crawlLinks` is enabled.

## Crawling Links

When `crawlLinks` is enabled (default: `true`), TanStack Start will extract links from prerendered pages and prerender those linked pages as well.

For example, if `/` contains a link to `/posts`, then `/posts` will also be automatically prerendered.
---
id: server-entry-point
title: Server Entry Point
---

# Server Entry Point

> [!NOTE]
> The server entry point is **optional** out of the box. If not provided, TanStack Start will automatically handle the server entry point for you using the below as a default.

This is done via the `src/server.ts` file.

```tsx
// src/server.ts
import handler, { type ServerEntry } from '@tanstack/react-start/server-entry'

export default {
  fetch(request) {
    return handler.fetch(request)
  },
} satisfies ServerEntry
```

The default export must conform to the `ServerEntry` interface:

```ts
export default {
  fetch(req: Request, opts?: RequestOptions): Promise<Response> {
    // ...
  },
}
```

Whether we are statically generating our app or serving it dynamically, the `server.ts` file is the entry point for doing all SSR-related work as well as for handling server routes and server function requests.

## Custom Server Handlers

You can create custom server handlers to modify how your application is rendered:

```tsx
// src/server.ts
import {
  createStartHandler,
  defaultStreamHandler,
  defineHandlerCallback,
} from '@tanstack/react-start/server'
import type { ServerEntry } from '@tanstack/react-start/server-entry'

const customHandler = defineHandlerCallback((ctx) => {
  // add custom logic here
  return defaultStreamHandler(ctx)
})

const fetch = createStartHandler(customHandler)

export default {
  fetch,
} satisfies ServerEntry
```

## Request context

When your server needs to pass additional, typed data into request handlers (for example, authenticated user info, a database connection, or per-request flags), register a request context type via TypeScript module augmentation. The registered context is delivered as the second argument to the server `fetch` handler and is available throughout the server-side middleware chain — including global middleware, request/function middleware, server routes, server functions, and the router itself.

To add types for your request context, augment the `Register` interface from `@tanstack/react-start` with a `server.requestContext` property. The runtime `context` you pass to `handler.fetch` will then match that type. Example:

```tsx
import handler, { type ServerEntry } from '@tanstack/react-start/server-entry'

type MyRequestContext = {
  hello: string
  foo: number
}

declare module '@tanstack/react-start' {
  interface Register {
    server: {
      requestContext: MyRequestContext
    }
  }
}

export default {
  async fetch(request) {
    return handler.fetch(request, { context: { hello: 'world', foo: 123 } })
  },
} satisfies ServerEntry
```

## Server Configuration

The server entry point is where you can configure server-specific behavior:

- Request/response middleware
- Custom error handling
- Authentication logic
- Database connections
- Logging and monitoring

This flexibility allows you to customize how your TanStack Start application handles server-side rendering while maintaining the framework's conventions.
---
id: client-entry-point
title: Client Entry Point
---

# Client Entry Point

> [!NOTE]
> The client entry point is **optional** out of the box. If not provided, TanStack Start will automatically handle the client entry point for you using the below as a default.

Getting our html to the client is only half the battle. Once there, we need to hydrate our client-side JavaScript once the route resolves to the client. We do this by hydrating the root of our application with the `StartClient` component:

```tsx
// src/client.tsx
import { StartClient } from '@tanstack/react-start/client'
import { StrictMode } from 'react'
import { hydrateRoot } from 'react-dom/client'

hydrateRoot(
  document,
  <StrictMode>
    <StartClient />
  </StrictMode>,
)
```

This enables us to kick off client-side routing once the user's initial server request has fulfilled.

## Error Handling

You can wrap your client entry point with error boundaries to handle client-side errors gracefully:

```tsx
// src/client.tsx
import { StartClient } from '@tanstack/react-start/client'
import { StrictMode } from 'react'
import { hydrateRoot } from 'react-dom/client'
import { ErrorBoundary } from './components/ErrorBoundary'

hydrateRoot(
  document,
  <StrictMode>
    <ErrorBoundary>
      <StartClient />
    </ErrorBoundary>
  </StrictMode>,
)
```

## Development vs Production

You may want different behavior in development vs production:

```tsx
// src/client.tsx
import { StartClient } from '@tanstack/react-start/client'
import { StrictMode } from 'react'
import { hydrateRoot } from 'react-dom/client'

const App = (
  <>
    {import.meta.env.DEV && <div>Development Mode</div>}
    <StartClient />
  </>
)

hydrateRoot(
  document,
  import.meta.env.DEV ? <StrictMode>{App}</StrictMode> : App,
)
```

The client entry point gives you full control over how your application initializes on the client side while working seamlessly with TanStack Start's server-side rendering.
---
id: hosting
title: Hosting
---

Hosting is the process of deploying your application to the internet so that users can access it. This is a critical part of any web development project, ensuring your application is available to the world. TanStack Start is built on Vite, a powerful dev/build platform that allows us to make it possible to deploy your application to any hosting provider.

## What should I use?

TanStack Start is **designed to work with any hosting provider**, so if you already have a hosting provider in mind, you can deploy your application there using the full-stack APIs provided by TanStack Start.

However, since hosting is one of the most crucial aspects of your application's performance, reliability, and scalability, we recommend using one of our **Official Hosting Partners**: [Cloudflare](https://www.cloudflare.com?utm_source=tanstack) or [Netlify](https://www.netlify.com?utm_source=tanstack).

## Deployment

> [!WARNING]
> The page is still a work in progress. We'll keep updating this page with guides on deployment to different hosting providers soon!

Once you've chosen a deployment target, you can follow the deployment guidelines below to deploy your TanStack Start application to the hosting provider of your choice:

- [`cloudflare-workers`](#cloudflare-workers): Deploy to Cloudflare Workers
- [`netlify`](#netlify): Deploy to Netlify
- [`nitro`](#nitro): Deploy using Nitro
- [`vercel`](#vercel): Deploy to Vercel
- [`railway`](#nodejs--railway--docker): Deploy to Railway
- [`node-server`](#nodejs--railway--docker): Deploy to a Node.js server
- [`bun`](#bun): Deploy to a Bun server
- ... and more to come!

### Cloudflare Workers ⭐ _Official Partner_

<a href="https://www.cloudflare.com?utm_source=tanstack" alt="Cloudflare Logo">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/cloudflare-white.svg" width="280">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/cloudflare-black.svg" width="280">
    <img alt="Cloudflare logo" src="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/cloudflare-black.svg" width="280">
  </picture>
</a>

When deploying to Cloudflare Workers, you'll need to complete a few extra steps before your users can start using your app.

1. Install `@cloudflare/vite-plugin` and `wrangler`

```bash
pnpm add -D @cloudflare/vite-plugin wrangler
```

2. Add the Cloudflare plugin to your `vite.config.ts` file

```ts
// vite.config.ts
import { defineConfig } from 'vite'
import { tanstackStart } from '@tanstack/react-start/plugin/vite'
import { cloudflare } from '@cloudflare/vite-plugin'
import viteReact from '@vitejs/plugin-react'

export default defineConfig({
  plugins: [
    cloudflare({ viteEnvironment: { name: 'ssr' } }),
    tanstackStart(),
    viteReact(),
  ],
})
```

3. Add a `wrangler.jsonc` config file

```json
{
  "$schema": "node_modules/wrangler/config-schema.json",
  "name": "tanstack-start-app",
  "compatibility_date": "2025-09-02",
  "compatibility_flags": ["nodejs_compat"],
  "main": "@tanstack/react-start/server-entry"
}
```

4. Modify the scripts in your `package.json` file

```json
{
  "scripts": {
    "dev": "vite dev",
    "build": "vite build && tsc --noEmit",
    // ============ 👇 remove this line ============
    "start": "node .output/server/index.mjs",
    // ============ 👇 add these lines ============
    "preview": "vite preview",
    "deploy": "npm run build && wrangler deploy",
    "cf-typegen": "wrangler types"
  }
}
```

5. Login with Wrangler to authenticate with your Cloudflare account.

```bash
npx wrangler login
```

or if using pnpm:

```bash
pnpm dlx wrangler login
```

To check current user use `wrangler whoami`.

6. Deploy

```bash
pnpm run deploy
```

Deploy your application to Cloudflare Workers using their one-click deployment process, and you're ready to go!

A full TanStack Start example for Cloudflare Workers is available [here](https://github.com/TanStack/router/tree/main/examples/react/start-basic-cloudflare).

### Netlify ⭐ _Official Partner_

<a href="https://www.netlify.com?utm_source=tanstack" alt="Netlify Logo">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/netlify-dark.svg" width="280">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/netlify-light.svg" width="280">
    <img alt="Netlify logo" src="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/netlify-light.svg" width="280">
  </picture>
</a>

### Netlify

Install and add the [`@netlify/vite-plugin-tanstack-start`](https://www.npmjs.com/package/@netlify/vite-plugin-tanstack-start) plugin, which configures your build for Netlify deployment and provides full Netlify production platform emulation in local dev.

```ts
// vite.config.ts
import { defineConfig } from 'vite'
import { tanstackStart } from '@tanstack/react-start/plugin/vite'
import netlify from '@netlify/vite-plugin-tanstack-start'
import viteReact from '@vitejs/plugin-react'

export default defineConfig({
  plugins: [tanstackStart(), netlify(), viteReact()],
})
```

Add a `netlify.toml` file to your project root:

```toml
[build]
  command = "vite build"
  publish = "dist/client"
[dev]
  command = "vite dev"
  port = 3000
```

Deploy your application using their one-click deployment process, and you're ready to go!

### Nitro

[Nitro](https://nitro.build/) is an abstraction layer that allows you to deploy TanStack Start applications to [a wide range of providers](https://nitro.build/deploy).

**⚠️ During TanStack Start 1.0 release candidate phase, we currently recommend using:**

- [@tanstack/nitro-v2-vite-plugin (Temporary Compatibility Plugin)](https://www.npmjs.com/package/@tanstack/nitro-v2-vite-plugin) - A temporary compatibility plugin for using Nitro v2 as the underlying build tool for TanStack Start.
- [Nitro v3's Vite Plugin (ALPHA)](https://www.npmjs.com/package/nitro) - An **ALPHA** plugin for officially using Nitro v3 as the underlying build tool for TanStack Start.

#### Using Nitro v2

**⚠️ `@tanstack/nitro-v2-vite-plugin` is a temporary compatibility plugin for using Nitro v2 as the underlying build tool for TanStack Start. Use this plugin if you experience issues with the Nitro v3 plugin. It does not support all of Nitro v3's features and is limited in its dev server capabilities, but should work as a safe fallback, even for production deployments for those who were using TanStack Start's alpha/beta versions.**

```tsx
import { tanstackStart } from '@tanstack/react-start/plugin/vite'
import { defineConfig } from 'vite'
import viteReact from '@vitejs/plugin-react'
import { nitroV2Plugin } from '@tanstack/nitro-v2-vite-plugin'

export default defineConfig({
  plugins: [
    tanstackStart(),
    nitroV2Plugin(/*
      // nitro config goes here, e.g.
      { preset: 'node-server' }
    */),
    viteReact(),
  ],
})
```

#### Using Nitro v3 (ALPHA)

**⚠️ The [`nitro`](https://www.npmjs.com/package/nitro) vite plugin is an official **ALPHA** plugin from the Nitro team for using Nitro v3 as the underlying build tool for TanStack Start. It is still in development and is receiving regular updates.**

```tsx
import { tanstackStart } from '@tanstack/react-start/plugin/vite'
import { defineConfig } from 'vite'
import viteReact from '@vitejs/plugin-react'
import { nitro } from 'nitro/vite'

export default defineConfig({
  plugins: [
    tanstackStart(),
    nitro(/*
      // nitro config goes here, e.g.
      { config: { preset: 'node-server' } }
    */)
    viteReact(),
  ],
})
```

### Vercel

Follow the [`Nitro`](#nitro) deployment instructions.
Deploy your application to Vercel using their one-click deployment process, and you're ready to go!

### Node.js / Railway / Docker

Follow the [`Nitro`](#nitro) deployment instructions. Use the `node` command to start your application from the server from the build output files.

Ensure `build` and `start` npm scripts are present in your `package.json` file:

```json
    "build": "vite build",
    "start": "node .output/server/index.mjs"
```

Then you can run the following command to build your application:

```sh
npm run build
```

You can start your application by running:

```sh
npm run start
```

### Bun

> [!IMPORTANT]
> Currently, the Bun specific deployment guidelines only work with React 19. If you are using React 18, please refer to the [Node.js](#nodejs--railway--docker) deployment guidelines.

Make sure that your `react` and `react-dom` packages are set to version 19.0.0 or higher in your `package.json` file. If not, run the following command to upgrade the packages:

```sh
bun install react@19 react-dom@19
```

Follow the [`Nitro`](#nitro) deployment instructions.
Depending on how you invoke the build, you might need to set the `'bun'` preset in the Nitro configuration:

```ts
// vite.config.ts
import { tanstackStart } from '@tanstack/react-start/plugin/vite'
import { defineConfig } from 'vite'
import viteReact from '@vitejs/plugin-react'
import { nitroV2Plugin } from '@tanstack/nitro-v2-vite-plugin'
// alternatively: import { nitro } from 'nitro/vite'

export default defineConfig({
  plugins: [
    tanstackStart(),
    nitroV2Plugin({ preset: 'bun' })
    // alternatively: nitro( { config: { preset: 'bun' }} ),
    viteReact(),
  ],
})
```

#### Production Server with Bun

Alternatively, you can use a custom server implementation that leverages Bun's native APIs.

We provide a reference implementation that demonstrates one approach to building a production-ready Bun server. This example uses Bun-native functions for optimal performance and includes features like intelligent asset preloading and memory management.

**This is a starting point - feel free to adapt it to your needs or simplify it for your use case.**

**What this example demonstrates:**

- Serving static assets using Bun's native file handling
- Hybrid loading strategy (preload small files, serve large files on-demand)
- Optional features like ETag support and Gzip compression
- Production-ready caching headers

**Quick Setup:**

1. Copy the [`server.ts`](https://github.com/tanstack/router/blob/main/examples/react/start-bun/server.ts) file from the example repository to your project root (or use it as inspiration for your own implementation)

2. Build your application:

   ```sh
   bun run build
   ```

3. Start the server:

   ```sh
   bun run server.ts
   ```

**Configuration (Optional):**

The reference server implementation includes several optional configuration options via environment variables. You can use these as-is, modify them, or remove features you don't need:

```sh
# Basic usage - just works out of the box
bun run server.ts

# Common configurations
PORT=8080 bun run server.ts  # Custom port
ASSET_PRELOAD_VERBOSE_LOGGING=true bun run server.ts  # See what's happening
```

**Available Environment Variables:**

| Variable                         | Description                                        | Default                                                                       |
| -------------------------------- | -------------------------------------------------- | ----------------------------------------------------------------------------- |
| `PORT`                           | Server port                                        | `3000`                                                                        |
| `ASSET_PRELOAD_MAX_SIZE`         | Maximum file size to preload into memory (bytes)   | `5242880` (5MB)                                                               |
| `ASSET_PRELOAD_INCLUDE_PATTERNS` | Comma-separated glob patterns for files to include | All files                                                                     |
| `ASSET_PRELOAD_EXCLUDE_PATTERNS` | Comma-separated glob patterns for files to exclude | None                                                                          |
| `ASSET_PRELOAD_VERBOSE_LOGGING`  | Enable detailed logging                            | `false`                                                                       |
| `ASSET_PRELOAD_ENABLE_ETAG`      | Enable ETag generation                             | `true`                                                                        |
| `ASSET_PRELOAD_ENABLE_GZIP`      | Enable Gzip compression                            | `true`                                                                        |
| `ASSET_PRELOAD_GZIP_MIN_SIZE`    | Minimum file size for Gzip (bytes)                 | `1024` (1KB)                                                                  |
| `ASSET_PRELOAD_GZIP_MIME_TYPES`  | MIME types eligible for Gzip                       | `text/,application/javascript,application/json,application/xml,image/svg+xml` |

<details>
<summary>Advanced configuration examples</summary>

```sh
# Optimize for minimal memory usage
ASSET_PRELOAD_MAX_SIZE=1048576 bun run server.ts

# Preload only critical assets
ASSET_PRELOAD_INCLUDE_PATTERNS="*.js,*.css" \
ASSET_PRELOAD_EXCLUDE_PATTERNS="*.map,vendor-*" \
bun run server.ts

# Disable optional features
ASSET_PRELOAD_ENABLE_ETAG=false \
ASSET_PRELOAD_ENABLE_GZIP=false \
bun run server.ts

# Custom Gzip configuration
ASSET_PRELOAD_GZIP_MIN_SIZE=2048 \
ASSET_PRELOAD_GZIP_MIME_TYPES="text/,application/javascript,application/json" \
bun run server.ts
```

</details>

**Example Output:**

```txt
📦 Loading static assets from ./dist/client...
   Max preload size: 5.00 MB

📁 Preloaded into memory:
   /assets/index-a1b2c3d4.js           45.23 kB │ gzip:  15.83 kB
   /assets/index-e5f6g7h8.css           12.45 kB │ gzip:   4.36 kB

💾 Served on-demand:
   /assets/vendor-i9j0k1l2.js          245.67 kB │ gzip:  86.98 kB

✅ Preloaded 2 files (57.68 KB) into memory
🚀 Server running at http://localhost:3000
```

For a complete working example, check out the [TanStack Start + Bun example](https://github.com/TanStack/router/tree/main/examples/react/start-bun) in this repository.
---
id: authentication-overview
title: Authentication
---

## Authentication vs Authorization

- **Authentication**: Who is this user? (Login/logout, identity verification)
- **Authorization**: What can this user do? (Permissions, roles, access control)

## Architecture Overview

### Full-Stack Authentication Model

**Server-Side (Secure)**

- Session storage and validation
- User credential verification
- Database operations
- Token generation/verification
- Protected API endpoints

**Client-Side (Public)**

- Authentication state management
- Route protection logic
- Login/logout user interface
- Redirect handling

**Isomorphic (Both)**

- Route loaders checking auth state
- Shared validation logic
- User profile data access

### Session Management Patterns

**HTTP-Only Cookies (Recommended)**

- Most secure approach - not accessible via JavaScript
- Automatic browser handling
- Built-in CSRF protection with `sameSite`
- Best for traditional web applications

**JWT Tokens**

- Stateless authentication
- Good for API-first applications
- Requires careful handling to avoid XSS vulnerabilities
- Consider refresh token rotation

**Server-Side Sessions**

- Centralized session control
- Easy to revoke sessions
- Requires session storage (database, Redis)
- Good for applications requiring immediate session control

### Route Protection Architecture

**Layout Route Pattern (Recommended)**

- Protect entire route subtrees with parent layout routes
- Centralized authentication logic
- Automatic protection for all child routes
- Clean separation of authenticated vs public routes

**Component-Level Protection**

- Conditional rendering within components
- More granular control over UI states
- Good for mixed public/private content on same route
- Requires careful handling to prevent layout shifts

**Server Function Guards**

- Server-side validation before executing sensitive operations
- Works alongside route-level protection
- Essential for API security regardless of client-side protection

### State Management Patterns

**Server-Driven State (Recommended)**

- Authentication state sourced from server on each request
- Always up-to-date with server state
- Works seamlessly with SSR
- Best security - server is source of truth

**Context-Based State**

- Client-side authentication state management
- Good for third-party auth providers (Auth0, Firebase)
- Requires careful synchronization with server state
- Consider for highly interactive client-first applications

**Hybrid Approach**

- Initial state from server, client-side updates
- Balance between security and UX
- Periodic server-side validation

## Authentication Options

### 🏢 Partner Solutions

- **[WorkOS](https://workos.com)**
- **[Clerk](https://clerk.dev)**

### 🛠️ DIY Authentication

Build your own authentication system using TanStack Start's server functions and session management:

- **Full Control**: Complete customization over authentication flow
- **Server Functions**: Secure authentication logic on the server
- **Session Management**: Built-in session handling with HTTP-only cookies
- **Type Safety**: End-to-end type safety for authentication state

### 🌐 Other Excellent Options

**Open Source & Community Solutions:**

- **[Better Auth](https://www.better-auth.com/)** - Modern, TypeScript-first authentication library
- **[Auth.js](https://authjs.dev/)** (formerly NextAuth.js) - Popular authentication library for React

**Hosted Services:**

- **[Supabase Auth](https://supabase.com/auth)** - Open source Firebase alternative with built-in auth
- **[Auth0](https://auth0.com/)** - Established authentication platform with extensive features
- **[Firebase Auth](https://firebase.google.com/docs/auth)** - Google's authentication service

## Partner Solutions

### WorkOS - Enterprise Authentication

<a href="https://workos.com/" alt="WorkOS Logo">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/workos-logo-dark.svg" width="280">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/workos-logo-light.svg" width="280">
    <img alt="WorkOS logo" src="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/workos-logo-light.svg" width="280">
  </picture>
</a>

- **Single Sign-On (SSO)** - SAML, OIDC, and OAuth integrations
- **Directory Sync** - SCIM provisioning with Active Directory and Google Workspace
- **Multi-factor Authentication** - Enterprise-grade security options
- **Compliance Ready** - SOC 2, GDPR, and CCPA compliant

[Visit WorkOS →](https://workos.com/) | [View example →](https://github.com/TanStack/router/tree/main/examples/react/start-workos)

### Clerk - Complete Authentication Platform

<a href="https://go.clerk.com/wOwHtuJ" alt="Clerk Logo">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/clerk-logo-dark.svg" width="280">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/clerk-logo-light.svg" width="280">
    <img alt="Clerk logo" src="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/clerk-logo-light.svg" width="280">
  </picture>
</a>

- **Ready-to-use UI Components** - Sign-in, sign-up, user profile, and organization management
- **Social Logins** - Google, GitHub, Discord, and 20+ providers
- **Multi-factor Authentication** - SMS, TOTP, and backup codes
- **Organizations & Teams** - Built-in support for team-based applications

[Visit Clerk →](https://go.clerk.com/wOwHtuJ) | [Sign up free →](https://go.clerk.com/PrSDXti) | [View example →](https://github.com/TanStack/router/tree/main/examples/react/start-clerk-basic)

## Examples

**Partner Solutions:**

- [Clerk Integration](https://github.com/TanStack/router/tree/main/examples/react/start-clerk-basic)
- [WorkOS Integration](https://github.com/TanStack/router/tree/main/examples/react/start-workos)

**DIY Implementations:**

- [Basic Auth with Prisma](https://github.com/TanStack/router/tree/main/examples/react/start-basic-auth)
- [Supabase Auth](https://github.com/TanStack/router/tree/main/examples/react/start-supabase-basic)

**Client-Side Examples:**

- [Basic Authentication](https://github.com/TanStack/router/tree/main/examples/react/authenticated-routes)
- [Firebase Auth](https://github.com/TanStack/router/tree/main/examples/react/authenticated-routes-firebase)

## Architecture Decision Guide

### Choosing an Authentication Approach

**Partner Solutions:**

- Focus on your core business logic
- Enterprise features (SSO, compliance)
- Managed security and updates
- Pre-built UI components

**OSS Solutions:**

- Community-driven development
- Specific customizations
- Self-hosted solutions
- Avoid vendor lock-in

**DIY Implementation:**

- Complete control over the auth flow
- Custom security requirements
- Specific business logic needs
- Full ownership of authentication data

### Security Considerations

- Use HTTPS in production
- Use HTTP-only cookies when possible
- Validate all inputs on the server
- Keep secrets in server-only functions
- Implement rate limiting for auth endpoints
- Use CSRF protection for form submissions

## Next Steps

- **Partner solutions** → [Clerk](https://go.clerk.com/wOwHtuJ) or [WorkOS](https://workos.com/)
- **DIY implementation** → [Authentication Guide](../authentication.md)
- **Examples** → [Working implementations](https://github.com/TanStack/router/tree/main/examples/react)

## Resources

**Implementation Guides:**

- [Authentication Patterns](../authentication.md)
- [Router Authentication Guide](/router/latest/docs/framework/react/guide/authenticated-routes.md)

**Foundation Concepts:**

- [Execution Model](../execution-model.md)
- [Server Functions](../server-functions.md)

**Step-by-Step Tutorials:**

- [Router How-to Guides](/router/latest/docs/framework/react/how-to/README.md#authentication)
---
id: authentication
title: Authentication
---

This guide covers authentication patterns and shows how to implement your own authentication system with TanStack Start.

> **📋 Before You Start:** Check our [Authentication Overview](../authentication-overview.md) for all available options including partner solutions and hosted services.

## Authentication Approaches

You have several options for authentication in your TanStack Start application:

**Hosted Solutions:**

1. **[Clerk](https://clerk.dev)** - Complete authentication platform with UI components
2. **[WorkOS](https://workos.com)** - Enterprise-focused with SSO and compliance features
3. **[Better Auth](https://www.better-auth.com/)** - Open-source TypeScript library

**DIY Implementation Benefits:**

- **Full Control**: Complete customization over authentication flow
- **No Vendor Lock-in**: Own your authentication logic and user data
- **Custom Requirements**: Implement specific business logic or compliance needs
- **Cost Control**: No per-user pricing or usage limits

Authentication involves many considerations including password security, session management, rate limiting, CSRF protection, and various attack vectors.

## Core Concepts

### Authentication vs Authorization

- **Authentication**: Who is this user? (Login/logout)
- **Authorization**: What can this user do? (Permissions/roles)

TanStack Start provides the tools for both through server functions, sessions, and route protection.

## Essential Building Blocks

### 1. Server Functions for Authentication

Server functions handle sensitive authentication logic securely on the server:

```tsx
import { createServerFn } from '@tanstack/react-start'
import { redirect } from '@tanstack/react-router'

// Login server function
export const loginFn = createServerFn({ method: 'POST' })
  .inputValidator((data: { email: string; password: string }) => data)
  .handler(async ({ data }) => {
    // Verify credentials (replace with your auth logic)
    const user = await authenticateUser(data.email, data.password)

    if (!user) {
      return { error: 'Invalid credentials' }
    }

    // Create session
    const session = await useAppSession()
    await session.update({
      userId: user.id,
      email: user.email,
    })

    // Redirect to protected area
    throw redirect({ to: '/dashboard' })
  })

// Logout server function
export const logoutFn = createServerFn({ method: 'POST' }).handler(async () => {
  const session = await useAppSession()
  await session.clear()
  throw redirect({ to: '/' })
})

// Get current user
export const getCurrentUserFn = createServerFn({ method: 'GET' }).handler(
  async () => {
    const session = await useAppSession()
    const userId = session.data.userId

    if (!userId) {
      return null
    }

    return await getUserById(userId)
  },
)
```

### 2. Session Management

TanStack Start provides secure HTTP-only cookie sessions:

```tsx
// utils/session.ts
import { useSession } from '@tanstack/react-start/server'

type SessionData = {
  userId?: string
  email?: string
  role?: string
}

export function useAppSession() {
  return useSession<SessionData>({
    // Session configuration
    name: 'app-session',
    password: process.env.SESSION_SECRET!, // At least 32 characters
    // Optional: customize cookie settings
    cookie: {
      secure: process.env.NODE_ENV === 'production',
      sameSite: 'lax',
      httpOnly: true,
    },
  })
}
```

### 3. Authentication Context

Share authentication state across your application:

```tsx
// contexts/auth.tsx
import { createContext, useContext, ReactNode } from 'react'
import { useServerFn } from '@tanstack/react-start'
import { getCurrentUserFn } from '../server/auth'

type User = {
  id: string
  email: string
  role: string
}

type AuthContextType = {
  user: User | null
  isLoading: boolean
  refetch: () => void
}

const AuthContext = createContext<AuthContextType | undefined>(undefined)

export function AuthProvider({ children }: { children: ReactNode }) {
  const { data: user, isLoading, refetch } = useServerFn(getCurrentUserFn)

  return (
    <AuthContext.Provider value={{ user, isLoading, refetch }}>
      {children}
    </AuthContext.Provider>
  )
}

export function useAuth() {
  const context = useContext(AuthContext)
  if (!context) {
    throw new Error('useAuth must be used within AuthProvider')
  }
  return context
}
```

### 4. Route Protection

Protect routes using `beforeLoad`:

```tsx
// routes/_authed.tsx - Layout route for protected pages
import { createFileRoute, redirect } from '@tanstack/react-router'
import { getCurrentUserFn } from '../server/auth'

export const Route = createFileRoute('/_authed')({
  beforeLoad: async ({ location }) => {
    const user = await getCurrentUserFn()

    if (!user) {
      throw redirect({
        to: '/login',
        search: { redirect: location.href },
      })
    }

    // Pass user to child routes
    return { user }
  },
})
```

```tsx
// routes/_authed/dashboard.tsx - Protected route
import { createFileRoute } from '@tanstack/react-router'

export const Route = createFileRoute('/_authed/dashboard')({
  component: DashboardComponent,
})

function DashboardComponent() {
  const { user } = Route.useRouteContext()

  return (
    <div>
      <h1>Welcome, {user.email}!</h1>
      {/* Dashboard content */}
    </div>
  )
}
```

## Implementation Patterns

### Basic Email/Password Authentication

```tsx
// server/auth.ts
import bcrypt from 'bcryptjs'
import { createServerFn } from '@tanstack/react-start'

// User registration
export const registerFn = createServerFn({ method: 'POST' })
  .inputValidator(
    (data: { email: string; password: string; name: string }) => data,
  )
  .handler(async ({ data }) => {
    // Check if user exists
    const existingUser = await getUserByEmail(data.email)
    if (existingUser) {
      return { error: 'User already exists' }
    }

    // Hash password
    const hashedPassword = await bcrypt.hash(data.password, 12)

    // Create user
    const user = await createUser({
      email: data.email,
      password: hashedPassword,
      name: data.name,
    })

    // Create session
    const session = await useAppSession()
    await session.update({ userId: user.id })

    return { success: true, user: { id: user.id, email: user.email } }
  })

async function authenticateUser(email: string, password: string) {
  const user = await getUserByEmail(email)
  if (!user) return null

  const isValid = await bcrypt.compare(password, user.password)
  return isValid ? user : null
}
```

### Role-Based Access Control (RBAC)

```tsx
// utils/auth.ts
export const roles = {
  USER: 'user',
  ADMIN: 'admin',
  MODERATOR: 'moderator',
} as const

type Role = (typeof roles)[keyof typeof roles]

export function hasPermission(userRole: Role, requiredRole: Role): boolean {
  const hierarchy = {
    [roles.USER]: 0,
    [roles.MODERATOR]: 1,
    [roles.ADMIN]: 2,
  }

  return hierarchy[userRole] >= hierarchy[requiredRole]
}

// Protected route with role check
export const Route = createFileRoute('/_authed/admin/')({
  beforeLoad: async ({ context }) => {
    if (!hasPermission(context.user.role, roles.ADMIN)) {
      throw redirect({ to: '/unauthorized' })
    }
  },
})
```

### Social Authentication Integration

```tsx
// Example with OAuth providers
export const authProviders = {
  google: {
    clientId: process.env.GOOGLE_CLIENT_ID!,
    redirectUri: `${process.env.APP_URL}/auth/google/callback`,
  },
  github: {
    clientId: process.env.GITHUB_CLIENT_ID!,
    redirectUri: `${process.env.APP_URL}/auth/github/callback`,
  },
}

export const initiateOAuthFn = createServerFn({ method: 'POST' })
  .inputValidator((data: { provider: 'google' | 'github' }) => data)
  .handler(async ({ data }) => {
    const provider = authProviders[data.provider]
    const state = generateRandomState()

    // Store state in session for CSRF protection
    const session = await useAppSession()
    await session.update({ oauthState: state })

    // Generate OAuth URL
    const authUrl = generateOAuthUrl(provider, state)

    throw redirect({ href: authUrl })
  })
```

### Password Reset Flow

```tsx
// Password reset request
export const requestPasswordResetFn = createServerFn({ method: 'POST' })
  .inputValidator((data: { email: string }) => data)
  .handler(async ({ data }) => {
    const user = await getUserByEmail(data.email)
    if (!user) {
      // Don't reveal if email exists
      return { success: true }
    }

    const token = generateSecureToken()
    const expires = new Date(Date.now() + 60 * 60 * 1000) // 1 hour

    await savePasswordResetToken(user.id, token, expires)
    await sendPasswordResetEmail(user.email, token)

    return { success: true }
  })

// Password reset confirmation
export const resetPasswordFn = createServerFn({ method: 'POST' })
  .inputValidator((data: { token: string; newPassword: string }) => data)
  .handler(async ({ data }) => {
    const resetToken = await getPasswordResetToken(data.token)

    if (!resetToken || resetToken.expires < new Date()) {
      return { error: 'Invalid or expired token' }
    }

    const hashedPassword = await bcrypt.hash(data.newPassword, 12)
    await updateUserPassword(resetToken.userId, hashedPassword)
    await deletePasswordResetToken(data.token)

    return { success: true }
  })
```

## Security Best Practices

### 1. Password Security

```tsx
// Use strong hashing (bcrypt, scrypt, or argon2)
import bcrypt from 'bcryptjs'

const saltRounds = 12 // Adjust based on your security needs
const hashedPassword = await bcrypt.hash(password, saltRounds)
```

### 2. Session Security

```tsx
// Use secure session configuration
export function useAppSession() {
  return useSession({
    name: 'app-session',
    password: process.env.SESSION_SECRET!, // 32+ characters
    cookie: {
      secure: process.env.NODE_ENV === 'production', // HTTPS only in production
      sameSite: 'lax', // CSRF protection
      httpOnly: true, // XSS protection
      maxAge: 7 * 24 * 60 * 60, // 7 days
    },
  })
}
```

### 3. Rate Limiting

```tsx
// Simple in-memory rate limiting (use Redis in production)
const loginAttempts = new Map<string, { count: number; resetTime: number }>()

export const rateLimitLogin = (ip: string): boolean => {
  const now = Date.now()
  const attempts = loginAttempts.get(ip)

  if (!attempts || now > attempts.resetTime) {
    loginAttempts.set(ip, { count: 1, resetTime: now + 15 * 60 * 1000 }) // 15 min
    return true
  }

  if (attempts.count >= 5) {
    return false // Too many attempts
  }

  attempts.count++
  return true
}
```

### 4. Input Validation

```tsx
import { z } from 'zod'

const loginSchema = z.object({
  email: z.string().email().max(255),
  password: z.string().min(8).max(100),
})

export const loginFn = createServerFn({ method: 'POST' })
  .inputValidator((data) => loginSchema.parse(data))
  .handler(async ({ data }) => {
    // data is now validated
  })
```

## Testing Authentication

### Unit Testing Server Functions

```tsx
// __tests__/auth.test.ts
import { describe, it, expect, beforeEach } from 'vitest'
import { loginFn } from '../server/auth'

describe('Authentication', () => {
  beforeEach(async () => {
    await setupTestDatabase()
  })

  it('should login with valid credentials', async () => {
    const result = await loginFn({
      data: { email: 'test@example.com', password: 'password123' },
    })

    expect(result.error).toBeUndefined()
    expect(result.user).toBeDefined()
  })

  it('should reject invalid credentials', async () => {
    const result = await loginFn({
      data: { email: 'test@example.com', password: 'wrongpassword' },
    })

    expect(result.error).toBe('Invalid credentials')
  })
})
```

### Integration Testing

```tsx
// __tests__/auth-flow.test.tsx
import { render, screen, fireEvent, waitFor } from '@testing-library/react'
import { RouterProvider, createMemoryHistory } from '@tanstack/react-router'
import { router } from '../router'

describe('Authentication Flow', () => {
  it('should redirect to login when accessing protected route', async () => {
    const history = createMemoryHistory()
    history.push('/dashboard') // Protected route

    render(<RouterProvider router={router} history={history} />)

    await waitFor(() => {
      expect(screen.getByText('Login')).toBeInTheDocument()
    })
  })
})
```

## Common Patterns

### Loading States

```tsx
function LoginForm() {
  const [isLoading, setIsLoading] = useState(false)
  const loginMutation = useServerFn(loginFn)

  const handleSubmit = async (data: LoginData) => {
    setIsLoading(true)
    try {
      await loginMutation.mutate(data)
    } catch (error) {
      // Handle error
    } finally {
      setIsLoading(false)
    }
  }

  return (
    <form onSubmit={handleSubmit}>
      {/* Form fields */}
      <button disabled={isLoading}>
        {isLoading ? 'Logging in...' : 'Login'}
      </button>
    </form>
  )
}
```

### Remember Me Functionality

```tsx
export const loginFn = createServerFn({ method: 'POST' })
  .inputValidator(
    (data: { email: string; password: string; rememberMe?: boolean }) => data,
  )
  .handler(async ({ data }) => {
    const user = await authenticateUser(data.email, data.password)
    if (!user) return { error: 'Invalid credentials' }

    const session = await useAppSession()
    await session.update(
      { userId: user.id },
      {
        // Extend session if remember me is checked
        maxAge: data.rememberMe ? 30 * 24 * 60 * 60 : undefined, // 30 days vs session
      },
    )

    return { success: true }
  })
```

## Working Examples

Study these implementations to understand different authentication patterns:

- **[Basic Auth with Prisma](https://github.com/TanStack/router/tree/main/examples/react/start-basic-auth)** - Complete DIY implementation with database and sessions
- **[Supabase Integration](https://github.com/TanStack/router/tree/main/examples/react/start-supabase-basic)** - Third-party service integration example
- **[Client-side Context Auth](https://github.com/TanStack/router/tree/main/examples/react/authenticated-routes)** - Client-only authentication patterns

## Migration from Other Solutions

### From Client-Side Auth

If you're migrating from client-side authentication (localStorage, context only):

1. Move authentication logic to server functions
2. Replace localStorage with server sessions
3. Update route protection to use `beforeLoad`
4. Add proper security headers and CSRF protection

### From Other Frameworks

- **Next.js**: Replace API routes with server functions, migrate NextAuth sessions
- **Remix**: Convert loaders/actions to server functions, adapt session patterns
- **SvelteKit**: Move form actions to server functions, update route protection

## Production Considerations

When choosing your authentication approach, consider these factors:

### Hosted vs DIY Comparison

**Hosted Solutions (Clerk, WorkOS, Better Auth):**

- Pre-built security measures and regular updates
- UI components and user management features
- Compliance certifications and audit trails
- Support and documentation
- Per-user or subscription pricing

**DIY Implementation:**

- Complete control over implementation and data
- No ongoing subscription costs
- Custom business logic and workflows
- Responsibility for security updates and monitoring
- Need to handle edge cases and attack vectors

### Security Considerations

Authentication systems need to handle various security aspects:

- Password hashing and timing attack prevention
- Session management and fixation protection
- CSRF and XSS protection
- Rate limiting and brute force prevention
- OAuth flow security
- Compliance requirements (GDPR, CCPA, etc.)

## Next Steps

When implementing authentication, consider:

- **Security Review**: Review your implementation for security best practices
- **Performance**: Add caching for user lookups and session validation
- **Monitoring**: Add logging and monitoring for authentication events
- **Compliance**: Ensure compliance with relevant regulations if storing personal data

For other authentication approaches, check the [Authentication Overview](../authentication-overview.md). For specific integration help, explore our [working examples](https://github.com/TanStack/router/tree/main/examples/react).
---
id: databases
title: Databases
---

Databases are at the core of any dynamic application, providing the necessary infrastructure to store, retrieve, and manage data. TanStack Start makes it easy to integrate with a variety of databases, offering a flexible approach to managing your application's data layer.

## What should I use?

TanStack Start is **designed to work with any database provider**, so if you already have a preferred database system, you can integrate it with TanStack Start using the provided full-stack APIs. Whether you're working with SQL, NoSQL, or other types of databases, TanStack Start can handle your needs.

## How simple is it to use a database with TanStack Start?

Using a database with TanStack Start is as simple as calling into your database's adapter/client/driver/service from a TanStack Start server function or server route.

Here's an abstract example of how you might connect with a database and read/write to it:

```tsx
import { createServerFn } from '@tanstack/react-start'

const db = createMyDatabaseClient()

export const getUser = createServerFn(async ({ ctx }) => {
  const user = await db.getUser(ctx.userId)
  return user
})

export const createUser = createServerFn(async ({ ctx, input }) => {
  const user = await db.createUser(input)
  return user
})
```

This is obviously contrived, but it demonstrates that you can use literally any database provider with TanStack Start as long as you can call into it from a server function or server route.

## Recommended Database Providers

While TanStack Start is designed to work with any database provider, we highly recommend considering one of our vetted partner database providers [Neon](https://neon.tech?utm_source=tanstack) or [Convex](https://convex.dev?utm_source=tanstack). They have been vetted by TanStack to match our quality, openness, and performance standards and are both excellent choices for your database needs.

## What is Neon?

<a href="https://neon.tech?utm_source=tanstack" alt="Neon Logo">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/neon-dark.svg" width="280">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/neon-light.svg" width="280">
    <img alt="Neon logo" src="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/neon-light.svg" width="280">
  </picture>
</a>

Neon is a fully managed serverless PostgreSQL with a generous free tier. It separates storage and compute to offer autoscaling, branching, and bottomless storage. With Neon, you get all the power and reliability of PostgreSQL combined with modern cloud capabilities, making it perfect for TanStack Start applications.

Key features that make Neon stand out:

- Serverless PostgreSQL that scales automatically
- Database branching for development and testing
- Built-in connection pooling
- Point-in-time restore
- Web-based SQL editor
- Bottomless storage
  <br />
  <br />
- To learn more about Neon, visit the [Neon website](https://neon.tech?utm_source=tanstack)
- To sign up, visit the [Neon dashboard](https://console.neon.tech/signup?utm_source=tanstack)

## What is Convex?

<a href="https://convex.dev?utm_source=tanstack" alt="Convex Logo">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/convex-white.svg" width="280">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/convex-color.svg" width="280">
    <img alt="Convex logo" src="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/convex-color.svg" width="280">
  </picture>
</a>

Convex is a powerful, serverless database platform that simplifies the process of managing your application's data. With Convex, you can build full-stack applications without the need to manually manage database servers or write complex queries. Convex provides a real-time, scalable, and transactional data backend that seamlessly integrates with TanStack Start, making it an excellent choice for modern web applications.

Convex's declarative data model and automatic conflict resolution ensure that your application remains consistent and responsive, even at scale. It's designed to be developer-friendly, with a focus on simplicity and productivity.

- To learn more about Convex, visit the [Convex website](https://convex.dev?utm_source=tanstack)
- To sign up, visit the [Convex dashboard](https://dashboard.convex.dev/signup?utm_source=tanstack)

## What is Prisma Postgres?

<a href="https://www.prisma.io?utm_source=tanstack&via=tanstack" alt="Prisma Logo">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/prisma-dark.svg" width="280">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/prisma-light.svg" width="280">
    <img alt="Prisma logo" src="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/prisma-light.svg" width="280">
  </picture>
</a>

Instant Postgres, Zero Setup: Get a production-ready Postgres database in seconds, then dive straight back into code. We handle connections, scaling, and turning knobs so your flow never breaks. Blends perfectly with TanStack Start.

- Edge-optimized: Local region routing means lower latency and fewer hops. Even complex queries are one fast round trip.
- Fits your stack: Works with your frameworks, libraries, and tools for a smooth DX.
- Web UI: A hosted interface to inspect, manage, and query data with your team.
- Auto-scaling: Grows from zero to millions of users without cold starts or manual tuning.
- Unikernel isolation: Each DB runs as its own unikernel for security, speed, and efficiency.
  <br />
  <br />
- To learn more about Prisma Postgres, visit the [Prisma website](https://www.prisma.io?utm_source=tanstack&via=tanstack)
- To sign up, visit the [Prisma Console](https://console.prisma.io/sign-up?utm_source=tanstack&via=tanstack)

## Documentation & APIs

Documentation for integrating different databases with TanStack Start is coming soon! In the meantime, keep an eye on our examples and guide to learn how to fully leverage your data layer across your TanStack Start application.
---
id: observability
title: Observability
---

Observability is a critical aspect of modern web development, enabling you to monitor, trace, and debug your application's performance and errors. TanStack Start provides built-in patterns for observability and integrates seamlessly with external tools to give you comprehensive insights into your application.

## Partner Solution: Sentry

<a href="https://sentry.io?utm_source=tanstack" alt='Sentry Logo'>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/sentry-wordmark-light.svg" width="280">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/sentry-wordmark-dark.svg" width="280">
    <img alt="Sentry logo" src="https://raw.githubusercontent.com/tanstack/tanstack.com/main/src/images/sentry-wordmark-light.svg" width="280">
  </picture>
</a>

For comprehensive observability, we recommend [Sentry](https://sentry.io?utm_source=tanstack) - our trusted partner for error tracking and performance monitoring. Sentry provides:

- **Real-time Error Tracking** - Catch and debug errors across your entire stack
- **Performance Monitoring** - Track slow transactions and optimize bottlenecks
- **Release Health** - Monitor deployments and track error rates over time
- **User Impact Analysis** - Understand how errors affect your users
- **TanStack Start Integration** - Works seamlessly with server functions and client code

**Quick Setup:**

```tsx
// Client-side (app.tsx)
import * as Sentry from '@sentry/react'

Sentry.init({
  dsn: import.meta.env.VITE_SENTRY_DSN,
  environment: import.meta.env.NODE_ENV,
})

// Server functions
import * as Sentry from '@sentry/node'

const serverFn = createServerFn().handler(async () => {
  try {
    return await riskyOperation()
  } catch (error) {
    Sentry.captureException(error)
    throw error
  }
})
```

[Get started with Sentry →](https://sentry.io/signup?utm_source=tanstack) | [View integration example →](https://github.com/TanStack/router/tree/main/e2e/react-router/sentry-integration)

## Built-in Observability Patterns

TanStack Start's architecture provides several opportunities for built-in observability without external dependencies:

### Server Function Logging

Add logging to your server functions to track execution, performance, and errors:

```tsx
import { createServerFn } from '@tanstack/react-start'

const getUser = createServerFn({ method: 'GET' })
  .inputValidator((id: string) => id)
  .handler(async ({ data: id }) => {
    const startTime = Date.now()

    try {
      console.log(`[SERVER] Fetching user ${id}`)

      const user = await db.users.findUnique({ where: { id } })

      if (!user) {
        console.log(`[SERVER] User ${id} not found`)
        throw new Error('User not found')
      }

      const duration = Date.now() - startTime
      console.log(`[SERVER] User ${id} fetched in ${duration}ms`)

      return user
    } catch (error) {
      const duration = Date.now() - startTime
      console.error(
        `[SERVER] Error fetching user ${id} after ${duration}ms:`,
        error,
      )
      throw error
    }
  })
```

### Request/Response Middleware

Create middleware to log all requests and responses:

```tsx
import { createMiddleware } from '@tanstack/react-start'

const requestLogger = createMiddleware().handler(async ({ next }) => {
  const startTime = Date.now()
  const timestamp = new Date().toISOString()

  console.log(`[${timestamp}] ${request.method} ${request.url} - Starting`)

  try {
    const response = await next()
    const duration = Date.now() - startTime

    console.log(
      `[${timestamp}] ${request.method} ${request.url} - ${response.status} (${duration}ms)`,
    )

    return response
  } catch (error) {
    const duration = Date.now() - startTime
    console.error(
      `[${timestamp}] ${request.method} ${request.url} - Error (${duration}ms):`,
      error,
    )
    throw error
  }
})

// Apply to all server routes
export const Route = createFileRoute('/api/users')({
  server: {
    middleware: [requestLogger],
    handlers: {
      GET: async () => {
        return json({ users: await getUsers() })
      },
    },
  },
})
```

### Route Performance Monitoring

Track route loading performance on both client and server:

```tsx
import { createFileRoute } from '@tanstack/react-router'

export const Route = createFileRoute('/dashboard')({
  loader: async ({ context }) => {
    const startTime = Date.now()

    try {
      const data = await loadDashboardData()
      const duration = Date.now() - startTime

      // Log server-side performance
      if (typeof window === 'undefined') {
        console.log(`[SSR] Dashboard loaded in ${duration}ms`)
      }

      return data
    } catch (error) {
      const duration = Date.now() - startTime
      console.error(`[LOADER] Dashboard error after ${duration}ms:`, error)
      throw error
    }
  },
  component: Dashboard,
})

function Dashboard() {
  const data = Route.useLoaderData()

  // Track client-side render time
  React.useEffect(() => {
    const renderTime = performance.now()
    console.log(`[CLIENT] Dashboard rendered in ${renderTime}ms`)
  }, [])

  return <div>Dashboard content</div>
}
```

### Health Check Endpoints

Create server routes for health monitoring:

```tsx
// routes/health.ts
import { createFileRoute } from '@tanstack/react-router'
import { json } from '@tanstack/react-start'

export const Route = createFileRoute('/health')({
  server: {
    handlers: {
      GET: async () => {
        const checks = {
          status: 'healthy',
          timestamp: new Date().toISOString(),
          uptime: process.uptime(),
          memory: process.memoryUsage(),
          database: await checkDatabase(),
          version: process.env.npm_package_version,
        }

        return json(checks)
      },
    },
  },
})

async function checkDatabase() {
  try {
    await db.raw('SELECT 1')
    return { status: 'connected', latency: 0 }
  } catch (error) {
    return { status: 'error', error: error.message }
  }
}
```

### Error Boundaries

Implement comprehensive error handling:

```tsx
// Client-side error boundary
import { ErrorBoundary } from 'react-error-boundary'

function ErrorFallback({ error, resetErrorBoundary }: any) {
  // Log client errors
  console.error('[CLIENT ERROR]:', error)

  // Could also send to external service
  // sendErrorToService(error)

  return (
    <div role="alert">
      <h2>Something went wrong</h2>
      <button onClick={resetErrorBoundary}>Try again</button>
    </div>
  )
}

export function App() {
  return (
    <ErrorBoundary FallbackComponent={ErrorFallback}>
      <Router />
    </ErrorBoundary>
  )
}

// Server function error handling
const riskyOperation = createServerFn().handler(async () => {
  try {
    return await performOperation()
  } catch (error) {
    // Log server errors with context
    console.error('[SERVER ERROR]:', {
      error: error.message,
      stack: error.stack,
      timestamp: new Date().toISOString(),
      // Add request context if available
    })

    // Return user-friendly error
    throw new Error('Operation failed. Please try again.')
  }
})
```

### Performance Metrics Collection

Collect and expose basic performance metrics:

```tsx
// utils/metrics.ts
class MetricsCollector {
  private metrics = new Map<string, number[]>()

  recordTiming(name: string, duration: number) {
    if (!this.metrics.has(name)) {
      this.metrics.set(name, [])
    }
    this.metrics.get(name)!.push(duration)
  }

  getStats(name: string) {
    const timings = this.metrics.get(name) || []
    if (timings.length === 0) return null

    const sorted = timings.sort((a, b) => a - b)
    return {
      count: timings.length,
      avg: timings.reduce((a, b) => a + b, 0) / timings.length,
      p50: sorted[Math.floor(sorted.length * 0.5)],
      p95: sorted[Math.floor(sorted.length * 0.95)],
      min: sorted[0],
      max: sorted[sorted.length - 1],
    }
  }

  getAllStats() {
    const stats: Record<string, any> = {}
    for (const [name] of this.metrics) {
      stats[name] = this.getStats(name)
    }
    return stats
  }
}

export const metrics = new MetricsCollector()

// Metrics endpoint
// routes/metrics.ts
export const Route = createFileRoute('/metrics')({
  server: {
    handlers: {
      GET: async () => {
        return json({
          system: {
            uptime: process.uptime(),
            memory: process.memoryUsage(),
            timestamp: new Date().toISOString(),
          },
          application: metrics.getAllStats(),
        })
      },
    },
  },
})
```

### Debug Headers for Development

Add helpful debug information to responses:

```tsx
import { createMiddleware } from '@tanstack/react-start'

const debugMiddleware = createMiddleware().handler(async ({ next }) => {
  const response = await next()

  if (process.env.NODE_ENV === 'development') {
    response.headers.set('X-Debug-Timestamp', new Date().toISOString())
    response.headers.set('X-Debug-Node-Version', process.version)
    response.headers.set('X-Debug-Uptime', process.uptime().toString())
  }

  return response
})
```

### Environment-Specific Logging

Configure different logging strategies for development vs production:

```tsx
// utils/logger.ts
import { createIsomorphicFn } from '@tanstack/react-start'

type LogLevel = 'debug' | 'info' | 'warn' | 'error'

const logger = createIsomorphicFn()
  .server((level: LogLevel, message: string, data?: any) => {
    const timestamp = new Date().toISOString()

    if (process.env.NODE_ENV === 'development') {
      // Development: Detailed console logging
      console[level](`[${timestamp}] [${level.toUpperCase()}]`, message, data)
    } else {
      // Production: Structured JSON logging
      console.log(
        JSON.stringify({
          timestamp,
          level,
          message,
          data,
          service: 'tanstack-start',
          environment: process.env.NODE_ENV,
        }),
      )
    }
  })
  .client((level: LogLevel, message: string, data?: any) => {
    if (process.env.NODE_ENV === 'development') {
      console[level](`[CLIENT] [${level.toUpperCase()}]`, message, data)
    } else {
      // Production: Send to analytics service
      // analytics.track('client_log', { level, message, data })
    }
  })

// Usage anywhere in your app
export { logger }

// Example usage
const fetchUserData = createServerFn().handler(async ({ data: userId }) => {
  logger('info', 'Fetching user data', { userId })

  try {
    const user = await db.users.findUnique({ where: { id: userId } })
    logger('info', 'User data fetched successfully', { userId })
    return user
  } catch (error) {
    logger('error', 'Failed to fetch user data', {
      userId,
      error: error.message,
    })
    throw error
  }
})
```

### Simple Error Reporting

Basic error reporting without external dependencies:

```tsx
// utils/error-reporter.ts
const errorStore = new Map<
  string,
  { count: number; lastSeen: Date; error: any }
>()

export function reportError(error: Error, context?: any) {
  const key = `${error.name}:${error.message}`
  const existing = errorStore.get(key)

  if (existing) {
    existing.count++
    existing.lastSeen = new Date()
  } else {
    errorStore.set(key, {
      count: 1,
      lastSeen: new Date(),
      error: {
        name: error.name,
        message: error.message,
        stack: error.stack,
        context,
      },
    })
  }

  // Log immediately
  console.error('[ERROR REPORTED]:', {
    error: error.message,
    count: existing ? existing.count : 1,
    context,
  })
}

// Error reporting endpoint
// routes/errors.ts
export const Route = createFileRoute('/admin/errors')({
  server: {
    handlers: {
      GET: async () => {
        const errors = Array.from(errorStore.entries()).map(([key, data]) => ({
          id: key,
          ...data,
        }))

        return json({ errors })
      },
    },
  },
})
```

## External Observability Tools

While TanStack Start provides built-in observability patterns, external tools offer more comprehensive monitoring:

### Other Popular Tools

**Application Performance Monitoring:**

- **[DataDog](https://www.datadoghq.com/)** - Full-stack monitoring with APM
- **[New Relic](https://newrelic.com/)** - Performance monitoring and alerting
- **[Honeycomb](https://honeycomb.io/)** - Observability for complex systems

**Error Tracking:**

- **[Bugsnag](https://bugsnag.com/)** - Error monitoring with deployment tracking
- **[Rollbar](https://rollbar.com/)** - Real-time error alerting

**Analytics & User Behavior:**

- **[PostHog](https://posthog.com/)** - Product analytics with error tracking
- **[Mixpanel](https://mixpanel.com/)** - Event tracking and user analytics

### New Relic Integration

[New Relic](https://newrelic.com/) is a popular application performance monitoring tool. Here's how to integrate it with TanStack Start.

#### SSR

To enable New Relic for server-side rendering, you will need to do the following:

Create a new integration on New Relic of type `Node`. You will be given a license key that we will use below.

```js
// newrelic.js - New Relic agent configuration
exports.config = {
  app_name: ['YourTanStackApp'], // Your application name in New Relic
  license_key: 'YOUR_NEW_RELIC_LICENSE_KEY', // Your New Relic license key
  agent_enabled: true,
  distributed_tracing: { enabled: true },
  span_events: { enabled: true },
  transaction_events: { enabled: true },
  // Additional default settings
}
```

```tsx
// server.tsx
import newrelic from 'newrelic' // Make sure this is the first import
import {
  createStartHandler,
  defaultStreamHandler,
  defineHandlerCallback,
} from '@tanstack/react-start/server'
import type { ServerEntry } from '@tanstack/react-start/server-entry'

const customHandler = defineHandlerCallback(async (ctx) => {
  // We do this so that transactions are grouped under the route ID instead of unique URLs
  const matches = ctx.router?.state?.matches ?? []
  const leaf = matches[matches.length - 1]
  const routeId = leaf?.routeId ?? new URL(ctx.request.url).pathname

  newrelic.setControllerName(routeId, ctx.request.method ?? 'GET')
  newrelic.addCustomAttributes({
    'route.id': routeId,
    'http.method': ctx.request.method,
    'http.path': new URL(ctx.request.url).pathname,
    // Any other custom attributes you want to add
  })

  return defaultStreamHandler(ctx)
})

export default {
  fetch(request) {
    const handler = createStartHandler(customHandler)
    return handler(request)
  },
} satisfies ServerEntry
```

```bash
node -r newrelic .output/server/index.mjs
```

#### Server Functions and Server Routes

If you want to add monitoring for server functions and server routes, you will need to follow the steps above, and then add the following:

```ts
// newrelic-middleware.ts
import newrelic from 'newrelic'
import { createMiddleware } from '@tanstack/react-start'

export const nrTransactionMiddleware = createMiddleware().server(
  async ({ request, next }) => {
    const reqPath = new URL(request.url).pathname
    newrelic.setControllerName(reqPath, request.method ?? 'GET')
    return await next()
  },
)
```

```ts
// start.ts
import { createStart } from '@tanstack/react-start'
import { nrTransactionMiddleware } from './newrelic-middleware'

export const startInstance = createStart(() => {
  return {
    requestMiddleware: [nrTransactionMiddleware],
  }
})
```

#### SPA & Browser

Create a new integration on New Relic of type `React`.

After you set it up, you will have to add the integration script that New Relic provides you with to your root route.

```tsx
// __root.tsx
export const Route = createRootRoute({
  head: () => ({
    scripts: [
      {
        id: 'new-relic',

        // either copy/paste your New Relic integration script here
        children: `...`,

        // or you can create it in your public folder and then reference it here
        src: '/newrelic.js',
      },
    ],
  }),
})
```

### OpenTelemetry Integration (Experimental)

[OpenTelemetry](https://opentelemetry.io/) is the industry standard for observability. Here's an experimental approach to integrate it with TanStack Start:

```tsx
// instrumentation.ts - Initialize before your app
import { NodeSDK } from '@opentelemetry/sdk-node'
import { getNodeAutoInstrumentations } from '@opentelemetry/auto-instrumentations-node'
import { Resource } from '@opentelemetry/resources'
import { SemanticResourceAttributes } from '@opentelemetry/semantic-conventions'

const sdk = new NodeSDK({
  resource: new Resource({
    [SemanticResourceAttributes.SERVICE_NAME]: 'tanstack-start-app',
    [SemanticResourceAttributes.SERVICE_VERSION]: '1.0.0',
  }),
  instrumentations: [getNodeAutoInstrumentations()],
})

// Initialize BEFORE importing your app
sdk.start()
```

```tsx
// Server function tracing
import { trace, SpanStatusCode } from '@opentelemetry/api'

const tracer = trace.getTracer('tanstack-start')

const getUserWithTracing = createServerFn({ method: 'GET' })
  .inputValidator((id: string) => id)
  .handler(async ({ data: id }) => {
    return tracer.startActiveSpan('get-user', async (span) => {
      span.setAttributes({
        'user.id': id,
        operation: 'database.query',
      })

      try {
        const user = await db.users.findUnique({ where: { id } })
        span.setStatus({ code: SpanStatusCode.OK })
        return user
      } catch (error) {
        span.recordException(error)
        span.setStatus({
          code: SpanStatusCode.ERROR,
          message: error.message,
        })
        throw error
      } finally {
        span.end()
      }
    })
  })
```

```tsx
// Middleware for automatic tracing
import { createMiddleware } from '@tanstack/react-start'
import { trace, SpanStatusCode } from '@opentelemetry/api'

const tracer = trace.getTracer('tanstack-start')

const tracingMiddleware = createMiddleware().handler(
  async ({ next, request }) => {
    const url = new URL(request.url)

    return tracer.startActiveSpan(
      `${request.method} ${url.pathname}`,
      async (span) => {
        span.setAttributes({
          'http.method': request.method,
          'http.url': request.url,
          'http.route': url.pathname,
        })

        try {
          const response = await next()
          span.setAttribute('http.status_code', response.status)
          span.setStatus({ code: SpanStatusCode.OK })
          return response
        } catch (error) {
          span.recordException(error)
          span.setStatus({
            code: SpanStatusCode.ERROR,
            message: error.message,
          })
          throw error
        } finally {
          span.end()
        }
      },
    )
  },
)
```

> **Note**: The above OpenTelemetry integration is experimental and requires manual setup. We're exploring first-class OpenTelemetry support that would provide automatic instrumentation for server functions, middleware, and route loaders.

### Quick Integration Pattern

Most observability tools follow a similar integration pattern with TanStack Start:

```tsx
// Initialize in app entry point
import { initObservabilityTool } from 'your-tool'

initObservabilityTool({
  dsn: import.meta.env.VITE_TOOL_DSN,
  environment: import.meta.env.NODE_ENV,
})

// Server function middleware
const observabilityMiddleware = createMiddleware().handler(async ({ next }) => {
  return yourTool.withTracing('server-function', async () => {
    try {
      return await next()
    } catch (error) {
      yourTool.captureException(error)
      throw error
    }
  })
})
```

## Best Practices

### Development vs Production

```tsx
// Different strategies per environment
const observabilityConfig = {
  development: {
    logLevel: 'debug',
    enableTracing: true,
    enableMetrics: false, // Too noisy in dev
  },
  production: {
    logLevel: 'warn',
    enableTracing: true,
    enableMetrics: true,
    enableAlerting: true,
  },
}
```

### Performance Monitoring Checklist

- [ ] **Server Function Performance**: Track execution times
- [ ] **Route Loading Times**: Monitor loader performance
- [ ] **Database Query Performance**: Log slow queries
- [ ] **External API Latency**: Monitor third-party service calls
- [ ] **Memory Usage**: Track memory consumption patterns
- [ ] **Error Rates**: Monitor error frequency and types

### Security Considerations

- Never log sensitive data (passwords, tokens, PII)
- Use structured logging for better parsing
- Implement log rotation in production
- Consider compliance requirements (GDPR, CCPA)

## Future OpenTelemetry Support

Direct OpenTelemetry support is coming to TanStack Start, which will provide automatic instrumentation for server functions, middleware, and route loaders without the manual setup shown above.

## Resources

- **[Sentry Documentation](https://docs.sentry.io/)**
- **[OpenTelemetry Documentation](https://opentelemetry.io/docs/)** - Industry standard observability
- **[Working Example](https://github.com/TanStack/router/tree/main/examples/react/start-basic)** - See observability patterns in action
---
id: path-aliases
title: Path Aliases
---

Path aliases are a useful feature of TypeScript that allows you to define a shortcut for a path that could be distant in your project's directory structure. This can help you avoid long relative imports in your code and make it easier to refactor your project's structure. This is especially useful for avoiding long relative imports in your code.

By default, TanStack Start does not include path aliases. However, you can easily add them to your project by updating your `tsconfig.json` file in the root of your project and adding the following configuration:

```json
{
  "compilerOptions": {
    "baseUrl": ".",
    "paths": {
      "~/*": ["./src/*"]
    }
  }
}
```

In this example, we've defined the path alias `~/*` that maps to the `./src/*` directory. This means that you can now import files from the `src` directory using the `~` prefix.

After updating your `tsconfig.json` file, you'll need to install the `vite-tsconfig-paths` plugin to enable path aliases in your TanStack Start project. You can do this by running the following command:

```sh
npm install -D vite-tsconfig-paths
```

Now, you'll need to update your `vite.config.ts` file to include the following:

```ts
// vite.config.ts
import { defineConfig } from 'vite'
import viteTsConfigPaths from 'vite-tsconfig-paths'

export default defineConfig({
  vite: {
    plugins: [
      // this is the plugin that enables path aliases
      viteTsConfigPaths({
        projects: ['./tsconfig.json'],
      }),
    ],
  },
})
```

Once this configuration has completed, you'll now be able to import files using the path alias like so:

```ts
// app/routes/posts/$postId/edit.tsx
import { Input } from '~/components/ui/input'

// instead of

import { Input } from '../../../components/ui/input'
```
---
id: tailwind-integration
title: Tailwind CSS Integration
---

_So you want to use Tailwind CSS in your TanStack Start project?_

This guide will help you use Tailwind CSS in your TanStack Start project.

## Tailwind CSS Version 4 (Latest)

The latest version of Tailwind CSS is 4. And it has some configuration changes that majorly differ from Tailwind CSS Version 3. It's **easier and recommended** to set up Tailwind CSS Version 4 in a TanStack Start project, as TanStack Start uses Vite as its build tool.

### Install Tailwind CSS

Install Tailwind CSS and it's Vite plugin.

```shell
npm install tailwindcss @tailwindcss/vite
```

### Configure The Vite Plugin

Add the `@tailwindcss/vite` plugin to your Vite configuration.

```ts
// vite.config.ts
import { defineConfig } from 'vite'
import tsConfigPaths from 'vite-tsconfig-paths'
import { tanstackStart } from '@tanstack/react-start/plugin/vite'
import tailwindcss from '@tailwindcss/vite'
import viteReact from '@vitejs/plugin-react'

export default defineConfig({
  server: {
    port: 3000,
  },
  plugins: [tsConfigPaths(), tanstackStart(), viteReact(), tailwindcss()],
})
```

### Import Tailwind in your CSS file

You need to create a CSS file to configure Tailwind CSS instead of the configuration file in version 4. You can do this by creating a `src/styles/app.css` file or name it whatever you want.

```css
/* src/styles/app.css */
@import 'tailwindcss';
```

## Import the CSS file in your `__root.tsx` file

Import the CSS file in your `__root.tsx` file with the `?url` query and make sure to add the **triple slash** directive to the top of the file.

```tsx
// src/routes/__root.tsx
/// <reference types="vite/client" />
// other imports...

import appCss from '../styles/app.css?url'

export const Route = createRootRoute({
  head: () => ({
    meta: [
      // your meta tags and site config
    ],
    links: [{ rel: 'stylesheet', href: appCss }],
    // other head config
  }),
  component: RootComponent,
})
```

## Use Tailwind CSS anywhere in your project

You can now use Tailwind CSS anywhere in your project.

```tsx
// src/routes/index.tsx
import { createFileRoute } from '@tanstack/react-router'

export const Route = createFileRoute('/')({
  component: Home,
})

function Home() {
  return <div className="bg-red-500 text-white p-4">Hello World</div>
}
```

That's it! You can now use Tailwind CSS anywhere in your project 🎉.

## Tailwind CSS Version 3 (Legacy)

If you are want to use Tailwind CSS Version 3, you can use the following steps.

### Install Tailwind CSS

Install Tailwind CSS and it's peer dependencies.

```shell
npm install -D tailwindcss@3 postcss autoprefixer
```

Then generate the Tailwind and PostCSS configuration files.

```shell
npx tailwindcss init -p
```

### Configure your template paths

Add the paths to all of your template files in the `tailwind.config.js` file.

```js
// tailwind.config.js
/** @type {import('tailwindcss').Config} */
export default {
  content: ['./src/**/*.{js,ts,jsx,tsx}'],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

### Add the Tailwind directives to your CSS file

Add the `@tailwind` directives for each of Tailwind's layers to your `src/styles/app.css` file.

```css
/* src/styles/app.css */
@tailwind base;
@tailwind components;
@tailwind utilities;
```

> [!NOTE]
> Jump to [Import the CSS file in your `__root.tsx` file](#import-the-css-file-in-your-__roottsx-file) to see how to import the CSS file in your `__root.tsx` file.
---
id: fetching-external-api
title: Calling an external API using TanStack Start
---

This guide demonstrates how to integrate external API calls into your TanStack Start application using route loaders. We will use TMDB API to fetch popular movies using TanStack Start and understand how to fetch data in a TanStack Start app.

The complete code for this tutorial is available on [GitHub](https://github.com/shrutikapoor08/tanstack-start-movies).

## What You'll Learn

1. Setting up external API integration with TanStack Start
2. Implementing route loaders for server-side data fetching
3. Building responsive UI components with fetched data
4. Handling loading states and error management

## Prerequisites

- Basic knowledge of React and TypeScript
- Node.js (v18+) and `pnpm` installed on your machine
- A TMDB API key (free at [themoviedb.org](https://www.themoviedb.org))

## Nice to know

- [TanStack Router](/router/latest/docs/framework/react/routing/routing-concepts)

## Setting up a TanStack Start Project

First, let's create a new TanStack Start project:

```bash
pnpx create-start-app movie-discovery
cd movie-discovery
```

When this script runs, it will ask you a few setup questions. You can either pick choices that work for you or just press enter to accept the defaults.

Optionally, you can pass in a `--add-on` flag to get options such as Shadcn, Clerk, Convex, TanStack Query, etc.

Once setup is complete, install dependencies and start the development server:

```bash
pnpm i
pnpm dev
```

## Understanding the Project Structure

At this point, the project structure should look like this:

```text
/movie-discovery
├── src/
│   ├── routes/
│   │   ├── __root.tsx                    # Root layout
│   │   ├── index.tsx                     # Home page
│   │   └── fetch-movies.tsx              # Movie fetching route
│   ├── types/
│   │   └── movie.ts                      # Movie type definitions
│   ├── router.tsx                        # Router configuration
│   ├── routeTree.gen.ts                  # Generated route tree
│   └── styles.css                        # Global styles
├── public/                               # Static assets
├── vite.config.ts                         # TanStack Start configuration
├── package.json                          # Project dependencies
└── tsconfig.json                         # TypeScript configuration

```

Once your project is set up, you can access your app at localhost:3000. You should see the default TanStack Start welcome page.

## Step 1: Setup a .env file with TMDB_AUTH_TOKEN

To fetch movies from the TMDB API, you need an authentication token. You can get this for free at themoviedb.org.

First, let's set up environment variables for our API key. Create a `.env` file in your project root:

```bash
touch .env

```

Add your TMDB API token to this file:

```dotenv
TMDB_AUTH_TOKEN=your_bearer_token_here
```

_Important_: Make sure to add `.env` to your `.gitignore` file to keep your API keys secure.

## Step 2: Defining Data Types

Let's create TypeScript interfaces for our movie data. Create a new file at `src/types/movie.ts`:

```ts
// src/types/movie.ts
export interface Movie {
  id: number
  title: string
  overview: string
  poster_path: string | null
  backdrop_path: string | null
  release_date: string
  vote_average: number
  popularity: number
}

export interface TMDBResponse {
  page: number
  results: Movie[]
  total_pages: number
  total_results: number
}
```

## Step 3: Creating the Route with API Fetch Function

Now let's create our route that fetches data from the TMDB API. Create a new file at `src/routes/fetch-movies.tsx`:

```typescript
// src/routes/fetch-movies.tsx
import { createFileRoute } from '@tanstack/react-router'
import type { Movie, TMDBResponse } from '../types/movie'

const API_URL =
  'https://api.themoviedb.org/3/discover/movie?include_adult=false&include_video=false&language=en-US&page=1&sort_by=popularity.desc'

async function fetchPopularMovies(): Promise<TMDBResponse> {
  const token = process.env.TMDB_AUTH_TOKEN
  if (!token) {
    throw new Error('Missing TMDB_AUTH_TOKEN environment variable')
  }

  const response = await fetch(API_URL, {
    headers: {
      accept: 'application/json',
      Authorization: `Bearer ${token}`,
    },
  })

  if (!response.ok) {
    throw new Error(`Failed to fetch movies: ${response.statusText}`)
  }

  const data = (await response.json()) as TMDBResponse
  return data
}

export const Route = createFileRoute('/fetch-movies')({
  component: MoviesPage,
  loader: async (): Promise<{ movies: Movie[]; error: string | null }> => {
    try {
      const moviesData = await fetchPopularMovies()
      return { movies: moviesData.results, error: null }
    } catch (error) {
      console.error('Error fetching movies:', error)
      return { movies: [], error: 'Failed to load movies' }
    }
  },
})
```

## Step 4: Building the Movie Components

Now let's create the components that will display our movie data. Add these components to the same `fetch-movies.tsx` file:

```tsx
// MovieCard component
const MovieCard = ({ movie }: { movie: Movie }) => {
  return (
    <div
      className="bg-white/10 border border-white/20 rounded-lg overflow-hidden backdrop-blur-sm shadow-md hover:shadow-xl transition-all duration-300 hover:scale-105"
      aria-label={`Movie: ${movie.title}`}
      role="group"
    >
      {movie.poster_path && (
        <img
          src={`https://image.tmdb.org/t/p/w500${movie.poster_path}`}
          alt={movie.title}
          className="w-full h-64 object-cover"
        />
      )}
      <div className="p-4">
        <MovieDetails movie={movie} />
      </div>
    </div>
  )
}

// MovieDetails component
const MovieDetails = ({ movie }: { movie: Movie }) => {
  return (
    <>
      <h3 className="text-lg font-semibold mb-2 line-clamp-2">{movie.title}</h3>
      <p className="text-sm text-gray-300 mb-3 line-clamp-3 h-10">
        {movie.overview}
      </p>
      <div className="flex justify-between items-center text-xs text-gray-400">
        <span>{movie.release_date}</span>
        <span className="flex items-center">
          ⭐️ {movie.vote_average.toFixed(1)}
        </span>
      </div>
    </>
  )
}
```

## Step 5: Creating the MoviesPage Component

Finally, let's create the main component that consumes the loader data:

```tsx
// MoviesPage component
const MoviesPage = () => {
  const { movies, error } = Route.useLoaderData()<{
    movies: Movie[]
    error: string | null
  }>()

  return (
    <div
      className="flex items-center justify-center min-h-screen p-4 text-white"
      style={{
        backgroundColor: '#000',
        backgroundImage:
          'radial-gradient(ellipse 60% 60% at 0% 100%, #444 0%, #222 60%, #000 100%)',
      }}
      role="main"
      aria-label="Popular Movies Section"
    >
      <div className="w-full max-w-6xl p-8 rounded-xl backdrop-blur-md bg-black/50 shadow-xl border-8 border-black/10">
        <h1 className="text-3xl mb-6 font-bold text-center">Popular Movies</h1>

        {error && (
          <div
            className="text-red-400 text-center mb-4 p-4 bg-red-900/20 rounded-lg"
            role="alert"
          >
            {error}
          </div>
        )}

        {movies.length > 0 ? (
          <div
            className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6"
            aria-label="Movie List"
          >
            {movies.slice(0, 12).map((movie) => (
              <MovieCard key={movie.id} movie={movie} />
            ))}
          </div>
        ) : (
          !error && (
            <div className="text-center text-gray-400" role="status">
              Loading movies...
            </div>
          )
        )}
      </div>
    </div>
  )
}
```

### Understanding How It All Works Together

```mermaid
sequenceDiagram
    autonumber
    actor U as User
    participant R as Router (TanStack Start)
    participant L as Route Loader (/fetch-movies)
    participant A as External API (TMDB)
    participant V as MoviesPage (UI)

    U->>R: Navigate to /fetch-movies
    R->>L: Invoke loader (server-side)
    L->>A: GET /movie/popular\nAuthorization: Bearer <TOKEN>
    A-->>L: JSON TMDBResponse
    alt response.ok
        L-->>R: { movies, error: null }
        R->>V: Render SSR with movies
        V-->>U: HTML with movie grid
    else non-ok / error
        L-->>R: { movies: [], error: "Failed to load movies" }
        R->>V: Render SSR with error alert
        V-->>U: HTML with error state
    end

    note over L,V: Loader validates response.ok,\nreturns data or error for initial render
```

Let's break down how the different parts of our application work together:

1. Route loader: When a user visits `/fetch-movies`, the loader function runs on the server
2. API call: The loader calls `fetchPopularMovies()` which makes an HTTP request to TMDB
3. Server-Side rendering: The data is fetched on the server reducing the load on the client side
4. Component rendering: The `MoviesPage` component receives the data via `Route.useLoaderData()`
5. Rendering UI: The movie cards are rendered with the fetched data

## Step 6: Testing Your Application

Now you can test your application by visiting [http://localhost:3000/fetch-movies](http://localhost:3000/fetch-movies). If everything is set up correctly, you should see a grid of popular movies with their posters, titles, and ratings. Your app should look like this:

![Netflix style movie setup](https://res.cloudinary.com/dubc3wnbv/image/upload/v1756512946/Screenshot_2025-08-29_at_5.14.26_PM_iiex7o.png)

## Conclusion

You've successfully built a movie discovery app that integrates with an external API using TanStack Start. This tutorial demonstrated how to use route loaders for server-side data fetching and building UI components with external data.

While fetching data at build time in TanStack Start is perfect for static content like blog posts or product pages, it's not ideal for interactive apps. If you need features like real-time updates, caching, or infinite scrolling, you'll want to use [TanStack Query](query/latest) on the client side instead. TanStack Query makes it easy to handle dynamic data with built-in caching, background updates, and smooth user interactions. By using TanStack Start for static content and TanStack Query for interactive features, you get fast loading pages plus all the modern functionality users expect.
