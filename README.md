# Trio - pixel perfect, E2E clone of Trello (Vue + Node.js).

Trio is a visually appealing and user-friendly project management tool built by a team of 3 Full-Stack developers. It utilizes the latest front-end and back-end technologies to provide an innovative solution for managing projects, tasks, and deadlines. Ideal for developers, project managers, or anyone needing to keep track of tasks.

Try it here: https://trio-j5ev.onrender.com


## Table of Contents

- [Trello Description](#trello-description)
- [Application Features](#application-features)
- [Technologies](#technologies)
- [Getting started](#getting-started)
- [Showcase](#showcase)

## Trello Description

Trello is an app in which you can manage projects and tasks using a kanban board. A board contains lists and tasks. Usually each project is a board, and the lists and cards are the tasks and subjects to do in the project. Users can modify the board and change list and card locations using Drag and Drop. Users can work together and watch live changes. There are many other features in Trello, such as labels, due date for tasks, members and more. Every thing Trello has, we also had. We even added color-blind mode and speaker assistant! More about it in the features section.

## Application Features

- **Create and Manage Boards and Projects:** Easily create, update, and remove lists and tasks using Drag and Drop (D&D) functionality.

- **Deep Task Customization:** Dive into task details with features like Labels, Due Dates, Members, Cover Images, Checklists, and an Activity Log. You can also perform actions like Copying, Moving, and Archiving tasks.

- **Enhanced Side Menu:** Customize your board background using the Unsplash Photo API. Filter tasks by members, labels, and access a comprehensive General Activity Log.

- **Advanced Features:** Enjoy secure authentication options alongside regular login. Benefit from encryption for data safety.

- **Trello Parity:** We've included all the intricate features that Trello offers, ensuring you won't miss out on any functionality.


## Technologies
The technology stack we used was MERN - MongoDB, Express, React, Node.js. The app uses webSockets to update the board in real-time. The API calls to the backend are done with the REST API method , and we used middlewares to authenticate and authorize actions.

We have used many thirs side libraries for many goals, such as Modal Popper, , D&D and more. The layout and pixel-perfect were made with Sass (functions, mixins, variables).

## Getting started

Head to the repository on top and clone the project or download the files.

```
git clone https://github.com/Shayzig/Trio
```

Enter the backend folder and make sure you have node_modules installed. After that we will initiate the server with 'npm start':
```
cd backend
npm i 
npm start
```

You shuold get a console ouput that the server is up and running at port 3030. Enter the frontend folder and repeat the same process.
```
cd frontend
npm i 
npm start
```
You shuold get a console ouput that the server is up and running at localhost:5173.

That's it! The App should be opened automatically, enjoy!



## Showcase

### Homepage
The landing page in which the user can sign up / login, or press the call to action button to start demo if the are limited with time.
<img width="1440" alt="homepage" src="https://github.com/Shayzig/Trio/assets/121104922/53278aaf-5329-47c4-afd1-275b96de22c5">

### Workspace
All of the user's boards. Here, in addition to create a board with the empty board box and navigate between their's boards, they are able to use the vocal-assistant we created with 3rd side library! Pressing on the button in the middle of the nav bar on top would open an modal with instructions that makes life a bit easier.
<img width="1440" alt="boardindex" src="https://github.com/Shayzig/Trio/assets/121104922/c2e20cf9-9e18-49ca-b6be-e815c2c79635">

### Board
All the functionality that you have in Trello. D&D, live-updates, editing tasks to the deepest level, side-menu, editing board members and much more...
<img width="1440" alt="boarddetails" src="https://github.com/Shayzig/Trio/assets/121104922/213ee77f-e3ae-4042-a07b-a79d7c8254f3">

### Task Details
Here the user can edit their tasks and to watch it happens live, in this page and behind. Every button on the right menu opens an dynamic modal which fits the content accordingly to the pressed button.
<img width="1440" alt="taskdetails" src="https://github.com/Shayzig/Trio/assets/121104922/d8da8607-8a7e-433d-9b61-626b0da2a737">

### Some mobile!
Just a taste of the mobile experience. We used different mixins, conditional rendering. The layout we have built from the very first moment enabled us to make the website responsive without a lot of effort.

<img width="150" alt="Mobile" src="https://github.com/Shayzig/Trio/assets/121104922/955ffaf8-db3b-48a1-b61c-1cd4fd51915e">

<br>

Authors:
- Shay Zigdon
- Alon Perlin
- Guy Dahan
