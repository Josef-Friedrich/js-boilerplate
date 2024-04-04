[![npm](https://img.shields.io/npm/v/express.svg)](https://npmjs.com/package/express)

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

# @/* paths path alias

```json
{
  "scripts": {
    "build:typescript": "tsc --project tsconfig.build.json && tsc-alias",
  }
}
```

tsconfig.json

```json
{
  "compilerOptions": {

    "paths": {
      "@/*": ["./src/*"]
    }
  }
}
```


vitest.config.ts

```ts
import { defineConfig } from 'vitest/config'

export default defineConfig({
  test: {
    alias: {
      '@/': new URL('./src/', import.meta.url).pathname
    }
  }
})
```

