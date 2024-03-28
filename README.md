# Brad Traversy's VSCode ESLint, Prettier & Airbnb Style Guide Setup
Updated: 28-3-2024

## Resources
* [Video: VSCode ESLint, Prettier & Airbnb Style Guide Setup](https://youtu.be/SydnKbGc7W8)

## Problem solving
* [Why do I keep getting Delete 'cr' [prettier/prettier]?](https://stackoverflow.com/questions/53516594/why-do-i-keep-getting-delete-cr-prettier-prettier)
* [no-undef message ESLint](https://medium.com/@jeryldev/a-beginners-story-how-to-setup-eslint-in-a-visual-studio-code-project-28b379a33cdb)

## Roadmap
### Installing ESLint & Prettier Visual Studio Code extensions
__Step 1__: 

[Install ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

__Step 2__: 

[Install Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

### VSCode settings
__Step 3__: 

Format on save: on.

__Step 4__: 

Prettier: Single quotes: on.

### Command Line/Bash
__Step 5__:
```bash
npm init -y
```
__Step 6__:
 ```bash
npm i -D eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-plugin-node eslint-config-node
```
__Step 7__:
 ```bash
npx install-peerdeps --dev eslint-config-airbnb
```
__Step 8__: (See .prettierrc configuration below. Copy-paste into this file)
 ```bash
touch .prettierrc
```
__Step 9__:
 ```bash
npm i -g eslint
```
__Step 10__:
 ```bash
eslint --init
```

### .prettierrc configuration:
__Step 11__: (Copy-paste into .prettierrc file)
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
### .eslintrc.json configuration:
__Step 12__: (Copy-paste into .eslintrc.json file)
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


