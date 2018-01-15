# gh-pages-auto-release

This node module will help you to publish your package to dist folder as a github page.

All you have to do is run `gh-pages-auto-release` in your release script

```json
{
  "name": "package-name",
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

### The `--git-repo` option

By default the output of your project is pushed to a branch on its own repository (designated by the `GIT_REMOTE_URL` environment variable). You can change this by pointing to a different repository using the `--git-repo` option.
 
For example: `bower-auto-release --git-repo git@github.com:wix/my-library-bower-component`

This option is typically used on monorepos that have multiple bower components to release. Since bower's design dictates one-to-one relationship between published component and git repository, you should create a separate repository for publishing and pass it using this option.

### Your page is automatically re-published every CI build

Once you're build is complete in CI, your page can be accessed at:
```sh
https://wix-private.github.io/package-name/
```
where `package-name` is the name you gave your git repository

obvious note: This url will work only if you have `dist/index.html` file generated by your build.
