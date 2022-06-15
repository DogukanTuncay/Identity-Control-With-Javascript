# Identity-Control-With-Javascript
### I USED TURKISH ID NUMBERS.
---
## Turkish ID Rules:
 *  ID cant start with 0 
 *  ID Must consist 11 numbers 
 *  Actually, Turkish id occurs to 9 numbers. 10. and 11 number is for verify.

 So, How? For example:
 
 My ID is : 44632337462
 
  ## my 10. number is 6, why?
  on my first 9 numbers:
  1. =4
  2. =4
  3. =6
  4. =3
  5. =2
  6. =3
  7. =3
  8. =7
  9. =4
   ---
  my odd and even numbers  is seperate.
  My odd numbers = 1. 3. 5. 7. 9. so:
   
  my 1. number =4
  
  my 3. number =6
  
  my 5. number =2
  
  my 7. number =3
  
  my 9. number =4
  
  ---
  
  My even numbers = 2. 4. 6. 8. so:
  
  my 2. number =4
  
  my 4. number =3
  
  my 6. number =3
  
  my 8. number =7
  
  ---
  
  My (sum of odd numbers *7 - sum of even numbers) % (mod) 10 = my 10. ID Number.
  
  My sum of odd numbers:
  
  4 + 6 + 2 + 3 + 4 = 19
  
  odd numbers *7:
  
  19 * 7 = 133
  
  sum of even numbers:
  
  4 + 3 + 3 + 7 = 17
  
  ---
  
  (odd numbers*7) - even numbers:
  
  133 - 17 = 116 --> this is result
  
  result %10 = 6 --> this is my 10. ID number. TRUE
  
  ---

  ## and my 11. number is 2, why? :
   
  Sum My first 10 numbers % 10 = My 11. ID number.
   
  sum of my first 10 numbers:
   
  4 + 4 + 6 + 3 + 2 + 3 + 3 + 7 + 4 + 6= 42
   
  42 % 10 = 2 --> This is my 11. ID number. TRUE
  # On Code:  
  ### My Variables:
  `
  var identity=document.querySelector('#tc'), // I reach to my input because the user's ID is here.
  resultTrue=document.querySelector('#resultTrue'), // I reach to my true paragraph because result can be true .
  resultFalse=document.querySelector('#resultFalse'), // I reach to my false paragraph because result can be false.
  btnControl=document.querySelector('#btn'), // I reach to my button because my javascript is working with onclick to button.
  odd=0, // My odd numbers
  even=0, // My even numbers
  number10Result=0, 
  number11Result=0;
 `
 ### My 10. and 11. numbers:
 
` btnControl.addEventListener('click',function()
 {

 for(var i=0;i<9;i++){ // On this loop I reach to sum of input value's first 9 numbers. ( odd and even)
  
 if(i%2==0){
  
    odd+=Number(identity.value[i]); // ARRAY IS START FROM 0 . DONT FORGET! so my first number is odd but it is my 0. value so even value.
     }
 else{
  
    even+=Number(identity.value[i]);
    
    }
    
 odd*=7;

 for(var j=0;j<10;j++){
  
    number11Result+=Number(identity.value[j]); // I reach to  sum of my value's first 10 numbers. 
     
    }
 `
