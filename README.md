# Client-APP-TodoIst
# Client - Project 3 Repository I
**TODOIST - Read Me - Client**


# Description
Improve your professional & Personal life satisfaction. Organize your to do tasks in an easy and clear way to simplify your daily routine.

## User Stories
- **404** - user warning that the page doesn’t exist 

- **500** -  user warning that something in the page isn’t working

- **homepage** -  Access the root to create the next To do list

- **sign up** - Access all the available features of the website login - log in to personal account

- **logout** - log out from personal account to main page 

- **To do list** - All the created todo´s 

- **create To do** - create a new To do 

- **edit To do ** - edit a created To do 

- **To do - written** - details of a task

- **Delete To do** -delete a task

- **profile** - personal list of To do’s

- **other profiles** - other users personal list of To do’s


## Backlog
Other features besides the mvp scope:
. Task Category (Professional/Personal)


## Frontend
Homepage
CSS
HTML


## Routes(Frontend):
- GET /
redirects to /auth/login if not logged in
redirects to /home if logged in

- GET /auth/login
redirects to /home if user logged in
renders the login form

- POST /auth/login
redirects to /home if user logged in
body:
email
password
GET /auth/signup
redirects to /home if user logged in
renders the signup form
POST /auth/signup
redirects to /home if user logged in
body:
first name
last name
email
password

- POST /auth/logout
body: (empty)
redirects to /auth/login

- GET /auth/:id/home
renders specific To do list
includes events attending

- GET /auth/home
renders logged in home
includes logout button

- POST /auth/home/
redirects to /auth/home
body:
first name
last name
email

- POST /auth/home
redirects to /auth/login
logs out user
body (empty)

- GET /todos
renders the todos list

- GET /todos/:id/
renders the list of todo´s

- GET /todo
renders a todo
create todo button to redirect to create form
includes dropdown filter list

- GET /todos/:id
renders the To do page

- Text box
Go back button

- POST /home/:id/todos
redirects to /auth/login if user is not logged in
redirects to /todos/:id if user logged in
updates todos and user with linked objectid
body: (empty - the user is already stored in the session)

- GET /todo/:id/edit
renders edit todo form

- POST /todo/:id/edit
redirects to /Todo/:id
todos:
To do 1
To do 2
To do 3

- GET /todo/filter/:completedtodos
renders events list filtered by precedence
includes dropdown filter list

- POST /todo/filter/:completed
renders filtered todos list

- GET /todo/createtodo
renders the new To Do form

- POST /todo/create
To do description:
To do text box description


# Models:
-``` To Do Model: 
 
const mongoose = require("mongoose");
const Todo = mongoose.Schema({
  text: {
    type: String,
  },
});
module.exports = mongoose.model("Todo", Todo);
```

- ``` User Model:
const mongoose = require('mongoose');
const Schema = mongoose.Schema;

const userSchema = new Schema({
  username: String,
  password: String
}, {
    timestamps: {
      createdAt: 'created_at',
      updatedAt: 'updated_at'
    }
  });

const User = mongoose.model('User', userSchema);
module.exports = User;
```

# Links:

# Trello:
Trello board

# Git:
Server Repository Link
Client Repository Link
