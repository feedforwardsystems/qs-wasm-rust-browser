# qs-wasm-rust-browser

## node

```shell
nvm install 16 && nvm use 16
```

newer versions requires `--openssl-legacy-provider`

## rust

```shell
curl https://rustwasm.github.io/wasm-pack/installer/init.sh -sSf | sh
cargo install cargo-generate
```

```shell
cargo generate --git https://github.com/rustwasm/wasm-pack-template
# project name: wasm
```

```shell
npm init wasm-app www && cd www && npm install
```

www/package.json

```json
  "dependencies": {
    "wasm": "file:../pkg"
  },
```

www/index.js

```js
import * as wasm from "wasm";
```

# build

```shell
wasm-pack build wasm/
npm install www/
```

# run

```
cd www/
npm run start
```
