# Building 
## Build dev
docker build -f Dockerfile.dev .

## Build prod
docker build .

# Running
## Run prod
docker run -p 8080:80 f4d302a7e32a
http://localhost:8080/

## Run dev
docker run -p 3000:3000 f9fd616eb3ca
http://localhost:3000

## Docker compose run dev
docker-compose up
http://localhost:3000

********

# File change detection on Windows
in .env file   
CHOKIDAR_USEPOLLING=true         

Allow Docker shared files and open Firewall port 445

******

# Travis
https://travis-ci.org/

# Elastic beanstalk 
* Create new application container              
  ** name: 'docker-react'       
  ** Create    
* Create an environment inside the container (create one now)                
  ** Web server environment
     *** Base configuration/ Platform / Docker
     *** Application code / Sample application 

* Create new IAM user 
  ** User name: docker-react-travis-ci
  ** Access type: Programmatic access
  ** Attach existing policies directly -> beanstalk -> provide full acces 
  ** Tags: null
  ** Review : Create user 
  Save secret access key (only shown this 1 time)

  * Travis secret
    ** Dashboard / More options / Settings / Environment variables 
       Access key ID / Secret Access key ID

  * Add deploy options to travis file
  * Add EXPOSE to Dockerfile (only for AWS)
  * Push changes to github 
  * Go to Amazon Beanstalk, click deploy URL 

**************************************
**************************************

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br>
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br>
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: https://facebook.github.io/create-react-app/docs/code-splitting

### Analyzing the Bundle Size

This section has moved here: https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size

### Making a Progressive Web App

This section has moved here: https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app

### Advanced Configuration

This section has moved here: https://facebook.github.io/create-react-app/docs/advanced-configuration

### Deployment

This section has moved here: https://facebook.github.io/create-react-app/docs/deployment

### `npm run build` fails to minify

This section has moved here: https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify
