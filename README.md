# Udacity Project Item Catalog 
This web app is a project for the Udacity [FSND Course](https://www.udacity.com/course/full-stack-web-developer-nanodegree--nd004).

## About
This project is a RESTful web application utilizing the Flask framework which accesses a SQL database that populates categories and their items. OAuth2 provides authentication for further CRUD functionality on the application. Currently OAuth2 is implemented for Google Accounts.

## Introduction
This project has one main Python file `project.py` which runs the Flask application. A SQL database is created using the `database_setup.py` module and you can populate the database with test data using `lotsofmenus.py`.(provided by Udacity)
The Flask application uses stored HTML templates in the tempaltes folder to build the front-end of the application. CSS/JS/Images are stored in the static directory. (provided by Udacity)

## How to Install
1. Install Vagrant & VirtualBox
2. Clone the Udacity Vagrantfile
3. Go to Vagrant directory and either clone this repo or download and place zip here
3. Launch the Vagrant VM (`vagrant up`)
4. Log into Vagrant VM (`vagrant ssh`)
5. Navigate to `cd/vagrant` as instructed in terminal
6. Setup application database `python /item-catalog/database_setup.py`
8. *Insert fake data `python /item-catalog/lotsofmenus.py`
9. Run application using `python /item-catalog/project.py`
10. Access the application locally using http://localhost:5000

## JSON Endpoints
The following are JSON endpoints:

Restaurant JSON: `/restaurant/JSON`
    - Displays the restaurants.

MenuItems JSON: `/restaurant/<int:restaurant_id>/menu/JSON`
    - Displays whole menu for particular restaurant.

Menu Item JSON: `/restaurant/<int:restaurant_id>/menu/<int:menu_id>/JSON`
    - Displays particular menu item.

