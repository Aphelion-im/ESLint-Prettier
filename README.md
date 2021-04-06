# Notes ESLint & Prettier
Updated: 7-4-2021

## Resources
* [VSCode - ESLint, Prettier & Airbnb Setup by Brad Traversy](https://gist.github.com/bradtraversy/aab26d1e8983d9f8d79be1a9ca894ab4)
* [Video: VSCode ESLint, Prettier & Airbnb Style Guide Setup](https://youtu.be/SydnKbGc7W8)
* [Prettier configuration](https://prettier.io/docs/en/configuration.html)

## Problem solving
* [Why do I keep getting Delete 'cr' [prettier/prettier]?](https://stackoverflow.com/questions/53516594/why-do-i-keep-getting-delete-cr-prettier-prettier)
* [no-undef message ESLint](https://medium.com/@jeryldev/a-beginners-story-how-to-setup-eslint-in-a-visual-studio-code-project-28b379a33cdb)


## Installing ESLint & Prettier
* [Install ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
* [Installer VSCode](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

## VSCode settings
* Format on save: on.
* Prettier: Single quotes: on.

## Command Line/Bash
 ```bash
npm init -y
```
 ```bash
npm i -D eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-plugin-node eslint-config-node
```
 ```bash
npx install-peerdeps --dev eslint-config-airbnb
```
 ```bash
touch .prettierrc
```
 ```bash
npm i -g eslint
```
 ```bash
eslint --init
```

## .prettierrc configuration:
```json
{
  "trailingComma": "none",
  "tabWidth": 4,
  "semi": true, 
  "singleQuote": true,
  "printWidth": 80,
  "jsxSingleQuote": true,
  "htmlWhitespaceSensitivity": "css"
}
```
## .eslintrc.json configuration:
```json
{
    "extends": ["airbnb", "prettier", "plugin:node/recommended"],
    "plugins": ["prettier"],
    "rules": {
        "prettier/prettier": ["error", { "endOfLine": "auto" }],
        "no-unused-vars": "warn",
        "no-console": "off",
        "func-names": "off",
        "no-process-exit": "off",
        "object-shorthand": "off",
        "class-methods-use-this": "off",
        "no-undef": "off"
    }
}
```


