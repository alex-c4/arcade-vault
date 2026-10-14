# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Arcade Vault** is an online gaming platform where users compete for the highest scores. The project uses **Spec Driven Design** based on `/spec` and `/spec-impl` patterns, following best practices from [fernando-skills](https://github.com/Klerith/fernando-skills).

## Tech Stack

- **Framework**: Next.js 16.4.1 with Turbopack
- **UI**: React 19.3.0 + Tailwind CSS 4
- **Language**: TypeScript 5 (strict mode enabled)
- **Path alias**: `@/*` maps to project root
- **Styling**: Tailwind CSS with Turbopack loader for optimized CSS processing
- **Experimental**: Agent feedback enabled in Next.js config

## Common Commands

```bash
# Development server (runs on http://localhost:3000)
npm run dev

# Production build
npm run build

# Start production server
npm start

# Run ESLint
npm run lint
```

## Project Structure

- **`app/`** - Next.js App Router directory
  - `layout.tsx` - Root layout with font configuration and global metadata
  - `page.tsx` - Home page (main entry point)
  - `globals.css` - Global Tailwind styles
- **`public/`** - Static assets
- **`node_modules/`** - Dependencies
- **`.next/`** - Build output (do not commit)

## Development Notes

- **Strict TypeScript**: All strict compiler options enabled; no `any` types without good reason
- **Tailwind with Turbopack**: CSS is bundled via `@tailwindcss/turbopack` for fast rebuilds
- **Component Caching**: `cacheComponents: true` enables React component caching for performance
- **Partial Prefetching**: `partialPrefetching: true` optimizes route prefetching
- **Spec-Driven Design**: New features should follow `/spec` pattern before implementation in `/spec-impl`

## Skills Integration

The project uses [fernando-skills](https://github.com/Klerith/fernando-skills) for Spec Driven Design patterns. Install with:

```bash
npx skills@latest add Klerith/fernando-skills
```

Use `/spec` skill to write specifications and `/spec-impl` to implement them.

## Git Branch Info

- **Current branch**: `master`
- **Main branch**: `main` (use for PRs)
- **Git user**: Alex Peñaloza
