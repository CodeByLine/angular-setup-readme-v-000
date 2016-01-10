# Angular Setup + directory structure

## Overview

We need to ensure that we have a level-headed way of structuring our applications from the beginning, otherwise we could end up with files everywhere, which means it's hard to know exactly what you are editing and where.

## Objectives

- Define the core structure of an Angular application
- Create a feature based file structure

## Core Structure

Angular supports modules, and our application file structure will reflect this. Each module will have directives, templates, controllers and services.

Like a normal application, we'll have separate folders for our JavaScript, CSS and images. However, inside our JavaScript folder we'll have individual folders for each module in our Angular application. Angular needs at least one module to kick things off, and we're going to call our main module "app".

This means that you'll end up with a directory structure like this -

- js/
  - app/
    - directives/
      - TodoEscape.js
      - TodoFocus.js
    - controllers/
      - TodoController.js
    - services/
      - TodoService.js
    - templates/
      - partials/
        - TodoForm.html
      - views/
        - Todo.html
    - app.js
  - angular.js
- img/
- css/
- index.html

This is a feature based file structure, as we're splitting off into individual modules instead of having all of our controllers/directives/etc. in one folder. Don't be scared - we will be touching on controllers/directives/modules/etc very soon!

There are plenty of other ways to structure your application. One other popular way is to just have folders for controllers, directives etc without having folders for each module, as follows - 

- js/
  - directives/
    - TodoEscape.js
    - TodoFocus.js
  - controllers/
    - TodoController.js
  - services/
    - TodoService.js
  - templates/
    - partials/
      - TodoForm.html
    - views/
      - Todo.html
  - app.js
  - angular.js
- img/
- css/
- index.html

This works too, but as your application gets bigger, the folders will end up with loads of files in them, without us knowing what part of the application they are responsible for.

This is why we separate our app into "modules". We can then immediately know what file is used in what part of the application just by looking at what folder it is in.