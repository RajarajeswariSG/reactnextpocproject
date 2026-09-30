# Entity Search

A Next.js App Router implementation of a responsive entity search workflow using React, TypeScript, Tailwind CSS, and Lucide React.

## Run Locally

```bash
npm install
npm run dev
```

Open [http://localhost:3000/entity-search](http://localhost:3000/entity-search).

## Architecture

The feature follows this dependency direction:

```text
UI Components -> useEntitySearch -> entityService -> Backend API
```

The backend integration is currently isolated behind a typed mock implementation in `src/services/entityService.ts`.

For the code-level diagrams, request sequence, hook state machine, component contracts, and backend replacement guidance, read the [Entity Search Architecture](docs/entity-search-architecture.md) guide.

For a step-by-step beginner walkthrough, read the [Beginner Development Guide](docs/beginner-development-guide.md). It explains the build order, each file's purpose, the React state flow, debugging method, and practice exercises.

The presentation-ready editable deck is [Entity-Search-React-Architecture.pptx](docs/Entity-Search-React-Architecture.pptx). Regenerate it with:

```bash
node scripts/generate-architecture-ppt.js
```

## Project Structure

```text
src/
├── app/
│   └── entity-search/page.tsx
├── components/
│   ├── layout/
│   └── entity-search/
├── hooks/
│   └── useEntitySearch.ts
├── services/
│   └── entityService.ts
├── types/
│   └── entity.ts
└── constants/
	└── navigation.ts
```

## Commands

```bash
npm run dev      # Start the development server
npm run lint     # Run ESLint
npm run build    # Create a production build
node scripts/generate-architecture-ppt.js # Regenerate the architecture deck
```
