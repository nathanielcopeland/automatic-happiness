## Javascript
- Normally run in browsers 
- Front end programming / logic
- Event driven -- runs code when events occur
  - Click
  - Hover / rollover
  - Load
  - Mousemove
  - Touch touchstart, touchmove and touchend

## Functions 
#### What is a function? 
A collection of commands, variables, statements and other functions.
	
#### Attaching functions to events

`element.addEventListener( eventname, function(){...})`

element is a DOM element -- (document object model = an abstracted representation of the HTML document structure)

eventname is the name of an event (string)

functionname is the name of a function


#### Two types of functions

1. Custom Function

    ```
    Function addNumbers(argument1,argument2)
    var result = argument1 + argument2;  
    }
    ```
    addNumbers is the name of the function written in camelcase (convention)  
    a function can take arguments (optional)  
    To stop code running in a function use return
2. Anonymous Function

    ``` 
    function(argument)} 
    var text = "Hello there";
    return text;
    ``` 
    Anonymous functions do not have a name  
    They are immediately executed in their context  
    
    #### Custom vs Anonymous
    - Custom functions can be called in many different contexts (reused), anonymous function can only be called within a single context.
    
    #### Execution order
    - functions are *hoisted* ie compiled first. it is possible to call a function before it is defined in your code.
    
    #### Objects
    Javascript Objects are written using a series of key value pairs.  
    
    ```
    var Employee = {
    "firstName" : "Jane",
    "lastName" : "Smith",
    "location" : "Melbourne"
    }
    ```
    Object Names are written with proper case,ie if made up of several words, the first letter of every word is capitalised.  
    
    To access object properties we use the dot syntax eg Object.property
    
    ```
    var EmployeeName = Employee.firstname + " " + Employee.lastname
    ```
    This structure is often reffered to as JSON (Javascript Object Notation).  
    ***
    A Different Employee obhect, with sub properties
    
    ```
    var Employee = {
    "name":{
    "first": "Jane"
    "last": "Smith"
    },
    "location" : "Melbourne"
    }
    ```
    ***
    To access the firstname
    ```
    var firstname = Employee.name.first;
    
    ```
    
    #### Classes
    
    in Javascript a class is a construct based on Javascript objects.
    
    A class needs to have a constructor, which is the function that creates/ sets the properties of the class with initial values.
    
    ```
    class Employee{
    constructor(firstname,lastname,location){
        this.name.first = firstname;
        this.name.last = lastname;
        this.location = location;
        return this;
        }
        getLocation(){
            return this.location;
        }
    }
    //create an instance of class Employee
    
    var jane = new Employee('Jane','Smith','Melbourne');
    var location = jane.getLocation();
    
    ```
    
     In the *Employee* class the constructor takes three arguments, *firstname*, *lastname* and *location*. These values are set by the constructor class when the class is instantiated. 
     
     *getLocation()* is called a method of the class. A method is a function in the class. *name* and *location* are called properties of the class.