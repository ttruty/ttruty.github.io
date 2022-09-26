---
layout: post
author: Tim Truty
title: A full stack web app to settle disputes
date: 2022-09-26
thumbnail: /assets/img/settld-it-app-post/title.jpg
category: Tech
summary: A full stack web application to settle disputes in a set time
---

#  Settld-It App
## A full stack web application for settling disputes
> It was late one night, I was laying down in my bed with my partner and we had a disagreement. Which was the preferred whipped topping of our family? I fervently argued that Cool Whip was better, while my partner maintained whipped cream is the ultimate dessert topping. We wanted to ask our friends what their preferences were, we could text them all but decided to try to make a web app to settle this dispute. We made a web app that would allow us to create and share simple questions. We would then tally the results and see who was right. We called it Settld-It.

Check out the web app here [Settld-it](https://settldit-app.web.app/).

##  The Key Features
 - User generated questions
 - Time limits for questions
 - Shareable button to send link to friends on different platforms
 - Answer questions and count
 - (in beta) - Text me when question closed
 - view all active questions
 - view all closed questions

##  The Tech Stack
  - Angular
  - Firebase Reatime Database
  - Firebase Hosting
  - Firebase Cloud Functions
  - Firebase Cloud Tasks
  - Twilio API for Text messages


##  The Process
###  The Idea
I was laying in bed with my partner and we were discussing the merits of Cool Whip vs Whipped Cream. We wanted to ask our friends what their preferences were, we could text them all but decided to try to make a web app to settle this dispute. We made a web app that would allow us to create and share simple questions. We would then tally the results and see who was right. We called it Settld-It.

###  The Design
I started rigging up the ui and other things with a cool white board web app I found [Excalidraw](https://excalidraw.com/).

![white board drawing]({{ "/assets/img/settld-it-app-post/white-board-1.png" | absolute_url }})
![white board drawing]({{ "/assets/img/settld-it-app-post/white-board-2.png" | absolute_url }})
![white board drawing]({{ "/assets/img/settld-it-app-post/white-board-3.png" | absolute_url }})
![white board drawing]({{ "/assets/img/settld-it-app-post/white-board-4.png" | absolute_url }})

The began the process of actual coding. The front end is developed with [Angular and Material Design](https://material.angular.io/)
For the back end I wanted to get more familiar with [Firebase](https://firebase.google.com/). I have used it in the past, but not for a full stack application. I used the realtime database to store the questions and answers. I used the cloud functions to create a task to send a text message to the user when the question is closed. I used the cloud tasks to schedule the task to run at the end of the question. I used the cloud hosting to host the web app.
The text messaging aspect is still in beta, as I am working through learning to process of learning and connect Twilio to Firebase. I am using the [Twilio API](https://www.twilio.com/docs/sms/api/message-resource) to send the text messages.

Some useful links for the tech.
[Connect Firebase Realtime NoSQL Cloud Database with Angular Project](https://medium.com/@digambersingh/connect-firebase-realtime-nosql-cloud-database-with-angular-project-d4cc693ac757)
[Angular Firebase Functions](https://firebase.google.com/docs/functions/schedule-functions)
[Building a web application with Angular and Firebase](https://developers.google.com/codelabs/building-a-web-app-with-angular-and-firebase#0)
[Angular Udemy Course](https://www.udemy.com/course/the-complete-guide-to-angular-2/)

![page]({{ "/assets/img/settld-it-app-post/page.png" | absolute_url }})

###  Conclusion
Through this project I brushed up on some concepts and became much more familar with the Firebase platform. I also learned a lot about Angular and Material Design. I am excited to continue to work on this project and add more features.


