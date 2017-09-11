# README

## Project Description

This repo implements the simple Instagram Clone shown in the YouTube tutorial [Make an instagram like site in under 30 minutes! (Ruby on Rails)](https://www.youtube.com/watch?v=MpFO4Zr0EPE). The tutorial walks viewers through how to create a Rails app with the abilty to register and login users and submit posts to a global feed.   



## App Functionality

### Home Page
![Home Page](/readmeImages/createpage.png)

### Registration
![Registration Page](/readmeImages/register.png)

### Login/Logout
![Login Page](/readmeImages/login.png)
![Logout Page](/readmeImages/logout.png)

### Creating Posts
![Create Page](/readmeImages/createpage.png)

### Navigation
![Navigation Page](/readmeImages/logout.png)





## Differences from the tutorial

I tried to follow the instructions in the tutorial as closely as possible, but there were acouple alterations.

1. We use more current versions of Bootstrap and Paperclip than used in the tutorial.

2. The files `applications.scss` and `posts.scss` contain additional styling for the home page.

3. The tutorial's confirmation popup did not work for me. This was fixed by replacing `confirm: 'Are you sure?'` with 		 `data: {confirm: 'Are you sure?'}` in `application.html.erb`.



# Running the Project

Clone this repository. Run `rails s` to start your local server.
