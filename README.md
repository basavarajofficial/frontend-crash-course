# frontend-crash-course
frontend crash course which includes html, css and javascript, will be helpful for beginners who wants to learn frontend web development.
---

---
marp: false
---

# Frontend crash course
# 1. Javascript : :
## 1.1 What is Javascript ?

  JavaScript is a programming language that is commonly used for creating dynamic and interactive web pages. It is a high-level, interpreted language, which means that it is executed directly by a web browser without the need for compilation.



### Some key features of JavaScript include:
---
 - Object-oriented programming: JavaScript is an object-oriented language, which means that it allows you to create and manipulate objects with properties and methods.

 - Event-driven programming: JavaScript is event-driven, which means that it allows you to respond to user actions (such as clicks or keystrokes) and other events (such as page loading or timer expiration).

 - Dynamically typed: JavaScript is dynamically typed, which means that variable types are determined at runtime, rather than being explicitly defined.

 - Prototypal inheritance: JavaScript uses prototypal inheritance, which allows objects to inherit properties and methods from other objects.

 ### Some common uses of JavaScript include :
---
 - Form validation: JavaScript can be used to validate user input in forms, ensuring that data is entered correctly before it is submitted.

 - User interface effects: JavaScript can be used to create dynamic effects on web pages, such as dropdown menus, animations, and slideshows.

 - Ajax: JavaScript can be used to create asynchronous web applications, allowing data to be sent and received without requiring a full page reload.

 - APIs: JavaScript can be used to interact with external APIs, allowing web applications to access and manipulate data from other sources.

 ### What is ECMAScript :
 ---
 - ECMAScript stands for European Computer Manufacturers Association Script. It is a scripting language specification standardized by ECMA International, a non-profit standards that develops and maintains standards for computing and communications technologies. The ECMAScript specification defines the syntax, semantics, and behavior of the JavaScript language, among others.

 

 ### ECMAScript Vs Javascript
 ---
 - Purpose and History: JavaScript was developed as a scripting language for web development, while Java was developed as a general-purpose programming language for a variety of applications.

 - Syntax: JavaScript syntax is based on C-style syntax, while Java syntax is more similar to C++. However, JavaScript is a loosely typed language, whereas Java is a strongly typed language.

 - Execution: JavaScript code is executed on a web browser or server, while Java code is executed on a Java Virtual Machine (JVM).

 - OOP: Java is a pure object-oriented language, whereas JavaScript is not. JavaScript can use object-oriented concepts, but it is also functional and can be used in a procedural programming style.

 - Libraries and frameworks: JavaScript has a wide variety of libraries and frameworks available for web development, such as React and Angular, while Java has a larger number of libraries and frameworks available for a variety of applications, such as Spring and Hibernate.

   ### *summary* : 
   > *JavaScript and Java are two different programming languages with distinct differences in their purpose, syntax, execution, object-oriented programming, and available libraries and frameworks.*
---



