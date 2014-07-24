# eFarmony ForwardJS Project Outline

- Welcome!
- **Part One** eFarmony Data Structures
    - 1A: Create animal object
    - 1B: Create animals collection array
    - 1C: Create relationships between the animals in the collection
    - 1D: Review
- **Part Two** Function Scope Exercises 
	- TDD scope exercises 

- **Part Three** eFarmony Functions (extra credit)
  - Scenario 0: General Helper Functions
  - Scenario 1: Profile Page
  - Scenario 2: Browse
  - Scenario 3: Search and Add Friends
  - Scenario 4: Edit Profile
  - Scenario 5: Edit Animal Collection 
  - Using Underscore.js

---


## Welcome
Welcome to the project portion of the workshop! Glad you are here masting objects, arrays and functions with us! This is document will guide you through the entire process of the project with plenty of extra work for you to take home and practice.

#### Free Tutoring??
If you keep track of typos and unclear directions, whoever submits the most mistakes to Bianca (bianca@hackreactor.com) by the end of the week gets one free tutoring session!

#### What is the goal of the project that we will be working on today?
Today we will be creating 2/3rds of our new dating app that will be taking over the San Francisco, eFarmony. This is a dating app that is breaking into a new niche, dating for animals! Animals need love too :) First we will create the data structures necessary for our application, then we will do some function scope exerciese and last we will implement the logic of our app in the function project exercise.

#### What will I need to do well in the class?
- You should have some exposure to JavaScript syntax fundamentals, such as loops and control flow, objects and arrays. **If you are relatively new to these concepts, please tell a TA quickly so we can take extra care in keep you on track during the exercises.**
- Some of the instructions are written with the assumption you're using [Google Chrome](www.google.com/chrome/). While you are welcome to use any browser you like, Chrome has some of the best dev tools available, and it's highly recommended you try it for the duration of this class.
- Any plain text editor will suffice for you to edit the exercise files. [Sublime Text](http://www.sublimetext.com/download) is a good choice.


#### What if I finish an exercise with extra time?
If you finish one of the assignments ahead of schedule, your best bet is to research and reinforce any previous concepts you'd felt shakey on, since each lecture is designed to build on a firm understanding of the previous ones. If you feel strong in all the material you've covered already, talk to an instructor and we will find some extra credit for you.

---
# Part 1: eFarmony Data Structures
In this section we will be setting up the data structures that we will be using throughout the project. We will be creating and nesting objects in arrays to reinforce concepts we learned in lecture.

**You will be placing all your code into the part1.js file.** 

##Before You Get Started
Explore the files in the **exercise01 Folder**.
 
You should find an **index.html** file which you should run in your browser. 

This is should be a blank document but will make all your javascript files available in the console so that you do not need to copy/paste every time. 

When you complete a section, feel free to comment out any console.logs so that you don't clutter up your console as you are testing your code. 

You should also find a part1.js file and a **part2.js file**. These are the files you will be coding in.  

---


### Step 1: Create a single animal object
This object will be the model of what our animal data will look like.

##### Step 1A - Object
We are going to create an object to hold our data using all the different ways of adding properties and values to an object.

- Create a variable and name it animal, assign it an empty object

- Using dot notation, add a property called 'species' and assign it a value
- Using dot notation, ensure that your species property exists on animal
- Using bracket notation, add a property called tagline and give it a value
- Using brakcet notation, check and make sure that your property exists on the animal object
- Using either bracket or dot notation, add a property called noises and assign it the value null
- Inspect your handiwork! your object should look something like this:
`{ species: 'duck', tagline: 'Afflack', noises: null } `


##### Step 1B - Array //TODO Refactor
We are going to create an array and practice the different ways of adding values.

- Create a variable called noiseArray and assign it to an empty array.
- Using bracket notation, add a noise as a string that your animal makes to the noiseArray.
- Using a native array method, add another noise to the end of the noiseArray.
- Using a different method, add a noise to the beginning of the noiseArray.
- Using bracket notation again, add another noise to the end.
- What is the length of the noiseArray? Check it.
- What is the last index on the noiseArray? How is it different than the length?
- Inspect your handiwork! What does the array you just created look like?


##### Step 1C - Nest the Array in the Object 
We are now going to put the noiseArray inside the animal object

- Create a variable called noises and assign it the string 'noises'.
- Use the noises variable with the animal object to access the value 'null'
- Now use the noises variable with the noiseArray to replace the value null with your noiseArray.
- inspect your data structure, it should look something like this:
	`{ species: 'duck', tagline: 'Afflack', noises: ['quack', 'honk', 'sneeze', 'growl'] }`
	
- Congrats! You just made a nested data structure :)  


