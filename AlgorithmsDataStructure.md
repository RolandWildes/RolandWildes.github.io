## Algorithms and Data Structures

### Overview

The base functionality for the event tracker was to load events from the database and display them to the user. Before the enhancements the application would read the events from the database and display them in the event screen. This is appropriate and technically what was required per the course requirements however this is not very helpful for the end user. For example if the user wanted to find a particular event they would need to scroll down the list until they found the event they wanted. If the list is very long then this could take a while given that the events were also not sorted in any way. 

To improve the structure and quality of life for the user I set to sort the events by date when they are loaded into the event screen. Thanks to the some built in functionality for calling dates in sql and the quires I created, the events now always return sorted my event date with the ones happening the soonest at the top. This makes finding events much easier as you can scroll to a particular date rather then searching at random. 

Speaking of searching I also implemented a search bar that allows the user to also search for a particular event in the database. This was a very good learning experience for me as I learned even more about sql databases while developing the code for the search. Since sql has built in sorting methods I created a feq statements that simply matched the partially entered date with any events containing that date, allowing the search to also show suggested events as you type rather then entering the entire date. 

#### Event sorting code example
![Event-sorting](/images/EventSorting.PNG)
