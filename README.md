# TypeScript Template

A modern TypeScript template for React-Astro projects with comprehensive tooling setup.

## Development Setup

1. Install dependencies:
```bash
npm install
```

2. Set up pre-commit hooks:
```bash
npm run prepare
```

### Code Quality Tools

This project uses several tools to ensure code quality:
- `eslint`: Code linting for TypeScript/JavaScript
- `prettier`: Code formatting
- `typescript`: Static type checking
- `husky`: Git hooks
- `lint-staged`: Run linters on staged files

You can run these manually:
```bash
# Lint
npm run lint

# Lint with auto-fix
npm run lint:fix

# Format code
npm run format
```

Or let the pre-commit hook run them automatically on `git commit`. If any check fails:
1. The commit will be aborted
2. The tools will make the necessary changes (if possible)
3. Stage the changes (`git add`) and try the commit again

### Project Structure
```
.
├── src/
│   └── styles/
│       └── global.css
├── .eslintrc.js
├── .prettierrc.js
├── .husky/
│   └── pre-commit
├── astro.config.mjs
├── tailwind.config.js
├── tsconfig.json
├── package.json
└── README.md
```

### Configuration Files
- `package.json`: Project metadata, dependencies, and scripts
- `tsconfig.json`: TypeScript configuration
- `.eslintrc.js`: ESLint rules and plugin settings
- `.prettierrc.js`: Prettier formatting rules
- `astro.config.mjs`: Astro configuration with React and Tailwind integrations
- `tailwind.config.js`: Tailwind CSS configuration

### Features

- ⚡️ **React** - UI library support
- 🎨 **Tailwind CSS** - Utility-first CSS framework
- 📝 **TypeScript** - Type safety and better DX
- 🔍 **ESLint** - Code linting
- ✨ **Prettier** - Code formatting
- 🪝 **Husky & lint-staged** - Git hooks and staged file linting
- 🚀 **Astro** - Static site generation

### Code Quality Enforcement

The template includes automatic code quality checks:

1. **Pre-commit Hook**: Runs on `git commit`
   - Lints staged files with ESLint
   - Formats code with Prettier
   - Runs type checking with TypeScript

2. **Manual Commands**:
```bash
# Run ESLint
npm run lint

# Fix ESLint issues
npm run lint:fix

# Format code with Prettier
npm run format
```

### Development Workflow

1. Start the development server:
```bash
npm run dev
```

2. Build for production:
```bash
npm run build
```

3. Preview production build:
```bash
npm run preview
```

All commits will automatically trigger the pre-commit hook, ensuring code quality standards are maintained.