##### Review
Let's go over some over-arching concepts:

- What are the different ways you can add properties and values to objects? 
- What about arrays?
- What if you wanted to add a property to an object that had a weird symbol?
- What about if it is a variable, how does that change the syntax?

---


### Step 2: Create a collection of animals
We are now going to take our one animal and add it to an array to create a collection of animals.

- Create a variable called animals and set it equal to an empty array
	- Note that this variable is animals(plural) while the variable in step 1 is animal(singular)
- Using any method you prefer, add your animal from step 1 to the animals array.
- Create a variable called quackers and assign it to the example object that I created above:
	- `{ species: 'duck', tagline: 'Afflack', noises: ['quack', 'honk', 'sneeze', 'growl'] }`
	
- Add quackers to the animal array using a different method than before.
- Inspect your animals array to ensure you have two objects inside.
- Create two more animal objects with these properties and values you create: 
	- species (with a string value) 
	- tagline, (with a string value)
	- noises (with an array of values)
- Check the length property of your array. It should give you 4

---
### Step 3: Create relationships between animals
Let's think about the best data structure to represent a relationship between two animals in our collection. Imagine that our app has a 'friendslist' on their profile where it lists out all of their friends. What do you think is the best way to represent this? Would you use an array or an object or some combination of both? Let's walk through the process together
##### 3a: Create a Friendslist
- Choose a data structure for the list of friends.
- Justify your decision.
- Create a variable called friends and assign it to the empty data structure.
- Using your animals array, add two species to the friends data structure.
	- ensure that you are just putting the species name, not the entire object
	- be careful not to use a destructive method like pop() that will remove the whole value from the animals array.
- Inspect your friends data structure. What does it look like?

##### 3b Create a Relationships object

Imagine now that we have more than one kind of relationship in our app, we have friends and then we have romantic matches. Let's create an object to organize these different relationships!

- Create a variable called relationships assign it to an empty object.
- Add your friends data structure to the relationships object.
- Inspect your object. What is it's length?
- Create a variable called matches and assign it to an empty array.
- Add the matches array to the relationships object. It should look like this:
	- `relationships = { friends: ['duck', 'camel'], matches: []}`
- Using the relationships object, add some species to the matches array
	- hint: the mathes array is now nested inside the relationships object!
- Inspect your object. Is the matches array now populated with some lucky species?
- Loop through your animals collection, adding the relationships object to each animal. Name the property relationships.
	- Note: it is ok that these are all the same relationship object. Later you will learn how to create a function that allows us to generate a relationships object for every animal.


#Part 2 Function Scope Exercises

##Before You Get Started
Explore the files in the **Functions** folder.
 
Run the **SpecRunner.html** file in a browser. 

This document shows one passed test and a series of failed tests.

The **functions.js** folder holds all the tests and you will be editing this file and using the **SpecRunner.html** to check your progress. This is just a javascript file so you can use console.log to help debug and inspect these functions.

A test block starts with an `it` function. The `it` function takes two arguments. The first one is a statement describing the rule addressed by the test. The second is a function that will either evaluate to true or false. The expect statement (`expect(ACTUAL === 'inner').to.be.true;`) will evaluate if the statement between the parens `ACTUAL === 'inner'` is true. You can almost read it like plain English. The expect statement below "expects that the variable ACTUAL equals the value 'inner' to be true".

      it('a function has access to its own local scope variables', 
      
      function () {
        var fn = function () {
          var name = 'inner';
          ACTUAL = name;
        };
        fn();
        expect(ACTUAL === 'inner').to.be.true;
      });
      


