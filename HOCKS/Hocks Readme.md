

**Here's an example of how to configure package.json to run tests with multiple tags:**
json
{
  "name": "webdriverio-project",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "wdio wdio.conf.js --cucumberOpts.tagExpression='@tag1 and @tag2'"
  },
  "dependencies": {
    ...
  },
  "devDependencies": {
    ...
  }
}
