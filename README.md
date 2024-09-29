# npm-package-template-tsup

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A template for creating npm packages with TypeScript, bundled using [Tsup](https://github.com/egoist/tsup) for optimized builds.

## Features

- **TypeScript**: Write in modern TypeScript and build for various JavaScript environments.
- **Tsup**: Fast and minimalistic bundling powered by esbuild.
- **Zero-config**: Ready to use with sensible defaults.
- **Tree-shaking**: Includes optimizations for smaller builds.
- **Release automation**: Simplified versioning and publishing using [release-it](https://github.com/release-it/release-it).

## Usage

This is a template repository designed to help you create your own npm package. To get started, by cloning the repository and customizing it:

```bash
git clone https://github.com/JavadAg/npm-package-template-tsup.git
cd npm-package-template-tsup
```

### Setup

1. **Install dependencies**:

    ```bash
    npm install
    ```

2. **Build**: Build the package for production:

    ```bash
    npm run build
    ```

3. **Release**: Automate versioning and publishing using [release-it](https://github.com/release-it/release-it):

    ```bash
    npm run release
    ```

    This command will prompt you for the version, update the `CHANGELOG`, and commit the release.

## Customizing the Template

### Configuration

You can customize the build process by editing the `tsup.config.ts` file. It supports various options such as specifying output formats (ESM, CJS) and setting environment variables.

Example `tsup.config.ts`:

```typescript
import { defineConfig } from 'tsup';

export default defineConfig({
  target: 'es2020',
  format: ['cjs', 'esm'],
  splitting: false,
  sourcemap: true,
  clean: true,
  dts: true
});
```

### Scripts

The following npm scripts are provided:

- **`npm run build`**: Builds the package.
- **`npm run release`**: Automates versioning and publishing.

## Contributing

Feel free to open issues or submit pull requests to improve the template.

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.
