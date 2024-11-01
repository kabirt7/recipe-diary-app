# recipe-diary-app

## Purpose

Problem: when trying a new recipe, it's often advised to make it multiple times in a row to iron out the kinks so to speak. However, I don't always think this is feasible due to ingredient availability, boredom, picky kids, life etc. I also find that even when I do perfect a recipe, if I come back to it after some time - I don't always remember the exact changes I made to perfect the dish.

Solution: I want to create a website where you can log attempts of making a dish. I want this to also be a platform where people can share their recipes. However, what makes this functionality different is that people can share their own takes on a recipe. I think this is a fun way to share how different people can put their own spin on the same dish. 

## MVP

* CRUD capability creating the recipe
  - ingredients
  - method
  - summary
  - tips

* Collection of your accounts recipes where you can log multiple attempts of this recipe.

* The ability to save someone elses recipe and save it to your collection of recipes which is then able to be edited, logged and re-shared.
  - this will always show where the original recipe came from
  
* Recipe viewing dashboard
* Accounts, admin and personal
  - ability to make ones own account
* Hosted on AWS using Docker

## Research Needed

* Accounts and Security
* Planning out the code

## Features

* banner with search bar, log in button, nav options (home, account, contact)

### HOME
* horizontal scroll through published recipes
  - you can 'like', 'comment' and 'rep-publish' your own version of recipes that come up (if logged in)
 
### ACCOUNT 
* MyRecipes
  - browse through your own recipes
  - can edit your recipe
  - can add diary logs of attemps to your recipe
 
* Create Recipe
  - engaging looking form component that will use the same component as when republishing recipes i.e. create and reshare have a very similar template
 
### CONTACT
* basic contact info about who I am, technologies used and the purpose of the site

## Technology
* TSX, Redux, AWS, mySQL, Java (SB)


## LOG

### 21/10/24

* initalised the front and back end
* planned out the nav bar appearance
* planned out the flow of the site including the home page and account page functionality

### 22/10/24

* working through this tutorial to get a better understanding of how to implement spring security https://spring.io/guides/gs/securing-web#scratch

### 30/10/24

* worked through the tutorial to understand the basics
* I want to implement a registration system for users which will require a different implementation
* from my research, the implementation will be as follows:

1. create a UserDetails entity
2. implement a UserDetailsService that loads the user from the database
3. configure spring security (similar to how the previous tutorial implemented it)
4. create endpoints for login, registration, logout

### 31/10/24

* added spring security to pom
* finished my User Entity - it includes lombok all and no args constructors for readability's sake
  - I still need to edit the Id to be serialised to work with the UserDetails interface
  - needed to add Authority portion for the UserDetails interface, override is necessary since it is an implementation
      
