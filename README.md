# Js-Interview-Questions 

var has  function scope or globl scope 

- we can redelclare it as many times as we want.
- value can be reassigned many times.

      var a = 50;

      var a =  20;

      console.log(a);                  // ans= 20;
  var a = 50;
{
      var a =  20;
}
      console.log(a);                    o/p = 20

let has block scope

- we  can accesse it only within that specific block.
- can't redeclare it but can be reassigned.

        {
          let a = 5;
         }
      console.log(a);                    // error (a is not defined)

   let a=5;   // having scope outside below scope
        {
           let a = 10;   // only have block scope
            console.log(a);     
        }
     

const has also block

- declare it only one time and we can not change the value of const variable
- reassignment and redelclare not allowed.

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



         


      
### Functions in JS :

- function expression
- function statement
- function declaration
- Anonymous function
- Arrow Function ()=>{}
- first class function:
