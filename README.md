# Snippets

A modern Next.js application for creating, editing, and managing code snippets. Features a rich Monaco code editor, PostgreSQL backend with server-side rendering (SSR), static site generation (SSG) for dynamic routes, client-side rendering (CSR) for interactive forms, and full caching control. Supports no-JS functionality via server actions and includes custom loading/404 pages.

## Features

- **Snippet CRUD**: Create, read, update, delete snippets with syntax-highlighted code.
- **Rich Editor**: Monaco Editor for JavaScript (and more) with dark theme and minimap disabled.
- **Database Integration**: PostgreSQL for persistent storage; queries optimized for SSR.
- **Rendering Modes**: SSR for dynamic data, SSG via `generateStaticParams` for instant loads on `/snippets/[id]`, CSR for forms with `useActionState`.
- **Server Actions**: Secure mutations (e.g., delete) without client JS; uses `startTransition` for smooth UX.
- **Caching**: Force-dynamic or revalidate (e.g., `revalidate = 3`); pre-renders all snippet pages for speed.
- **UI/UX**: Tailwind CSS, custom icons, loading spinners, and a fun 404 page.
- **No-JS Support**: Core pages work without browser JS.

## Tech Stack

- **Framework**: Next.js 14+ (App Router) – SSR, SSG, CSR, routing.
- **Database**: PostgreSQL – Direct queries via `pg` lib.
- **Editor**: Monaco Editor (`@monaco-editor/react`).
- **Styling**: Tailwind CSS.
- **State/Actions**: React hooks (`useActionState`, `useState`), server actions for forms.
- **Other**: Next.js `Link`, `notFound`, `generateStaticParams`.

## Prerequisites

- Node.js v18+
- PostgreSQL v12+ (with a `snippet` table: `id`, `title`, `code` columns).

## Installation

1. Clone the repo:
