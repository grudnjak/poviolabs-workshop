# Poviolabs Workshop

At today's workshop we will cover technologies, general guidelines and tips for simpler and standardized development of web applications with an emphasis on the front-end design.

These instructions will guide you to setup and get started with a test project.

## Git and Github

Software developers working in teams are continually writing new source code and changing existing source code. The code for a project, app or software component is typically structured in file tree. One developer in the team may be working on a new feature while another developer fixes a bug on a different one, each developer can make changes in several branches of the file tree.

Version control software keeps track of every modification to the code and helps teams solve code conflicts or compare earlier versions when a mistake is made.

1. Create an empty repository on your GitHub account.
2. Create a new project locally with all files needed.
3. Now, the local project needs to be converted to Git repository (instead of simple files).
```
git init
```
4. Add a `.gitignore` file.
5. Add `README.md` file.
6. Connect your local reporitory with the remote repository
```
git remote add origin git@github.com:poviolabs/poviolabs-workshop.git
```
7. If you want to check your file status.
```
git status
```
8. Commit all files and pust to master branch.
```
git commit -m "project init"
git push -u origin master
```
9. Now create a `develop` branch from `master`
```
git checkout -b develop
```

## Webpack

In order to write transparent and readable code it’s essential to divide JavaScript and CSS code into small and concise parts (modules). We make it easier for ourselves and others to manage it, and also to understand and maintain it later.

On the other hand, browsers prefer as few files as possible.  We don’t want to have multiple js files loaded in the app, because every time we go to the website it makes many requests which of course is bad for the performance.

So, we can use [Webpack](https://webpack.js.org/configuration/) to bundle all of our CSS and JavaScript files into a single production ready file.

1. Download and install [Node](https://nodejs.org/en/) and npm
```
npm install -g
```
Or just check their versions and make sure you have the latest.
```
npm -v
node -v
```
2. Create package.json file
```
npm init
```
3. [Install Webpack](https://webpack.js.org/guides/installation/)
```
npm install webpack --save-dev
npm install webpack-cli --save-dev
```
4. Create webpack.config.js in the root of your project.
5. Install and setup the following loaders and plugins:

 [css-loader](https://webpack.js.org/loaders/css-loader/#src/components/Sidebar/Sidebar.jsx), [sass-loader](https://webpack.js.org/loaders/sass-loader/#src/components/Sidebar/Sidebar.jsx), [node-sass](https://github.com/sass/node-sass), [mini-css-extract-plugin](https://webpack.js.org/plugins/mini-css-extract-plugin/#src/components/Sidebar/Sidebar.jsx) to generate Sass files.

 ```
 npm install css-loader sass-loader node-sass mini-css-extract-plugin --save-dev

 ```
 [optimize-css-assets-webpack-plugin](https://github.com/NMFR/optimize-css-assets-webpack-plugin), [uglifyjs-webpack-plugin](https://webpack.js.org/plugins/uglifyjs-webpack-plugin/#src/components/Sidebar/Sidebar.jsx) to compress Css and Js files.
 ```
 npm install optimize-css-assets-webpack-plugin uglifyjs-webpack-plugin --save-dev
 ```
 [copy-webpack-plugin](https://webpack.js.org/plugins/copy-webpack-plugin/#src/components/Sidebar/Sidebar.jsx) to copy files into /dist folder.
 ```
 npm install copy-webpack-plugin --save-dev
 ```
 [url-loader](https://webpack.js.org/loaders/url-loader/#src/components/Sidebar/Sidebar.jsx) as a helper for .png, .jpg, .svg files.
 ```
 npm install url-loader --save-dev
 ```
 [devServer](https://webpack.js.org/configuration/dev-server/#src/components/Sidebar/Sidebar.jsx) to start a local server.



## File structure
