# Deploy Vite + Github Pages

## Install

```sh
npm i gh-pages -D
```

## vite.config.js

-   [ver punto 1](https://vitejs.dev/guide/static-deploy.html#github-pages)

```js{7}
import { defineConfig } from "vite";
import react from "@vitejs/plugin-react";

// https://vitejs.dev/config/
export default defineConfig({
    plugins: [react()],
    base: "/el-nombre-de-tu-repositorio/",
});
```

## package.json

`"deploy": "gh-pages -d dist"`

```json{5}
"scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview",
    "deploy": "gh-pages -d dist"
}
```

## Git init

```sh
git init
git add .
git commit -m "first commit"
```

## Crear repositorio en Github

Subir el proyecto a Github

```sh
git remote add origin https://github.com/${nombre-cuenta}/${nombre-repositorio}.git
git branch -M main
git push -u origin main
```

## npm run build && npm run deploy

```sh
npm run build
```

```sh
npm run deploy
```

## Esperar... y listo!
