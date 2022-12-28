# Deploy Vite + Github Pages

## Install gh-pages

-   [más info](https://ull-esit-pl-1617.github.io/tareas-iniciales-Edu-Guille-Oscar-Sergio/Tutorial/gh-pages/gh-pages.html): El módulo gh-pages es un módulo de npm (Node Package Manager) que **permite automatizar la publicación de archivos en una rama gh-pages** de un repositorio de GitHub (o cualquier otra rama u otro servicio).

```sh
npm i gh-pages -D
```

## vite.config.js

-   [ver punto 1](https://vitejs.dev/guide/static-deploy.html#github-pages)

```js
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

```json
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

Estos comandos se repiten por cada actualización del proyecto:

```sh
npm run build
npm run deploy
```

## Esperar... y listo!