##Function Scope Exercises

It is your mission to go through the **function.js** file and change all the `'???'` in such a way that all the tests pass true. 

---

# Part 3: eFarmony Functions (**Extra Credit**)
####This is extra credit and will not be completed during the workshop unless you have extra time. Take these home so that you can continue practicing these concepts!

##Before You Get Started
Explore the files in the **Day4 Folder**.
 
Run the **index.html** file in a browser. 

This document appears to be blank but makes all your javascript files available in the console so that you do not need to copy/paste every time. 

When you complete a section, feel free to comment out any console.logs so that you don't clutter up your console as you are testing your code. 

Your code goes into the **part3.js** file.

---

## Helper Functions
Note that these exercises emulate real problems you will encounter when making an app. Your task is to respond with solutions to the challenges presented. This is a free-form exercise so be creative!

**You will be placing all your code into the part3.js file.**

### Scenario 0: General Helper Functions
Write the following helper functions as a warm-up. You may use some or all of them as you create your app.

- `objKeyPrinter` loops through the properties of any object and returns a string of all the keys. 
	- example input: `{ species: 'duck', tagline: 'Afflackk', noises: ['quack', 'honk', 'sneeze', 'growl'] }` 
	- example output: `"species tagline noises"` 
	

- `objValuePrinter` loops through all the properties in any object and returns a string of all the values that are strings.
	- example input: `{ species: 'duck', tagline: 'Afflack', noises: ['quack', 'honk', 'sneeze', 'growl'] }` 
	- example output: `"duck tagline"` 
	
	
- `arrValuePrinter` takes any array and returns the values as a string 
	- example input: `['quack', 'honk', 'sneeze', 'growl']` 
	- example output: `"quack honk sneeze growl"`

-  `dataTypeChecker` takes either an array or object and returns either `'array'` or `'object'` as appropriate.
	- example input: `['quack', 'honk', 'sneeze', 'growl']` 
	- example output: `"array"`
	- example input: `{}` 
	- example output: `"object"`
	
- `capitalizeVals` takes an object, capitalizes the first letter of each string value in the object, and returns the object. Ignore any non-string values like arrays, numbers or objects.
	- example input: `{ species: 'duck', tagline: 'Afflack', noises: ['quack', 'honk', 'sneeze', 'growl'] }` 
	- example output: `{ species: 'Duck', tagline: 'Afflack', noises: ['quack', 'honk', 'sneeze', 'growl'] }`
- `strCapitalizer` takes a string, capitalizes the first letter of each word, and returns the string.
 	- example input: `"my name is bristol"` 
	- example output: `"My Name Is Bristol"`
- `unique` takes an array, removes any duplicate values and returns the array.
	- input: `[1,2,3,3,4]` 
	- output: `[1,2,3,4]`
- `extend` takes two objects and copies the properties of the first object on to the second. It does not return anything. 

### Scenario 1: Animal Profile Page
In our first scenario, we want to create a profile page for one of our animals. We will create functions that will help organize our data and present it to the user in a human-readable way.

##### 1a: Log the Animal Personal Data
- Write a function named `welcomeMessage` that takes an animal object like this one: `{ species: 'duck', tagline: 'Afflack', noises: ['quack', 'honk', 'sneeze', 'growl'] }` 
	and returns a string that says "Welcome, \<species>!".
	- Your result should look like this: `"Welcome, Duck!"`
	- use your `strCapitalizer` function inside `welcomeMessage` to ensure correct capitalization.
- Write a function named `profileData` that takes an animal object like the duck example in the previous exercise. It returns a string that includes both the species and tagline with their corresponding values. The result should look like this:
	- `"species: duck, tagline: Afflack"`
	- note: do not include the noises array for now
	- use `strCapitalizer` inside of `profileData` to ensure proper capitalization
		-new output will look like this: `"Species: Duck, Tagline: Afflack"`
