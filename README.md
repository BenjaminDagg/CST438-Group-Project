
### **Park Activity Group Finder**

Team:
Benjamin Dagg, QA Manager
Email: bdagg@csumb.edu
Github: https://github.com/BenjaminDagg
Slack: @bdagg

Ben Holland, Wizard
Email: bholland@csumb.edu
Github: https://github.com/BenjaminHolland
Slack: @Ben Holland

Jason Sagisi, Project Manager
Email: jsagisi@csumb.edu
Github: https://github.com/Jsagisi
Slack: @JasonS

Anders Kjoelberg, INSERT YOUR ROLE
Email: akjoelberg@csumb.edu
Github: https://github.com/AndersKjoelberg
Slack: @Anders Kjoelberg

### Deliverable 

We will create a website that allows users to find pick up games for sports in parks in their area. Users will be able to see local games happening in their area via an embedded map and form teams and plan games with other users with a built in chat room. When a users’ team wins a game in a park they upload the winner of the match to the website and their team logo is displayed over the park on the map, allowing other teams to fight to contest the park. Additionally, the website will keep stats for individual players and teams such as wins, losses, and a friends list.

#### Link 
https://cst438-group-jabb.herokuapp.com/map/locations/-LDo1ofRZXVIGKjSimhx

### Motivation

It is difficult to find enough people to start a pickup game  at a local park ,whether an individual player is looking or a group. Additionally, a team of players cannot find an opponent team unless they join a local league and they have no way to compare their team to others. Our app makes it easy for a player to quickly find a team to play their favorite sport with and enjoy a competitive environment to rank their team against other local players.

### Technologies and Approach

Front end: Angular
We will use the AngularJS framework to develop our websites user interface and provide real time changes to the interface. We will also make server calls from the interface to pull in data and update components in real time based on the data.

Back end: Node JS
Node Js will help us create a server to take in requests from the front end and exchange data between it and the database. The server will also have our TCP sockets to implement the chat room.
Socket.io

Socket.io will be used as an server to provide real time updates in our chat room between all clients and the server. The sockets will carry messages between clients and server.
Database: MongoDB
Mongo will be our database to store map information such as coordinates of parks, team owned locations, and locations of all map markers. The database will also store all user info such as login info, teams, friends, and stats. Our server will exchange database information between the client and database. Mongodb stores data as JSON which makes it easily passable through HTTP messages.
Map
We will use Google Maps API to display the map on the front end and easily display markers and images on the map
![](https://github.com/Jsagisi/CST438-Group-Project/blob/master/design.jpg)
 



### Dependencies and Risks

Our app relies on a connection to the Google Maps API to display the map and its data which is the majority of the front end. If the API fails then users will not be able to find matches based on the map. The app relies on the Node JS server being up to interact with the database and to use socket.io to connect with other users in the chat feature. Our app relies on users giving location services permissions to the web page so that the user’s town can be displayed on the map accurately. To deploy our app we rely on Heroku to setup the web page.

### Milestones

### Milestone 1
By milestone 1 the core functionality of our app will be complete. The core functionality is displaying a google map on the client web page. The map will show locations of local parks with map markers. There will be a search bar for the user to search for a specific location in their area for a game. The user can click on any marker and select to join an existing game at the park or create and schedule a new game at the park. Our database will be up and store information about the games at each park such as the players, time, and teams. The client will be able to contact the server via HTTP to update and pull information from the database. At this milestone we will be focusing more on functionality than appearance so the web page will not be styled.

### Milestone 2
By milestone 2 we will implement additional features that provide ease of access and social features to the app. We will implement the chat room so users who are in the same area can chat with each other to plan games at local parks. We will implement the teams features so that users can form teams with each other and schedule games with other teams in the area. We will also introduce the team competition feature where teams can fight over a park to have their logo displayed on the map.

### Milestone 3
For milestone 2 we will improve the style and appearance of the web page to make it more appealing and easier to use. If time permits we will introduce a ranking system for teams by ranking teams based off of wins and losses and provide leaderboards for teams in the users area. We will also work on fixing bugs introduced in the first two milestones and testing the app for weaknesses. 

### Mockup

![alt text](https://github.com/Jsagisi/CST438-Group-Project/blob/master/mockup.jpg)

### User Stories

User Story #1) As a user I should be able to search for locations on the map, so that I can quickly find the location I am looking for.

* A search bar is present on screen where I can enter the name or address of a location
* When I click enter the map centers on the entered area and a marker is displayed on the map for the location
* If no location is found an error message is displayed

User Story #2) As a user I should be able to see a list of current pick up games happening in my area, so that I can find a game to join.
* A list of current pickup games is displayed on the left side of the screen including location, time and number of players, and which sport
* An icon is displayed over locations on the map indicating that a game is happening or scheduled at this location

User Story #3) As a user I should be able to start a new pickup game at a location and indicate which sport, time, and number of players so that I can find a game to join when none are listed.
* A list of current pickup games in displayed on the left side of the screen. There is an add button on the top of the list to create a new game
* When the add button is clicked a form appears asking the user to fill out information of the game
* When clicking on a location on the map, an add button appears 
* When click on add button a form appears asking user to fill out information on the game.

User Story #4) As a user I should be able to send messages to other players in my area so that I can invite them to a game, add them as a friend, or invite them to my team.
* A chat box is displayed at the bottom of the screen 
* Users of a certain radius are automatically entered into the chat room with each other
* Users can enter a message at the bottom of the chat box then click send button to send the message to other users
* An add button appears to the right of each user which gives option to add them as friend 

User Story #5) As a user I should be able to login with facebook so that users don’t have to go through a sign-up page.
A button to sign in with facebook.
* Login button will redirect me to Facebook's oauth process.
* Profile picture is displayed.
* Profile name is displayed.

User Story #6) As a user I should be able to report scores of games played so that users can keep track of their match history.
* An area to submit scores is shown when a game is initialized.
* Scores submitted are saved into a database.
* A user match history can be shown.

User story #7) As a user I should be able to choose a casual match or competitive mode so that there is varying levels of competition.
* The best team on competitive matches will be able to see their logo displayed on the park based on game type.
* Casual mode will have the option to randomize teams.

User story #8) As a user I should be a able to notify people that someone’s looking for a game so that it increases the chances of finding a game.
* Users will be notified what park is requesting games.
* Information on the sport and game mode is shown.
* Having options to turn off notifications.

User story #9) As a user I should be able to form a team with other users so that we can compete with other teams in our area and track our statistics
* A “find team” button appears on the left side of the dashboard
* When clicking find team button a list of teams from around the users area is displayed with a join button next to each team


User story #10) As a user I should be able to invite my friends to join my team via a text message and email so that I can play with my friends who may not have the app.
* A button appears on the dashboard to “invite friends”
* The button opens a window to enter a friends phone or email
* An email or text message is sent to the user to invite them to sign up for the service

