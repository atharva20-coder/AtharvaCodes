---
title: 'How to make a React⚛️ App with Node Backend🍃'
date: 2021-04-30 05:21:13
category: 'Node🍃'
draft: false
---

# How to make <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" style="vertical-align:middle" alt="react-background"> App with <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" style="vertical-align:middle" alt="Node badge"> Backend: The complete guide.

A React frontend connected to a Node backend is a rock-solid combination for any application you want to build.

This guide is designed to help you create full-stack projects with React as easy as possible.

Let’s see how to set up an entire project using React and Node from scratch and deploy it to the web.
<br><br>
![https://miro.medium.com/max/2000/1*XbC2_y9our-PX-wkxIV0fA.png](https://miro.medium.com/max/2000/1*XbC2_y9our-PX-wkxIV0fA.png)
<br><br>

# Tools You Will Need

1.  Make sure Node and NPM installed on your computer. You can download both at nodejs.org (NPM is included in your Node installation)
2.  Use a code editor of your choice. I am using and would personally recommend using VSCode. You can download VSCode at code.visualstudio.com.
3.  Make sure you have Git installed on your computer. This is necessary for deploying our application with Heroku. You can get it at git-scm.com
4.  An account at heroku.com. We will use Heroku to publish our app to the web entirely free.
    <br><br>

# Step 1: Create your Node (Express) backend🍃

First create a folder for your project, called react-node-app (for example).

Then, drag that folder into your code editor.

To create our Node project, run the following command in your terminal:

```
npm init -y

```

<br><br>
This will create a package.json file which will allow us to keep track of all our app scripts and manage any dependencies our Node app needs.
<br><br>
Our server code will live in a folder of the same name: server. Let’s create that folder.
<br><br>
In it, we’ll place a single file, out of which we’ll run our server: index.js
<br><br>
We’ll use Express to create simple web server for us which runs on port 3001 if no port is provided as an environment variable (Heroku will set this value when we deploy our app).
<br><br>

```
// server/index.js

const express = require("express");

const PORT = process.env.PORT || 3001;

const app = express();

app.listen(PORT, () => {
  console.log(`Server listening on ${PORT}`);
});

```

Then in our terminal, we will install Express as a dependency to use it:

```
npm i express

```

And then create a script in package.json that will start our web server when we run it with

`npm start`

```
// server/package.json

...
"scripts": {
  "start": "node server/index.js"
},
...

```

Finally, we can run our app using this script by running npm start in our terminal and we should see that it is running on port 3001:

```
npm start

> node server/index.js

Server listening on 3001

```

<img src="https://reedbarger.com/wp-content/uploads/2021/06/clip-1.gif" alt="clip">

# Step 2: Create an API Endpoint

We want to use our Node and Express server as an API, so that it can give our React app data, change that data or do some other operation only a server can do.

In our case, we will simple send our React app a message that says “Hello from server!” in a JSON object.

The code below creates an endpoint for the route /api.

If our React app makes a GET request to that route, we respond (using res, which stands for response) with our JSON data:

```
// server/index.js
...

app.get("/api", (req, res) => {
  res.json({ message: "Hello from server!" });
});

app.listen(PORT, () => {
  console.log(`Server listening on ${PORT}`);
});

```

_Note:Make sure to place this above the app.listen function._
<br><br>
Since we’ve made changes to our Node code, we need to restart our server.
<br><br>
To do that, end your start script in the terminal by pressing Command/Ctrl + C. Then restart it by running npm start again.
<br><br>
And to test this, we can simply visit http://localhost:3001/api in our browser and see our message:
<br><br>

<img src="https://reedbarger.com/wp-content/uploads/2021/06/clip-2.gif" alt="clip">

<br><br>

# Step 3: Create your React ⚛️ frontend

<br>
After creating our backend, let’s move to the frontend.
<br>
Open another terminal tab and use create-react-app to create a new React project with the name client:
<br><br>

```
// server/index.js
...

app.get("/api", (req, res) => {
  res.json({ message: "Hello from server!" });
});

app.listen(PORT, () => {
  console.log(`Server listening on ${PORT}`);
});

```

_Note:Make sure to place this above the app.listen function._

Since we’ve made changes to our Node code, we need to restart our server.

To do that, end your start script in the terminal by pressing Command/Ctrl + C. Then restart it by running npm start again.

And to test this, we can simply visit http://localhost:3001/api in our browser and see our message:

```
npx create-react-app client
```

After that, we will have a React app with all of its dependencies installed.

The only change we have to make is to add a property called proxy to our package.json file.

This will allow us to make requests to our Node server without having to provide the origin it is running on (http://localhost:3001) every time we make a network request to it:
<br><br>

```
// client/package.json

...
"proxy": "http://localhost:3001",
...
```

Then we can start up our React app by running it’s start script, which is the same as our Node server. First make sure to cd into the newly-created client folder.

After that, will start up on localhost:3000:
<br><br>

```
cd client
npm start

Compiled successfully!

You can now view client in the browser.

Local:            http://localhost:3000
```

<br><br>
<img src="https://reedbarger.com/wp-content/uploads/2021/06/clip-3.gif" alt="clip">

# Step 4: Make HTTP Requests from React to Node

Now that we have a working React app, we want to use it to interact with our API.
<br><br>
Let’s see how to fetch data from the /api endpoint that we created earlier.
<br><br>
To do so, we can head to the App.js component in our src folder and make an HTTP request using useEffect.
<br><br>
We will make a simple GET request using the Fetch API to our and then have our data returned as JSON.
<br><br>
Once we have the data returned to us, we will get the message property (to grab our greeting that we sent from the server) and then put it in a state variable called data.
<br><br>
This will allow us to display that message in our page if we have it. We are using a conditional in our JSX to say that if our data is not there yet, show the text “Loading…”.
<br><br>

```
// client/src/App.js

import React from "react";
import logo from "./logo.svg";
import "./App.css";

function App() {
  const [data, setData] = React.useState(null);

  React.useEffect(() => {
    fetch("/api")
      .then((res) => res.json())
      .then((data) => setData(data.message));
  }, []);

  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>{!data ? "Loading..." : data}</p>
      </header>
    </div>
  );
}


export default App;
```

<br><br>
<img src="https://reedbarger.com/wp-content/uploads/2021/06/clip-4.gif" alt="clip">
<br><br>

# Step 5: Deploy your app to the web with Heroku

Finally, let’s deploy our application to the web.
<br><br>
First, within our client folder, make sure to remove the Git repo that is automatically initialized by create-react-app.
<br><br>
This is essential to deploy our app, because we are going to set up a Git repo in the root folder of our project (react-node-app), not in client:
<br><br>

```
cd client
rm -rf .git
```

<br><br>
When we deploy, both our Node backend and React frontend are going to be served on the same domain (i.e. mycoolapp.herokuapp.com).
<br><br>
We see how our requests are being handled by our Node API, so we need to write some code that will display our React app when it is requested by our user (for example, when we go to the home page of our app).
<br><br>
We can do this back in server/index.js by adding the following code:
<br><br>

```
const path = require('path');
const express = require('express');

...

// Have Node serve the files for our built React app
app.use(express.static(path.resolve(\_\_dirname, '../client/build')));

// Handle GET requests to /api route
app.get("/api", (req, res) => {
res.json({ message: "Hello from server!" });
});

// All other GET requests not handled before will return our React app
app.get('\*', (req, res) => {
res.sendFile(path.resolve(\_\_dirname, '../client/build', 'index.html'));
});
```

<br><br>
This code will first allow Node to access our built React project using the express.static function for static files.
<br><br>
And if a GET request comes in that is not handled by our /api route, our server will send back to our React app.
<br><br>
<Strong>This code allows our React and Node app to be deployed together on the same domain.</Strong>
<br><br>
Then, we can tell our Node App how to do that by adding a build script to our server package.json file that builds our React app for production:
<br><br>

```
// server/package.json

...
"scripts": {
"start": "node server/index.js",
"build": "cd client && npm install && npm run build"
},
...
```

<br><br>
I would also recommend providing a field called “engines”, where you want to specific the Node version you are using to build your project. This will be used for deployment.
<br><br>
You can get your Node version by running node -v and you can put the result in “engines” (i.e. 14.15.4):
<br><br>

```
// server/package.json

"engines": {
"node": "your-node-version"
}
```

<br><br>
After this, we’re ready to deploy using Heroku, so make sure you have an account at <a href="https://www.heroku.com/">Heroku.com</a>.
<br><br>
Once you are signed in and are looking at your dashboard, you’ll select New > Create New App and provide a unique app name.
<br><br>
After that, you’ll want to install the Heroku CLI on your computer so you can deploy your app whenever you make any changes using Git. We can install the CLI by running:
<br><br>

```
sudo npm i -g heroku
```

<br><br>
Once that’s installed, you will log in to Heroku through the CLI using the heroku login command:
<br><br>

```
heroku login
```

<br><br>
Press any key to login to Heroku
<br><br>
Once you have logged in, just need to follow the deployment instructions for our created app in the “Deploy” tab.
<br><br>
The following four commands will initialize a new Git repo for our project, add our files to it, commit them, and add a Git remote for Heroku.
<br><br>

```
git init
heroku git:remote -a insert-your-app-name-here
git add .
git commit -am "Deploy app to Heroku"
```

<br><br>
Then the very last step is to publish our app by pushing the Heroku Git remote we just added using:
<br><br>

```
git push heroku master
```

<br><br>
Congratulations! Our full-stack React and Node app is live! 🎉

<img src="https://reedbarger.com/wp-content/uploads/2021/06/clip-5.gif">

When you want to make changes to your app going forward (and deploy them), you just have to use git to add your files, commit them and then push to our Heroku remote:
<br><br>

```
git add .
git commit -m "my commit message"
git push heroku master
```

<br><br>
