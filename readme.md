create a new microfrontend from scratch

If pnpm is not installed globally then copy and paste the below command in cmd
npm install -g pnpm

to check the version of pnpm type the following in cmd : pnpm -v

pnpm init

pnpm add react react-dom

pnpm add @babel/runtime

// adding devDependencies

pnpm add @babel/core @babel/plugin-transform-runtime @babel/preset-env @babel/preset-react autoprefixer babel-loader css-loader html-webpack-plugin postcss postcss-loader style-loader webpack webpack-cli file-loader clean-webpack-plugin webpack-dev-server eslint eslint-plugin-react eslint-plugin-react-hooks eslint-plugin-react-refresh html-loader -D

// package.json

remove : "description": "" and "main": "index.js", and add "private": true,

then add:

"scripts": {
"build": "webpack --mode production",
"build:dev": "webpack --mode development",
"build:start": "cd dist && PORT=8080 npx serve",
"start": "webpack serve --open --mode development",
"start:live": "webpack serve --open --mode development --live-reload --hot",
"lint": "eslint . --ext js,jsx --report-unused-disable-directives --max-warnings 0"
},

copy webpack.config.js, .gitignore, src, .babelrc, .eslintrc.cjs files and paste it in project

pnpm start
