---
title: 'How to learn React ⚛️'
date: 2021-04-25 20:02:13
category: 'React⚛️'
draft: false
---

# How to learn <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" style="vertical-align:middle" alt="react-background"> : The 7 skills you need to know

You want to learn react - The most in demand javascript library in the world. But what steps do you need to take to get there? Let's walk through the seven skills you should learn to become a <Strong>professional React developer.</Strong>
<br><br>
![https://miro.medium.com/max/2048/1*h5UGPzaL1E4dIy_JWDrsAw.png](https://miro.medium.com/max/2048/1*h5UGPzaL1E4dIy_JWDrsAw.png)
<br><br>
As you're piecing together your React learning path, it's easy to feel overwhelmed and say, _"It's impossible to learn it all. There are too many I need to learn!"_
<br><br>
<Strong>To be successful with React, don't attempt to learn everything. Focus on learning the right things.</Strong>
<br><br>
Let's break down the seven key skills that you need to focus on to build impressive applications and become an in-demand React developer:
<br><br>

# Step 1: Become confident with the core fundamentals of <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" style="vertical-align:middle" alt="react-background">, <img src="https://img.shields.io/badge/CSS-239120?&style=for-the-badge&logo=css3&logoColor=white" style="vertical-align:middle" alt="react-background"> and <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" style="vertical-align:middle" alt="react-background">.

The first step in learning React is actually somewhat of a step a backwards.

The building blocks of the web and every single webpage are HTML, CSS and JavaScript. Any good react developer should know how to use them. React builds upon them to help you to create apps that run on web.
<br><br>
If you've build something with HTML, CSS and JavaScript already, you're in good place to start. For example you built a complete landing page or a small website.
<br><br>
Out of the three technologies, <Strong>React is most concerned with JavaScript</Strong>. React is JavaScript with some added features. For that reason, you'll need to have solid JavaScript skills.
<br><br>
<Strong>What JavaScripts concepts should you know for <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" style="vertical-align:middle" alt="react-background"> ?</Strong>

- Basic data structures: variables, objects, and arrays
- Array methods and working with array data: .map(), .filter(), .reduce()
- Be very familiar with functions and little bit with classes
- Asynchronus JavaScript; promises, making HTTP requests with fetch API, async/await syntax can help
- The DOM: learn to create, select and modify HTML elements as well as their attributes
- Object and array destructuring are helpful for working with data
  <br><br>
  Many developers claim that you should know _"ES6/ES7/ES8/ESNext JavaScript" (In other words the latest JavaScript features)_ to better learn React. Knowing more JavaScript can help, but new features can also serve as a distraction for new learners.

  First become confident with the JavaScript concepts I've listed above by building some small projects that require JavaScript. After that, you can take a look at some newer features of the language.
  <br><br>

# Step 2: Learn React fundamentals and React hooks

Once you're confident with JavaScript, you're now ready to learn React and its core concepts.
<br><br>
These fundamentals are all React-specific and they exist to help us build application with React, using patterns that JavaScript it self does not have.

**What React fundamentals you need to know?**

- How to structure JSX elements (and how it differs from plain HTML)
- How to render (show) JSX elements and how to show or hide elements based on certain conditions
- How to split JSX into components and how to reuse and organize those components to make our app interface.
- How to pass data (+ JSX elements and components) to components using props and when to do so
- How to store and update data within components using state and how to **_"lift state up"_** to other components
- How to use event data in React and handle events from onClick, onChange, and onSubmit events (i.e events from buttons, inputs, and forms)

As a 7-year old library, React's features have changed overtime. A question I'm often asked is **what should you learn first: the old or new syntax?** At the end of 2018, React received a large update that included features called React Hooks.
<br><br>
Hooks were great improvement. They made React apps simpler, more powerful, and allow us to write less code. What's important for you to know is the five core React hooks.
<br><br>
**What are 5 React Hooks you need to know most of all?**
<br><br>

- **useState:** to store and manage data within individual components
- **useEffect:** to perform actions like HTTP requests or worrking with browser API
- **useRef:** to access data from React
- **useContext:** to access data from React Context to share data among components more easily [than passing props]
- **useReducer:** to store and manage data across multiple components

<br><br>
There are more hooks than these five, but the other are not needed as often. So yes, you should learn the latest React features. Jump into using hooks right away. They will be the basis of every React app you make.

# Step 3: Learn to fetch data from both REST and GraphQL API's

A React app is the frontend of a complete application. in every application, you will likely have both a React frontend, which the user interacts with as well as a backend that our React code interacts with. The backend is where we get our data from and do other things like authenticate oyur users.
<br><br>
There are two ways of working with data from the backend. The standard way of getting data is from what's called a REST API. **REST APIs** are the most common form of API. And the newer way is what's called a GraphQL API.
<br><br>
You'll encounter both types of API in your work,
so become familiar with using React to interact with both.
<br><br>

# Step 4: Learn to style your React apps with a component library or utility class library

Every React app needs styling for its appearance. One choice is to use plain CSS. You can write your own styles and put them in a separate style sheet.
<br><br>
But besides CSS, many React developers use what’s known as a component library for easier styling. A component library gives us reusable components that have their own pre-made styles. The most popular component library for React is Material UI. There are many others you can choose from.
<br><br>
Developers also use tools that provide pre-made class names, called utility class libraries. Unlike a component library, a utility class library comes with pre-made classes to style your elements. You can style your app by applying classnames to each element. This removes the need to write any styles yourself. The most popular utility class library is Tailwind CSS.
<br><br>
You’ll encounter both of these as a developer, so become familiar with both a component library and a utility class library.

# Step 5: Manage state in React with React context

**What is state management?** It’s the process of deciding where to locate data and how to work with it across our app. To manage state across your app’s components, use React Context.
<br><br>
**React Context** is a tool that’s built into the core React library and allows us to pass data across our app’s components without using props. It helps us solve the problem of prop-drilling which involves passing props (data) down to components that are deeply nested into one another. With React Context, we place a value on the context we create and then access it using the useContext() React hook.
<br><br>
**What about Redux?** Redux is a popular library for managing state in React apps. It is a far more complex tool than you need for most apps you’ll build. While Redux is still relied upon for very large applications, React Context will be enough for any app you make.
<br><br>
Plus you can get many benefits of Redux, by combining React Hooks and React Context. This is a great advantage as compared to learning an extra library.

# Step 6: Learn a React router. In particular, react-router-dom

**What is a router?** Any website we visit has many pages we can browse by going forward or backward in our browser’s history. To create these different pages or routes in React, we need need to use what’s called a router. React itself does not come with its own router, so we’re going to need to use a third party library, one called react-router-dom.
<br><br>
**react-router-dom** is necessary for creating pages in our app, as well as navigating the user around each page. It lets us create links to different pages of our app and navigate them or redirect them to other pages if we need.
<br><br>
**What features of react-router-dom do you need to know?**
<br><br>

- How to create app routes using the <Route />, <Switch />, and <BrowserRouter /> components
- How to navigate users to different pages using the <Link /> component and programmatically using the useHistory() hook
- How to create dynamic routes using the path prop (i.e. <Route path=”/posts/:post-slug” component={Post} />) and get the path’s value using the useParams() hook
- How to redirect users from protected content using the <Redirect /> component (see number 7)
  <br><br>

# Step 7: Learn patterns for authentication in React

Authenticated users are people who have signed in to use our app. And we want to give those users access to different things. For that reason, authentication goes hand in hand with routing. This is because authenticated users should be able to see certain pages that unauthenticated users cannot.
<br><br>
**What do you need to know about authentication as a React developer?** There is one main thing. You should learn how to show certain content to authenticated users and hide that content from unauthenticated ones.
<br><br>
In review, these are all the core skills you need to have as a React developer, capable of building complete applications and working as a hired frontend developer.
<br><br>
Beyond these 7 skills, note that there are many that can deepen your understanding as a developer. For example, learning more about browsers, HTTP, and APIs, to name a few. But if you follow all these steps, you’ll have a solid understanding of React and be able to build applications of any scale.
