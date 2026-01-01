# Core Concepts

Understanding the key concepts of SuperInstance.

## Modular Architecture

SuperInstance is built on the principle of **modularity**:

- Each package is **standalone** - works independently
- Each package is **composable** - works with other packages
- **Zero overhead** - only pay for what you use

## Packages vs Applications

### Packages (@superinstance/*)

These are npm packages that provide specific functionality:

```typescript
import { retry } from '@superinstance/async';
import { Chat } from '@superinstance/chat';
```

### Applications

These are end-user applications built using SuperInstance packages:

- **PersonalLog** - Everyday personal use
- **MakerLog** - Tools for creators
- **Murmur** - Wiki/TensorDB interface
- **ec2mud** - Game MUD

## The Core Dashboard

`SuperInstanceCore` is the central dashboard that:
- Discovers available packages
- Lets you load/unload modules
- Monitors resource usage
- Manages API keys for cloud services

It's not an end-user application itself, but a tool for developers to manage the ecosystem.

## Foundation vs Feature Packages

### Foundation Primitives
Core utilities with no dependencies on other SuperInstance packages:
- async, validate, cache, events, config, storage, provider-base, logger

### Feature Packages
Higher-level tools that may depend on foundation packages:
- chat, tts, asr, memory, dreamer, rag, etc.

## Design Philosophy

1. **Independence First** - Every package works alone
2. **Interfaces Over Implementation** - Well-defined contracts
3. **Zero Overhead** - Tree-shakeable, no unused code
4. **TypeScript** - Full type safety
5. **Developer Experience** - Simple, joyful to use

## Next Steps

- [Installation](./installation.md)
- [Package Reference](../packages/README.md)
- [Guides](../guides/README.md)
