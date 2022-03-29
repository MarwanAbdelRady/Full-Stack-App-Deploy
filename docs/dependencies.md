# Application Dependencies

## Udagram Backend

This application uses **Express** API and **TypeScript**

### Deployment Steps

_Before following the steps below ensure that AWS EB CLI and NodeJS (v14.19.1) are properly installed_

1. Use `cd udagram/udagram-api` to navigate to the project's api directory.
2. Run `npm install` to install all project dependencies in the **package.json** file.
3. Run `npm run build` to build the project and create a **zip** Archive folder.
4. Run `eb deploy` to deploy the api to AWS Elastic Beanstalk.

### Environment

- Nodejs v14.19.1
- Expressjs
- AWS Elastic Beanstalk **(Needs to be configured as a web server)**

## Udagram Frontend

A Udagram web application that uses **Angular** and **TypeScript**

### Deployment

_Before following the steps below ensure that AWS CLI and NodeJS (v14.19.1) are properly installed_

1. Use `cd udagram/udagram-frontend` to navigate to the project's frontend directory.
2. Run `npm install` to install all project dependencies.
3. Run `npm run build` to build the project's frontend files.
4. Run the following command to deploy the built files to AWS S3

```
aws s3 cp --recursive --acl public-read ./www s3://marwansbucket/
```

### Environment

- NodeJS v14.19.1
- Ionicframework
- AngularJS
- AWS S3 **(Requires public accessibility and static website enabled)**
