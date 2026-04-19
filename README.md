#### Install Requirements

npm install zod
npm install express
npm install --save-dev @types/express
npm install --save-dev prisma
npm install winson -> for logging
npm install bcrypt
npm install --save-dev @types/bcrypt
npm install uuid
npm install --save-dev @types/uuid
npm install --save-dev jest @types/jest
npm install --save-dev babel-jest @babel/preset-env

edit package.json

```"scripts": {
    "test": "jest"
  },
  "jest": {
    "transform": {
      "^.+\\.[t|j]sx?$": "babel-jest"
    }
  }
```

buat babel.config.json

```{
  "presets": ["@babel/preset-env"]
}
```

npm install --save-dev @babel/preset-typescript
npm install --save-dev @jest/globals

edit babel.config.json

```{
  "presets": [
  "@babel/preset-env",
  "@babel/preset-typescript"
}
```

npm install --save-dev supertest @types/supertest
npm install --save-dev typescript

npx tsc --init

- Semua konfigurasi akan dibuat di file tsconfig.json
- Ubah “module” menjadi “commonjs”
- Ubah "moduleResolution" menjadi "Node"
- Tambahkan include src/\*_/_
- Ubah outDir menjadi “./dist”

#### Setup Database
