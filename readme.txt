1. mkdir webpacke-demo
cd webpacka-demo
npm init -y
npm install webpack webpack-cli --save-dev

2. Create folder structure

webpack-demo 
    |- package.json
    


3. Edit package.json

Remove "main": "index.js", from package.json file and put "private" :  true

4. Creating a Bundle


To bundle the lodash dependency with index.js, we'll need to install the library locally:

    npm install --save lodash

Edit: src/index.js, import lodash in our script.
Edit: dist/index.html, we removed lodash entery and src/index.js and put main.js
5. Run command npx webpacka
6. Create new config file webpack.config.js and add the following connection code which can connect source and output file:

const path = require('path');

module.exports = {
    entry: './src/index.js',
    output: {
        filename: 'main.js',
        path: path.resolve(__dirname, 'dist'),
    },
};

7. Run command npx webpack --config webpack.config.js 

8. Aplly NPM Scripts command inside package.json and do the following changes:

    "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1",
        "build": "webpack"
    },

9. Run the command: npm run build

10. Our final project looks like this: 
