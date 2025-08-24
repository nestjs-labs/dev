# NestJS Labs Dev

A monorepo for NestJS development environment, providing reusable ESLint and TypeScript
configurations.

## 🚀 Project Overview

This monorepo contains various configuration packages for NestJS development, designed to provide a
consistent and high-quality development experience.

## 📦 Included Packages

### `@nestjs-labs/eslint-config`

Provides modular ESLint configurations supporting multiple project types:

- **Base**: Basic configuration
- **Node.js**: Node.js project configuration
- **NestJS**: NestJS project configuration
- **Next.js**: Next.js project configuration
- **React**: React project configuration
- **Jest**: Test files configuration

### `@nestjs-labs/typescript-config`

Provides TypeScript configuration files:

- **Base**: Basic TypeScript configuration
- **NestJS**: NestJS project specific configuration
- **Next.js**: Next.js project specific configuration
- **React Library**: React library project configuration

## 🛠️ Tech Stack

- **Package Manager**: pnpm
- **Build Tool**: Turbo
- **Language**: TypeScript
- **Code Quality**: ESLint + Prettier
- **Node.js**: >= 20

## 📋 Requirements

- Node.js 18+
- pnpm 9.0.0+

## 🚀 Quick Start

### Install Dependencies

```bash
pnpm install
```

### Development

```bash
# Start development mode
pnpm dev

# Build all packages
pnpm build

# Lint code
pnpm lint

# Type checking
pnpm check-types

# Format code
pnpm format
```

## 📁 Project Structure

```
nestjs-labs-dev/
├── packages/
│   ├── eslint-config/          # ESLint configuration package
│   │   ├── src/
│   │   │   ├── base.ts         # Base configuration
│   │   │   ├── nest.ts         # NestJS configuration
│   │   │   ├── next.ts         # Next.js configuration
│   │   │   ├── react.ts        # React configuration
│   │   │   ├── node.ts         # Node.js configuration
│   │   │   ├── jest.ts         # Jest configuration
│   │   │   └── index.ts        # Main entry
│   │   └── package.json
│   └── typescript-config/      # TypeScript configuration package
│       ├── base.json           # Base configuration
│       ├── nestjs.json         # NestJS configuration
│       ├── nextjs.json         # Next.js configuration
│       └── package.json
├── package.json
├── pnpm-workspace.yaml
├── turbo.json
└── README.md
```

## 🔧 Usage Examples

### ESLint Configuration

Install and use ESLint configuration in your project:

```bash
pnpm add -D @nestjs-labs/eslint-config
```

Create `eslint.config.js`:

```javascript
// Use complete NestJS configuration
import nestJsConfig from '@nestjs-labs/eslint-config/nest';
export default nestJsConfig;
```

### TypeScript Configuration

Install and use TypeScript configuration in your project:

```bash
pnpm add -D @nestjs-labs/typescript-config
```

Extend configuration in `tsconfig.json`:

```json
{
  "extends": "@nestjs-labs/typescript-config/nestjs"
}
```

## 📄 License

MIT License

## 🙏 Acknowledgments

This project is inspired by and references the excellent work from
[@polkadot-js/dev](https://github.com/polkadot-js/dev), which provides shared development
configurations and CI scripts for the Polkadot.js ecosystem. Their approach to creating reusable
development tooling has been a great inspiration for this project.

## 🔗 Related Links

- [NestJS Official Website](https://nestjs.com/)
- [Turbo Documentation](https://turbo.build/)
- [pnpm Documentation](https://pnpm.io/)
- [@polkadot-js/dev](https://github.com/polkadot-js/dev) - Inspiration for this project
