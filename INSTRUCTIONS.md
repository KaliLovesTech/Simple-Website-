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

    ## Django project and app setup
        
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

# Setup Communication, Routing, and Views

    ## Add 'app' database and route to 'project'

        1. setup database connection
            - run this command in a terminal/cmd:
                - python manage.py migrate  
                <!-- creates database -->

        2. add app to project settings
            - inside project folder, find the settings.py file
                - add app to settings.py file:
                    '(name of app)'
                    ex. 'site_app'
        
        3. import include in project's urls.py file
        
        4. add app's 'url' path to project's urls.py
            - app's default url path is app's name.urls
            - ex. path('', include('site_app.urls')),
              <!-tells site_project to route users to "site_app's urls-  -->
        
    ## Setup routing and views for app

        1. create urls.py file in app's folder
            - import 'app' views.py file
                "from 'app' import views"  
            - import 'path' from the django urls module
                "from django.urls import path"
        
        2. add path(s) from views file
            "path('', views.base, name='base'),"
            <!-- tells app when users choose the default path, the function 'base' in the views file will handle the logic-->
        
        3. add the function 'home' to the views file
            "def home(request):
                return render(request, 'base.html')"
            <!-- when 'base' function is called the base html file is rendered -->
        
    ## Create and setup Template file paths

    1. inside of the 'app' folder create another folder called 'templates'
        - create the html file to be rendered
        <!-- I name my file 'base.html',  and use 'template inheritance' for more complex apps. -->

    2. Setup html file
    <!-- I used a basic html file with a few 'h' tags to show django functionality in this lesson-->