## 1.2 Javascript variables :
---
   Variables are containers for storing data (storing data values)

 - **let** : variables declared using *let* have **block scope**, which means they are only accessible within the block where they are defined.
   In other words, a variable declared using *let* can only be accessed within the **{}** block where it is defined. If you try to access the variable outside of its block, you will get a **ReferenceError**.

   Example :
     ```javascript
     if(true){
        let counter = 20;
     }
     console.log(counter);  // ReferenceError: counter is not defined
     ```
     ```javascript
     let a = 10;
     if(true){
        let a = 20;
        console.log(a);  // 20
     }
     console.log(a);  // 10
     ```

 -  **var** :  variables declared using *var* have **functional scope**, which means they can be accessible anywhere within the function. However, if a variable is defined outside of a function using *var*, it becomes a global variable and can be accessed from anywhere in the code. Variables declared using *var* can be reassigned, and if they are not assigned a value, they will have the value undefined.

    Example :
    ```javascript
    var x =10;
    if(true){
        var x = 20;
        console.log(x);
    }
    console.log(x);
    ```

 -  **const** :  -  *const* also has a **block scope**, but it cannot be reassigned after it has been declared. A const variable must be assigned a value when it is declared and cannot be left uninitialized.

      Example: 
      ```javascript
      const PI = 3.14;
      console.log(PI); // Output: 3.14

      PI = 3.1415; // This will result in an error
      ```

      ### Javascript Data Types :
      ---
      In Javascript mainly there are two types They are :
      - Primitive data type
      - Object/Non-primitive data type

  
      In JavaScript, a primitive data type is a data type that represents a single, immutable value, which means that the value cannot be changed. 
      
      #### Primitive Data Types :
      ---
      - There are five primitive data types in JavaScript : 
          * string 
          - number
          - boolean
          - null
          - undefined
          - BigInt
          - symbol
  

      
   + String : A sequence of characters enclosed in quotes (single or double)
      ```javascript
      let name = "John" ;
      let country = 'India';
      ```
      
   + number : A numeric value, Numbers in JavaScript are always stored as floating-point numbers.
      ```javascript
      let age = 25 ;
      ```
   
   + Boolean : A logical value that can be either true or false. 
      ```javascript
      let isStudent = true; 
      ```

   + null : A special value indicating a null or non-existent value.
      ```javascript
      let value = null;
      ```
      *NOTE : All primitive types, except null, can be tested by the typeof operator. typeof null returns "object", so one has to use === null to test for null.*

      Example :
      ```javascript
      function checkValue(str){
         let a = str;
         if(a === null){
            return 0;
         }
         return a.length;
      }
      console.log(checkValue(null));
      ```

   + undefined :  The Undefined type is inhabited by exactly one value: **undefined**.
      - Conceptually, *undefined* indicates the absence of a value, while *null* indicates the absence of an object (which could also make up an excuse for typeof null === "object"). The language usually defaults to undefined when something is devoid of a value:
  
      Example:
      + A return statement with no value (return;) implicitly returns *undefined*.
         ```javascript
         function checkValue(num){
            let a =10;
            if(a === num){
               return; // if a === num will return #undefined
               }
            return num;
            }
         console.log(checkValue(10));
         ```

      + Accessing a nonexistent object property (obj.iDontExist) returns *undefined*.
         ```javascript
         let myObject = {
            name : "John",
            age : 30
         }
         console.log(myObject.city)  // undefined, because city property is not exist in the object.

         ```
      + A variable declaration without initialization (let x;) implicitly initializes the variable to undefined.
         ```
         let x;
         console.log(x) // undefined because x variable is declared but not defined yet.
         ```
   + BigInt : All JavaScript numbers are stored in a a 64-bit floating-point format.

     - JavaScript BigInt is a new datatype (2020) that can be used to store integer values that are too big to be represented by a normal JavaScript Number.   
  
      Example :
      ```
      let x = BigInt("123456789012345678901234567890");
      ```


      #### Differenece between undefined and null : 
      ---
         typeof null; // "object" (not "null" for legacy   reasons)
         typeof undefined; // "undefined"
         null === undefined; // false
         null == undefined; // true
         null === null; // true
         null == null; // true
         !null; // true
         Number.isNaN(1 + null); // false
         Number.isNaN(1 + undefined); // true
      


      #### Object/Non-primitive Data Types :
      ---
      - There are mainly three types :
          + object
          + array
          + date

   - Object : The Object type represents one of JavaScript's data types. It is used to store various keyed collections and more complex entities. Objects can be created using the Object() constructor or the object initializer / literal syntax.

     * Example

     ```javascript
      let car = {
         name: "fiat",
         model: 500,
         weight: "850kg",
         color : "white",
         start: function() {
            console.log(`Hello,I am  ${this.name} and I am  ${this.model} model, I can start now`);
            }
         };

         //using dot(.) notation
         console.log(car.name); // "fiat"

         //using bracket notation
         console.log(car["model"]); // 500 

         console.log(car.color); // "white"

         // car object with start method
         car.start(); //  Hello,I am  fiat and I am  500 model, I can start now.
     ```
     
      ![object Image](./images/object.jpeg)


   * array : In JavaScript, an array is a collection of items or values, which can be of any data type such as numbers, strings, objects, or even other arrays. Arrays in JavaScript are defined as objects with numbered indexes, where each item or element is identified by an index, starting from zero.

   > JavaScript arrays can be created using the Array()  constructor or by using the array literal notation, which is simply a comma-separated list of values enclosed in square brackets ([]). 

   

