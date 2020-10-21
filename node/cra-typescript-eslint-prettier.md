---
title: 'CRA + Typescript 프로젝트 Eslint, Prettier 설정'
date: 2020-10-21 23:42:29
category: 'node'
draft: true
---


```shell
$ yarn create react-app cra-settings --template typescript
$ cd cra-settings
$ yarn add eslint @typescript-eslint/parser @typescript-eslint/eslint-plugin prettier eslint-config-prettier eslint-plugin-prettier -D
```

`.eslintrc`
```json
{
  "parser": "@typescript-eslint/parser",
  "extends": [
    "plugin:react/recommended",
    "plugin:@typescript-eslint/recommended",
    "prettier/@typescript-eslint",
    "plugin:prettier/recommended"
  ],
  "parserOptions": {
    "ecmaFeatures": {
      "jsx": true
    }
  },
  "rules": {
    // Place to specify ESLint rules.
    // Can be used to overwrite rules specified from the extended configs
    // e.g. "@typescript-eslint/explicit-function-return-type": "off",
  },
  "settings": {
    "react": {
      "version": "detect"
    }
  },
  "ignorePatterns": ["*.config.js"]
}

```

`.prettierrc`
```json
{
  "singleQuote": true,
  "semi": true,
  "useTabs": false,
  "tabWidth": 2,
  "trailingComma": "all",
  "printWidth": 80
}

```