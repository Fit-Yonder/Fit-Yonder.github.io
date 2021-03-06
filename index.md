
# Visit us
<a href="http://fityonder.meteorapp.com/">http://fityonder.meteorapp.com/</a>

![](images/FitYonderLogo.png)

# About Fit Yonder

Fit Yonder is an application providing a platform for students and health and fitness professionals that allows them to post ideas for flexible and personalized fitness routines, things such as yoga etc. that can be done in one’s dorm room, or somewhere on campus.  When you come to the site, you are greeted by the following landing page:

![](images/mockuplandingpage.png)

It can be difficult to fit a consistent fitness routine into an already packed college student schedule. Many people are intimidated by the idea of going to the gym to work-out. Also, the hours of the gym on campus sometimes don’t work out for a variety of schedules.

Students are able to post their fitness goals and/or other constraints which can then be matched against the fitness routines available in on Fit Yonder. Fit Yonder can also enable students to log their time, frequency of workouts, and other measures of progress. Fit Yonder's workout page lists which routines are popular based provide user-generated reviews and completions.

# User Guide

Upon visiting the web app, you will be greeted with a description of Fit Yonder:

![](images/landingp.png)
![](images/landing2.png)

Upon clicking the register button you will be directed to the sign-up page, which will ask for your name, e-mail, and your selected password:

![](images/signup.png)

>FitYonder is currently under developement. If you would like to test out our web app feel free to sign in with one of our test accounts.

Admin:
username: admin@foo.com
password: changeme

User:
username: john@foo.com
password: changeme
  
After creating a profile, you will be listed on the members page:

![](images/directory.png)

Fityonder also provides a filter page, available to those who can login to the system with their UH account. The filter page allows you to display all portfolios with a given interest category (yoga, running, gym, etc):

![](images/filter.png)

Once logged in, you will have the opportunity to see the community's created workouts and events. Each workout includes the workout title, the categories it might belong to, a brief description, and a descriptive image. You can add a workout to your personal list of workouts by clicking the "Join workout!" button. The workouts you add will be listed on your profile:

![](images/feed.png)

Fit Yonder is all about community collaboration. Users can add their own workouts and events for others to see and join:

![](images/add.png)

Adding a workout/event is easy. Users need only add the basic workout information. To add a descriptive image a URL address is needed. To access an image address, simply right-lick on your image and select "Copy image address", then paste the address on the appropriate field. 

![](images/form.png)
![](images/address2.png)

The profile section of Fit Yonder features user profile pictures, brief biography, and a list of workouts:

![](images/prof.png)

# Application Design

## Landing Page

The landing page is the first page that users will be greated when our url is entered.

## Workouts Page

The workouts page lists all the avaialable workouts that are on the site. There will be options to sort the page by user rating, completeion. The user is also able to add a new workout session to the page. Pending an admins approval other users will then be able to request permision to join in with the original posters workout.
 
## Profile Page

This is the users profile where interests and achievments will be displayed.

## Login And Signup Page

Here UH students are able to login to their accounts or signup.

