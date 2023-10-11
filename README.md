<div align=center>

![views] ![stars] ![forks] ![issues] ![license] ![repo-size]

![](/public/favicon.png)

# SvelteKit Starter Template

### A Minimal SvelteKit Starter Template with TypeScript, Tailwind CSS, and pre-configured with ESLint, Prettier, and Husky.

</div>

## Features

- ⚡ **[SvelteKit](https://kit.svelte.dev/)** - Cybernetically enhanced web apps
- 🎨 **[Tailwind CSS](https://tailwindcss.com/)** - A Utility-First CSS Framework for Rapid UI Development
- 📦 **[TypeScript](https://www.typescriptlang.org/)** - A typed superset of JavaScript that compiles to plain JavaScript
- 📝 **[ESLint](https://eslint.org/)** - The pluggable linting utility for JavaScript and JSX
- 🛠 **[Prettier](https://prettier.io/)** - An opinionated code formatter
- 🐶 **[Husky](https://typicode.github.io/husky/#/)** - A tool that makes Git hooks easy
- 🚫 **[lint-staged](https://github.com/okonet/lint-staged)** - Run linters against staged git files
- 📄 **[commitlint](https://commitlint.js.org/#/)** - Lint commit messages
- 📦 **[bun](https://bun.sh)** - A JavaScript runtime w/ Fast, disk space efficient package manager

## Getting Started

**Install `degit` globally**

```bash
bun i -g degit || pnpm i -g degit || yarn global add degit || npm i -g degit
```

**Create a new project from this template**

```bash
degit rajput-hemant/sveltekit-template <project-name>
cd <project-name>
```

**Install dependencies**

```bash
bun i || pnpm i || yarn || npm i
```

**Initialize a new git repository _(Optional)_:**

```bash
git init
git add .
git commit --no-verify -m "init"
```

## Available Scripts

In the project directory, you can run:

| **Script**    | **Description**                                   |
| ------------- | ------------------------------------------------- |
| `dev`         | Runs the app in the development mode.             |
| `build`       | Builds the app for production.                    |
| `start`       | Runs the built app in the production mode.        |
| `preview`     | Builds and serves the app in the production mode. |
| `lint`        | Runs next lint on the project.                    |
| `check`       | Runs SvelteKit checks.                            |
| `check:watch` | Runs SvelteKit checks in watch mode.              |
| `fmt:check`   | Checks if the code is formatted with Prettier.    |
| `fmt:write`   | Formats the code with Prettier.                   |
| `prepare`     | Installs husky git hooks.                         |

## Folder Structure

```bash
.
├── public
│   └── favicon.png
├── src
│   ├── components
│   │   └── tailwind-indicator.svelte
│   ├── lib
│   │   └── utils.ts
│   ├── routes
│   │   ├── +layout.svelte
│   │   └── +page.svelte
│   ├── types
│   │   └── reset.d.ts
│   ├── app.css
│   ├── app.d.ts
│   └── app.html
├── bun.lockb
├── LICENSE
├── package.json
├── postcss.config.js
├── README.md
├── renovate.json
├── svelte.config.js
├── tailwind.config.js
├── tsconfig.json
└── vite.config.ts
```

## After Installation Checklist

- [ ] Update `package.json` with your project details.
- [ ] Update `README.md` with your project details.
- [ ] Update `LICENSE` with your name and year.

## Switching Package Manager

This template uses [bun](https://bun.sh/docs/cli/install) as the default package manager. If you want to use `pnpm`, `npm` or `yarn`, you need to remove the `bun.lockb` file and run `pnpm i`, `npm i` or `yarn` to generate the lock file for the respective package manager.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributors:

<div align=center>

[![][contributors]][contributors-graph]

_Note: It may take up to 24h for the [contrib.rocks][contrib-rocks] plugin to update because it's refreshed once a day._

</div>

<!----------------------------------{ Labels }--------------------------------->

[views]: https://komarev.com/ghpvc/?username=sveltekit-template&label=view%20counter&color=red&style=flat
[repo-size]: https://img.shields.io/github/repo-size/rajput-hemant/sveltekit-template
[issues]: https://img.shields.io/github/issues-raw/rajput-hemant/sveltekit-template
[license]: https://img.shields.io/github/license/rajput-hemant/sveltekit-template
[forks]: https://img.shields.io/github/forks/rajput-hemant/sveltekit-template?style=flat
[stars]: https://img.shields.io/github/stars/rajput-hemant/sveltekit-template
[contributors]: https://contrib.rocks/image?repo=rajput-hemant/sveltekit-template&max=500
[contributors-graph]: https://github.com/rajput-hemant/sveltekit-template/graphs/contributors
[contrib-rocks]: https://contrib.rocks/preview?repo=rajput-hemant%sveltekit-template
