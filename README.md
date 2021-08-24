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

As of right now, the core functionality which qualifies this as an MVP has been implemented and tested in real time.

Moving forward, integration tests will be implemented to ensure that all endpoints are functioning as expected. Also, advanced searches through common characteristics would also be incredibly useful to let users search by tags, key words, image sizes, types, and more to create a more seamless experience.

Another feature that was considered was the possibility of buying and selling images by leveraging Non-Fungible Tokens (NFT) and blockchain technologies. Doing so would require an incredible upfront time and financial investment along with more knowledge and a community to support the development, which was way beyond the scope of the original project.

Lastly although not a feature, legal paperwork (terms of use agreements & privacy policy) would be great to have to cover any liabilities on the individual user and and Fanimage & related entities. This is clearly beyond the scope of the project so it has not been pursued (nor do I think it ever will).

## Edge Cases ⚠️

This app was created without much thought for longetivity and robustness because the goal was to demonstrate raw knowledge on APIs and server architecture. That being said, there are a lot of edge cases to cover (aside from what would be covered by integration tests as mentioned in the roadmap).

### Variable Image Card Sizes 🚩

For one, the UI is still clunky. Image cards contain variable amounts of whitespace and change depending on the largest card in the row. The inconsistency in sizes is really 'hard on the eyes' (ugly) and makes the platform feel buggier than it really is.

To help with this, a masonry layout for the images (similar to [pinterest](https://pinterest.com)) would be a better fit for the nature of these posts.

### Lacking Middleware 🚩

Another shortcoming is the authentication middleware. Authentication is mostly handled in the client with the endpoints mostly being exposed. An example of this flaw can be seen when a user is only able to upload images if they are logged in but can still upload images by hitting the endpoint via [Postman](https://www.postman.com/) or something along those lines. The server will throw an error because the endpoint checks to see if a user exists before uploading but it should not get to this point to begin with.

To fix this, custom middleware should be added to the endpoints to ensure proper authentication. The only real validation right now is ensuring a user is authenticated. Validating a user owns posts before updating or deleting is a big security flaw that was acknowledged but not implemented due to the scope of this project.

### Notes 🖍

This is by no means an exhaustive list but only a few of the more critical points.
