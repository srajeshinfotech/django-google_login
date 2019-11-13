# django-google_login - Rajesh Sakkarai <srajeshinfotech@gmail.com>

This is very simple library to login your site with Django service


# Steps to run the application
1. Clone this repo
2. Open the cmd promt and make sure you installed the python latest version
3. execute below commands to install the requried libraries
		
		virtualenv env -p python3

		pip install social-auth-app-django

		pip install psycopg2

		pip install python-social-auth

		cd django-google_login
 
4. After this most important part comes that Google auth key and secret key.
To create an API key:

   Go to the Google Developers Console
	 
   Create a project and fill in all the details
		
   On the right side there is credentials tab, select it .
	 
   Click on Create Credentials then Oauth Client ID. Select application type Webapp , Give any name of your choice.
	
   Under Authorized JavaScript origins fill
	
   http://localhost:8000
	 
   Authorized redirect URIs
	 
   http://localhost:8000/account/complete/google-oauth2/

5. Copy the CLient ID and Client Secret Under setting.py

   SOCIAL_AUTH_GOOGLE_OAUTH2_KEY =''  #Paste CLient Key
	 
   SOCIAL_AUTH_GOOGLE_OAUTH2_SECRET = '' #Paste Secret Key
	 
 6. And now we are ready to fire up the console.
   
		 $ python manage.py makemigrations

		 $ python manage.py migrate

		 $ python manage.py runserver

		 June 21, 2017 - 19:10:37

		 Django version 1.11, using settings 'login.settings'

		 Starting development server at http://127.0.0.1:8000/

		 Quit the server with CONTROL-C.

 7. Open up the browser http://localhost:8000/
