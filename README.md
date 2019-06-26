# Meesterproef Joost Flick

## Table of contents

- [Meesterproef Joost Flick](#Meesterproef-Joost-Flick)
  - [Table of contents](#Table-of-contents)
  - [Description](#Description)
  - [Wikiminds](#Wikiminds)
    - [What is Wikiminds](#What-is-Wikiminds)
    - [Core functionalities](#Core-functionalities)
  - [Learning Goals](#Learning-Goals)
    - [Browser tech](#Browser-tech)
    - [Web design](#Web-design)
    - [Web app from scratch](#Web-app-from-scratch)
    - [Performance matters](#Performance-matters)
    - [Real Time Web](#Real-Time-Web)
  - [Progress meetings with the UX students and the Wikiminds founders](#Progress-meetings-with-the-UX-students-and-the-Wikiminds-founders)
  - [Coaching Sessions](#Coaching-Sessions)
  - [Code Reviews](#Code-Reviews)
  - [Conclusion](#Conclusion)

## Description

This Read me contains my personal documentation for the end assignment of the Web Design minor. In this document I will describe the assignment, my learning goals during this project and what I did to reach those goals.

## Wikiminds

### What is Wikiminds

There's a lot of concepting being done all over the world, but the majority of those concepts are willingly or unwillingly being kept behind closed doors. It can be hard for people to share their ideas and/or issues and brainstorm about them with people from all over the world. We are hoping to tackle this issue by creating Wikiminds.

Wikiminds is a platform where issues and innovative minds meet. This leads to the creation of new and out of the box ideas to better the world.

When completed, Wikiminds should be a multisided platform free for anyone to use. The goal is to create an application in which users think about issues (e.g. environmental issues) together and come up with creative solutions.

Without users actively contributing there wouldn't be any content on Wikiminds, which is why it is extremely important for users to want to use this platform.

People partaking in Wikiminds projects should be proud of their achievements on the platform and be able to show those achievements on their profile page.

### Core functionalities

- View issues posted by others
- Submit issues
- Submit possible solutions to issues
- Vote on issues
- Vote on solutions
- Bring solutions and issues together
- View the progress of Wikiminds projects
- Ability for people to contribute their practical skills / knowledge

## Learning Goals

### Browser tech

- Student kan de core functionaliteit van een use case doorgronden (translation: Student has the ability to determine the core functionality of a use case)

I have capitalized on this use case by having multiple meetings with our client. I tried to ask more than just the basic questions to really determine the core functionalities of the application. The idea was kind of vague at first (there were no designs or prototypes, just a concept that was presented to us verbally) but because of our questioning we we're able to formulate a good use case to solve.

- Student laat zien hoe Progessive Enhancement toe te passen in Web Development (translation: Student demonstrates how to apply Progressive Enhancement in Web Development)

I demonstrated my understanding of progressive enhancement in the comment section of our application. Here the user can voice their opinion by up or downvoting certain comments. If the user has no Javascript enabled (for example when using an older browser or a device which doesn't allow for Javascript) up or downvoting is done via a regular GET request. However if the user is browsing the site using a Javascript compatible device, the application will make use of socket.io to give the user realtime feedback on their actions. This way the page doesn't have to reload, bettering the user experience.

### Web design

- Er zijn verschillende tests gedaan en verwerkt om het ontwerp te verbeteren

We did multiple user tests by sending our prototype to different users. We tried not giving the users any instructions and just let them use our application, which seemed to work out fine. Meanwhile I also kept notes about the user tests on which we iterated for the next test. This also partially applies to the following learning goal:

- De student kan een MVP(Minimal Viable Prototype) _rapid prototypen_ om hiermee experimenten te doen (translation: The user can rapid prototype a Minimal Viable Prototype to experiment with)

Because of our limited time to work on the application, we were determined to quicly finish a initial prototype to start collecting user feedback. After one week of work we determined the Tech Stack and the next week we finished our first usable prototype, to start testing the basic functionalities. Each feedback session we iterated on the original prototype to improve the quality of our tests. During the last two feedback sessions with the Wikiminds founders and four other students we were able to simultaneously test the application, each on their own device.

### Web app from scratch

- Je kan data ophalen, manipuleren en dynamisch omzetten naar html elementen mbv templating. Je begrijpt hoe je middels asynchrone code met een externe API kan werken (translation: You are able to retrieve, manipulate and dynamically convert data to HTML elements using templating. You understand how you can use asynchronous code to work with an external API)

I used the knowledge learned during the earlier parts of the minor to build a more extensive data manipulation model than I ever have before. Data can be manipulated, stored and displayed using a database and asynchronous code. Socket.io and EJS templates are used to transfer from the front- to the backend. The application makes use of the Twitter API to determine a popularity score for certain subjects.

### Performance matters

- Je weet het verschil tussen client side en server side renderen en kan server side rendering toepassen voor het tonen van data uit een API (translation: You know the difference between client- and serverside rendering and are able to apply server side rendering in order to show data from an API)

The application makes use of both client- and serverside rendering, and we have made a clear distinction between the two in the code base. The client and server correspond via sockets, but most of the data is being passed to the clientside via an EJS rendering. The server communicates with our database and the Twitter API, and sends the retrieved information to the client using Promises (asynchronous code).

### Real Time Web

- De user kan door interactie met de app het datamodel van de server in real time beïnvloeden door direct data aan te passen. (translation: Via interaction with the app the user is able to influence the datamodel of the server in real time by directly manipulating data)

Like described earlier in the Browser Tech learning goals I used sockets to communicate between the client and the server. In our application the user has the ability to up or downvote a comment, which will trigger an event on the serverside to update the database, and on the clientside to update the view. This is done in realtime so without any delays or page reloads. If something goes wrong during voting on a comment the client side will receive the error from the server and display it to the user immediately.

## Progress meetings with the UX students and the Wikiminds founders

We attended multiple meetings with the founders of Wikiminds (consisting partially of Roland Ritmeester, who will also be grading our project).

## Coaching Sessions

The following text will describe the meetings with our assignment coach (Janno Kapritsias) and how we implemented the results of those meetings into our final product.

## Code Reviews

## Conclusion
