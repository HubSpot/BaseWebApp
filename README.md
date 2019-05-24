# Base Web App

Check it out at: https://intense-depths-97149.herokuapp.com/

Today, we’ll get you up and running with a basic web application that you’ll then be able to build off of. But first, there are a few accounts you’ll need to set up and technologies you’ll need to install on your computer.

## Part One: Getting the code on your machine

#### 1. Install the tools:
- [ ] Create a <a href="https://signup.heroku.com/" target="_blank">Heroku account</a> (Make sure to set your primary language as "Node")
- [ ] Download and install <a href="https://toolbelt.heroku.com/" target="_blank">Heroku's command line tools</a>
- [ ] Create a <a href="https://github.com/join" target="_blank">GitHub account</a>
- [ ] Download and install <a href="https://help.github.com/articles/set-up-git/#setting-up-git" target="_blank">git (GitHub's command line tool)</a>
- [ ] Download and install <a href="https://nodejs.org/en/download/" target="_blank">Node.js</a>
- [ ] Download and install a text editor (we recommend <a href="https://code.visualstudio.com/" target="_blank">Visual Studio Code</a>)
Use Google to search for any error messages you receive when installing the tools. Google is a great resource to get through roadblocks like these.

#### 2. Make a copy of the existing project on GitHub by forking it at https://github.com/HubSpot/BaseWebApp.git
Since we believe that building a project that's all your own is more important than understanding how to set up a Node and Express app from scratch, you'll be copying a basic existing project today as a starting point. You do this by "forking" the repo, which creates a copy on your GitHub account. 

<img width="600" src="https://cdn2.hubspot.net/hubfs/51294/HubSpot_BaseWebApp.png">

#### 3. Find and open your terminal 
The terminal is a basic way of interacting with your computer through text commands. It'll be very useful in setting your application up. On Windows, it might be called Command Prompt, Git Shell, or Git BASH.

<img width="115" alt="screen shot 2017-04-21 at 11 43 48 am" src="https://cloud.githubusercontent.com/assets/17851174/25285319/ce48dafe-2687-11e7-9fba-3262f406235f.png">

#### 4. Use the command line to navigate to your desktop:
```
	cd ~/Desktop  
```
Then, use the `ls` (on Mac) or `dir` (on PC) command to list all files in a directory. It will show you all the items on your desktop, like so:

![oct-12-2016 21-51-18](https://cloud.githubusercontent.com/assets/17851174/25285297/b97b3586-2687-11e7-8d0a-075baed899c4.gif)


#### 5. Clone the Repository 
When you create (or in this case, fork) a repository on GitHub, it exists as a remote repository — that means it exists on a server somewhere, but not on your machine. In order to edit the code, you can clone your repository to create a local copy on your computer and sync between the two locations. Use the command line to 
 - (1) clone your project from Github onto your own computer, making sure to replace YourUserName with, well, your username:
```
 	git clone https://github.com/YourUserName/BaseWebApp.git 
```
_Tip: Press enter after each line._
 - (2) navigate into the project:
```
	cd BaseWebApp
```
 - (3) list all the files in the project:
```
	ls
```

#### 6. Initialize the app for Heroku
Use the command line to create an app on Heroku. Heroku is the server you'll be pushing your code to. This prepares Heroku to receive your source code (and creates a url for you):
_Once again, be sure to run these lines one at a time, pressing enter after each command_
```
	heroku login
	heroku create
```

*Note: On Windows, the first command might 'hang' for quite some time (even up to 10-15 minutes) - do not cancel and restart it, usually after this first 'long' run, it works without issues later on.*

If you experience any issues with using Heroku on the command line, please refer to [this documentation] (https://devcenter.heroku.com/articles/heroku-cli#troubleshooting) and your error log file.

#### 7. Install the dependencies
Dependencies are all the outside pieces of code your app needs to run. Install the project’s dependencies using npm, a tool used to install any other packages your project needs. View the dependencies your app needs [here](https://github.com/HubSpot/BaseWebApp/blob/master/package.json). 
```
	npm install 
```

#### 8. Run the project on your machine (your local server)
```
	heroku local web	
```

#### 9. View the project running locally
Open a browser and navigate to `localhost:5000`


#### 10. Make a change in the code and refresh the page running at `localhost:5000`
Open the project with Visual Studio Code, or whichever text editor you have installed. Make a change to your code. For example, in `index.ejs`, you could change the header text. Then, refresh your web browser, and you should see the change.

EJS is a templating language that stands for embedded JavaScript. It's like HTML but with some useful tools added. It lets you add JavaScript that gets compiled to HTML before it's sent to the browser. 

#### 11. Link your GitHub repo to Heroku
Next, you're going to connect GitHub to Heroku in order to save you steps when deploying your code. Heroku will monitor your repository, and whenever it sees you push a change, it will automatically re-deploy your application so that your changes are incorporated in your live site. 

 - Go to https://dashboard.heroku.com/apps
 - Select your app
 - Click the tab ‘Deploy’ 
 - In ‘Deployment Method’, select ‘Connect to Github’
 - Search for your Repo — remember, it's "BaseWebApp"
 - Click 'connect' and then 'Enable Automatic Deploys'
 
_*We use automatic deploys at HubSpot - but ours go to a 'QA' or 'staging' site. Can you think of why we might do that?_

#### 12. Push that change to GitHub, which will automatically deploy to Heroku
*If your server is still running from before (it probably is), you can press control + c to halt it. Note that on a Mac, it's still 'control' not 'command'

```
	git add .
	git commit -m “made my first change” 
	git push origin master
```
*Git is very powerful, and has lots of features. In order to learn more about git, we recommend [this resource](https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners).*

#### 13. View your app live! (it might take a few seconds to finish deploying)
```
	heroku open 
```	

## Part 2 - Continue to build on your app 

A few tips before you begin:
 - **Test often**- when you make a change, make sure it works. You don't want to add a bunch of stuff and spend tons of time tracking a small bug down.
 - **Google everything!** - Google is a developer's best friend. No one actually just _knows_ this stuff... you just get really good at knowing what to Google, then reading/incorporating the answers you find. 
 - **Ask for help** - People are dying to help you out! Don't be afraid to ask, no matter how silly you think your question is (because trust me, it's not). Ask a friend, or post on [StackOverflow](https://stackoverflow.com/).

[Option 1 - Personal website](https://github.com/HubSpot/StyledWebApp): Add additional pages, navigation, and styling to your app.

[Option 2 - Incorporate an API](https://github.com/HubSpot/APIWebApp): Learn about how APIs make dynamic web apps possible, and practice integrating one into your app.

[Option 3 - Set up a database](https://github.com/HubSpot/DatabaseWebApp): Learn how to set up a database, do user authentication, and submit and display user-generated data.
	

Step-by-step instructions for these can be found in the repo READMEs. 


----------------------------------------------------------------------------------------------


### Other resources

Here are some external resources we've gathered to help you with further development.

**Git and GitHub tutorials**
Version control is an important tool for every developer, and git is the most popular one. Learn more [useful git commands](https://try.github.io/levels/1/challenges/1), discover [the branching]( https://learngitbranching.js.org/) and then check [how to use GitHub](https://guides.github.com/activities/hello-world/) for your own project.

**Web App tutorials (HTML, CSS, JavaScript)**
There are plenty of different and more comprehensive tutorials and online resources to learn HTML, CSS and JavaScript. 


- FreeCode Camp interactive web development tutorial: https://www.freecodecamp.org/ 
- Khan Academy free html and css tutorial: https://khanacademy.org/computing/computer-programming/html-css 
- Comprehensive web development tutorial/documentation by Mozilla: https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web

- CSS visual guide: https://cssreference.io/ 
- Flexbox tutorial: http://flexboxfroggy.com/ 

- HTML cheatsheet: http://www.hostingreviewbox.com/html5-cheat-sheet/

**More Web App tutorials (FE frameworks)**
Once you have comfortability with JS, CSS and HTML, try out a frontend framework to take your skills to the next level.

- Learning React with create-react-app: https://medium.com/in-the-weeds/learning-react-with-create-react-app-part-1-a12e1833fdc

**Inspiration and problem solving**
To practice your problem solving skills and find some inspiration, please check the following pages: 
- [StackOverflow](https://stackoverflow.com/) is a great place to ask any question (or search for it first, because it’s very likely that someone has already asked the same question and got an answer :))
- [Code Pen](https://codepen.io/) is a great source of inspiration with a lot of projects based on HTML, CSS and JavaScript
- [Dev.to](https://dev.to/) is a blog platform where you can find plenty of useful posts from other developers.
