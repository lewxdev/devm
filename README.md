# devrm

> [!WARNING]
> Early development. This project is experimental and built with cutting-edge tooling. Expect breaking changes.

Toolchain version manager using devEngines to install and auto-switches runtimes and package managers.

Supports Node.js, Bun, Deno, npm, Yarn, pnpm.

## Install

```shell
npm install --global devrm
```

## Usage

Run `devrm use <runtime>` to update the `devEngines` field in your project's `package.json`.

Use an exact version
```shell
devrm use node@25.8.1
```

Use an alias (`latest`, `lts`)
```shell
devrm use node@latest
```

`devrm` provides shims so toolchain CLIs resolve versions from your project's `devEngines`.

Example `package.json`
```json
{
  "devEngines": {
    "packageManager": {
      "name": "npm",
      "version": "11.11.0"
    },
    "runtime": {
      "name": "node",
      "version": "25.8.1"
    }
  }
}
```
