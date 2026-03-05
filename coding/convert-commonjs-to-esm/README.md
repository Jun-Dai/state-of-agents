# Task: Convert CommonJS to ESM

**Category:** Coding

## Description

Ask the agent to convert a CommonJS module to ES Module (ESM) syntax.

## Prompt

> Convert the following CommonJS module to ESM syntax:
>
> ```js
> const fs = require('fs');
> const path = require('path');
>
> const BASE_DIR = path.resolve(__dirname, 'data');
>
> function readFile(name) {
>   return fs.readFileSync(path.join(BASE_DIR, name), 'utf8');
> }
>
> module.exports = { readFile };
> ```

## Results

| Agent | Score | Notes |
|---|---|---|
| | | |

## Evaluation Criteria

- **Correctness**: Does the converted code use valid ESM syntax (`import`/`export`)?
- **Equivalence**: Does it preserve the original behavior?
- **`__dirname` handling**: Does the agent correctly replace `__dirname` with an ESM equivalent (e.g., `import.meta.url` + `fileURLToPath`)?
- **Named exports**: Is `module.exports` correctly converted to a named `export`?
