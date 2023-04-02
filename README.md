# Recipe-App-API
This repository contains the code for a recipe app API made with Django and Django REST Framework.
The API allows users to store and retrieve recipe data, including ingredients, tags, and categories. Users can also create and edit their own recipes, as well as share and review other users' recipes.
The purpose of this application is to demonstrate how to create an API with authentication, test-driven development (TDD), and Docker.

## Features
Some of the features of this application include:

* User authentication (using Django's built-in authentication system)
* Token-based authentication (using Django REST Framework's built-in TokenAuthentication)
* API endpoints for ingredients and recipes
* Filtering and sorting by name and tags fields
* Handles image upload for the recipes endpoint
* Unit and integration tests using TDD

## Getting Started
To get started with this project, follow the steps below:

Clone or download the project code from this repository.
```bash
  git clone git@github.com:Zahra-Nasiri/recipe-app-api.git
```
Install the dependencies:
```bash
   pip install -r requirements.txt
```
Run the tests:
```bash
  python manage.py test
```
Start the development server:
```bash
  python manage.py runserver
```
That's it! You can now browse the API endpoints locally at http://localhost:8000/api/.

## Using Docker
This project can also be run inside a Docker container. To get started with Docker, follow the steps below:

Install Docker on your machine.

Build the Docker image:
```bash
  docker build .
```
Start the Docker container:
```bash
  docker-compose up
```
Run the tests inside the Docker container:
```bash
  docker-compose run app sh -c "python manage.py test && flake8"
```
That's it! You can now browse the API endpoints locally at http://localhost:8000/api/.

## API Endpoints
The following API endpoints are available in this project:

* /api/user/create/ (POST)
* /api/user/token/ (POST)
* /api/user/me/(GET, PUT, PATCH)
* /api/recipe/ (GET, POST)
* /api/recipe/<recipe_id>/ (GET, PUT, PATCH, DELETE)
* /api/recipe/tags/ (GET)
* /api/recipe/tags/<tag_id>/ (PUT, PATCH, DELETE)
* /api/recipe/ingredients/ (GET)
* /api/recipe/ingredients/<ingredient_id>/ (PUT, PATCH, DELETE)
* For more information about these endpoints, refer to the views.py file in the recipe app.

## Authors

- [Zahra Nasirmohammadi](https://github.com/Zahra-Nasiri)


## 🚀 About Me
I'm a  back-end developer...

you can read more about me on my [linkedin account](https://www.linkedin.com/in/zahra-nasirmohammadi-73584b241/)
