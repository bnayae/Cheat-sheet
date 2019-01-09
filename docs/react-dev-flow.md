# install react environment cli

npm install -g create-react-app

# create react app

create-react-app {app-name}

# add TypeScript support

[reference](https://facebook.github.io/create-react-app/docs/adding-typescript)

- for TypeScript file use {file-name}.tsx

npm install --save typescript @types/node @types/react @types/react-dom @types/jest

# update

npm install

# fix vulnerability

npm audit fix

# production

npm run build

# lint

[Setting Up Your Editor](https://facebook.github.io/create-react-app/docs/setting-up-your-editor)

## add the following entry into .eslintrc.json

{
"extends": "react-app"
}

# debug

[Debug React](https://github.com/piotrwitek/typesafe-actions-todo-app/tree/master/#visual-studio-code)

# react + TypeScript

[cheat Sheet](https://github.com/sw-yx/react-typescript-cheatsheet)

# material-ui

[material-ui ref](https://material-ui.com/getting-started/installation/)
npm install @material-ui/core

## Roboto Font (for material-ui)

[Roboto Font ref](https://material-ui.com/style/typography/#general)

<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto:300,400,500">
or
npm install typeface-roboto --save
import 'typeface-roboto';
