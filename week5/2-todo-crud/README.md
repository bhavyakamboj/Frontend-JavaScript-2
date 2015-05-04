# Week 5 : Task 2 : Todo CRUD App

## Reference
- http://learn.jquery.com/code-organization/concepts/
- http://contribute.jquery.org/style-guide/js/


## Last time
- got the code from week 4
- created and inited a new project
- replaced dom modifications and event handling with jQuery
- added "finish task" logic

## Today
- no npm & express
- code refactoring
- CRUD pattern
- Module pattern

## New Project Steps
for more info see week1 1-hello-node

- initial file structure
    - create new files and directories
    - copy the files with repeating functionality 
- inits and dependencies (bower, npm)
- initial interface 
- initial functionality


## Directory Structure

```
. 
├── .bowerrc    # change public/lib to just lib here
├── bower.json  # generated by bower init
├── index.html
├── js
│   ├── app.js  # TodoApp = (fucntion(){...})()
│   └── init.js # $(document).ready(...) here
└── lib
    └── jquery  # bower install --save jquery
```

## What is a collection

```js
var task = {
  id: 25,
  name: "Do the dishes"
  finished: false
}

var tasks = [
  {
    id: 15,
    name: "Get some groceries",
    finished: true
  },
  {
    id: 20,
    name: "Call grandma",
    finished: false
  },
  {
    id: 25,
    name: "Do the dishes"
    finished: false
  }
]
```

## app.js

http://learn.jquery.com/code-organization/concepts/#the-module-pattern

```js
var TodoApp = (function() {
  // private vars
  var tasks = [];
  var index = 0;

  // (optional) store the reference with the jQuery selectors here
  var refs = {
    addTask: "input#addTask",
    container: "#container"
  }

  // (optional) interface for setting the 
  var setSelectorRefs = function(refs){

  }

  var addTask = function(taskName) {
    // add to tasks
  };

  var finishTask = function(id) {
    // update task
  };

  var displayList = function() {
    // clear the contents
    // loop through the tasks
    // append each task
  };

  // public api
  return {
    createTask: addTask,
    finishTask: finishTask,
    displayList: displayList
  };
})();

// access via
TodoApp.addTask("Do the dishes")

```

## init.js

```js
'use strict'

$(document).ready(function(){
  // init stuff
})
```