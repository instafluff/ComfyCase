# ComfyCase
Comfiest ESLint Settings!

ComfyCase prefers spaces between parentheses, camelCase syntax except for object properties, double quotes, Stroustrup style braces, and indentation with tabs.

# Instructions
How to configure your project to use these ESLint settings.

## TypeScript
To set up ESLint with this configuration in your TypeScript project, you can follow these steps:

1. Install the necessary dev dependencies along with ComfyCase:
```Bash
npm install --save-dev eslint @typescript-eslint/parser @typescript-eslint/eslint-plugin eslint-config-comfycase
```
2. Create an `.eslintrc.json` file in the root of your project and define your configuration rules, extending from ComfyCase:
```JavaScript
{
  "env": {
    "node": true,
    "es6": true
  },
  "extends": [ "eslint:recommended", "comfycase" ],
  "parser": "@typescript-eslint/parser",
  "parserOptions": {
    "ecmaVersion": 2018,
    "sourceType": "module"
  },
  "plugins": ["@typescript-eslint", "node"],
  "rules": {
    // your configuration rules go here
  }
}
```
3. Add a script to your `package.json` file to run ESLint on your project:
```JavaScript
{
  "scripts": {
    "lint": "eslint . --ext .js,.ts"
  }
}
```
4. You can then run the lint script with `npm run lint` or automatically fix them with `npm run lint -- --fix`.

## JavaScript
To setup ESLint with this configuration in your JavaScript project, you can follow these steps:

1. Install the necessary dev dependencies:
```Bash
npm install --save-dev eslint eslint-config-comfycase
```
2. Create an `.eslintrc.json` file in the root of your project and define your configuration rules:
```JavaScript
{
  "env": {
    "node": true,
    "es6": true
  },
  "extends": [ "eslint:recommended", "comfycase" ],
  "parserOptions": {
    "ecmaVersion": 2018,
    "sourceType": "module"
  },
  "rules": {
    // your configuration rules go here
  }
}
```
3. Add a script to your `package.json` file to run ESLint on your project:
```JavaScript
{
  "scripts": {
    "lint": "eslint . --ext .js"
  }
}
```
4. You can then run the lint script with `npm run lint` or automatically fix them with `npm run lint -- --fix`.