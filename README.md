

# Formating

https://prettier.io/


https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode

# Build

`rimraf ./dist && tsc --project tsconfig.build.json`

`tsconfig.build.json`

```json
{
  "extends": "./tsconfig.json",
  "exclude": [
    "src/**/*.test.ts"
  ]
}
```

