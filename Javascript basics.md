#   Operands, Operator
        https://javascript.info/operators

#   Use strict
        https://javascript.info/strict-mode

#   Null vs undefined
        null is an assigned value. It means nothing.
        undefined means a variable has been declared but not defined yet.
        null is an object. undefined is of type undefined.
        null !== undefined but null == undefined.

#   Function declaration vs function expression vs arrow functions
        * Functions always return something. If there’s no return statement, then the result is undefined.
        * Functions are values. They can be assigned, copied or declared in any place of the code.
        * If the function is declared as a separate statement in the main code flow, that’s called a “Function Declaration”.
        * If the function is created as a part of an expression, it’s called a “Function Expression”.
        * Function Declarations are processed before the code block is executed. They are visible everywhere in the block.
        * Function Expressions are created when the execution flow reaches them.
        https://javascript.info/function-expressions-arrows

#   Falsy Values
        false — boolean false
        0 — number zero
        “” — empty string
        null
        undefined
        NaN — Not A Number

        When comparing any of our first three falsy values with loose equality, they will always be equal!
        When comparing null and undefined, they are only equal to themselves and each other:

#   var vs let vs const 
        https://wesbos.com/let-vs-const/

#   Variable Hoisting
        https://www.w3schools.com/js/js_hoisting.asp

#   Data Types
        There are 7 data types:

        number - for both floating-point and integer numbers,
        string - for strings,
        boolean - for logical values: true/false,
        null – a type with a single value null, meaning “empty” or “does not exist”,
        undefined – a type with a single value undefined, meaning “not assigned”,
        object and symbol – for complex data structures and unique identifiers, we haven’t learnt them yet.

#   Tail Call Optimization
        * Tail call optimization means that it is possible to call a function from another function without growing the call stack.
        * Stack considering it is one of the most commonly seen data structures. It is a LIFO (last-in first-out) queue with two primary operators — push and pop. 

#   Objects
        * https://javascript.info/object
                The Object.entries() method returns an array of a given object's own enumerable property [key, value] pairs

#   Garbage Collection
        * The main concept of memory management in JavaScript is reachability. It monitors all objects and removes those that have become unreachable.
        * The basic garbage collection algorithm is called “mark-and-sweep”.
        * The garbage collector tries to run only while the CPU is idle, to reduce the possible effect on the execution.
        * Garbage collection is performed automatically. We cannot force or prevent it.

#   Array methods
        * arr.push(...items) – adds items to the end,
        * arr.pop() – extracts an item from the end,
        * arr.shift() – extracts an item from the beginning,
        * arr.unshift(...items) – adds items to the beginning.
        * arr.splice(str) method is a swiss army knife for arrays. It can do everything: add, remove and insert elements.
                
                let arr = ["I", "study", "JavaScript", "right", "now"];
                arr.splice(0, 3, "Let's", "dance");      // remove 3 first elements and replace them with another
                alert( arr )                            // now ["Let's", "dance", "right", "now"]

                let arr = ["I", "study", "JavaScript"];
                arr.splice(2, 0, "complex", "language");
                alert( arr ); // "I", "study", "complex", "language", "JavaScript"
        * arr.slice is much simpler than similar-looking arr.splice.It returns a new array where it copies all items start index          "start" to "end"
        * arr.concat joins the array with other arrays and/or items. 
        * indexOf
        * lastIndexOf
        * includes
        * find
        * findIndex
        * filter
        * map
        * sort
        * reverse
        * split 
        * join
        * reduce
        * forEach
        * isArray
#   Destructuring
        * Destructuring assignment is a special syntax that allows us to “unpack” arrays or objects into a bunch of variables, as sometimes they are more convenient.
                1. Array destructuring
                        // destructuring assignment
                        let [firstName, surname] = arr;

                        alert(firstName); // Ilya
                        alert(surname);  // Kantor
                2. Object destructuring
                        We have an existing object at the right side, that we want to split into variables. The left side contains a “pattern” for corresponding properties. In the simple case, that’s a list of variable names in {...}.
                3.rest ‘…’
                        If we want not just to get first values, but also to gather all that follows – we can add one more parameter that gets “the rest” using three dots "...":
                
#   Map
       * Map is a collection of keyed data items, just like an Object. But the main difference is that Map allows keys of any type.
       * Unlike objects, keys are not converted to strings. Any type of key is possible.
       * Map can also use objects as keys.

#   Call vs Apply vs Bind
        * https://medium.com/@ivansifrim/the-differences-between-call-apply-bind-276724bb825b

#   Function expression vs function declaration
        * Function expression
                var x = function (a, b) {return a * b};

                After a function expression has been stored in a variable, the variable can be used as a function. Functions stored in variables do not need function names. They are always invoked (called) using the variable name.
        * Function declaration
                Function declarations load before any code is executed while Function expressions load only when the interpreter reaches that line of code.
                There are several different ways that function expressions become more useful than function declarations.
                       * As closures
                       * As arguments to other functions
                       * As Immediately Invoked Function Expressions (IIFE)

# Functions using new keyword
        * The major difference from other ways we’ve seen is that the function is created literally from a string, that is passed at run time.It is used in very specific       cases, like when we receive code from a server, or to dynamically compile a function from a template. The need for that usually arises at advanced stages of          development.
                let sum = new Function('a', 'b', 'return a + b');
                alert( sum(1, 2) ); // 3

#  Closures
#  IIFE
#  Currying
#  Memoization

        
        
        
