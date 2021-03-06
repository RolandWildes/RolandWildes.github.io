# Software Capstone Project

## Databases

### Overview

When I created the event tracker application we were instructed to use sql databases as a means of storing the user and event data. Sql databases are very easy to set up, manage, and modify thanks to the query setup and large amount of functionality built into the sql structure. With the sql databases I was able to create, manage and modify two databases storing user and event data with ease. Previously I had used sql databases in a Lunix environment where we would create and modify databases with simple structures and read/write to them. With this project I learned a lot more about sql and its many features which helped while implementing a better user experience and functionality through my enhancements. 

The goal of these enchantments from the previous version was to add a way to separate personal user events with access being determined through the login. The previous version would show all events whenever anyone logged in so I set to implementing the changes for separate users. If you watched my code review you may notice that my first idea was to create separate event databases for each user. This would work and technically would be one of the most secure ways of implementing the desired functionality however if we had many users actively using the application, the storage though negligible with a few databases, could add up and hinder the device. 

I looked at this idea and scrapped it on the basis that the storage requirement was a negative and there are better ways of implementing the functionality. Instead of separate databases I chose to stick with the single database however each event now has a user tag that is associated with each user. Now when a user logs in the database only loads the events with the users tag into the application completing the desired separate events without the storage overhead. In regards to security I also changed all the sql query statements that have inputs to use prepared statements to avoid sql injection attacks. 

#### Event database example
![EventDatabase](/images/EventDatabase.PNG)