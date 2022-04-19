# djangoVideoChat
### This is a django based web application for video chat among multiple users. This application uses WebRTC ( Agora sdk : https://www.agora.io/) to enable real-time voice and video interaction inside our django application.
## Initial setup and download
* Run the following command to install mysqlclient since this project uses mysql database<br>
 ```$ pip install mysqlclient```
* Download Agora sdk (https://docs.agora.io/en/All/downloads)

## Database
Configure database connection in setting.py file:
````
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'djangoVideoChat',
        'USER': 'root',
        'PASSWORD': 'root',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
````
Change USER and PASWORRD if necessary.

## Database migration
* Run the following commands to migrate the database tables.
```
$ python manage.py makemigrations
$ python manage.py migrate
```
* This will create all the requred database table.

# Start project
Run the following command to run the project on the local server 'http://127.0.0.1:8000/'
```
$ python manage.py runserver
```
* Use a new room_name and a username to initiate a nwe room for video stream. 
* To join a room that is already created use that specific room_name and username.
* Use video button and mic button to toggle the camera and the microphone respectively. 

This project is done by following a code along tutorial on youtube for the purpose of learning.
Youtube link : https://www.youtube.com/watch?v=Oxnz8Us1QAQ&ab_channel=DennisIvy
