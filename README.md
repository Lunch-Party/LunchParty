Original App Design Project - README Template
===

# Lunch Party 

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
For our IOS App idea we decided to create a mobile app solution for making lunch party plans with friends and coworkers. The IOS app will allow users to suggest, share, and vote on lunch spots seamlessly, making decisions even easier!

### App Evaluation
- **Category:** 
Lifestyle, Social
- **Mobile:**
Uses location and maps to display restaurants close to the user. 
- **Story:**
Allows users to make decisions faster and intuitively using the apps features of suggesting, sharing, and voting.

- **Market:**
Anyone who eats out at restaurants can use this app. Colleagues and coworkers alike can vote on polls for favorite places to eat.

- **Habit:**
Users can access the app to eat at least three times a day for breakfast, lunch, dinner. Users can create lists of favorite restaurants. 

- **Scope:**
Lunch Party is a stripped down Yelp app with voting as its main user interaction. It will be feasible to complete in the six week period remaining. 

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**
* User can share their location.
* User can see local restaurants in area. 
* User can vote for a restaurant.
* User can see others' votes.
* User can login.
* User can follow/unfollow another user.
* User can create an account.
* User can search for another user.
* User can create list of favorite restaurants.

**Optional Nice-to-have Stories**

* Advanced search features
    * Filter by: 
        * restaurant type
        * allergy
        * diet
        * time of day
        * type of meal (breakfast, lunch, or dinner)
* User can add tags to make find their profile easier 
* Tapping on a photo / restaruant to add suggest / add as your vote 

### 2. Screen Archetypes

* Login Screen
   * User can login.
* Registration Screen
   * User can create an account. 
* Stream
    * User can see local restaurants in area. 
    * User can vote for a restaurant.
* Detail
    * User can see other users' votes.
* Creation
    * User can create list of favorite restaurants.
* User Profile
    * User can showcase their list or photos of food they've taken and post it
* Search
    * User can search for another user.
    * User can follow/unfollow another user.
* Settings
    * User can share their location.

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Home Feed
* Search User or Restaurant
* Post a Photo
* Start a Poll
* Manage Profile 

**Flow Navigation** (Screen to Screen)

* Launch Login Screen
   * Login Button
   * Register Button
* Home Feed Screen
   * Search Button
   * Following Menu Button
   * Vote Menu Button
* Following Feed Screen
    * List of restaurants followed such as a Instagram feed
* Vote Menu Screen
    * Start a Poll Menu Button
    * Feed displayed of past polls and their results
* Start A Poll Screen
    * Shows information of poll and what is being voted on
    * Screen looks like a messaging chat room with other users
    * Users vote here on where to eat
    * Results Menu Button at the bottom
* Results Screen 
    * Shows visualized poll data with percentages
    * GPS Map with a "Get Directions" menu button
* Search Screen
    * User can see Images of search results
    * Description and Reviews can be picked
    * Filters screen is overlayed over the Search screen
        * This allows the user to set a filter of what they are searching for
* User Profile Screen
    * User Profile Screen highlights all the details of the user like a social app as Instagram would do
        * List of followers, following, # of posts, sponsors, location and bio are all found here
    * Highlights user submitted images 

## Wireframes
We decided to put our focus on a digital wireframe since we would all be able to work on it and add our input. The link for this can be found under "Digital Wireframes & Mockups" and "Interactive Prototype" shows it in action as a GIF!

<img src="http://g.recordit.co/IK0yWmi6Y7.gif">

### [BONUS] Digital Wireframes & Mockups
https://www.figma.com/file/UtHHkhvTuEr4tc50VPssR8/Frame-I?node-id=0%3A1

### [BONUS] Interactive Prototype
http://g.recordit.co/IK0yWmi6Y7.gif
https://recordit.co/IK0yWmi6Y7 *additional search capability
## Schema 
### Models
#### Poll

   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | option     | String   | name of one restaurant option |
   | author        | Pointer to User| image author |
   | image         | File     | image that user posts |
   | likesCount    | Number   | number of votes for the restaurant option |
   | createdAt     | DateTime | date when post is created (default field) |
   
#### Post

   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | objectId      | String   | unique id for the user post (default field) |
   | author        | Pointer to User| image author |
   | image         | File     | image that user posts from restaurant |
   | caption       | String   | image caption by author |
   | commentsCount | Number   | number of comments that has been posted to an image |
   | likesCount    | Number   | number of likes for the post |
   | createdAt     | DateTime | date when post is created (default field) |
   | updatedAt     | DateTime | date when post is last updated (default field) |

### Networking
* Launch Login Screen
   * Login Button
   * Register Button
* Home Feed Screen
   * Search Button
   * Following Menu Button
   * Vote Menu Button
* Following Feed Screen
    * (Read/GET) Query all posts from users user follows.
* Vote Menu Screen
    * (Create/POST) Create a poll.
    * (Delete) Delete existing or past polls.
    * (Read/GET) Display feed of past polls and results.
* Start A Poll Screen
    * (Read/GET) Display poll information like time remaining, number voted, options.
    * (Read/GET) Display messages/updates in between options and votes.
    * (Create/POST) User creates a vote on a restaurant option.
* Results Screen 
    * (Read/GET) Display poll data with number of votes per restaurant option.
    * (Read/GET) Query a GPS map to display location of winning restaurant.
* Search Screen
    * User can see Images of search results
    * Description and Reviews can be picked
    * Filters screen is overlayed over the Search screen
        * This allows the user to set a filter of what they are searching for
* User Profile Screen

- [Create basic snippets for each Parse network request]
- [OPTIONAL: List endpoints if using existing API such as Yelp]
