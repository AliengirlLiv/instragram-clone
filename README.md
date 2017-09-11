# README

## Project Description

This repo implements the simple Instagram Clone shown in the YouTube tutorial [Make an instagram like site in under 30 minutes! (Ruby on Rails)](https://www.youtube.com/watch?v=MpFO4Zr0EPE). The tutorial walks viewers through how to create a Rails app with the abilty to register and login users and submit posts to a global feed.



## App Functionality

### Home Page
The home page contains a  shows a list of all images created by all users, organized chronologically (newest on top). 
![homepage](https://user-images.githubusercontent.com/12390123/30258758-0cadef6a-9671-11e7-8f04-7d46c13421d6.PNG)

### Registration
Users can register with an email and password. This was implemented using the Devise library.
![register](https://user-images.githubusercontent.com/12390123/30258757-0cab6d80-9671-11e7-881b-f2084c0d7bf2.PNG)

### Login/Logout
Users can login with an email and password. This was implemented using the Devise library.
![login](https://user-images.githubusercontent.com/12390123/30258760-0cbfc7f8-9671-11e7-96ff-2deeb8595328.PNG)

The same library has build-in functionality to allow users to recover forgotten passwords.
![forgotpassword](https://user-images.githubusercontent.com/12390123/30258863-de3235be-9671-11e7-8c77-35c3700c244c.PNG)

Once a user is logged in, the navigation bar gives them the option to log out.
![logout](https://user-images.githubusercontent.com/12390123/30258759-0cbf1e0c-9671-11e7-8744-64461bb29b1e.PNG)

### Creating Posts
Users create a post by uploading an image and providing a description. Users have to be logged in to post. 
![create](https://user-images.githubusercontent.com/12390123/30258756-0ca86d6a-9671-11e7-973f-4b9ce4165222.PNG)


## Differences from the tutorial

I initially tried to follow the instructions in the tutorial as closely as possible. To see the Instagram Clone as shown in the tutorial, see [this commit](https://github.com/AliengirlLiv/instragram-clone/tree/e540db6ca308ec936625cdd6d27f4ccbe66d6589).

### Additional Features

1. We use more current versions of Bootstrap and Paperclip than used in the tutorial.

2. The files `applications.scss` and `posts.scss` contain additional styling for the Home and Create Post pages.

3. The tutorial's confirmation popup did not work for me. This was fixed by replacing `confirm: 'Are you sure?'` with 		 `data: {confirm: 'Are you sure?'}` in `application.html.erb`.

4. Users must be logged in to post images.

5. Both the image and description fields are required for a post to be submitted.

6. Timestamps are displayed on images, and the images are ordered with the most recent on top.
![homepage](https://user-images.githubusercontent.com/12390123/30258758-0cadef6a-9671-11e7-8f04-7d46c13421d6.PNG)

7. Confirmation alerts after the user completes an action (e.g. logging in) disappear after a few seconds (thanks to [this SO post](https://stackoverflow.com/questions/26772839/auto-hide-the-flash-messages-in-rails) with instructions for implementing it).

8. (in progress) I tried to make users choose a username when registering so that this username could be displayed on their posts. This is not functional yet, but there are some lines of code related to this new feature (e.g. a username in the "users" table in `schema.rb`.



## Running the Project

0. Make sure you have Rails installed.
1. Clone this repository. 
2. cd into the `insta` directory
3. Run `rails db:migrate`.
4. Run `rails s` to start your local server.
5. Go to `localhost:3000` to view the app.
