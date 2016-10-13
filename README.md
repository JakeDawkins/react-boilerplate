# markdown-editor

This project was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app).

### About

This repo is a basic create-react-app instance that has had the following changes:
1. Ejected
2. Components folder and pages folder added
3. Added SCSS preLoaders
3. Mapped SCSS files to a stub for jest testing files that import SCSS files


### Make your own instead
- Good for making sure everything is up to date

```
create-react-app project-name
cd project-name
npm run eject
npm install sass-loader node-sass --save-dev
```

__Add the following to /config/webpack.config.dev.js and /config/webpack.config.prod.js__
__Add to the preLoaders array__
```
{
  test: /\.scss$/,
  include: paths.appSrc,
  loaders: ["style", "css", "sass"]
}
```

__Lastly, to ignore SCSS imports for testing__
__Add to moduleNameMapper in package.json__
```
"^.+\\.scss$": "<rootDir>/config/jest/CSSStub.js"
```
