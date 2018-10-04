# README

## Pre-requisites
A basic Express installation has been bootstrapped using the following commands. 
In this instance, the Twig template engine has been selected.
```
$ npm install -g express-generator
$ express --view twig spike-express
```

A set of AWS credentials under the profile 'claudia' will be required for the purpose of this spike.
This step has not been included within this spike although the dependence on the 'claudia' profile is implicit.

The default 'package.json' file has been updated to set the version number and include the claudia scripts.

## Go serverless

### Install dependencies
```
$ npm install
```
At this point it should be possible to start the Express server on port 3000 and view a 'Welcome to Express' page.
```
$ npm start
```

### Install claudia
```
$ npm run claudia:install
```

### Install the AWS serverless wrapper for Express
```
$ npm run claudia:generate
```

### Create the serverless lambda wrap for Express and note the URL returned
If the 'claudia' profile in ~/.aws/credentials is not used then edit package.json scripts to point to the alternate profile ( --profile new-profile )
```
$ npm run claudia:create
```

### Test the lambda invocation
```
$ npm run claudia:test
```
Additionally, test the lambda via browser using the URL returned from the create step (above)

### Make code changes and update the lambda
```
$ npm run claudia:update
```
