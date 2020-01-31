## Table of Contents

- [General project requirements](#General-project-requirements)
  - [UI \ UX design](#UI--UX-design)
  - [Page interactivity](#Page-interactivity)
- [Development milestones](#Development-milestones)
  - [1. Topic selection](#1-Topic-selection)
  - [2. UX wireframe with HTML](#2-UX-wireframe-with-HTML)
  - [3. UI design](#3-UI-design)
  - [4. Front-end basics](#4-Front-end-basics)
  - [5. The Final Frontier](#5-The-Final-Frontier)

# General project requirements

The project should be implemented as a single-page application (SPA) with client-side routing (via browser's History API). Communication with remote data source has to be performed via AJAX.

Upon implementation, a showcased version of the project should be deployed and hosted via web-server (local or remote one). You can use one of free hosting services across The Web ([Firebase Hosting](https://firebase.google.com/docs/hosting), etc), or run instance locally.

## UI \ UX design

User experience (UX) have to be considered prior to layout implementation. Interface should be clear for user. Main actions within each page should be somehow visible for the user at the first sight (using layout, color accents, hints, etc.).

The interface of the application has to be marked down via HTML (HTML version 5). The markup itself has to be semantically correct (e.g. `<a>` tag can be used for links, but not for buttons). Different page sections should utilize existing HTML5 tags to keep page division clear for developers (`<nav>, <header>, <article>, ...`).

Interface of the web-site must properly be displayed at least on following screens: 1440x900 (desktop) and your mobile device of choice. (You can use Chrome's emulator to test your site).

Styling solution for this project is plain CSS (or pre-processor of your choice: SCSS, Less). **No third-party styling libraries (such as Bootstrap) are allowed by default.** Any library dependency have to be discussed personally prior to inclusion in project.

### Tools:

* [Figma](https://www.figma.com) — online tool for UI design
* [Moqups](https://app.moqups.com/) — another online tool
* [Adobe Photoshop / Illustrator](https://rutracker.org/)

### Things to explore:

* [HTML overview](https://www.w3schools.com/html/default.asp)
* [HTML5 semantic elements](https://www.w3schools.com/html/html5_semantic_elements.asp)
* [HTML Academy](https://htmlacademy.ru/)
* [Material Design reference](https://material.io/design/)
* [Material Design colour system](https://material.io/design/color/the-color-system.html#color-theme-creation)
* [MDN's CSS reference and guides](https://developer.mozilla.org/en-US/docs/Web/CSS)

## Page interactivity

Front end part of this project has to be implemented in JavaScript programming language (all latest language features are allowed and welcomed, no backward compatibility is mandatory). **No external libraries are allowed by default (except for vital ones: Firebase / Amazon connectivity libraries, etc.)** TypeScript may be used as a wrapper over JS.

### Framework usage

The main idea behind this course is for you to get a bit familiar with JavaScript as a programming language of web platform. While there are lots of different less or more popular frameworks that will make your life as a front-end developer easier, the basics of the language and ability to solve fundamental problems using zero-dependency approach is very valuable and can give you a better understanding of what this language and related APIs are capable of. There are lots of pros and cons of each framework in comparison to others, which may affect your decision to use one or another in particular project, but understanding core concepts is mandatory to use any of them.

Thus, it is not recommended to use frameworks within this course, because any knowledge-check will be primarily focused on JavaScript itself. Albeit it is not strictly forbidden, you are encouraged to try task implementation in pure JS environment. However, if you still have plans to learn particular JavaScript framework during this semester or have previous hands-on experience you want to extend or utilize during it, this information should be provided along with project topic selection. Personal knowledge check will be adjusted accordingly. **At the end of the semester a framework-based project will not be accepted if major lack of framework understanding will be discovered. You have been warned!**


### Things to explore:

* [JavaScript: The Definitive Guide](https://rutracker.org/) — a good place to start
* [JavaScript: The Good Parts](https://rutracker.org/)
* [JavaScript: The Right Way](http://jstherightway.org/)
* [Codecademy's introduction to JS](https://www.codecademy.com/learn/introduction-to-javascript
) — alternative place to start
* [MDN's JavaScript section](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
* [Clean code concepts: JS version](https://github.com/ryanmcdermott/clean-code-javascript)
* [Building SPA in plain JS](https://dev.to/rishavs/making-a-single-page-app-in-ye-good-olde-js-es6-3eng)

### Tools:

* [VS Code](https://code.visualstudio.com/) — a very good and fast IDE by Microsoft (surprisingly)
* [JetBrains WebStorm](https://www.jetbrains.com/ru-ru/webstorm/) — well, not very fast, but a very powerful IDE

## Examples:

* [Google I/O 2016 web client](https://github.com/google/ioweb2016)
* TBE

# Development milestones
## 1. Topic selection

#### 0. _PUT_YOUR_TOPIC_HERE_

It is much better, if you could come up with your own idea for project to implement during this course, while it will stimulate your curiosity in some way. So feel free to explore provided topics below and try to think of some web-application of similar complexity. Don't be lazy!

#### 1. Expense manager

Personal finance tracker. You can record all your spendings and income to understand where does your money actually go.

##### Basic functions:
- Authentication
- Transaction list (Add / Edit / Remove transaction functions)
  - Two types of transactions: income / expense
  - Each transaction should contain following data: amount, date, place (optional), comment (optional), image (optional).
- Categories for transactions (Add / Edit / Remove category functions)
- Statistics for user per period (month, year, week)
  - Total spendings (and per category)
  - Total income (and per category)
 
**Examples:** [ZenMoney](https://zenmoney.ru/), [Spendee](https://www.spendee.com/)

#### 2. Community-driven dictionary

A website, where anyone can add a new word with its definition and extra description. Community can then upvote or downvote that word. If some word gets too many downvotes, it gets removed. On the main page there is a feed with top-rated words. Only authenticated users can add or vote for words in dictionary. Unauthenticated users can only see the dictionary itself.

##### Basic functions:
- Authentication
- Main word feed (can be sorted by rating or creation date)
  - Each word card in feed can contain word itself and short definition (limited by character count)
- Word of the day on main page (selected randomly from words with positive rating)
- Add new word. Entity should contain following data: word itself, definition, extra comments (optional), one or more links to external sources (other dictionaries, articles)
  - Each word can have more than one entry created by different users (for example, for different contexts)
- Ability to upvote / downvote specific word from feed or word page (only for authenticated users). Only one vote from each user is allowed, but user can cancel xe's vote.
- A button to report a word entry for inappropriate content (user can add comment to tell moderators, why this word should be deleted)
 
**Example:** [Urban Dictionary](https://www.urbandictionary.com/)

#### 3. CV-constructor

A website, where user can create or edit its CVs.

##### Basic functions:
- Authentication
- Main page: list of user's CVs
- Create / edit page: a complex form with different sections (only one section at a time is visible, user can go through pages in any order)
  - Main info (CV title, user name, surname, CV position (developer / tester / designer)
  - Summary (employee's professional summary)
  - Key skills (a list with one or more skills employee wants to highlight as vital)
  - Technical skills (a list of technical skills: software, methodology knowledge, etc) with level of knowledge (basic, intermediate, advanced)
  - Language knowledge (language name, knowledge level)
  - Previous projects (project name, description, start date, end date)
  - **User input should be validated on the client side before submission (e.g. no empty fields, no invalid data)**
  
**Example:** [LinkedIn's](https://www.linkedin.com) profile editor

#### 4. Tea database

A website, that can be a library for different teas. Each user can add a new variety of tea. Other users can upvote or downvote each entity and also leave comments.

##### Basic functions:

- Authentication
- Main page with top-5 library entities and 10 recently added varieties
- Add new tea
  - User can type in tee name, description, price, place, where xe got it (can be empty) and a photo of tea (can be empty). This data can be edited or deleted later.
- Other users can comment created entity. They also can rate it (give a tea 1-5 stars) and report a price they bought it for (on the same form, as rating).
- On a page dedicated to the particular tea variety, user can see tea data, average price and comments.
- A search page, where user can browse database by tea name and price constraints (min, max)

**Examples:** [Untappd](https://untappd.com/), [ViVino](https://www.vivino.com/)

#### 5. Chat application

Yet another chat application.

##### Basic functions:
- Authentication
- User profile: nickname, avatar change
- 'User is typing' indicator
- Message statuses: not delivered, delivered, read
- User can send stickers (stickers are ought to be hard-coded)
- Channels (more than two users can be in one channel)
  - Public - visible to everyone
  - Protected - visible to everyone but protected by password (set upon creation)
- Dark theme (automatic by browser media query and manual - in settings)
- Local or remote notification by browser's notification API

**Examples**: Slack, Telegram

#### 6. Group expenses app

An application to manage group bills paid by one person.

##### Basic functions:
- Authentication
- English and Russian language support (switch in header)
- Dashboard
  - Current balance (I owe, others owe me)
  - Recent payments
- Add expense (total amount, photo (can be empty), participants (list with suggested names of people user already added to other transactions), split method (equal, particular amount)
- Edit / Delete expense
- Mark expense as 'repaid'

**Example:**: [Spliwise](https://www.splitwise.com/)

#### 7. Scandinavian crossword constructor

A website where user can create a crossword, obtain a unique ID for it, send it to friend and see, if xe can solve it!

##### Basic functions:
- Authentication
- Constructor
  - Define grid dimension (horizontal and vertical cell number)
  - Add a word to grid and define a question for it, that participant will see
  - When crossword is constructed, creator gets a unique ID that other user can type on 'Solver' page to solve created crossword
- Solver - provide crossword ID to solve it
  - Solving progress is tracked for each user, which means more than one user can solve the same crossword independently
  - Validation is performed only when all words were filled

**Example:**: [Crossword maker](https://onlinetestpad.com/en/crosswordmaker)

#### 8. Calendar

Time- and activity-management application. User can set appointments, tasks and reminders.

##### Basic functions:
- Authentication
- Calendar view (year, month, week view). Days with appointments should be marked by colour of appointment (or multiple colours in case of more than one appointment)
- Upcoming appointment for current day / pending tasks are on top of the page 
- Appointment creation
  - title
  - description
  - start / end date and time
  - place (may be empty)
  - zero, one or more reminders (user can type in when to remind)
  - colour (to distinguish tasks)
- Task creation (tasks have a 'completed' status. After user marked task as 'completed', it will disappear from 'pending' section)
- Ability to edit / delete appointment or task

**Examples:** [TickTick](https://ticktick.com/) and well, any calendar.

#### 9. Music player

Music catalogue / player application.

##### Basic functions:
- Authentication
- Upload music track
  - set / update its title, performer name, cover image
  - assign one or more genres
  - attach lyrics to track
- User can perform a search across all uploaded music by all users
- Create / edit / delete / duplicate playlists

**Examples:** [Yandex.Music](https://music.yandex.ru/), [Spotify](https://www.spotify.com/)

#### 10. Cocktail database

A website, where user can share own unique cocktail recipe or rate cocktails created by others

##### Basic functions:
- Authentication
- **Main feature: visualization** ([examples](https://trendland.com/wp-content/uploads/2013/01/shoot-em-up-infographic-of-30-shots.jpg))
  - each cocktail should have a dynamically generated visual representation based on ingredients selected by user upon creation
  - glass form may be identical for all recipes
  - ingredients are hard-coded by developer (minimum 10 visually different ingredients are required)
  - each ingredient should have specific color or texture to display
  - order and proportion of ingredients affect visual representation
- Main feed with top-rated cocktails, their average rating and their images
- Cocktail constructor
  - name
  - description
  - recipe: an ordered list of ingredients with their volumes for this cocktail
- An ability to rate cocktails (1-5 stars rating system) and leave a comment

## 2. UX wireframe with HTML
### Acceptance criteria
To pass the milestone, you must provide images (hand-drawn, digitally created) for most of the pages your web-site will have (for both display sizes). Each block should be represented by corresponding HTML-tag. Utilized HTML tags should be semantically-correct in terms of block function on the page.

**Example:** [UX wireframe example (without HTML)](https://file.mockplus.com/image/2017/11/e8bbb60f-f2da-49cf-9c3b-64dbefe77b27.png) (your final result has to be more detailed, than the provided image)

## 3. UI design
### Acceptance criteria
Milestone's acceptance criteria: a semi-finalized set of pages with production-ready design (can be updated on later stages of development) **for both screen sizes**.

**Disclaimer:** as we do not study UI design in this course, there are no strict requirements to your project interface appearance. However, a more or less meaningful UI is required to pass this milestone, beacuse it will enforce you to use a good amount of CSS. Consider yourself advised to look through at least [Material Design reference](https://material.io/design/) to have a basic idea of how a good UI might look like. You can make a quick search over the internet to find a good reference your project may follow. Get ready for additional tasks during your project showcase on this milestone.

## 4. Front-end basics
### Acceptance criteria
At this point you must provide a working skeleton of the website: basic navigation, routing, authentication (if required), state-management, networking, etc. A check-point to see if everything is going well before the final stage of development.

## 5. The Final Frontier
### Acceptance criteria
A web-site that implements all requirements within selected topic.
