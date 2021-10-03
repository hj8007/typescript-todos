# TypeScript
[![Reference](https://img.shields.io/badge/-co--studying-000000?style=flat&logo=GitHub&link=https://github.com/co-studying/typescript-todos)](https://github.com/co-studying/typescript-todos)

### 1. 기본 프로젝트 생성
```
$ npm init -y
```


### 2. 패키지 설치
```
$ npm i -D @babel/core
$ npm i -D @babel/preset-env
$ npm i -D @babel/preset-typescript
$ npm i -D @typescript-eslint/eslint-plugin
$ npm i -D @typescript-eslint/parser
$ npm i -D eslint
$ npm i -D eslint-plugin-prettier
$ npm i -D prettier
$ npm i -D typescript
```


### 3. tsconfig.json & .eslintrc.js 파일 생성
`tsconfig.json`
```
{
    "compilerOptions": {
        "allowJs": true,
        "checkJs": true,
        "noImplicitAny": true,
    },
    "include": ["./src/**/**"]
}
```

`.eslintrc.js`
```
module.exports = {
  root: true,
  env: {
    browser: true,
    node: true,
    jest: true,
  },
  extends: [
    'eslint:recommended',
    'plugin:@typescript-eslint/eslint-recommended',
    'plugin:@typescript-eslint/recommended',
  ],
  plugins: ['prettier', '@typescript-eslint'],
  rules: {
    'prettier/prettier': [
      'error',
      {
        singleQuote: true,
        semi: true,
        useTabs: false,
        tabWidth: 2,
        printWidth: 80,
        bracketSpacing: true,
        arrowParens: 'avoid',
      },
    ],
    '@typescript-eslint/no-explicit-any': 'off',
    'prefer-const': 'off',
  },
  parserOptions: {
    parser: '@typescript-eslint/parser',
  },
};
```




