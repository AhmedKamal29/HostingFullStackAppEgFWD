<h1>Hosting a FullStack Application on AWS </h1>
<h2>Project Documentation</h2>

<h1>Infrastructure description</h1>

![deployment infra](https://user-images.githubusercontent.com/53512084/222455094-d09e47c3-5872-48dd-9649-e39faf1181b5.jpg)

<h1>App Dependencies</h1>
<h3>Udagram-API Package.json Dependancies</h3>

```
 "dependencies": {
    "@types/bcryptjs": "2.4.2",
    "@types/jsonwebtoken": "^8.3.2",
    "aws-sdk": "^2.429.0",
    "bcryptjs": "2.4.3",
    "body-parser": "^1.18.3",
    "class-validator": "^0.14.0",
    "cors": "^2.8.5",
    "dotenv": "^8.2.0",
    "email-validator": "^2.0.4",
    "express": "^4.16.4",
    "jsonwebtoken": "^9.0.0",
    "pg": "^8.7.1",
    "reflect-metadata": "^0.1.13",
    "rimraf": "^4.1.2",
    "sequelize": "^6.5.0",
    "sequelize-typescript": "^2.1.3"
  },
  "devDependencies": {
    "@types/bluebird": "^3.5.26",
    "@types/cors": "^2.8.6",
    "@types/express": "^4.16.1",
    "@types/node": "^11.11.6",
    "@types/sequelize": "^4.27.44",
    "@types/validator": "^13.7.12",
    "@typescript-eslint/eslint-plugin": "^2.19.2",
    "@typescript-eslint/parser": "^2.19.2",
    "chai": "^4.2.0",
    "chai-http": "^4.2.1",
    "copyfiles": "^2.4.1",
    "eslint": "^6.8.0",
    "eslint-config-google": "^0.14.0",
    "mocha": "^10.2.0",
    "ts-node-dev": "^1.0.0-pre.32",
    "typescript": "^4.2.3"
  }
```

<h3>Udagram-Frontend Package.json Dependancies</h3>

```
  "dependencies": {
    "@angular/common": "^8.2.14",
    "@angular/core": "^8.2.14",
    "@angular/forms": "^8.2.14",
    "@angular/http": "^7.2.16",
    "@angular/platform-browser": "^8.2.14",
    "@angular/platform-browser-dynamic": "^8.2.14",
    "@angular/router": "^8.2.14",
    "@ionic-native/core": "^5.0.0",
    "@ionic-native/splash-screen": "^5.0.0",
    "@ionic-native/status-bar": "^5.0.0",
    "@ionic/angular": "^4.1.0",
    "core-js": "^2.5.4",
    "rxjs": "~6.5.4",
    "zone.js": "~0.9.1"
  },
  "devDependencies": {
    "@angular-devkit/architect": "~0.12.3",
    "@angular-devkit/build-angular": "^0.803.24",
    "@angular-devkit/core": "~7.2.3",
    "@angular-devkit/schematics": "~7.2.3",
    "@angular/cli": "~8.3.25",
    "@angular/compiler": "~8.2.14",
    "@angular/compiler-cli": "~8.2.14",
    "@angular/language-service": "~8.2.14",
    "@ionic/angular-toolkit": "~1.4.0",
    "@types/jasmine": "~2.8.8",
    "@types/jasminewd2": "~2.0.3",
    "@types/node": "~10.12.0",
    "@typescript-eslint/eslint-plugin": "^2.20.0",
    "@typescript-eslint/parser": "^2.20.0",
    "codelyzer": "~4.5.0",
    "jasmine-core": "~2.99.1",
    "jasmine-spec-reporter": "~4.2.1",
    "karma": "~3.1.4",
    "karma-chrome-launcher": "~2.2.0",
    "karma-coverage-istanbul-reporter": "~2.0.1",
    "karma-jasmine": "~1.1.2",
    "karma-jasmine-html-reporter": "^0.2.2",
    "protractor": "~5.4.0",
    "ts-node": "~8.0.0",
    "tslint": "~5.12.0",
    "typescript": "^3.5.3"
  }
```

<h1>Circle CI Pipeline process</h1>

![circleci diagram](https://user-images.githubusercontent.com/53512084/222455165-56f378a6-e80b-4b8e-a497-31102a16ccb6.jpg)

1. When the developer pushes a new code to the repo the Circle ci is triggred to begin automating the build and deployment. 
2. We begin first with the building where the pipline begins setting u the build environment by doing the following: 
    - Preparing the env variables 
    - Install node js
    - Install both frontend and backend dependencies
    - Build front end 
    - Build backend
3. The piplines goes on hold waiting for the developers approval on the process
4. We reach the deployment phase where the pipline executes the following: 
    - Setting up elastic beanstalk CLI 
    - Install AWS CLI - latest version
    - Configure AWS CLI with the access key and secret key
    - Begin deploying the app based on the configuration yml located in the project
5. The App is successfully deployed

<h1 align="center">No you are all set and ready good to go😉</h1>
