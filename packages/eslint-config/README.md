# ESLint Configuration

This package provides modular ESLint configurations for different project types.

## Available Configurations

### Base Configuration

```javascript
// eslint.config.js
import baseConfig from '@nestjs-labs/eslint-config/base';
export default baseConfig;
```

### Node.js Projects

```javascript
// eslint.config.js
import nodeJsConfig from '@nestjs-labs/eslint-config/node';
export default nodeJsConfig;
```

### NestJS Projects

```javascript
// eslint.config.js
import nestJsConfig from '@nestjs-labs/eslint-config/nest';
export default nestJsConfig;
```

### Next.js Projects

```javascript
// eslint.config.js
import nextJsConfig from '@nestjs-labs/eslint-config/next';
export default nextJsConfig;
```

### React Projects

```javascript
// eslint.config.js
import reactConfig from '@nestjs-labs/eslint-config/react';
export default reactConfig;
```

### Jest Test Files

```javascript
// eslint.config.js
import jestConfig from '@nestjs-labs/eslint-config/jest';
export default jestConfig;
```

### Full Configuration (All Features)

```javascript
// eslint.config.js
import fullConfig from '@nestjs-labs/eslint-config';
export default fullConfig;
```

## Legacy Extends Support

For projects that need to use the legacy `extends` syntax, you can import named exports:

```javascript
// eslint.config.js
import { nodeEslint, nestEslint, jestEslint } from '@nestjs-labs/eslint-config';

export default [
  ...nodeEslint,
  ...nestEslint,
  ...jestEslint,
  // Your additional rules here
];
```

Available named exports:

- `baseEslint` - Base configuration
- `nodeEslint` - Node.js configuration
- `nestEslint` - NestJS configuration
- `nextEslint` - Next.js configuration
- `reactEslint` - React configuration
- `jestEslint` - Jest configuration

## Features

- **TypeScript Support**: Full TypeScript linting with strict rules
- **Import Sorting**: Automatic import organization
- **Code Style**: Consistent formatting rules
- **React Support**: JSX and React Hooks rules
- **Next.js Support**: Next.js specific optimizations
- **NestJS Support**: NestJS decorator and class rules
- **Testing Support**: Jest and test file specific rules
- **Node.js Support**: Node.js specific globals and rules

## Requirements

- Node.js 18+
- TypeScript 5.8+
- ESLint 9.31+
- typescript-eslint 8.37+
