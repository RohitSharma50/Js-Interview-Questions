# Js-Interview-Questions  


## var has  function scope or globl scope 

- we can redelclare it as many times as we want.
- value can be reassigned many times.
- we can use it before declaring var

  
      var a = 50;
      var a =  20;
      console.log(b);            // ans= undefined
      var b=87;
      console.log(a);                  // ans= 20;
      var a = 50;{
      var a =  20;
         }
      console.log(a);                    o/p = 20

      var globalVar = 77;
      function scopeTest() {
        var localVar = 88;
       }

      console.log(localVar);           // ReferenceError: localVar is not defined (it have block scope only)





  ## let has block scope

- we  can accesse it only within that specific block.
- can't redeclare it but can be reassigned.
- we can't use let and const before declaring it like var

      {
          let a = 5;
         }
      console.log(a);                    // error (a is not defined)

      let a=5;   // having scope outside below scope
        {
           let a = 10;   // only have block scope
            console.log(a);     
        }
     

  ### const has also block

- declare it only one time and we can not change the value of const variable
- reassignment and redelclare not allowed.
- Variables declared with const must be assigned during declaration.
  
      const a = 25;
            a = 50;                                 //error
      console.log(a); 
    
       const x = 10;
      {
        const x = 5;
        console.log(a);                          // o/p=>5   only block scope
      }
         console.log(a);                       // o/p=>10      outside block scope

### Truthy & Falsy values:
All values are truthy except 0, false, -0, 0n, "", null, undefined, NaN,{},Infinity,-Infinity are falsy values.
JavaScript uses type coercion in Boolean contexts.

**Type coercion is the automatic or implicit conversion of values from one data type to another (such as strings to numbers)**

               console.log(false);                            o/p=> false 
               console.log(+false);                           o/p=> 0         // we uses + to convert data type into a number 
         
               console.log(false == []);                      o/p=> true  
               console.log(false == ![]);                     o/p=> true
                read below for Explanation ⬇️

### In first case
== convert [](i.e empty array) into empty string(""), now it look like (false == "") due difference in data types == convert them into numbers then it look like 0==0 so this return true.

### second case 
here [](empty array) is a truthy value as according to above rules and after negating it it return false it look like this false==false so this return 0.



         


      
## Functions in JS :  
### What is the difference between an expression and a statement in JavaScript?
       Expression: produces a value
       Statement: performs an action
       Expression statement: produces a value and performs an action
       you can print it or assign it to a variable, it’s an expression. If you can’t, it’s a statement.
function decelaration and expression are same but the difference is function expression are assigned to a variable.
There are many more concepts and ideas in functional programming.
Here are some of the most important ones:

- First-class functions
      these are simple values that can be
  
      - pass to other functions 
      - save in a variable
      - return from other
- Higher-order function
  
    is a function that has either one or both of the following characteristics:
  
            It accepts other functions as arguments
            It returns functions when invoked

- Pure functions and side-effects

      A pure function returns the exact same result as long as it's given the same values.
      An example of a pure function is the addTwoNums(), this function return the same output as long as the input is same.
  

- Anonymous function
 
      A function having no name is called anonymouse function it can be assigned to a variable and can be pass as callback
      const square = function (num){
       return num*num; }
- Arrow Function ()=>{}
- first class function
     a function that can be treated like variable are called first class functions. these can be return manipulated and can do anythis that an variable can do.

       const square = function (num){
       return num*num;
       }
       const display(fn){
       console.log(fn(5));
       }
      display(square);    // 25
 - What is IIFE?


 ## ways to center align a img in a div
     - Flexbox
     - Grid css
     - table css
     - position css
     - margin css 

## find the output 
     function f(a,b,c){
    m=["1","2","3"];
    a=3;
    b[0]="x";
    c.first=false;
    } 
     var x=4;
    var y=["A","b","c"];
    var z={first:true}; 

    f(x,y,z);
    console.log(x,y,z);                         // 4 [ 'x', 'b', 'c' ] { first: false }


  here in above example x is immutable so it is pass by value its value get copied into a and in change in a it wouldn't affect the value at x;
  and in case of y and z values are pass by reference so any change in b and c will affect the values present in y and z.

 ## here are some baseic data types in js and all basic data types are immutable the are only pass by values (used in abole case)
                       
                number, string, BigIn, Null, Undefined, Boolean,Symbol. almost everything start with New keyword are all mutable. 
  ## What is CSS BEM? 
                        
                        BEM stands for Block Element Modifier which is an explanation for its structure.
                          /* block component */
            .block {
                     }

                 /* element */
             .block__element {
                                     }
                       /* modifier */
                              .block__element--modifier {
                                    }
   ## What is the difference between the equality operators == and ===?
      Triple equals (===) checks for strict equality, which means both the type and value must be the same. Double equals (==) on the other 
      hand first performs type coercion so that both operands are of 
                 the same type and then applies strict comparison.
  ## What is the difference between an element and a component in React?
         
           Elements are immutable, plain objects that describe the DOM nodes or components you want to render.
          Components can be either classes or functions, that take props as an input and return an element tree as the output.
                                  const Component = () => "Hello"
                                  const componentElement = <Component />
                                     const domNodeElement = <div />
## What is the difference between em and rem units?
            em units inherit their value from the font-size of the parent element
            rem units inherit their value from the font-size of the root element (html)

 ## out based Question 
            let a=[]; 
            let b=[];
            console.log(a==b); 
            console.log(a===b); 
                 
                           //if empty array is compared then it compare their memory location  
                          //so here two arrays can't have same memory location so it return false
### console.log(typeof NaN);              
                         // Number
  ## let a=[1,2,3,4];
  console.log(...a);
                        
                          // 1 2 3 4 (... destructure the array its element came out of array)
## an object is not iterable. For example: 

        const car = {
    speed: 100,
    color: "blue"
      }

            for(prop of car) {
           console.log(prop)
           }                                //TypeError: car is not iterable

## Template literals (Template strings)

      Template literals are literals delimited with backtick (`) characters, allowing for multi-line strings, string interpolation with embedded expressions, and special constructs called tagged templates.

      `string text ${expression} string text`
      Template literals are sometimes informally called template strings, because they are used most commonly for string interpolation (to create strings by doing substitution of placeholders).
      Template Strings allow both single and double quotes inside a string:
      Template Strings allow multiline strings:

### Spread Operator 
          The advantage of this approach is that you don't have to list each individual member of the array that you want to pass to your function. 
          you can do simpely like 
           a[5]=[1,2,3,4,5];
           f(...a)  // passing an array to a function 
     
### next 