- Edit your profileData function to include the noises array with its values
	- `"species: duck, tagline: Afflack, noises: quack, honk, sneeze, growl"` 

  
##### 1b: Animal Relationship Data
- Create a function called `relationshipLogger` that takes an animal object and returns the relationship object if it contains one. Otherwise, have your function log `"You have no relationships :("` 

- Write a function that takes two parameters, the species name and an animal object. The function returns the relationship between the species and animal. 
	- Suggested outputs:'\<species> is a match of \<animal>', '\<species> is a friend of \<animal>', '\<species> and \<animal> have no relation yet', etc. 
	- Make sure you test all these different scenarios so that
- `addFriend` is a function that allows your animal object to add a friend. It takes a species (this could be just the name or the entire object depending on how you want to architect your app) and an animal object and adds that species on to the animal object 
	- Remember the friendslist in the relationship obejct? That is where you should store data on about friends on your animal object
- Similar to `addFriend`, `addMatch` should add a match to your animal object. 
    
### Scenario 2: Browse Animals Page
In this scenario, we will show all the animals in our collection so that a user can browse through and see who is out there on our app. This page or the profile page might be the homepage application.

- `nonFriends` is a function that shows which animals in your collection are not in your friendlist. You don't want current friends to show up while you are browsing for new friends.
	- You can choose to present this data in a way that makes the most sense to you and how you want to present this data to your user. 

### Scenario 3: Search and Add Friends
All social networking sites have a search component so that you can find a particular user. You also need to be able to add friends and matches. Let's do these exercises and see what that might look like in code. 

- `search` takes a seach query and returns an array of animal objects that contain an exact match anywhere in the body of the object. 
	- Note: the match must be exact for this to work and won't work with objects or arrays. Just primitive types (numbers, strings, booleans, etc.) 
	- You will be searching through your entire animals collection
- Extra credit: How can you make this work with any type of nested data structure? Assuming we might want to change the structure of our data in the future and won't want it to break our code.
- Write a function that ensures that no friends in your friendslist are repeated. It might take an array and return that array without any duplicate entries.

### Scenario 4: Edit Animal Profile Page
What if you wanted to edit your profile page? Let's create the logic that goes into that!

- Create a function that takes your animal object, the key you wish to change and the new value.
	- if the the property doesn't yet exist, add it! 
	


### Scenario 5: Edit Animal Collection Data
What if you wanted to change the data on the whole collection? For example, species doesn't really make sense since we are using it more like a name. This might be for the administrator of the website/database

- Write a function that creates a new animal object and adds it to the animals collection. You might want to pass in the species values, friends, etc as arguments into your function. 
	- How could the arugments keyword come in handy here?
- `cleanseData` is a function that takes the animals collection and a series of key names. It will remove any properties on the animal objects that are not given as arguments
	- input `cleansData([{'a': 'b', 'c': 'd'},{'a': 'q'}], 'a');`
	- output `[{'a': 'b'},{'a': 'q'}]`
	 

###Using Underscore.js
[Underscore.js](http://underscorejs.org/) is one of the most popular utility libraries. It provides a collection of helper methods to simplify your development. Rewrite your functions above to incorporate some underscore.js methods. You can use as many as you want! **[Read through the documentation](http://underscorejs.org/)** to familiarize yourself with what underscore.js can do. Here are some commonly used methods to get you started:

- [where](http://underscorejs.org/#where) `_.where(list, properties) `
	- Looks through each value in the list, returning an array of all the values that contain all of the key-value pairs listed in properties.
	- What function above could you use this with?
	
- [each](http://underscorejs.org/#each) `_.each(list, iterator, [context])` Alias: forEach 
	- Iterates over a list of elements, yielding each in turn to an iterator function. The iterator is bound to the context object, if one is passed. Each invocation of iterator is called with three arguments: (element, index, list). If list is a JavaScript object, iterator's arguments will be (value, key, list). Delegates to the native forEach function if it exists, and returns the original list for chaining.
	- What helper function can we replace with each?
	
The underscore library is already loaded in your index.html file so you do not need to worry about that. Just get to coding!

