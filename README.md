# COP3060Project Event Planning and Coordination

1. Project Proposal
* What challenge or inefficiency exists today?

  We need one platform for events. Moreover, because events are distributed across multiple channels such as Instagram, Fizz, and Email, users don't have a reliable single source of information. This leads to less social engagement which affects event participation.

* Why is this problem worth solving?

  This is worth solving because it will increase sociability and student engagement.  Event planners will be able to see and coordinate with other events. Wether it is a volunteering service, a spot to get free resources, or the next social event, with a more consistent planner, events and selections can be made more efficiently and reliably.

* Target users: 

  Students,
  Visitors
  Alumni
  Clubs // Organizations
  Vendors // Sponsers

VALUE PROPOSITION

* Users would want to use my application because it would be campus orientated.
* Instagram has a variety of events but because of its congestion it can be easy to forget. 
* Fizz no easy search for events, and congrestion with other media forms. Reliant on replies
* Emails can be easily lost and forgotten if this event is not a high priority.

Value proposition
* At minimum this application will be allow for organizations to upload a flyer, annouce an event 

Core Functionality (MVP)
1. User Accounts
Users can sign up and log in.
Two types of users: students (attendees) and event creators.
2. Create Events
Event creators can post events.
Each event includes: title, date, time, location, and description.
3. View and Find Events
All users can see a central list of events.
Users can search and filter events by category or date.
4. Engagement Features
Users can RSVP or mark interest in events.
Users can upvote events.
Popular events appear in a “trending” section ( time and popularity ).
5. Study Groups
Students can create or join study groups.
Groups can organize study-related events or meetups.
6. Basic Moderation
Events must follow required fields (no empty or spam posts).
Users can report inappropriate events.

----------------------------

SYSTEM DECOMPOSITION:
 MAJOR MODULES
1. Authentication & User Management
  Handles user sign-up, login, and logout
  Differentiates user roles (student vs event creator)
  Manages basic user account information
2. Event Management System
   Delete events
   Holds event details
3. Community & Group System
  Supports study groups and informal communities
  Allows users to join or create groups
  Helps organize group-based events and meetups

ENTITIES DATA OBJECTS
1. User - Represents anyone using the system.
id
name
email
role (student, organizer)

3. Event - A scheduled activity or gathering.
id
title
description
date_time
location
category (study, chess, social, giveaway, etc.)
organizer_id
upvotes_count

4. Group (Interest Group) - Represents ongoing communities like study groups, chess meetups, etc.
id
name (e.g., “Math Study Group”, “Campus Chess Club”)
description
interest_type (study, chess, sports, social, etc.)
created_by
members_count
created_at

User → Event (1 to many)
One user can create many events, but each event has only one creator.
User → Group (many to many)
A user can join many groups, and each group can have many users.
Group → Event (1 to many, optional)
One group can host many events, and an event may belong to a group.
User → Event (interaction)
Users can RSVP and upvote many events, and each event can have many users interacting with it.
