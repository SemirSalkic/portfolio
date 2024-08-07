# portfolio

This is a portfolio website built with Vue.js, TypeScript, Tailwind CSS, Pinia and TresJs.

## Built With

- [Vue.js](https://vuejs.org/) - The web framework used
- [TypeScript](https://www.typescriptlang.org/) - For static type checking
- [Tailwind CSS](https://tailwindcss.com/) - For styles
- [Pinia](https://pinia.esm.dev/) - State management
- [TresJs](https://tresjs.org/) - For 3D rendering

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Vue - Official](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (previously Volar). The extension provides syntax highlighting, TypeScript support, and intellisense for template expressions and component props.

## Type Support for `.vue` Imports in TS

In editors, we need [Vue - Official](https://marketplace.visualstudio.com/items?itemName=Vue.volar) + built-in `TypeScript and JavaScript Language Features` extension to make the TypeScript language service aware of `.vue` types.

Install [Vue - Official](https://marketplace.visualstudio.com/items?itemName=Vue.volar) and if you don't have `TypeScript and JavaScript Language Features` extension enabled, follow these steps:

1. Run `Extensions: Show Built-in Extensions` from VSCode's command palette.
2. Find `TypeScript and JavaScript Language Features`, right click and select `Enable`
3. Reload the VSCode window by running `Developer: Reload Window` from the command palette.

To avoid conflicts, disable the Vetur and Volar extensions if installed. Here's how:

1. Click on the Extensions view icon on the Sidebar or press `Ctrl+Shift+X`.
2. Find `Vetur` or `TypeScript Vue Plugin (Volar)`, right click and select `Disable (Workspace)`.
3. Reload the VSCode window by running `Developer: Reload Window` from the command palette.

## Quick Start

Clone the repo, install dependencies, and start the development server.

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Type-Check, Compile and Minify for Production

```sh
npm run build
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```

## Deployment

The app is deployed on [Netlify](https://www.netlify.com/).

You can view the live site here: [https://portfolio-semir-salkic.netlify.app](https://portfolio-semir-salkic.netlify.app)

It automatically deploys from the main branch on GitHub.
