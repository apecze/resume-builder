# Resume-builder

WORK IN PROGRESS

Resume web application based on Django

This project is based on a freecodecamp Tutorial https://www.youtube.com/watch?v=0oSsLbh_Kv4

My own added value is the containeraization and a configured docker-compose to easily manage the project:
 - Starting the development server
 - Starting unit tests & linting

## Requirements

Tho following tools needs to be installed on your environment to test this application:
 - Docker
 - Docker-Compose
 - Git

## Deployment for development & testing purposes

 1. Clone this repository to your environment `git clone git@github.com:apecze/resume-builder.git`
 2. navigate to the root folder of the application "/resume/"
 3. To start the development server please run
    ```
    docker-compose up
    ```
    ![dockr_cmpose_up](https://github.com/user-attachments/assets/723d5391-56c6-4d9f-8eee-aea143e3fde9)

 4. You should see the following output if the development server is started successfully (it can be closed with "ctrl+c" anytime)

    ![dev_success](https://github.com/user-attachments/assets/c901e403-0978-43e7-a1fd-1ddccd205b1f)

 5. Please open another terminal navigate to te root folder and run:
    ```
    docker-compose run --rm app sh -c "python manage.py createsuperuser"
    ```
    Then please enter your test credentials:
    Examples for testing purposes
     - User: test
     - Password: test
     - Email: test@test.com

 7. Once you entered your test credentials please open: [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin) and sign in with your test credentials
 8. Open `User-Profiles` on django admin page and upload your avatar, skills & your cv
    Please note that the project contains the "test_files" folder where you can use imgages and txt file for avatar, cv, & key-skill imgs.
 9. Navigate to [http://127.0.0.1:8000](http://127.0.0.1:8000) to test the site.

    You should see the following result:

    ![success](https://github.com/user-attachments/assets/fd43c532-7b35-4665-bba6-9ff039893813)

 10. Press ctrl+c to shut down development server.
 11. For decomissinoning please run: `docker-compose down`
