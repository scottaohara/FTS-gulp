# FTS-gulp

Fresh Tilled Soil's default gulp config.


## Getting Started

```
git clone
cd FTS-gulp
npm install
```

## Commands

```
// Run build and watch for changes
npm start

// Build dist folder
npm run dist
```

## Project Structure

All development is limited to the `/src` folder.
Running `npm start` will run a gulp task to compile and build a `/dist` folder which
is referenced via the built in server at [localhost:3000](http://localhost:3000).
With gulp running, saving a file within the `/src` folder will run the
associated gulp task and update the `/dist` folder accordingly.

## Developer
FTS uses linter configs to ensure consistent code. The `npm start` task will watch JS and SCSS files and run
a linting report every time they are changed. While this is helpful, sometimes it's nice to have an automated
way to make the suggested changes. If you're using the Atom browser, install the following plugins:
- linter-eslint
- stylefmt
- linter-stylelint

The two linter plugins will allow you to see in real time in your editor any linting warnings and errors.
When you want to try an automated fix within atom, open the command panel (shift cmd P) and then run:
`stylefmt: execute` or `Linter Eslint:Fix File`

You could also install the command line utilities if you prefer, and run:
`stylefmt src/assets/css/**/*.css` or `eslint --fix src/assets/js/**/*.js`

For now, this solution is preferred instead of a gulp task so the developer still has final say over
the file format.

## Tasks

### serve()
[BrowserSync](https://www.npmjs.com/package/browser-sync)

### html()
Moves .html files to `/dist` folder.

### svgmin()
[gulp-svgmin](https://www.npmjs.com/package/gulp-svgmin)

### fonts()
Moves font files to `/dist` folder.

### imagemin()
[gulp-imagemin](https://www.npmjs.com/package/gulp-imagemin)

### styles()
[gulp-sass](https://www.npmjs.com/package/gulp-sass)

[gulp-autoprefixer](https://www.npmjs.com/package/gulp-autoprefixer)

### es6()
[webpack](https://webpack.github.io/)

### fileinclude()
[gulp-file-include](https://www.npmjs.com/package/gulp-file-include)
