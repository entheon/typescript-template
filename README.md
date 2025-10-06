# TypeScript Template

A minimal modern TypeScript template for React-Astro projects with comprehensive tooling setup.

## Development Setup

1. Install dependencies:

```bash
pnpm install
```

2. Set up pre-commit hooks:

```bash
pnpm prepare
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
pnpm lint

# Lint with auto-fix
pnpm lint:fix

# Format code
pnpm format
```

Or let the pre-commit hook run them automatically on `git commit`. If any check fails:

1. The commit will be aborted
2. The tools will make the necessary changes (if possible)
3. Stage the changes (`git add`) and try the commit again

### Project Structure

```
.
├── src/
│   ├── layouts/
│   │   └── BaseLayout.astro
│   ├── pages/
│   │   ├── index.astro
│   │   └── page.astro
│   ├── styles/
│   │   └── base.css          # Tailwind v4 config
│   └── env.d.ts
├── public/
│   └── favicon.svg
├── .husky/
│   └── pre-commit
├── astro.config.mjs
├── tsconfig.json
├── eslint.config.js
├── package.json
├── .gitignore
└── README.md
```

> [!NOTE]
> This template is configured with Strict TypeScript, and includes all `.ts, .tsx, .astro` files found under `/src`

> [!WARNING]
> This project uses **Tailwind CSS v4** which has a CSS-first configuration approach (no `tailwind.config.js`). For proper editor setup and syntax highlighting, see the [Tailwind CSS editor setup guide](https://tailwindcss.com/docs/editor-setup).

### Template Pages

The template includes two starter pages:

- **index.astro**: A clean landing page with feature highlights
- **page.astro**: A generic second page you can customize for any purpose

Both pages use a centered card layout with a gradient background for a modern, professional look.

### Development Workflow

1. Start the development server:

```bash
pnpm dev
```

2. Build for production:

```bash
pnpm build
```

3. Preview production build:

```bash
pnpm preview
```

All commits will automatically trigger the pre-commit hook, ensuring code quality standards are maintained.
