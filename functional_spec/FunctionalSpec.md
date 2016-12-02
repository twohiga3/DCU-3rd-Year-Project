# Functional Specification for Meeting-Organiser

## 1.Introduction

**1.1 Overview**

The system will be a webapp which will utilise its user’s calendar to organise meetings between multiple users. Users will create logins for the webapp and will have a calendar associated to each login, which has all their scheduled events for the weeks ahead. The users can then create groups of users to organise a meeting with. Each group will have an admin - the user who created the group by default, though this privilege can be passed among users in the group, and multiple admins will be allowed but not advised. Groups will have a built in chat client, and the admin of the group can set parameters for a meeting to organise, as well as assign some users as high priority for meetings, such as a meeting between students and a lecturer would assign high priority to the lecturer. Some of the possible parameters will include: how long a meeting will last; meeting locations as specified (see below for description); high priority users for meetings. Meeting locations will adhere to necessities for users, such as accessibility for disabled users, computers, conference call functionality and more. Behind the scenes, the application will compare each user in a group’s calendar to find suitable times which adhere to user’s available time. In the instance of the application returning multiple possible meeting times, users in the group can vote for which time suits them best. High priority users will have a higher weighting for voting. In the event of a tie, the option voted for by the highest priority user will be chosen, or the group admin will gain privilege to choose which time should be used. Once a meeting is organised, the webapp will add this meeting to the user’s calendars.  

Other functionality of the webapp will include automated emailing to users with group invitations and meeting details. Users in a group will have the option to upload notes of scribed meetings, which can be sent via email from the webapp to each user in the group, or to users in the group who could not attend a meeting. Businesses will be able to create groups, which can host all their meeting locations and all their members of staff. These business groups can then have subgroups to organise meetings from, and will be able to use the meeting rooms the business owns as suitable meeting locations. This will allow our webapp to note when a location is available or unavailable also. It is aspired that the webapp will be able to handle meetings between different time zones, without setting a “redeye” meeting for some user(s).  

**1.2 Glossary**

_Webapp_ - a web based application  
_API_ - Application Programming Interface  
_Admin_ - Abbreviation of administrator, although an admin on our site will not do much administrating, we decided this is the most appropriate word to define the creator of a group.  
_HTML_ - HyperText Markup Language  
_CSS_ - Cascading Style Sheet  
_SQL_ - Standard Query Language  
_PHP_ - PHP originally stood for Personal Home Page, but it now stands for the recursive acronym PHP: Hypertext Preprocessor.  
_Java_ - Slang lingo for coffee. Also refers to the programming language by oracle which will be used in the development of the application.  

***

## 2.General Descriptions

**2.1 System Functions**

_Users_  
Users of the webapp will create a login for our site using a gmail account. Through use of Google API this will allow the webapp to access the user’s google calendar and send emails to the users. Users will be able to alter some settings, such as what they will receive email notifications about, which users can contact them, if their details display to other users in groups and other expected user functions.  

_Groups_  
Groups will hold any number of users from 2+. High user count groups will be unadvised but will still be permitted. Each group will have a chat client. Groups can have subgroups, which are purposed for businesses but can be used by anyone. Groups will have the option to be for a once off meeting. This means that after a meeting is scheduled the group will be disbanded. This function is for once-off meetings.  

_Group Admins_  
When a user creates a group they automatically become the admin of the group. Admins decide when all users have joined the group, when to organise a meeting, which users are high priority, settle tied votes, set meeting requirements.  

_Interface_  
The interface of our website will be programmed through HTML and CSS. It will be easy to use for a first time user, but also rewardingly fast for an experienced user through use of shortcuts and memory of users most used tasks.  

_Meetings_  
The core function of the webapp. When the admin of a group clicks the “Organise a Meeting” button, the meeting function begins operating. It will dissect each user in the group’s calendar, taking out each available free time which adheres to parameters set by the group admin. It will compare each user’s list of free times and return all the suitable times it found.  

_Voting_  
In the event of the meeting function returning multiple possible meeting times, user’s will be given the option to vote for their preferential meeting times through highest importance voting - ie they rank their most suited time 1, and their least suited time n where n is the number of meetings returned.  


  




