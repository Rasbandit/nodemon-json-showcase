# Nodemon.json

This file should be put in the root of your project in the same directory as where you run nodemon. This is going to fix a few issues that is run into when running nodemon at the root.

- Node won't restart when front end files change.
- React app won't run into a race condition when both services restart at the same time.
- Node will now restart when an SQL file changes in the db folder.
- Double checks that nodemon will ignore the .git folder and the node_modules

properties that it can take,
- restartable: a string that changes the restart command
- ignore: ignores these folders and wont restart if files in those change.
- watch: nodemon will only watch for changes in these folders
- NODE_ENV: set the NODE_ENV process.env variable to development.
- ext: file extensions that will be watched for changes

Alternatively the config object can be put in package.json associated with a "nodemonConfig" key.
[nodemon docs](https://github.com/remy/nodemon#packagejson)
