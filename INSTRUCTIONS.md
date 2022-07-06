# Django Instructions for Basic WebSite 

    ## Python setup
        
        1. Download Python [installer](https://www.python.org)
        
        2. Install python using default settings
        
        3. Check to make sure you have the current version
            - run this command in a terminal: 
                - python --version which
                - this command shows the current version

    ## Django setup
        
        1. Create a folder that will contain the project
        
        2. Inside the folder create a virtual environment
            - run this command in a terminal: 
                - virtualenv (name of your virtual environment)
                - this command creates a virtual environment
        
        3. Activate the virtual environment
            - run this command in a terminal: 
                - win: 
                    name_of_your_venv\Scripts\activate.bat
                - mac/linux:
                    source name_of_your_venv/bin/activate
                
        4. Install Django using pip command
            - run this command in a terminal/cmd: 
                - win: 
                    name_of_your_venv\Scripts\activate.bat
                - mac/linux:
                    source name_of_your_venv/bin/activate

    ## Django project setup
        
        1. Create a django project
            - run this command in a terminal/cmd:
            - django-admin startproject (name of project)
            <!--initiates django project folder structure -->
        
        2. cd into your newly created project directory

        3. Create django application
            - run this command in a terminal/cmd:
            - python manage.py startapp
            <!-- initiates django app folder structure -->
        
        4. Verify server is working
            - run this command in a terminal/cmd:
            - python manage.py runserver
            -navigate to server port 127.0.0.1:"xyz"

# Customize Django application
