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