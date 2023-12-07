# Js-Interview-Questions 

var has  function scope or globl scope 

- we can redelclare it as many times as we want.
- value can be reassigned many times.

      var a = 50;

      var a =  20;

      console.log(a); // ans= 20;
  var a = 50;
{
      var a =  20;
}
      console.log(a);             o/p = 20

let has block scope

- we  can accesse it only within that specific block.
- can't redeclare it but can be reassigned.

        {
          let a = 5;
         }
      console.log(a);           // error (a is not defined)

   let a=5;   // having scope outside below scope
        {
           let a = 10;   // only have block scope
            console.log(a);     
        }
     

const has also block

- declare it only one time and we can not change the value of const variable
- reassignment and redelclare not allowed.

      const a = 25;
            a = 50;                //error
      console.log(a); 
    
       const x = 10;
      {
        const x = 5;
        console.log(a);   // o/p--5   only block scope
      }
         console.log(a);   // o/p--10      outside block scope
      
