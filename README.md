# Getting Started with Create React App
## Ecosystem:
### 1. React init
### 2. folder structure
### 3. State Management
### 4. Navigation
### 4. UI framework
### 5. Typization
### 6. Formating & cleanCode
### 9. Work white Medias
### 10. SEO
### 11. API calls



# 1. React 

## sets up your development environment with 'npx create-react-app app-name'
##### Let’s remove almost everything (logo, images, content and styling) and keep the bare skeleton application.


# 2. Folder Structure

## /src/… :

- All the resources generated by the team for our application must reside within this directory.
- This will be the core application source code.
- “/src/app.js” file is the container of our app and serves as an entry point.

## /assets :

- As the name suggests, all the static assets should reside here.
- Each asset should be registered and exported from the /index.js
- All assets will be accessible and imported from ‘/assets’
- This can include images, logos, vector icons, fonts, etc.

## /shared:

Only shared components used across features are placed here.
All the components should be registered and exported from /index.js for a single access point.
All the components should bear named export. This will avoid any conflicts.


## /config :

- the app’s configurations are to be kept at this path.
-This can consist of date format, default language, some master data set or anything like so.


## /i18n :

-Internationalization or multi-lingual support is achieved by the use of the “i18next” library.
-It mainly consists of a configuration file and all the language translations in independent language.json files.


## /navigation or Routing :

- As the name suggests, all the routing logic resides here.
- Our app uses “react-router-dom” for routing implementation.
- Mainly 2 types of routes are included, public & private, where private being the ones that require authentication.
- “RouterConfig.js” will have all the routes of the application defined within at one place.
- “PrivatRoute.js” is a component to add a check for user authentication for secure/private routes.
- CONSTANTS.js consists of all the constants for various available routes within our app. Reason is simply to avoid typos and easy renaming of routes when required.
- “/components” directory can be added to hold all the navigation specific components like header, nav-bar, side navbar, like so.

## /redux or store :

- It holds all the redux resources at one place.
- This includes action creators, reducers and a redux store of our app.
- CONSTANTS.js has all the action types.
- “/actions” dir consists of all the action files. Each action file includes feature based action-creators. As the name suggests, appActions will have app config based actions and userActions will have all user state related actions.
- “/reducer” dir follows the same practice like actions. reducer reduces all the actions and applies corresponding changes to store. These reducers are later merged into a root-reducer redux’s combineReducers function.
- “/store.js” is the central state of the application. This incorporates all the mapping between reducer, store and middle-wares if any.
- We have a redux-thunk middleware in our app for enabling asynchronous dispatching of actions.
Configuration for enabling dev tools for redux is done in store.js.
- Above files are enough for a “small to medium” sized applications.
- For a large application with tens of features, each having tens of actions, types and individual initial states, it is recommended to have corresponding action.js, reducer.js, constants in the feature specific directory. Finally, it can be combined into a single store in the same way it is done now.


## Pages / :
- All the various features/screens/pages are defined here. In this case, “Home”, “Page1” and “Page2” are 3 different pages of our app.
- Each screen consists of an “index.js” file which exports the screen’s container as default module which makes the screen available as a functional component.
- Each page will have a “components” dir. This will hold all the components that are required by only this page.
- Home page consists of “Authentication”, “Dashboard” & “LanguageSelection” components that are nested within.

##  /styles :
- This module holds our application-level styles.
- It can include theme definition (font, colours, typography) of the app UI, and global or commonly used styles.


# 3. State Management
- State management is simply a way to engender communication and sharing of data across components. It creates a concrete data structure to represent your app's State that you can read and write.
## Example  
![This is an image](https://www.loginradius.com/blog/async/static/878d2cde053633bfea88a8bfcfc28e89/29007/image1.png)


# 4. Navigation
##### npm install @reduxjs/toolkit
- react-router-dom will avail routing and navigation capability to our React js app. It provides us with various features like widely used browser-router, hash-router, link, redirect, switch and many more.
- React-router-dom library also provides features like maintaining history of user journeys.

# 4. UI framework