# Installation
First, [install Meteor](https://www.meteor.com/install).

Second, [clone our repository](https://github.com/Fit-Yonder/fit-yonder).
  
Third, cd into the app/ directory and install libraries with:

```
$ meteor npm install
```

Fourth, run the system with:

```
$ meteor npm run start
```

If all goes well, the application will appear at [http://localhost:3000](http://localhost:3000). If you have an account on the UH test CAS server, you can login.  

# Development History

The development process for Fit Yonder conformed to [Issue Driven Project Management](http://courses.ics.hawaii.edu/ics314f16/modules/project-management/) practices. In a nutshell, development consists of a sequence of Milestones. Milestones consist of issues corresponding to 2-3 day tasks. GitHub projects are used to manage the processing of tasks during a milestone.  

The following sections document the development history of Fit Yonder.

## Milestone 1: Mockup development

This milestone started on December 6, 2016 and ended on January 31, 2017.

The goal of Milestone 1 was to create a set of HTML pages providing a mockup of the pages in the system. To simplify things, the mockup was developed as a Meteor app. This meant that each page was a template and that FlowRouter was used to implement routing to the pages. 

Mockups for the following four pages were implemented during M1:

<img width="200px" src="images/mockuplandingpage.png"/>
<img width="200px" src="images/mockupprofile.png"/>
<img width="200px" src="images/mockupworkouts.png"/>
<img width="200px" src="images/loginmockup.png"/>
<img width="200px" src="images/mockupsignup.png"/>

Milestone 1 was implemented as [Fit Yonder GitHub Milestone M1](https://github.com/Fit-Yonder/fit-yonder/projects/1)::

![](images/milestone1.png)


Milestone 1 consisted of five issues, and progress was managed via the [Fit Yonder GitHub Project M1](https://github.com/Fit-Yonder/fit-yonder/projects/1):

![](images/m1-project.png)

Each issue was implemented in its own branch, and merged into master when completed:

![](images/m1-branch-graph.png)

## Milestone 2: Data model development 

This milestone started on Jan 31, 2017 and ended on Feb 2, 2017.

The goal of Milestone 2 was to implement the data model: the underlying set of Mongo Collections and the operations upon them that would support the  application.  We implemented the data model as a set of Javascript classes. The BaseCollection class provides common fields and operations. The ProfileCollection and InterestCollection classes inherit from BaseCollection and provide the persistent data structures useful for BowFolios. 
 
Also in this milestone, we implemented a set of mocha tests for the data model classes. These tests make sure we can create, manipulate, and delete the data model documents successfully.  These tests are documented above.

Milestone 2 was implemented as [Fit Yonder GitHub Milestone M2](https://github.com/Fit-Yonder/fit-yonder/projects/2)::

![](images/m2-milestone.png)


Milestone 2 consisted of 17 issues, and progress was managed via the [Fit Yonder GitHub Project M2](https://github.com/orgs/Fit-Yonder/projects/4):

<img width="200px" src="images/m2-landing.png"/>
<img width="200px" src="images/m2-login.png"/>
<img width="200px" src="images/m2-addevent.png"/>
<img width="200px" src="images/m2-addworkout.png"/>
<img width="200px" src="images/m2-feed.png"/>
<img width="200px" src="images/m2-admin.png"/>

Each issue was implemented in its own branch, and merged into master when completed:

![](images/m2-branch-graph.png)

## Milestone 3: Connect UI to data model

This milestone started on April 24, 2018 and ended on May 4, 2018.

The goal of Milestone 3 was to connect finish up the website and deployment. We tied together the the Meteor account system with our profile database. This allowed us to store individual's data and display them on a per account basis. To complete the profile page we also added a way for users to update and change their profile data. We also updated our feed to seperate events from workouts.

![](images/updateprofile.png)
![](images/editprofile.png)

Milestone 3 was implemented as [Fit Yonder GitHub Milestone M3](https://github.com/Fit-Yonder/fit-yonder/projects/4)::

![](images/m3-milestone.png)


Milestone 3 consisted of 20 issues, and progress was managed via the [Fit Yonder GitHub Project M3](https://github.com/Fit-Yonder/fit-yonder/projects/4):

![](images/m3-project.png)

Each issue was implemented in its own branch, and merged into master when completed:

![](images/m3-branch-graph.png)


# Community Feedback

## Creighton Gorai

"Fit Yonder is a great helper for random convenient workouts anywhere with a nice user friendly looking website."

## Tyler Chong

 "Computer Science majors work out?"

## Christine Le

"As someone who doesn't do traditional work outs or maintain a workout schedule, I could see myself using this webapp. I like the idea of users creating their own workouts. It encourages non-traditional forms of workout like yoga or cycling, which you wouldn't find in a traditional gym."

## Chris Smith

"I have been a swimmer since I can remember, meaning the only way I know how to workout is in the water. An application like Fit-Yonder helps me figure out land workouts that I would otherwise not explore." 

## Jason Jin

"The website looks inviting, I like the colors and the Facebook-feel to it. I would appreciate if it could be more personalized to track other things, such as weight loss journey, muscle gain process, etc."










