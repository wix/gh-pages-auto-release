# gh-pages-auto-release

This node module will help you to publish your package to dist folder as a github page.

All you have to do is run `gh-pages-auto-release` in your release script

```json
{
  "name": "my-package",
  "version": "1.0.0",
  "scripts": {
    "build": ":", 
    "test": ":",
    "release": "gh-pages-auto-release",
  },
  "devDependencies": {
    "gh-pages-auto-release": "*"
  }
}
```

### Your package is automatically re-published every CI build

Once you're build is complete in CI, your package can be accessed at:
```sh
https://wix-private.github.io/package-name/
```
where `package-name` is the name you gave your git repository

This url will obviously work only if you have `dist/index.html` file generated by your build.
