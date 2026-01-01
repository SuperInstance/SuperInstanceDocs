# Installation

Get started with SuperInstance by installing the packages you need.

## Prerequisites

- Node.js 18+ installed
- pnpm 8+ (recommended), npm, or yarn

## Installing Individual Packages

Each SuperInstance package is independent and can be installed on its own:

```bash
# Using npm
npm install @superinstance/async

# Using pnpm
pnpm add @superinstance/async

# Using yarn
yarn add @superinstance/async
```

## Installing Multiple Packages

You can install multiple packages at once:

```bash
pnpm add @superinstance/async @superinstance/cache @superinstance/chat
```

## Core Dashboard

The SuperInstance Core dashboard helps you discover and manage modules:

```bash
git clone https://github.com/SuperInstance/SuperInstanceCore.git
cd SuperInstanceCore
pnpm install
pnpm dev
```

Visit http://localhost:3001 to see the dashboard.

## Package Categories

### Foundation Primitives

Core utilities that other packages build upon:

- `@superinstance/async` - Async utilities
- `@superinstance/validate` - Schema validation
- `@superinstance/cache` - Multi-level caching
- `@superinstance/events` - Event emitter
- `@superinstance/config` - Configuration
- `@superinstance/storage` - Storage abstraction
- `@superinstance/provider-base` - Provider base classes
- `@superinstance/logger` - Structured logging

### Feature Packages

Higher-level toolkits:

- `@superinstance/chat` - Multi-LLM chat
- `@superinstance/tts` - Text-to-speech
- `@superinstance/asr` - Speech recognition
- `@superinstance/memory` - Memory systems
- `@superinstance/dreamer` - Generative AI workflows
- `@superinstance/rag` - RAG pipeline
- And more...

See the [Package Reference](../packages/README.md) for complete details.
