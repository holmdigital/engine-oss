# Holm Digital Accessibility Engine

> The core compliant accessibility testing engine powering Holm Digital's ecosystem.

This monorepo contains the open-source core of our accessibility technology, allowing developers to integrate regulatory-grade accessibility testing into their own workflows.

## Packages

| Package | Description | Version |
|---------|-------------|---------|
| [`@holmdigital/engine`](./packages/engine) | The testing engine itself. Bridges `axe-core` with legal regulations (EN 301 549). | ![npm](https://img.shields.io/npm/v/@holmdigital/engine) |
| [`@holmdigital/standards`](./packages/standards) | Machine-readable regulatory database for WCAG, EN 301 549, and DOS-lagen. | ![npm](https://img.shields.io/npm/v/@holmdigital/standards) |

## Getting Started

You can install the engine directly from the GitHub Package Registry or npm (once publicly released).

```bash
# First, configure npm to use GitHub Package Registry:
npm config set @holmdigital:registry https://npm.pkg.github.com

# Then install:
npm install @holmdigital/engine
```

### Usage

```typescript
import { RegulatoryScanner } from '@holmdigital/engine';

const scanner = new RegulatoryScanner({ url: 'https://example.com' });
const result = await scanner.scan();
console.log(result.score);
```

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.
