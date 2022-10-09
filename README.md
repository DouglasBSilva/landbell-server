## **Landbell Challenge Project**

This repository is an "**orchestrator**" to manage and create the front and backend applications.

**To see the code for the front and backend access respectively:**

*   [https://github.com/DouglasBSilva/landbell-laravel](https://github.com/DouglasBSilva/landbell-laravel)
*   [https://github.com/DouglasBSilva/landbell-vuejs](https://github.com/DouglasBSilva/landbell-vuejs)

#### HOW TO INSTALL:

*   Requirements
    *   [Git](https://git-scm.com/downloads)
    *   [Docker](https://docs.docker.com/get-docker/)
    *   [Docker-Compose](https://docs.docker.com/compose/install/)
    *   Free Ports: 80,8000,3306
*   Clone this repository

```plaintext
git clone git@github.com:DouglasBSilva/landbell-server.git
```

*   Enter the folder

```plaintext
cd landbell-server
```

*   Initialize the submodules

```plaintext
git submodule update --init
```

*   Run the containers

```plaintext
docker-compose up -d
```

*   Run the migrations

```plaintext
docker-compose exec api php artisan migrate
```

*   Populate the data

```plaintext
docker-compose exec api php artisan db:seed
```

#### HOW TO ACCESS:

*   The front end will be available at [http://localhost](http://localhost)
*   The backend will be available at [http:]( http://localhost:8000)[//localhost:8000]( http://localhost)

#### ABOUT THE PROJECT:

*   Front end:
    *   endpoints: 
        *   “/” => Should display a list of all users available and one button to see details about the user
        *   “/users/:id” => Should display details about the chosen user 
*   Backend:
    *   endpoints (v1):
        *   “/users” => List all users with pagination
        *   “/users/:id” => Get details about the chosen user
        *   “/users/:id/friends” => Get the list of Direct Friends
        *   “/users/:id/suggestions” => Get a list of friends suggestions
        *   “/users/:id/cityRecommendations” => Get a list of city recommendations
        *   “/users/:id/friendsOfFriends” => Get a list of 2 depth friends
