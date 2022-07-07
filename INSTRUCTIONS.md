# Django Instructions for Basic WebSite 

    ## Python setup
        
        1. Download Python [installer](https://www.python.org)
        
        2. Install python using default settings
        
        3. Check to make sure you have the current version
            - run this command in a terminal: 
                - python --version which
                - this command shows the current version

    ## Django and VirtualEnvironment setup
        
        1. Create a folder that will contain the project
        <!-- I used 'Django_Basic_Website' -->
        
        2. Inside the folder create a virtual environment
            - run this command in a terminal: 
                - 'virtualenv (name of your virtual environment)'
                <!-- creates a virtual environment -->
        
        3. Activate the virtual environment
            - run this command in a terminal: 
                - win: 
                    'name_of_your_venv\Scripts\activate.bat'
                - mac/linux:
                    'source name_of_your_venv/bin/activate'
                
        4. Install Django using pip command
            - run this command in a terminal/cmd: 
                'pip install django'
                <!-- installs django -->

    ## Django project and app setup
        
        1. Create a django project
            - run this command in a terminal/cmd:
                'django-admin startproject (name of project)'
                <!--initiates django project folder structure -->
                <!-- I used 'site_project' as the name of my project -->
        
        2. cd into your newly created project directory

        3. Create django application
            - run this command in a terminal/cmd:
                'python manage.py startapp'
                <!-- initiates django app folder structure -->
                <!-- I used 'site_app' as the name of my app -->
        
        4. Verify server is working
            - run this command in a terminal/cmd:
                'python manage.py runserver'
            -navigate to development server port in your browser
            <!-- you can choose the server port by running this command in a terminal/cmd:
                'python manage.py runserver (port number)'-->

    ## <u>Setup Communication, Routing, and Logic</u> 

    ## Add 'app' to 'project'

        1. setup database connection
            - run this command in a terminal/cmd:
                'python manage.py migrate'  
                <!-- creates database file -->

        2. add 'app' to 'project' settings
            - inside 'project' folder, find the settings.py file
                - add 'app' to settings.py file:
                    '(name of app)'
                    <!-- I used 'site_app' -->
        
        3. import include method from django url module into the project's urls.py file
        
        4. add 'app' path to 'project' urls.py
            - app's default url path is app's name.urls
            - ex. path('', include('site_app.urls')),
              <!-tells site_project to route users to "site_app's urls-  -->
        
    ## Setup routing and views for 'app'

        1. create urls.py file in 'app' folder and:
            - import the 'app' views.py file
                "from 'app' import views"  
            - import 'path' from the django urls module
                "from django.urls import path"
        
        2. add path(s) from views file to urls.py file by:
            "path('', views.base, name='base'),"
            <!-- tells app when users choose the default path, the function 'base' in the views file will handle the logic-->
        
        3. add the function 'base' to the views file
            "def base(request):
                return render(request, 'base.html')"
            <!-- when the 'base' function is called the base html file is rendered -->
        
    ## Create and setup template file paths

    1. inside of the 'app' folder create another folder called 'templates'
        - create the html file to be rendered
        <!-- I named my file 'base.html', because I may use 'template inheritance' for more complex apps. -->

    2. Setup html file
    <!-- I used a basic html file with a few 'h' tags to show django functionality in this lesson-->
