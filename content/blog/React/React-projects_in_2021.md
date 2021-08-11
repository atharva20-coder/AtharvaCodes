---
title: '7 React projects in 2021 ⚛️🍃'
date: 2021-05-05 13:21:13
category: 'Node🍃'
draft: false
---

# 7 Must do <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" style="vertical-align:middle" alt="react-badge"> Projects

React is a JavaScript library that is ideal for creating impressive apps. There are countless projects that you can make with React, but here are seven that are on my list to build in 2021.
<br><br>
<img src="https://www.crio.do/blog/content/images/size/w2000/2021/03/Javascript-projects--React.png" alt="7 react projects in 2021">
<br><br>

Why have I selected these seven projects in particular? I picked them because they build off of one another. They require you to know similar, essential concepts like authentication, working with an API and database, using a React router for adding pages to your app, and playing media like audio or video.
<br><br>
Plus, many applications can be (and often are) integrated into one another. Social media apps can include chat apps, music or video apps can include e-commerce apps, and so on.
<br><br>
In other words, building any of these projects will give you the skills and knowledge required to build the rest of the apps on the list, including your own personal projects.
<br><br>
Along with each project, I have provided several real-world examples which you can use to find inspiration, plus some ideas about what tools I would possibly use to build each app.
<br><br>

# 1. Realtime Chat App 💬

**Real-world examples:** <img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white" style="vertical-align:middle" alt="Slack"> <img src="https://img.shields.io/badge/Messenger-00B2FF?style=for-the-badge&logo=messenger&logoColor=white" style="vertical-align:middle" alt="Messenger"> <img src="https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white" style="vertical-align:middle" alt="Discord">
<br><br>
Virtually all of use some kind of realtime chat app, whether it’s a mobile application like WhatsApp or Viber or a productivity tool like Slack or Discord. It could also be part of a chat widget within a website where customers can directly talk with the site owners.
<br><br>
All chat apps allow users to send messages to others in realtime, to react to messages, and they show when users are online or offline.
<br><br>

## How to build a realtime chat app:

- Build your project with create-react-app or Next.js.
- Use a service like Firebase or GraphQL subscriptions to create and get messages in realtime to users.
- Add reactions to message with emoji using the npm package emoji-mart
- Deploy to the web using Firebase Tools
  <br><br>

# 2. Social Media App

**Real-world examples:** <img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" style="vertical-align:middle" alt="Facebook"> <img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" style="vertical-align:middle" alt="Instagram"> <img src="https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white" style="vertical-align:middle" alt="Twitter">
<br><br>
The app you’re likely most familiar with is a social media application. In many ways it’s similar to a chat app, but expanded to a larger community of users.
<br><br>
These users can interact with each other in different ways: they can follow one another to receive their posts, add media like images and video to share with others, and enable users to interact with posts such as liking or commenting on them.
<br><br>

## How to build a social media app:

- Build your frontend with create-react-app, and backend using a Node API
- Use a database like Postgres or MongoDB, along with an ORM like Prisma (Postgres) or Mongoose (MongoDB)
- Use social authentication with Google, Facebook or Twitter, using Passport or a simpler service like Auth0
- Deploy the backend to Heroku, frontend to Netlify
  <br><br>

# 3. E-Commerce App 🛒

**Real-world examples:** Shopify, Etsy, Dev.to Storefront

Storefronts where we can buy digital or physical products online are everywhere. E-commerce apps add the ability for users to add and remove items from a shopping cart, view their cart, and checkout using a credit card, as well as other payment options like Google Pay and Apple Pay.

If you’re looking for inspiration, checkout out some simpler storefronts like a Shopify storefront, rather than looking at a massive retailer like Amazon or Walmart.
<br><br>

## How to build an e-commerce app:

- Create the app with create-react-app or Next.js
- Add the stripe NPM package, plus use-shopping-cart to easily handle payments directly with Stripe Checkout
- Build a Node API to handle creating sessions with Stripe
- Deploy the backend to Heroku, frontend to Netlify (or deploy both on Heroku)
  <br><br>

# 4. Video Sharing App

