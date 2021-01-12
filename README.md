# AngularSless1

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.1.0.

## Development server

Run `ng run server` for a dev server. Navigate to `http://localhost:8080/`. The app will automatically reload if you change any of the source files.

## Serverless Environment

`@ng-toolkit/serverless@8.1.0` have been used with this project to convert the normal angular app into serverless angular app.

## Installing all the dependencies

Run `npm install` as a first step in your local once you have cloned this repo, in order to clear any ambiguity

## Configure Serverless Environment

Make sure to install and authenticate the serverless environment in your local, Please refer [Setting Up Your Credentials for AWS](https://coursetro.com/posts/code/165/Deploying-your-Angular-App-to-a-Serverless-Environment-)

## Configure the serverless yaml to update your AWS region 

Make sure to change the value of the `provider:region:` under the serverless.yml as per your AWS region. 

## Deployment to aws serverless

Run `npm run build:serverless:deploy` to deploy this app to your AWS

## Changes made in order to correct the deployment process to AWS

Added `- '!node_modules/@vendia/**'` in the `package:exclude:` section of the serverless.yml file
Updated tsconfig.json file to correct the default configuration of `esModuleInterop` to `false`.
Added the `npm install --save-dev serverless-api-compression` additionally for the compression of the output to be deployed on the AWS serverless environment.
These settings and the correct versions of the dependencies made this app run successfully on the AWS serverless environment.
