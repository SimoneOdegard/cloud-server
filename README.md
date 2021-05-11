# cloud-server

## Links to Deployed Servers

- [GUI Deploy](http://cloudserver3-env.eba-iipm2wic.us-west-2.elasticbeanstalk.com/)
- [CLI Deploy](http://cloud-server-2-env.eba-tp74mrnp.us-west-2.elasticbeanstalk.com/)

## GUI Deploy

1. Go to the service, *Elastic Beanstalk*
1. Click environments
1. Create a new environment
1. Select environment tier. Select web server
1. Creating your new environment
  - Create application name
  - Create environment name
  - Choose your platform. We will be using ```Node.js```, choose the most up to date branch and make sure the version is the most recent
  - Upload your code which will need to be in a .zip file without node_modules and packagelock.json
6. Create environment and let it deploy

**Note** If it doesn't deploy, check the names of your files. We had to change index.js to app.js in order to get it to work properly.

## CLI Deploy/EB Deploy

**Note** In order to get eb deploy to work, you must ACP first. If you miss this step, you'll get an error message returned back to you saying you're missing files.

1. ```eb init``` follow the steps that are asked. Remember, we are in region us-west-2, Oregon. Do not say yes to using codeCommit or SSH.
2. ```eb create cloud-server-2```
3. ```eb deploy```

## Github Actions

**Note** Anytime you update your repo, you need to change the version.

1. On your repo via github, add your access key and secret to settings > secrets > new repository secret.
1. Update your YML from master to main
1. Update your application name and environment name
1. Make sure you are in region us-west-2
1. Update your deployment package
1. Update the version label

[Github Actions](https://github.com/SimoneOdegard/cloud-server/actions)