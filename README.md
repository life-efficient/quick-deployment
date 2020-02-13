# deploy-npm-package

This simple bash script sequentially:
- builds your project by running `npm run build`
- adds all files to staging and commits them, asking you for a commit message
- pushes them to github
- runs `np` to publish them on npm
