<p>
  <img src="https://assets.solidjs.com/banner?project=Library&type=solid-lightning" alt="SolidJS Lightning" />
</p>

# SolidJS Lightning

Is a UI framework for [Lightning 3 Renderer](https://lightningjs.io/) built with [SolidJS](https://www.solidjs.com/) Universal Renderer. It allows you to declaratively construct lightning nodes with reactive primitives, just as you would construct a DOM tree in SolidJS.

## Documentation

[SolidJS Lightning Docs](https://lightning-tv.github.io/solid/)

## Demo App

[Solid TMDB Demo App](https://github.com/lightning-tv/solid-demo-app)

## Playground

[playground.solidjs.com](https://playground.solidjs.com/anonymous/ad962850-b492-4f6f-ac68-668469f5f22e)

## Quick Start

Clone starter template:

```sh
> npx degit lightning-tv/solid-starter-template my-app
> cd my-app
> npm i # or yarn or pnpm
> npm start # or yarn or pnpm
```

## Video Quick Start

[![Watch the video](https://img.youtube.com/vi/mWJ9CEiizeE/0.jpg)](https://www.youtube.com/watch?v=mWJ9CEiizeE)

### Hello World

```jsx
import { render, Text } from '@lightningtv/solid';

render(() => <Text>Hello World</Text>);
```

For a more detailed Hello World guide check out the [Hello World](HelloWorld.md) guide.

## Migration Guide from previous repo:

If you're migrating from https://github.com/lightning-js/solid

Find and replace:
"@lightningjs/solid-primitives" with "@lightningtv/solid/primitives"
"@lightningjs/solid" with "@lightningtv/solid"

Update vite.config to dedupe solid:

```js
resolve: {
    dedupe: [
      "solid-js",
      "@lightningtv/solid",
      "@lightningtv/solid/primitives",
      "@lightningjs/solid-ui",
      "@lightningjs/renderer",
    ],
  },
```

If you don't want to find and replace you can use alias

```js
resolve: {
    alias: {
      theme: "@lightningjs/l3-ui-theme-base",
      "@lightningjs/solid": "@lightningtv/solid",
      "@lightningjs/solid-primitives": "@lightningtv/solid/primitives",
    },
  },
```
