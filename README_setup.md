# Cookbook 101 - How to create a new app project from scratch

These are the commands to create a new project using Node, Express, Bootstrap from scratch on a new machine.

## Setup the DEV ENV for Node.js

### 1. Install the development stack:

- WINDOWS:

  > \$ `choco install chrome git visualstudio2017-workload-vctools python2 node`

- MAC:

  > \$ `brew install git python2`  
  > \$ `wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash`  
  > \$ `nvm install node`

### 2. Install NPM Global packages:

> \$ `npm install -g pm2@latest nodemon express-generator`

### 3. Set default NPM vars:

> \$ `npm set init.author.email "tag.dev@icloud.com"`  
> \$ `npm set init.author.name "Thiago A.Gallo"`

## Create the project structure

### Use express generator to create the project:

> \$ `npx express-generator --view=pug --css=sass --git MyApp`  
> \$ `cd MyApp`  
> \$ `npm install`

### Customize _package.json_ adding this:

`"description": "", "author": "Thiago A.G. <tag.dev@icloud.com> (https://github.com/tagallo)", "scripts": { "start": "node ./bin/www", "debug": "nodemon --inspect ./bin/www" }, "nodemonConfig": { "ext": "pug, css, js, json" }, "engines": { "node": "12.16.1" },`

### Instal modules and add dependencies

> \$ `cd MyApp`  
> \$ `npm install bootstrap jquery popper body-parser express-validator acorn`  
> \$ `npm install nodemon eslint prettier @prettier/plugin-pug --save-dev`

<!-- : Do I need pug-bootstrap? -->

## To run the project:

On MacOS or Linux, run the app with this command:

> \$ `DEBUG=MyApp:* npm start`

On Windows, use this command:

> \$ `set DEBUG=MyApp:* & npm start`

Then load http://localhost:3000/ in your browser to access the app.
