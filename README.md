<h2 align="center">Bootstrap 4.6 | Starter Template</h2>

<p align="center">A NPM template project for Bootstrap prototyping and customization.</p>

<hr>

### Summary

- [About](#about)
- [Main Files](#main-files)
- [Usage](#usage)
- [Scripts](#scripts)
- [Copyright](#copyright)

<hr>

### [About](#about)

`bootstrap4-starter-template` is a template for building Bootstrap 4.6 projects, using NPM. You can use it for prototyping and specially for customizing Bootstrap themes. It was **inspired** by the [bootstrap-npm-starter](https://github.com/twbs/bootstrap-npm-starter), made by [@mdo](https://twitter.com/mdo). **It's neither a fork nor a copy**, I built it from scratch using my own project file structure and with the tools I like. For example, I switched from [node-sass](https://www.npmjs.com/package/node-sass) (because it's now deprecated) to [Dart Sass](https://sass-lang.com/dart-sass). I also removed [nodemon](https://www.npmjs.com/package/nodemon) and [serve](https://www.npmjs.com/package/serve) to use [lite-server](https://www.npmjs.com/package/lite-server) instead, for simplicity. [Popper.JS](https://popper.js.org/), [jQuery](https://jquery.com/) and Bootstrap JS (`bootstrap.min.js`) are being provided separately via CDN.

<hr>

### [Main Files](#main-files)

- An HTML page (`src/index.html`) with a simple `jumbotron` and `modal` to test Bootstrap and JavaScript;
- [Bootstrap](https://getbootstrap.com) (currently using v4.6.0), source files via NPM;
- NPM scripts (`package.json`) for useful tasks (consult the [Scripts section](#scripts) for more detailed information);
- Stylesheet (`src/scss/main.scss`) to import Bootstrap Sass partials and custom variables;
- Stylesheet (`scss/_custom-variables.scss`) to override Bootstrap and make your own variables;

<hr>

### [Usage](#usage)

**You'll need [Node.js](https://nodejs.org/) and [Git](https://git-scm.com/) installed to clone and run this project.**

First, clone the repository and get into the project's folder

```shell
git clone https://github.com/evfjunior/bootstrap4-starter-template.git
cd bootstrap4-starter-template
```

Install packages and dependencies

```shell
npm i
```

Start the demo project...

```shell
npm start
```

...or start coding (Sass will watch for changes).

```shell
npm run dev
```

<hr>

### [Scripts](#scripts)

- **`compile-watch`**: Runs [Dart Sass](https://sass-lang.com/dart-sass) with the `--watch` flag to watch for changes during development;
- **`compile-css`**: Only compiles source SASS to CSS without watching;
- **`server`**: Starts [lite-server](https://www.npmjs.com/package/lite-server), configured to open `src/index.html` on default port (3000);
- **`prefix-css`**: Runs [Autoprefixer](https://github.com/postcss/autoprefixer) on the compiled `src/css/main.css`;
- **`purge-css`**: Runs [PurgeCSS](https://purgecss.com) to clean and remove unused CSS rules;
- **`build-css`**: Runs `compile-css` and `prefix-css`;
- **`lint-css`**: Runs a Linter using the official Bootstrap's Stylelint configuration, [stylelint-config-twbs-bootstrap](https://github.com/twbs/stylelint-config-twbs-bootstrap). You can use it to configure your [Github Actions](https://github.com/features/actions) workflow (`ci.yml` file not included);
- **`dev`**: Runs `compile-watch` and `server` for development environment;
- **`build`**: Runs `lint-css`, `build-css` and `purge-css` to build a production-ready version;
- **`start`**: Runs `build` and `server` to demo the final project.

<hr>

### [Copyright](#copyright)

&copy; evfjunior 2021 and licensed MIT.
