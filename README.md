# react-upload
This is the repository which help in deploying react app on Github Page
Procedure :

1- First create a repository named my-app using create-react-app.

npm init react-app my-app

2- We need to install GitHub Pages package as a dev-dependency.

cd my-app
npm install gh-pages --save-dev

3- Add properties to package.json file.

The first property we need to add at the top level homepage second we will define this as a string and the value will be "http://{username}.github.io/{repo-name}" {username} is your GitHub username, and {repo-name} is the name of the GitHub repository you created it will look like this :

"homepage": "http://username.github.io/my-app"

Second in the existing scripts property we to need to add predeploy and deploy.

"scripts": {
//...
"predeploy": "npm run build",
"deploy": "gh-pages -d build"
}

4- Create a Github repository and initialize it and add it as a remote in your local git repository.

Now, create a remote GitHub repository with your app name and go back initialize this
git init
add it as remote
git remote add origin git@github.com:username/my-app.git

5- Now deploy it to GitHub Pages.

just run the following command :

npm run deploy
The  app will be pulished on hompage url
