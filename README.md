This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:  
You can use NPM instead of YARN (Up to you)  

### `yarn start` OR `npm run start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `yarn test` OR `npm run test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build` OR `npm run build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject` OR `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Manual deploy: `npm run s3:deploy` or `npm run build:s3:deploy`
Build and upload application to S3 bucket. Created CloudFront distribution should be invalidated manually.

```
S3 Bucket: https://s3.console.aws.amazon.com/s3/buckets/task-2-subtask-1
CloudFront URL: d2tialaojpj1gu.cloudfront.net
```

### Automated deployment: `cloudfront:update:build:deploy` or `npm run cloudfront:deploy`
Create/update S3 bucket and CloudFront distribution (using CloudFormation). 
This `cloudfront:build:deploy` command will upload S3 bucket and invalidate CloudFront distribution.

```
S3 Bucket: https://s3.console.aws.amazon.com/s3/buckets/task-2-subtask-2-app
S3 website: http://task-2-subtask-2-app.s3-website-eu-west-1.amazonaws.com/
Cloud Distribution: d9y9cpn13n9ls.cloudfront.net
```

### `cloudfront:domainInfo`
Retrieve Domain Name for deployed application.

```
Serverless: Web App Domain: d9y9cpn13n9ls.cloudfront.net
```
