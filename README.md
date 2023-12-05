# a
## How to deploy a ReactAPP on GitHub Pages
1) Install gh-pages
```bash
npm install gh-pages --save-dev
```

2) vite.config.ts
```ts
import { defineConfig } from "vite";
import react from "@vitejs/plugin-react";

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [react()],
  base: "/el-nombre-de-tu-repositorio/",
});
```

3) Add the next lines in the package.json
* With **predeploy** we compile the application. 
* With **deploy** we deploy the site on github.
```json
{
    "scripts":{
        "predeploy": "npm run build",
        "deploy": "gh-pages -d dist"
    }
}
```