
```bash
$ npm install -g npm@10.9.0
$ npm install -g pnpm

$ sudo chown node node_modules
$ sudo chown node .pnpm-store

$ pnpm create vite
# edit port in vite.config.ts
$ pnpm install
$ pnpm run dev

$ pnpm install -D tailwindcss postcss autoprefixer
$ pnpm dlx tailwindcss init -p
# edit tailwind.config.js
# edit index.css
$ pnpm run dev

$ pnpm dlx storybook@8 init
```

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