**Real-world examples:** <img src="https://img.shields.io/badge/Snapchat-FFFC00?style=for-the-badge&logo=snapchat&logoColor=white" style="vertical-align:middle" alt="Snapchat"> <img src="https://img.shields.io/badge/TikTok-000000?style=for-the-badge&logo=tiktok&logoColor=white" style="vertical-align:middle" alt="TikTok"> <img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" style="vertical-align:middle" alt="YouTube"> <img src="https://img.shields.io/badge/Netflix-E50914?style=for-the-badge&logo=netflix&logoColor=white" style="vertical-align:middle" alt="NetFlix">

A video sharing app is probably the most broad category, as video is used across so many different apps and in many different ways.

You have video sharing apps like YouTube, which allow you to search any browser and look for any video that you could imagine that users have created. Also, tik tok and Snapchat give us the ability to watch videos from other users that are recorded in a much shorter, more accessible format, and are more oriented around interactions like likes and views.

## How to build a video sharing app:

- Create the app with create-react-app, and create the backend with Node/Express
- Use Cloudinary for image and video uploads to the Cloudinary API
- Use a database like Postgres or MongoDB, along with an ORM like Prisma (Postgres) or Mongoose (MongoDB)
- Deploy the backend to Heroku, frontend to Netlify (or deploy both on Heroku)
  <br><br>

# 5. Blogging / Portfolio App

**Real-world examples:** <img src="https://img.shields.io/badge/Medium-12100E?style=for-the-badge&logo=medium&logoColor=white" style="vertical-align:middle" alt="Medium.com"> <img src="https://img.shields.io/badge/Hashnode-2962FF?style=for-the-badge&logo=hashnode&logoColor=white" style="vertical-align:middle" alt="HashCode"> <img src="https://img.shields.io/badge/dev.to-0A0A0A?style=for-the-badge&logo=devdotto&logoColor=white" style="vertical-align:middle" alt="Dev">

This app example is perhaps the most practical. The most immediately practical choice for you to build a blogging or portfolio app is something that showcases your skills. It allows you to show off what you can do as a developer, while also allowing you to include posts and content that reflect what you know.

Making these applications with tools like Gatsby or Nextjs (which are both React frameworks) is now easier than ever.

## How to build a blogging or portfolio app:

- Create the app with Gatsby or Next.js
- Use markdown for blog posts with a special markdown transformer plugin such as remark
- Deploy the site to Netlify or Vercel
  <br><br>

# 6. Forum App

**Real-world examples:** <img src="https://img.shields.io/badge/Reddit-FF4500?style=for-the-badge&logo=reddit&logoColor=white" style="vertical-align:middle" alt="Reddit"> <img src="https://img.shields.io/badge/Stack_Overflow-FE7A16?style=for-the-badge&logo=stack-overflow&logoColor=white" style="vertical-align:middle" alt="StackoverFloow">

A forum application is where we go when we want to get help, and as programmers we visit forums like Reddit and Stack Overflow to get our coding questions answered.

Forums also combine many elements of chat and social media apps through posts, comments, and reactions. A forum is more of a more organized version of a social media app where users can more easily find answers to questions they’re looking for.
##How to build a forum app:

- Build your frontend with create-react-app, and backend using a Node API
- Use a database like Postgres or MongoDB, along with an ORM like Prisma (Postgres) or Mongoose (MongoDB)
- Use social authentication with Google, Facebook or Twitter, using Passport or a simpler service like Auth0
- Deploy the backend to Heroku, frontend to Netlify
  <br><br>

# 7. Music Streaming App

**Real-world examples:** <img src="https://img.shields.io/badge/Spotify-1ED760?&style=for-the-badge&logo=spotify&logoColor=white" style="vertical-align:middle" alt="Spotify"> <img src="https://img.shields.io/badge/SoundCloud-FF3300?style=for-the-badge&logo=soundcloud&logoColor=white" style="vertical-align:middle" alt="SoundCloud">

Just as React applications are perfect for serving video content, they’re also great for streaming media like music.

Music apps have a similar structure to video sharing apps and may or may not allow users to upload their own music. They do allow users to listen to music, like songs, comment on them, and perhaps even purchase music.

In this way, a streaming music app can combine elements of a video sharing app as well as an e-commerce app.

## How to build a music streaming app:

- Create the app with create-react-app, and create the backend with Node/Express
- Use Cloudinary for image and video uploads to the Cloudinary API
- Use a database like Postgres or MongoDB, along with an ORM like Prisma (Postgres) or Mongoose (MongoDB)
- Deploy the backend to Heroku, frontend to Netlify (or deploy both on Heroku)

<br><br><br>
