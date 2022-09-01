# Homework 1

* Assigned: 9/8
* Due:
    * Part 1: 9/16 11:59PM on Gradescope
    * Part 2: TBA
    * (Part 1 and Part 2 are due separately!)
* Value: 3.75% of your grade
* Done and submitted individually (as with all the homeworks) **via [Gradescope](https://www.gradescope.com)**
* For ER diagrams, please limit what you use in your diagrams to what was covered in class.  We will penalize ER diagrams that use features not covered.


# Part 1


## 1.1 (5 points) ER design: Calendar Events

You will design a database for a Calendar application (like Google Cal)
for tracking events.  The database will include users, calendars, events, and other relevant info.

### Description

Users

* **Users** have an **email** address, **name**, and **birthdate**.  A user always has an email address that uniquely identifies them.

Calendars

* **Calendars** have a **calendar_id** and an **ispublic** attribute that signifies if it is a public or private calendar.  
* Each calendar is **owned** by a single user.  A calendar cannot exist without an owner, and its **calendar_id** is unique globally across all users.  
* A calendar can be shared with many users, and a user can have multiple calendars shared with them.

Events

* **Events** have **event_id**, **title**, and **description**. **event_id** is unique globally.  
* Events keep track of **when** they occur.    
* Each **when** has a date,  and may optionally  **recur** weekly on the same day of the week as the date.  If so, the user can optionally state the date when the recurring event should end.
* Each **when** is either  **all day** or a **time range**. A time range also has a **start** and **end** hour.
* Events only occur at one **when**.
* An event is either a **meeting** or a **focustime**.
* A meeting can **invite** any number of users as guests.
* A focustime uses a boolean **autodecline** to automatically decline meetings during the focus time.
* An event **must be owned** by exactly one calendar, and cannot exist without a calendar.

Rooms

* **Rooms** have **room_id**, **floor**, and **building**.
* **room_id** uniquely identifies the room.
* Each meeting can optionally have a room. However, each meeting can have at most one room. 
* Each room has an optional **link** for remote attendees.

State any assumptions you make.

### Your Task

1. Render the calendar database in the version of the ER diagram that we studied in class, with exactly the constraints and requirements specified above. 
2. Please state any assumptions that you make, but make sure that
  you don’t introduce new constraints that are not listed in the problem definition.
3. Suppose we now want to let users record notes for a given instance of a meeting (if a meeting is recurring, an instance is the meeting on a specific day).    Given the ER diagram you drew. state in 1-2 sentences how it could be extended to support this new use case, or why it would be difficult to extend the diagram. 


Notes

* You can draw the diagram by hand and scan it, or use an app like powerpoint or https://app.diagrams.net/
* If you scan a diagram, make sure it is easily legible.  Parts that the staff cannot read/interpret will be considered incorrect.
* If the specification does not explicitly provide a key attribute for an entity set, you can assume there is an id.



## 1.2. (5 points) More Database Design

GitHub is a web based Git repository hosting service that provides version control and source code management functionality. It provides several collaboarative features like bug tracking, task management, and contribution analytics for every project. Handling big code bases and with multiple people working on them, indeed becomes a tedious task, GitHub helps to make this exercise easier. GitHub’s bug tracker is called Issues, and has its own section in every repository. Issues are kind of like shared e-mails, and a great way to keep track of tasks, enhancements, and bugs for the projects. You may learn more about github issues at [Github-Issues](https://guides.github.com/features/issues/) 

Visit the issues page of any public repository on Github, For example, visit [Tensorflow-Issues](https://github.com/tensorflow/tensorflow/issues). Analyze the page and the linked issue pages to understand its data requirements.  

Then, 

* Design an E-R diagram for the website that captures its main functionality of issues, and comments.
* Include at least 4 entities, 4 relationships, and 3 constraints, in the same format as part 1 of this homework.
* 2 of the entities should be **Issues** and **comments**.  You are free to choose the other two.
* For each entity, relationship and constraint, include a 1-2 sentence description that justifies your decision to include it and design it in the matter that you did.


# Part 2

## TBA
