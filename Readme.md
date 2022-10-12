## Introduction

This is a simple Todo application built off Django (including the Django REST Framework) and React.

## Requirements

- Python3
- NodeJS(`https://nodejs.org/en/download/`)
- Django(`https://www.djangoproject.com/download/`)
- Pipenv(`https://pipenv.pypa.io/en/latest/`)
- Django Rest Framework(`https://www.django-rest-framework.org/`)

## Getting started

1. Clone the project to your machine `git clone https://github.com/RootBreaker/ToDoList`
2. Navigate into the diretory `cd ToDoList`
3. Source the virtual environment `pipenv shell`
4. Install the dependencies `pipenv install`
5. Navigate into the frontend directory `cd frontend`
6. Install the dependencies `npm install`

## Run the application

You will need two terminals pointed to the frontend and backend directories to start the servers for this application.

1. Run this command to start the backend server in the `backend` directory: `python manage.py runserver` (You have to run this command while you are sourced into the virtual environment(`pipenv shell` to the root directory ))
2. Run this command to start the frontend development server in the `frontend` directory: `npm start` (This will start the frontend on the adddress [localhost:3000](http://localhost:3000))

## Errors

1. Error: No module named "corsheaders"
   Solution:
   Using pip : `pip install django-cors-headers`
   Using pipenv : `pipenv install django-cors-headers`
2. Error: "npm run build" = "react-scripts: Permission denied" (MacOS)
   Solution:
   `npm install react-scripts --save`
   `sudo chmod +x node_modules/.bin/react-scripts`

## Built With

- [React](https://reactjs.org) - A progressive JavaScript framework.
- [Python](https://www.python.org/) - A programming language that lets you work quickly and integrate systems more effectively.
- [Django](http://djangoproject.org/) - A high-level Python Web framework that encourages rapid development and clean, pragmatic design.

## Congratulations

If you made it this far, then you have successfully run `ToDoList`. Thanks for your testing!
