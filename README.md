# gleam

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

### Run Unit Tests with [Vitest](https://vitest.dev/)

```sh
npm run test:unit
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```

## Assumptions:
- Badge is to show a number only with a fixed icon (diamond). If the value is not a number (or a string of numbers) it would show a warning in the console.
- Buttons can receive any icon (not just the plus sign).
- SVGs are rendered inline as Vue components. This is what I normally do in React as well.
- I can't figure out the pattern of the paddings so let's assume that I got an agreement with the designer to have a universal padding of 10px for all button variants.
- Same with the loading icon. I'm always putting the loading at the tail of the button and assume that all types of buttons can have a loading state (including disabled).
- Tested in Chrome, Firefox and Safari (Mac)
