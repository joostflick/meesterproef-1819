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
    - [Debriefing meeting 1](#Debriefing-meeting-1)
    - [Debriefing meeting 2](#Debriefing-meeting-2)
    - [Debriefing meeting 3](#Debriefing-meeting-3)
    - [Debriefing meeting 4](#Debriefing-meeting-4)
  - [Coaching Sessions](#Coaching-Sessions)
    - [Coaching session 1](#Coaching-session-1)
    - [Coaching session 2](#Coaching-session-2)
  - [Code reviews](#Code-reviews)
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

### Debriefing meeting 1

<details>
<summary>
Debriefing Wikiminds Sustainability meeting 1, click to expand
</summary>
Innovative free minds -> ideas <- issues
When issues and innovative free minds get together ideas are born.

Multi sided platform, you need users to contribute to your ‘empty’ website.

Innovation warehouse, an example of how it shouldn’t be done. Looks like a product that was made just because they needed something to show for G20.

Grand debat, let users (citizens) freely contribute ideas on a large scale; how do you process these ideas.

As many people as possible should be able to contribute to the platform.

Person can submit an idea for a certain problem.

Person can submit a problem which needs ideas.

What are we creating?
Concepts for an application that supports and provides a platform for Wikiminds.

First physical/clickable prototype to give everyone who’s interested an impression of how the platform would work/behave.

Intuitive, user wants to use Wikiminds, and wants to be a part of the brand.

This will also give them initiative to post about it/ be proud of their Wikiminds work.

_Core functionality:_

- See issues
- Submit issues
- Submit possible solutions to issues
- Vote on solutions
- Contact people proposing solutions
- Ability to post results on wiki minds when something takes off
- Ability for people to contribute their practical skills / knowledge to ideas
- Possible functionality:
- Share your issues/problems somewhere to make people contribute
- News source with relevant news
- Show your experience / contributions

_Questions to think about in relation to the concept phase:_

- Why would people contribute? How to make it attractive to use this website?
- What works about youtube/facebook in terms to attracting and keeping a large user base?
- What doesn’t?
- Account system, show people what you’ve done? How would this work?
- Verified education / linked verification for skills etc. Show your experience.
- Which ways of voting are there? (useful for voting on ideas/solutions)
- What happens when an idea is in progress (do people see the progress?)
- What happens when an idea is done
- What to deliver:
- A web application showcasing a possible approach to such a platform
- Multiple concepts of which one is more developed
  </details>

### Debriefing meeting 2

<details>
<summary>
Debriefing Wikiminds Sustainability meeting 2, click to expand
</summary>
Inspiratie UX’ers:
Journey met updates
Filter/sorteer soorten
Set up, eerste keer bezoeken van de website
Horizontaal swipen met kaarten (tinderlike?)
Profiel opbouwen, achievements
Top answer, meest ge upvote antwoord
Levels om steeds ingewikkeldere problemen op te gaan lossen
Kleine persoonlijke problemen, how can I persuade the neighbour to use the car less
Vragen Roland:
Volgende core functionaliteit? minimal viable product
Bezig met een ux app, webapplicatie?
multi sided platform, dus ja
Meteen ingelogd of kun je alles bekijken zonder ingelogd te zijn?
niet meteen
Welke informatie geef je op een kaartje
-
Upvote/downvote, manier van voten
-
Punten systeem per profiel
Kan helpen, niet alles bepalend
Rollen?
Gebruikers, zelfde profiel 
 v
 v
 v
Vraagsteller
  Oplosser
  Bekijker
    Voter
Genres?
Maatschappij
Milieu
Problemen op nati
Beste testpersonen, persona
Trending/recommended
Update platform
Hoelang is data beschikbaar?
Wat voor formulier om in te vullen
Foto’s uploaden, mensen uitleg geven over wat voor foto en waarom een foto relevant zou kunnen zijn
Suggesties om op verder te werken
Ideeën:
aangeraden voor jou (youtube achtig systeem)
guide om een aantrekkelijk probleem te maken
Google analytics over je post, heel veel mensen lezen maar weinig reactie?
Kleine ideeën met snelle oplossingen
Niet meteen hoeven inloggen zodat je ideeën aan iedereen kan laten zien
Categorieën kleine / grote problemen, alles oplossen
Problemen op nationaal niveau voor mensen van die nationaliteit
Bij het aanmaken van een issue krijg je bestaande issues te zien
</details>

### Debriefing meeting 3

<details>
<summary>
Debriefing Wikiminds Sustainability meeting 3, click to expand
</summary>
Roland Ritmeester & UX’ers 3

Software used by grand debat useful for wikiminds?

Provide solutions without issues

Ideaboard, show others your ideas

Completing a profile
^ expertise
^ education
^ full name
^ biography

Raise the participation level

Progress bar of an issue

chat groups

recognition for helping/asking questions -> stack overflow

subscribing to a certain category

challenge instead of issue/problem

being able to invite others

when someone asks to join, there needs to be a place to accept joiners

use the search function on choosing a new title so you can see if similar problems already exist

How do you give users the feeling of community when there’s a lot of users

The bigger the issue the bigger the reward

people who make issues can use their points to award people contributing and providing solutions

see solved issues, ways to solve an issue

Earning badges for different accomplishments

How to determine whether an issue is small or big

quick brainstorm session

Questions:

What added functionality are you guys most enthusiastic about and want us to implement the most?

Functionalities:

- Notifications
- Complete profile
- Combination of twitter popularity and news sites
  </details>

### Debriefing meeting 4

<details>
<summary>
Debriefing Wikiminds Sustainability meeting 4, click to expand
</summary>
Notes on the user test:

Don’t have an account yet too small

password hidden

Adding skills; checkboxes + own skill

Show uploaded picture

In menu -> go to favorites

no redirects

Double Posting

Contributing

Show live tweets

Reageren op reacties

Roland seemed pretty excited about the prototype when using it on his phone

Recommended for you

Meeting 2 koop

Comments weergeven op pagina

Issue op detail page -> description

Belangrijkste flow 100% duidelijk voor een leek

Wat moet er donderdag staan

</details>

## Coaching Sessions

The following text will describe the meetings with our assignment coach (Janno Kapritsias) and how we implemented the results of those meetings into our final product.

### Coaching session 1

<details>
<summary>
Coaching session 1, click to expand
</summary>
1 gezamenlijke repo

individuele repo met leerdoelen, link met de rubrics

Github tickets scrum, linken aan leerdoelen in persoonlijke repo
project repo is voor de klant met engelse documentatie
beide repo’s met readme, die voor de klant is voor professionele presentaties
laat leerdoelen zien
Hoeveel leerdoelen? css/ wafs/ browser tech/ real time. 5/6/7 uitlichten
Prototype, laat de belangrijke dingen zien
Janno vrijdag afspraak 13u bph.

1. repos opzetten (branches, pullen, mergen), goede backups maken
2. overview van tickets op GitHub van wat we moeten doen
3. welke leerdoelen wil ik koppelen, 3/4 vakken per criterium van de rubric, laten zien waar je beter in bent geworden
4. context van het project, wat gaan we daar in koppelen. Scope.
5. Tech stack bepalen en toelichten

Vragen Janno:

1. Kaarten zo goed? Hoe zie je wie wat doet?
2. Core functionaliteiten?
   </details>

### Coaching session 2

<details>
<summary>
Coaching session 2, click to expand
</summary>
Vragen Janno:

Design rationale / Product biography:

Persoonlijke repo:

Wie ben ik
Meesterproef beginkennis
Leerdoelen + rubric
Case Korte beschrijving project
Wie zijn de stakeholders/gebruikers
user requirements -> features bv login
^^ linken aan de leerdoelen
Waar liep ik tegen aan, wat heb ik gedaan per week
Logboek meetings met Roland
Observeren, reflecteren, leren van fouten

Product / biografie:

concept
tech stack en waarom
functionaliteiten
wishlist

Donderdag beoordeling 1330 media lounge

Visuele casus, (poster?), korte pitch daarna interactie
proberen te breken

welke read me is wat? content van die read me?

logboeken meetings, leerdoelen

Polijsten rest

</details>

## Code reviews

I also had two code reviews with Koop, where we reflected on my learning goals and how to achieve them.

<details>
<summary>
Code review, click to expand
</summary>
Gesprek Koop

reflecteren op mijn rol als frontender

basis en tech stack neergezet, daardoor code hergebruiken en opnieuw proberen

snel itereren op onze stack, testen kan daardoor snel

mooi product neerzetten

testen

productbiografie - procesboek, individueel readme, leerdoelen, dit gesprek, proces

design rationale - bij het product, wij vorm, readme over installeren ed.

_ga iets cools maken_

</details>

## Conclusion

My final conclusion on this project
