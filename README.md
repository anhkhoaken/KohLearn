# Vite React TypeScript Project

A modern React application built with TypeScript and powered by Vite for fast development and optimized builds.

## Tech Stack

- **React 19.1.0** - Modern React with concurrent features
- **TypeScript 5.8.3** - Type-safe JavaScript development
- **Vite 7.0.0** - Fast build tool with Hot Module Replacement (HMR)
- **ESLint** - Code linting with TypeScript support

## Getting Started

### Prerequisites
- Node.js 18+ 
- npm or yarn

### Installation & Development

1. Install dependencies:
   ```bash
   npm install
   ```

2. Start the development server:
   ```bash
   npm run dev
   ```

3. Open your browser and navigate to `http://localhost:5173`

### Available Scripts

- `npm run dev` - Start development server with HMR
- `npm run build` - Build for production
- `npm run preview` - Preview production build locally
- `npm run lint` - Run ESLint for code quality checks

## Project Structure

```
├── src/
│   ├── App.tsx          # Main React component
│   ├── main.tsx         # Application entry point
│   ├── index.css        # Global styles
│   └── App.css          # Component-specific styles
├── public/              # Static assets
├── index.html           # HTML template
└── vite.config.ts       # Vite configuration
```

## Development Features

- **Hot Module Replacement (HMR)** - Instant updates during development
- **TypeScript Support** - Full type checking and IntelliSense
- **ESLint Integration** - Automated code quality and style checking
- **Modern React Features** - React 19 with concurrent features support

## Build & Deployment

The project uses Vite for building, which provides:
- Fast builds with tree-shaking
- Optimized bundle splitting
- Modern ES modules output
- Legacy browser support via Rollup

Build the project:
```bash
npm run build
```

The built files will be in the `dist/` directory, ready for deployment to any static hosting service.

## ESLint Configuration

This project uses modern ESLint configuration with TypeScript support. The current setup includes:

- React-specific linting rules
- TypeScript-aware ESLint rules
- React Hooks linting
- Code formatting and style consistency

For production applications, consider enabling type-aware lint rules by updating your ESLint configuration:

```js
// eslint.config.js
export default tseslint.config([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      ...tseslint.configs.recommendedTypeChecked,
      // For stricter rules:
      // ...tseslint.configs.strictTypeChecked,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
    },
  },
])
```

## Next Steps

- Add routing with React Router
- Implement state management (Redux Toolkit, Zustand, etc.)
- Add UI component library (Material-UI, Chakra UI, etc.)
- Configure testing with Vitest and React Testing Library
- Set up CI/CD pipeline
- Add PWA features
