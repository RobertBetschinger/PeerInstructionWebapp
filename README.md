# Bachelor thesis: Webapplication for Peer Instruction Teaching Method

!!!Important: This repository is still under active development.!!!

Within this bachelor thesis  two web apps were developed to provide teachers/professors/etc. with a simple and modern way to implement Peer Instruction Teachning Method into their class. Peer Instruction is a teaching method originally developed by Eric Mazur in 1990s at the University of Harvard, which shows significant positive impact on students learning succes.

The Peer lecturer app is the part of this project that is intended for professors and teachers. This web service allows to query concept questions to the students and monitor their answers. The Questions are downloaded from a MONGODB Databse. It is possible to create new Questions at this Database whith the so called "Dozentenapp", an other Project at the Chair of Information Systems(University of Regensburg). Further it is possible to communicate with the Students over an chat application.

The Peer student app offers the students the possibility to answer the questions and to see the results, if the Lecteur reveals them. Of Course Students also can use the Chat application, maybe to discuss in an virtual class, because the discussion is one central Point of the Peer Instruction Teaching Method. Students also see in which phase of the Workshop they are currentlly.

The Core of the Project is the Peer Socket Server. It is an Socket Server(Socket.IO) which is responsible for all real time data transfer between the above mentioned webapps. It also keeps track of all Students/Teachers which are currently part of the Workshop.

These WebApplications will be used in a Digital Forensc Workshop.

The Forensic Workshop is hosted by the "TRIO Forschungsprojekt".


## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them

Install Node.js and a Code Editor by your Choise

### Installing

A step by step series of examples that tell you how to get a development env running:

So as you can see this Repository is splitted into 3 Submodules or child-repositorys:
- Socket Server
- Peer Lecteur App
- Peer Student App

# Cloning
1. Possibility:

Now we’ll clone this project with a submodules in it. When you clone such a project, by default you get the directories that contain submodules, but none of the files within them yet.
You must run two commands: git submodule init to initialize your local configuration file, and git submodule update to fetch all the data from that project and check out the appropriate commit listed in your superproject:

2. Possibility:

Use "git clone --recurse-submodules" to direct initialize and update each submodule.


Now when you have successfully cloned these projects:

All of these Projects use Node.js in one way or a other so you will have to install all needed node.js packages. To do so follow these steps:

##Deployment

1: Open up a Terminal and jump into a Project

2: Run "npm init -y"

3: Run "npm install"

4: For Peer Lecteur App and Peer Student App run "npm install chart.js"

5: For Socket Server run "npm i --save-dev nodemon"

6: For NodeJSServer create a .env File in the Repository. Of Course this File is normally not included into the repository.
   In this File create a new Variable with the connection String to your MongoDB Atlas cluster.
   Example:
   
  DATABASE_URL=mongodb+srv://brad:1234@projektseminar-oibte.mongodb.net/test?retryWrites=true&w=majority

## Running the tests

Once you installed all required Dependencies, you should start the "Peer Lecteur App" and the "Peer Student App" with a Live Server(extension for VSC) and test it. 

IMPORTANT: Depending on testing the Socket Server locally or already hostet on a Server(We recommend hosting the Socket Server on Heroku) you have to change the URL to the Socket Server in both the "Peer Student App" and the "Peer Lecteur App".

In Both Apps you have to change the URL in the "index.html" and the "script.js" file.

To test the SocketServer open up a terminal and run(On the Project Folder) : npm run devStart


## Deployment

To create an fully working Learning Environment System you should(of course) have a MongoDb Atlas Cluster in the Background to download Questions into the "Peer Lecteur App". Feel Free to contact the Chair of Information Systems(University of Regensburg) or E-Mail robert-betschinger@outlook.de.

## Built With

Socket.IO
NodeJS
Mongoose
SaSS
Chart.js
emojiOneArea.min.js
JavaScript
Express.js

## Contributed/Authors

Created by:
 - robertbetschinger
