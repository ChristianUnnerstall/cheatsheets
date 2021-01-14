#### Init
````
npm init
````
#### Run script
````
npm run <script>
````
e.g.
````
npm run watch
````
#### Install Module
````
npm install --save <module>
````
#### Uninstall Module
````
npm uninstall <module>
npm install <module> --global
````
#### package.json Scripts block Example
````
...
"scripts": {
    "start": "node ./index.js",
    "watch": "nodemon ./index.js",
    "test": "echo \"Error: no test specified\" && exit 1"
},
...
````
