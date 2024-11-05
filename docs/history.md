
## https://vite.dev/

```bash
$ npm create vite@latest
Need to install the following packages:
create-vite@5.5.5
Ok to proceed? (y) y


> npx
> create-vite

✔ Project name: … .
✔ Current directory is not empty. Please choose how to proceed: › Ignore files and continue
✔ Select a framework: › React
✔ Select a variant: › TypeScript + SWC

Scaffolding project in /workspaces/storybook8-react...

Done. Now run:

  npm install
  npm run dev

npm notice
npm notice New minor version of npm available! 10.8.3 -> 10.9.0
npm notice Changelog: https://github.com/npm/cli/releases/tag/v10.9.0
npm notice To update run: npm install -g npm@10.9.0
npm notice
```

## https://tailwindcss.com/
- https://tailwindcss.com/docs/guides/vite

```bash
$ npm install -D tailwindcss postcss autoprefixer

$ npx tailwindcss init -p
```

## Storybook
- https://storybook.js.org/docs/get-started/frameworks/react-vite?renderer=react

```bash
$ npx storybook@8 init

Need to install the following packages:
storybook@8.4.1
Ok to proceed? (y) y

╭──────────────────────────────────────────────────────╮
│                                                      │
│   Adding Storybook version 8.4.1 to your project..   │
│                                                      │
╰──────────────────────────────────────────────────────╯
 • Detecting project type. ✓
Installing dependencies...


up to date, audited 236 packages in 1s

67 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
 • Adding Storybook support to your "React" app • Detected Vite project. Setting builder to Vite. ✓

  ✔ Getting the correct version of 9 packages
    Configuring eslint-plugin-storybook in your package.json
  ✔ Installing Storybook dependencies
. ✓
Installing dependencies...


up to date, audited 415 packages in 2s

125 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

attention => Storybook now collects completely anonymous telemetry regarding usage.
This information is used to shape Storybook's roadmap and prioritize features.
You can learn more, including how to opt-out if you'd not like to participate in this anonymous program, by visiting the following URL:
https://storybook.js.org/telemetry

╭──────────────────────────────────────────────────────────────────────────────╮
│                                                                              │
│   Storybook was successfully installed in your project! 🎉                   │
│   To run Storybook manually, run npm run storybook. CTRL+C to stop.          │
│                                                                              │
│   Wanna know more about Storybook? Check out https://storybook.js.org/       │
│   Having trouble or want to chat? Join us at https://discord.gg/storybook/   │
│                                                                              │
╰──────────────────────────────────────────────────────────────────────────────╯

Running Storybook

> storybook8-react@0.0.0 storybook
> storybook dev -p 6006 --initial-path=/onboarding --quiet

@storybook/core v8.4.1

info Using tsconfig paths for react-docgen
5:16:47 AM [vite] ✨ new dependencies optimized: @storybook/blocks
5:16:47 AM [vite] ✨ optimized dependencies changed. reloading
```
