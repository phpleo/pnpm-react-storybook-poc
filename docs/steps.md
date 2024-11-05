
## 1. Initial project structure

```bash
.
├── .devcontainer
│   └── devcontainer.json
├── .editorconfig
├── .gitignore
└── docs
    └── steps.md
```

## 2. `devcontainer.json` configuration

```javascript
  // "customizations": {},
  "customizations": {
    "vscode": {
      "extensions": [
        "EditorConfig.EditorConfig",
        "GitHub.copilot",
        "GitHub.copilot-chat"
      ]
    }
  },

  // Mounts for the workspace
  // https://code.visualstudio.com/remote/advancedcontainers/improve-performance
  "mounts": [
    "source=${localWorkspaceFolderBasename}-node_modules,target=${containerWorkspaceFolder}/node_modules,type=volume",
    "source=${localWorkspaceFolderBasename}-.pnpm-store,target=${containerWorkspaceFolder}/.pnpm-store,type=volume"
  ]
```

### 2.1. Run `Dev containers: Rebuild and reopen in container` in VSCode

## 3. chown mount folders

```bash
$ sudo chown node node_modules
$ sudo chown node .pnpm-store
```

## 4. Update and install basic node packages

```bash
$ npm install -g npm@latest
$ npm install -g npm@10.9.0
```

```bash
$ npm install -g pnpm
```

## 5. Install https://vite.dev/

```bash
$ pnpm create vite
```

```bash
✔ Project name: … .
✔ Current directory is not empty. Please choose how to proceed: › Ignore files and continue
✔ Select a framework: › React
✔ Select a variant: › TypeScript + SWC

Scaffolding project in /workspaces/pnpm-react-storybook-poc...

Done. Now run:

  pnpm install
  pnpm run dev
```

### 5.1. Edit port in `vite.config.ts`

```javascript
export default defineConfig({
  plugins: [react()],
  server: {
    port: 3000,
    host: '127.0.0.1',
  }
})
```

### 5.2. Run & test Vite

```bash
$ pnpm install
$ pnpm run dev
```

## Install `https://tailwindcss.com/`
- https://tailwindcss.com/docs/guides/vite

```bash
$ pnpm install -D tailwindcss postcss autoprefixer
$ pnpm dlx tailwindcss init -p
```

- Edit tailwind.config.js
- Edit index.css

```bash
$ pnpm run dev
```
