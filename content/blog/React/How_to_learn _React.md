---
title: 'How to learn React ⚛️'
date: 2021-04-25 20:02:13
category: 'React⚛️'
draft: false
---

# How to learn <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" style="vertical-align:middle" alt="react-background"> : The 7 skills you need to know

You want to study react, the world's most popular javascript library. But, in order to get there, what measures do you need to take? Let's go over the seven abilities you should learn in order to become a <strong>skilled React developer.</strong>
<br><br>
![https://miro.medium.com/max/2048/1*h5UGPzaL1E4dIy_JWDrsAw.png](https://miro.medium.com/max/2048/1*h5UGPzaL1E4dIy_JWDrsAw.png)
<br><br>
It's easy to become overwhelmed while piecing together your React learning path and declare,_"It's impossible to learn it all." I have far too many to learn!”_
<br><br>
<Strong>Don't try to learn everything to be successful with React. Concentrate on acquiring the necessary knowledge.</Strong>
<br><br>
Let's go over the seven key skills you'll need to master if you want to build impressive apps and become a sought-after React developer.
<br><br>

# Step 1: Become confident with the core fundamentals of <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" style="vertical-align:middle" alt="react-background">, <img src="https://img.shields.io/badge/CSS-239120?&style=for-the-badge&logo=css3&logoColor=white" style="vertical-align:middle" alt="react-background"> and <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" style="vertical-align:middle" alt="react-background">.

The first step in learning React is a bit of a backwards step.

HTML, CSS, and JavaScript are the foundations of the web and each individual webpage. Any competent react developer should be able to make use of them. React extends them to assist you in developing web-based applications.

You're in a good place to start if you've already created something with HTML, CSS, and JavaScript. As an example, suppose you purchased
<br><br>
If you've build something with HTML, CSS and JavaScript already, you're in good place to start. For example you built a complete landing page or a small website.
<br><br>

**React is most concerned with JavaScript** out of the three technologies. React is JavaScript with some extra features. As a result, you'll need to be fluent in JavaScript.

<br><br>
<Strong>What JavaScripts concepts should you know for <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" style="vertical-align:middle" alt="react-background"> ?</Strong>

- Basic data structures: variables, objects, and arrays
- Array methods and working with array data: .map(), .filter(), .reduce()
- Be very familiar with functions and little bit with classes
- Asynchronus JavaScript; promises, making HTTP requests with fetch API, async/await syntax can help
- The DOM: learn to create, select and modify HTML elements as well as their attributes
- Object and array destructuring are helpful for working with data
  <br><br>
  Many developers claim that in order to learn React, you should be familiar with _“ES6/ES7/ES8/ESNext JavaScript”_ (the most recent JavaScript features). Knowing more JavaScript can be beneficial, but new features can also be distracting for new learners.

  First, practise the JavaScript concepts I've listed above by creating some small projects that require JavaScript. Following that, you can look at some of the language's newer features.

<br><br>

# Step 2: Learn React fundamentals and React hooks

Once you've mastered JavaScript, you're ready to dive into React and its key concepts.
<br><br>
These basics are all React-specific, and they exist to assist us in building applications using React that use patterns that JavaScript lacks.

**What React fundamentals you need to know?**

- How to structure JSX elements (and how it differs from plain HTML)
- How to render (show) JSX elements and how to show or hide elements based on certain conditions
- How to split JSX into components and how to reuse and organize those components to make our app interface.
- How to pass data (+ JSX elements and components) to components using props and when to do so
- How to store and update data within components using state and how to **_"lift state up"_** to other components
- How to use event data in React and handle events from onClick, onChange, and onSubmit events (i.e events from buttons, inputs, and forms)

React's features have evolved over the course of its seven-year existence. One of the most common questions I get is _**whether you should master the old or new syntax first.**_ React had a major update towards the end of 2018 that introduced capabilities known as React Hooks.
<br><br>
Hooks were a significant improvement. They simplified and enhanced React apps, allowing us to write less code. What you should be aware of are the five fundamental React hooks.
<br><br>
**What are 5 React Hooks you need to know most of all?**
<br><br>

- **useState:** to store and manage data within individual components
- **useEffect:** to perform actions like HTTP requests or worrking with browser API
- **useRef:** to access data from React
- **useContext:** to access data from React Context to share data among components more easily [than passing props]
- **useReducer:** to store and manage data across multiple components

<br><br>
There are more hooks than these five, although they aren't used as frequently. So, absolutely, you should learn the most recent React functionalities. Begin utilising hooks straight away. They will serve as the foundation for every React app you create.

# Step 3: Learn to fetch data from both REST and GraphQL API's

A React app is the user interface of a larger application. Every application will most likely have both a React frontend with which the user interacts and a backend with which our React code communicates. The backend is where we acquire our data and do other functions such as user authentication.
<br><br>
There are two approaches to working with data from the backend. A REST API is the most common technique to obtain data. **REST APIs** are the most frequent type of API. A GraphQL API is a modern method.
<br><br>
You'll meet both forms of API in your work,
so practice interacting with both using React.
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
