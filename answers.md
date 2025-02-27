1. Challenge 1:
  - Answer: none > xyz, abc
  - Explanation: first it takes the function, which is why xyz is output, then the variable foo is output, but this was declared outside the function above
  - correct answer: As no new foo with let, const or var was declared in the bar() function, the function accesses the existing global variable foo and changes its value.

If a new local variable had been declared within the function (e.g. with let foo = “xyz”;), the second console.log would still have output “abc” because the global variable would have remained unchanged.


2. Challenge 2:
  - Answer: c 
  - Explanation: first the function is output which overwrites a with the number 10 and therefore outputs 10 first. then in the second console.log a is output which was initialized with 1 outside the function above
  - extended explanation: The decisive difference to Challenge 1:

In Challenge 1, no parameter variable is used, but the global variable is changed directly.

In Challenge 2, the parameter a is declared in the function definition function example(a). This creates a new local variable a within the function, which receives the value (not the reference) of the global variable. Changes to this local variable do not affect the global variable.

For primitive data types (such as numbers, strings), a value is passed in JavaScript (pass by value), not a reference. The global variable a therefore remains unchanged at 1.




3. Challenge 3:
  - Answer: c
  - Explanation: as the function is hoisted upwards, the function can already be executed beforehand and Hi there is output


4. Challenge 4:
  - Answer: a
  - Explanation: you cannot change a const, only add something, so an error would come out
- correct answer: a = { num: 100 } would not be allowed because it tries to change the reference
a.num = 90, on the other hand, is allowed because only the content of the object is changed

5. Bonus - Challenge 5:
  - Answer:
  - Explanation:
