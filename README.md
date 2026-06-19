# Neroupath

A modern TypeScript monorepo for building scalable applications with a structured packages-and-apps architecture.

## Overview

Neroupath is a TypeScript-based project structured as a monorepo using a workspace setup. It provides a foundation for developing multiple applications and shared packages with proper separation of concerns and type safety.

## Project Structure

```
neroupath/
├── apps/                    # Application packages
├── packages/
│   └── types/              # Shared TypeScript type definitions
│       └── src/
├── package.json            # Root package configuration
└── [configuration files]   # ESLint, Git, etc.
```

### Key Directories

- **`apps/`** - Contains all application implementations that use the shared packages
- **`packages/types/`** - Centralized TypeScript type definitions and interfaces shared across apps
- **`packages/types/src/`** - Source files for type definitions

## Tech Stack

- **Language**: TypeScript 99.3%
- **Architecture**: Monorepo with multiple apps and packages
- **Package Manager**: npm or Yarn compatible

## Getting Started

### Prerequisites

- Node.js (v16 or higher recommended)
- npm or Yarn package manager
- Git

### Installation

1. Clone the repository:
```bash
git clone https://github.com/AbdullahSalimee/Neroupath.git
cd Neroupath
```

2. Install dependencies:
```bash
npm install
# or
yarn install
```

## Development

### Project Commands

```bash
# Install all dependencies
npm install

# Build all apps and packages
npm run build

# Run type checking
npm run type-check

# Lint code
npm run lint

# Format code
npm run format
```

> **Note**: Specific scripts depend on your root `package.json` configuration. Check it for available commands.

### Working with the Monorepo

To work on a specific app or package:

```bash
# Navigate to the specific app or package
cd apps/[app-name]
cd packages/types

# Install and run commands within that workspace
npm install
npm run build
```

## Project Architecture

### Types Package

The `packages/types` directory contains all shared TypeScript type definitions:

```
packages/types/
├── src/
│   └── [type definitions]
└── package.json
```

This package should be imported by all applications that need shared type definitions, ensuring consistency across your monorepo.

### Apps Directory

Each application in the `apps/` directory is an independent project that:
- Uses shared types from `packages/types`
- Maintains its own dependencies (if needed)
- Can be built and deployed independently
- Follows consistent coding standards

## Contributing

1. Create a new branch for your feature: `git checkout -b feature/your-feature-name`
2. Make your changes and commit them: `git commit -m 'Add your feature'`
3. Push to the branch: `git push origin feature/your-feature-name`
4. Submit a pull request

### Code Style

This project uses TypeScript for type safety. Please:
- Ensure all TypeScript code is properly typed
- Run linting and formatting before committing
- Add types to new functions and variables
- Update shared types in `packages/types` when needed

## Configuration Files

- `.gitattributes` - Git configuration for file handling
- `.gitignore` - Git ignore rules
- `package.json` - Root workspace configuration
- TypeScript configuration files for the monorepo

## Troubleshooting

### Installation Issues

If you encounter dependency issues:
```bash
# Clear node modules and reinstall
rm -rf node_modules
npm install
```

### Build Errors

For TypeScript compilation errors:
```bash
# Run type checking to identify issues
npm run type-check

# Check your TypeScript configuration
npx tsc --version
```

## License

This project is currently unlicensed. Please check the repository for license information.

## Author

**Abdullah Salimee** - [@AbdullahSalimee](https://github.com/AbdullahSalimee)

## Support

For issues, feature requests, or questions, please [open an issue](https://github.com/AbdullahSalimee/Neroupath/issues) on GitHub.

---

**Last Updated**: June 2026
