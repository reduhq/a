# a
## How to deploy a ReactAPP on GitHub Pages
1) Install gh-pages
```bash
npm install gh-pages --save-dev
```

2) Add the next lines in the package.json
* With **homepage** we indicate where the site is going to be deployed. 
* With **predeploy** we compile the application. 
* With **deploy** we deploy the site on github.
```json
{
    "homepage": "https://{Github Username}.github.io/{NombreRepo}",

    "scripts":{
        "predeploy": "npm run build",
        "deploy": "gh-pages -d build"
    }
}
```