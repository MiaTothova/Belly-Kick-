# BellyKick

[View the live project here.](https://bellykick.herokuapp.com/)

![](https://github.com/MiaTothova/Belly-Kick-/blob/main/images/responsive.png)

## UX
I aimed to create a simple blog app aimed at pregnant moms and dads or people trying to concieve. It is aimed at anyone interested in this topic.

#### The ideal client:
* Adults
* Parents
* English Speaking
* Anyone looking to educate themselves.
* Women 
* Men

### The website will help clients to:
* Navigate easily through the website
* View content of interest
* Sign up / login
* Contact admin
* Comment, like and share the content wih people of interest.

### User Stories and Manual Testing
All of these user stories have been tested and all functionality works.

1. As a Site User I can view a paginated list of posts so that select a post to view.
* On the main blog page, the viewer can view posts that have been posted to the blog by an admin. If the blogs posts count exceeds 6, it automatically adds a next button directing to the next page to see the rest of the published posts.

2. As a Site User I can view a list of posts so that I can select one to read.
* On the main blog page, the viewer can view posts that have been posted to the blog by an admin. The user can then decide which post to read.

3. As a Site User I can click on a post so that I can read the full text.
* The user can click on any published post to read it.

4. As a Site User / Admin I can view the number of likes on each post so that I can see which is the most popular. or viral.
* Both the user (logged in or not) and the admin can see how many likes have been given to any published post.

5. As a Site User / Admin I can view comments on an individual post so that I can read the conversation.
* Both the user and the admin can view comments that have been left on a post. 

6. As a Site User I can register an account so that I can comment and like.
* In the navigation bar, I have a Register link which brings the user to the registration form. After completing registration the user can then comment and like posts.

7. As a Site User I can leave comments on a post so that I can be involved in the conversation.
* This can be achieved after registering/loggig in.

8. As a Site User I can like or unlike a post so that I can interact with the content.
* * This can be achieved after registering/loggig in.

9. As a Site Admin I can create, read, update and delete posts so that I can manage my blog content.
* All of this is fully functioning. The admin has a full power over the app.

10. As a Site Admin I can create draft posts so that I can finish writing the content later.
* All of this can be achieved via the admin panel.

11. As a Site Admin I can approve or disapprove comments so that I can filter out objectionable comments.
* All of this can be done via the admin panel. After a user submits a comment, it then needs to aproved by the admin before it shows up on the blog post.

12. As a user I can fill out a form so that the page admin can contact me.
* After clicking the Contact us button on the main page. The user then fills out the contact form and it sends the users information the the admin pannel. The admin then can view the contact details and the message, and can contact the user accordingly.

### The Scope
To achieve my goal, I included the following features my website:

1. Main blog page.  
2. Fully functioning navigation bar and footer to navigate through the site.
3. Contact us button featured on the main page, for anyone wanting to contact the admin.
4. Register page, where people can sign up and create a username in order to acces the commenting and likes functionalities.
5. Login page 
6. contact us page, which gets accesed through the main page and includes a form.
7. Sign out link.

### The skeleton
The blog application consists of 5 pages in total including the signout link.
Here are just rough wireframes : 

* [Web view](https://github.com/MiaTothova/Belly-Kick-/blob/main/images/web.png)

* [Tablet view](https://github.com/MiaTothova/Belly-Kick-/blob/main/images/tablet.png)

* [Phone view](https://github.com/MiaTothova/Belly-Kick-/blob/main/images/phone.png)

* [Schema](https://github.com/MiaTothova/Belly-Kick-/blob/main/images/schema.png)

## Features

Landing page:
* Navigation bar: This is the same for all navigation links. The nav bar displays diferently whether user is logged in or not.
* Footer: Same for all link pages. contains social media links and copyright.
* Main blog content: Each blog post is diferent, discussing a different topic in regards to pregnancy.
* Contact us link: Directs the user to a contact form.

Register page:
* Contains a Sign Up form where the user sellects a username, email and a password.

Login page:
* Features a sign in form

Contac us:
* Features a contact form for when the user wants to reach the admin.

Logout page:
* Asks for confirmation to see if the user is really ready to sign out.

### Future features
1. A library containig all pregnancy topic bestsellers.
2. A library of links navigating to other usefull websites.

## Technologies Used
* HTML
* CSS
* Python
* Java Script - used to create messages in the blog eg. login logout messages
* Django Web Application Framework
* Bootstrap - for responsivness
* Gitpod - used for coding my code
* Github - to save the project code
* Heroku - to host the app
* Allauth - for sign up, login and logout
* Claudinary - to store my images 
* Am I responsive -  to test responsivness
* Balsamiq - to create the wireframes
* Lucidchart - to create schema image

## Code Validation
I used dev tools to continuesly inspect my code and check my responsivnes in diferent screen sizes.
I also  Nu HTML Checker and W3C CSS Validator Services as well as PythonCheker to ensure there were no errors in the project.
* Nu HTML Checker
* W3C CSS Validator
* PythonChecker

[Web view](https://github.com/MiaTothova/Belly-Kick-/blob/main/images/css-check.png)

[Web view](https://github.com/MiaTothova/Belly-Kick-/blob/main/images/html-check.png)

[Web view](https://github.com/MiaTothova/Belly-Kick-/blob/main/images/python-check.png)

## Deployment
### Start
In Gitpod workspace:
1. Install Django and gunicorn into the terminal window 
*  pip3 install django gunicorn 
2. Install suporting libraries 
*  pip3 install dj_database_url psycopg2
*  pip3 install dj3-cloudinary-storage
3. Requirements.txt
*  pip3 freeze --local > requirements.txt
4. Create a new project name: use the name you want to use for your app 
* django-admin startproject bellykick
5. python3 manage.py startapp blog
6. Now you need to open settings.py file in bellykick and add 'blog' into installed apps.
7. Now you need to migrate the changes in the terminal :
* python3 manage.py migrate
8. Then python3 manage.py runserver 
* open the browser and see that your basic skelleton in runing.

In Heroku:
1. Create new app name and select europe.
2. Then Click - Resources Tab - Add-ons enter - Postgres and then select - Heroku postgres
3. Then select the settings tab, click reveal Config vars and then copy the DATABASE_URL


Back in Gitpod:
1. Create env.py file in the same directory as manage.py file 
* import os
* then enter os.environ["DATABASE_URL"] = PASTE THE URL FROM HEROKU CONFIG VAR DATABASE_URL WITH STRING.
* then os.environ["SECRET_KEY"] = "YOUR SECRET KEY"
* then copy the secret key value and paste this in Heroku Reveal config var section in settings tab without string.
2. Then settings.py
* import os
* import dj_database_url
* if os.path.isfile("env.py"):
* import env
* In SECRET_KEY section remove the value and add it like this:
SECRET_KEY = os.environ.get('SECRET_KEY')
* then scroll down to : DATABASES and comment out all that section.
* And add new section like this:
DATABASES = { 'default': dj_database_url.parse(os.environ.get('DATABASE_URL')) }
3. Then use the migrate comand in the terminal again : python3 manage.py migrate#

4. Create the Cloudinary Account and then copy the Cloudinary Api, Paste in the env.py file and heroku Reveal config vars. After this add 'cloudinary_storage', 'cloudinary', in to the INSTALLED_APPS in settings.py
5. Then add templates in TEMPLATES_DIR in settings.py.
6. Then add to ALLOWED_HOST:
* ALLOWED_HOSTS = ['bellykick.herokuapp.com', 'localhost']
7. Then Create Procfile and inside the Procfile add
* web: gunicorn dosaproject.wsgi:application
8. Then back in the terminal:
* git add
* git commit -m "Deploy Commit"
* git push
9. Then Go heroku app select deploy tab connect the Github and then select Manual deploy. it will create the app run successfully.

### Final
After finishing the project these are the final steps:
1. Debug= False in settings.py
2. git add . git commit -m "deployment commit" git push
3. heroku setting remove DISABLE_COLLECTSTATIC
4. Then Deploy and can view the App in Heroku.

### Content
The main idea for this blog has come from Thing before I blog walkthrough. I have followed many of the steps taken to develop that blog in my own project. I have also researched and watched allot of youtube clips on django models.

## Credits
* I would like to thank the slack community for sharing many discusions in relation to this topic which were very helpfull.
* I would like to thank my mentor Guido Cecilio Garcia Bernal for many tips and ideas and always being there when I needed advice. 
* I would also like to thank my class coordinator Kasia Bogucka for answering any questions that I have been having throughout the procces. 


