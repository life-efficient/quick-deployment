# quick-deployment

*When you move fast, even deployment becomes a bottleneck*

This repo contains tools that I use to frequently deploy different types of code including:
- NPM packages
- websites & webapps

Some scripts only currently support my stack:
- serving websites through AWS S3, which are built with create-react-app

Listed below are the different bash scripts and their explanations

## deploy-np

This simple bash script sequentially:
- builds your project by running `npm run build`
- adds all files to staging and commits them, asking you for a commit message
- pushes them to github
- runs `np` to publish them on npm

## deploy-webapp

This script sequentially:
- builds your project by running `npm run build`
- adds all files to staging and commits them, asking you for a commit message
- pushes them to github
- syncs the `build` folder with the bucket you are prompted to enter

## deploy-lambda

From within a folder, which must be entitled the name of the lambda function that you want to deploy, this script zips up everything in the ```src``` directory into a deployment package, and updates the code within the associated lambda function on AWS.
