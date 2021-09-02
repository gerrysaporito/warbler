# Warbler 

## Introduction 🎩

This web app is a clone of Twitter, a popular social media site. The goal was to create an client & api that allows users to post and see updates of people in their network.

## Description 📝

This repository contains the client and api for the warbler site, built with Typescript & MongoDB, Express, React, and Node (MERN stack).

### INSPIRATION ✨

This app was originally created as a capstone for a [Udemy](https://www.udemy.com/course/the-advanced-web-developer-bootcamp/) course I took. This Udemy course was probably one of the most important ones I've ever taken as it taught me about the interaction between servers and modern technologies (React & Node).

### Learning Experience 📚

When I started this course, I didn't know what I was going to learn. All I knew was it was the next step in a 2 part series of courses for modern day web development. I now realize that what I learned was the theory and implementation of server architecture and design patterns which is the foundation in a lot of web applications today.

This project gave me a chance to work with new technolgies including:

- [Typescript](https://www.typescriptlang.org/)
- [Node](https://nodejs.org/en/)
- [Express](https://expressjs.com/)
- [React](https://reactjs.org/)

This project also taught me more about:

- API architecture
- Client architecture
- Server communication architecture

## Getting Started 🏁

### Requirements ✅

- Node & npm
- MongoDB

### Installation 💾

1. Download this repository
2. Rename `.env.example` -> `.env` and fill out the information
3. Open a command line window, navigate to the `warbler-api` folder & run `npm run start`
4. Open another command line window, navigate to the `warbler-client` folder & run `npm run start`
5. Go to [http://localhost:3000](http://localhost:3000)

### Notes 🖍

- If you try to open the url in chrome and you get a 'this connection is not safe', click anywhere on the page and type the phrase `thisisunsafe` to bypass security

## Features 🧩

This app has the following functionalities:

- Sign in/up
- Follow people
- Create, update, & delete a posts
- Like posts
- Comment on posts

## Roadmap 🗺

Because this app was created during a Udemy course, the current features were all created alongside the course instructors & TAs. That doesn't mean there isn't any room for improvements though!

In the future, I see profile pages for users to further personalize their accounts. Profile pages can contain profile pictures, email validation, likes and dislikes, birthdays, and more.

Also I would start writing integration tests to ensure the platform is working as intended and speed up testing during development.

## Edge Cases ⚠️

Because this app was created by following instructors, most of the kinks are already fleshed out. There aren't too many edge cases but below are a few I was able to identify.

### Load Testing 🚩

Because this app isn't as optimized as it could be, heavy loads could cause slow responses from the API.

To help with this, adding mongoose hooks to schemas can marginally reduce the amount of database requests going through.

### Notes 🖍

This is by no means an exhaustive list but only a few of the more critical points.
