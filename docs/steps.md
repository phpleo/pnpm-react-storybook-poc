
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
# Or with specific version:
$ npm install -g npm@10.9.0
```

```bash
$ npm install -g pnpm
```

## 5. Install https://vite.dev/

```bash
$ pnpm create vite
```

Output:
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

## Install Storybook 8 (The slow part, take a ☕)
- https://storybook.js.org/docs/get-started/frameworks/react-vite?renderer=react

```bash
$ pnpm dlx storybook@8 init
```

Output:
```bash
╭──────────────────────────────────────────────────────╮
│                                                      │
│   Adding Storybook version 8.4.2 to your project..   │
│                                                      │
╰──────────────────────────────────────────────────────╯
 • Detecting project type. ✓
Installing dependencies...

Lockfile is up to date, resolution step is skipped
Already up to date
Done in 920ms
 • Adding Storybook support to your "React" app • Detected Vite project. Setting builder to Vite. ✓

  ✔ Getting the correct version of 9 packages
    Configuring eslint-plugin-storybook in your package.json
  ✔ Installing Storybook dependencies
. ✓
Installing dependencies...

Lockfile is up to date, resolution step is skipped
Already up to date
Done in 1.2s

attention => Storybook now collects completely anonymous telemetry regarding usage.
This information is used to shape Storybook's roadmap and prioritize features.
You can learn more, including how to opt-out if you'd not like to participate in this anonymous program, by visiting the following URL:
https://storybook.js.org/telemetry

╭──────────────────────────────────────────────────────────────────────────────╮
│                                                                              │
│   Storybook was successfully installed in your project! 🎉                   │
│   To run Storybook manually, run pnpm run storybook. CTRL+C to stop.         │
│                                                                              │
│   Wanna know more about Storybook? Check out https://storybook.js.org/       │
│   Having trouble or want to chat? Join us at https://discord.gg/storybook/   │
│                                                                              │
╰──────────────────────────────────────────────────────────────────────────────╯

Running Storybook

> storybook8-react@0.0.0 storybook /workspaces/storybook8-react
> storybook dev -p 6006 "--initial-path=/onboarding" "--quiet"

@storybook/core v8.4.2

info Using tsconfig paths for react-docgen
7:08:02 PM [vite] ✨ new dependencies optimized: @storybook/blocks, @mdx-js/react
7:08:02 PM [vite] ✨ optimized dependencies changed. reloading
```
