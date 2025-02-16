### **Assignment: Exploring JavaScript Fundamentals and DOM Manipulation** 🌟

---

#### **Objective:**
This assignment aims to test your understanding of JavaScript basics, control structures, and the Document Object Model (DOM). You will demonstrate your skills by creating an interactive webpage that uses variables, data types, operators, control structures, and DOM manipulation.

---

### **Instructions:**

1. **Create a new HTML file** and include an external JavaScript file for your script.  
2. Name your HTML file as `assignment.html` and your JavaScript file as `script.js`.  
3. Follow the tasks below and ensure you structure your code for readability with proper comments.  

---

### **Tasks:**

#### **Part 1: JavaScript Basics**



1. **Variables and Data Types**:
   - Declare variables of different types: string, number, boolean, array, and object.  
   - Use `console.log()` to print their values and types in the browser console.  

   **Example Output**:  
   ```
   Name: John Doe (Type: string)  
   Age: 25 (Type: number)  
   Is student: true (Type: boolean)  
   ```
 

This webpage includes interactive elements:

1. **Change text color** – Clicking a button changes the heading color.
2. **Counter functionality** – A button increments a counter.
3. **Live input feedback** – Typing in an input field updates a message dynamically.

### Variables and Data Types:
   - Declare variables of different types: string, number, boolean, array, and object.  
   - Use `console.log()` to print their values and types in the browser console.  

```javascript

let name = "John Doe";
let age = 25;
let isStudent = true;
let myArray = [1, 2, 3, 4, 5];
let myObject = { name: "Alice", age: 25 };

console.log("Name:", name, "(Type:", typeof name + ")");
console.log("Age:", age, "(Type:", typeof age + ")");
console.log("Is student:", isStudent, "(Type:", typeof isStudent + ")");
console.log("Array:", myArray, "(Type:", typeof myArray + ")");
console.log("Object:", myObject, "(Type:", typeof myObject + ")");
```

**Example Output**:  
```
Name: John Doe (Type: string)  
Age: 25 (Type: number)  
Is student: true (Type: boolean)  
```

Would you like to add more features or enhance the design? 🚀

2. **Operators**:
   - Write a simple calculator function that performs addition, subtraction, multiplication, and division using two numbers provided by the user (use `prompt()` for input).  
   - Use arithmetic and comparison operators to validate user input and display appropriate messages.

   **Example Output**:  
   ```
   Enter the first number: 10  
   Enter the second number: 2  
   Choose an operation (+, -, *, /): *  
   Result: 20
   ```

   function calculator() {
    let num1 = parseFloat(prompt("Enter the first number:"));
    let num2 = parseFloat(prompt("Enter the second number:"));
    let operator = prompt("Choose an operation (+, -, *, /):");

    if (isNaN(num1) || isNaN(num2)) {
        console.log("Invalid input! Please enter valid numbers.");
        return;
    }

    let result;
    switch (operator) {
        case "+":
            result = num


3. **Functions**:
   - Create a function named `greetUser` that takes a name as a parameter and returns a greeting message. Display the message in an HTML element.  

---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Greeting App</title>
</head>
<body>
    <h2>Enter Your Name</h2>
    <input type="text" id="nameInput" placeholder="Type your name">
    <button onclick="displayGreeting()">Greet</button>
    <div id="greeting"></div>

    <script>
        function greetUser(name) {
            return `Hello, ${name}! Welcome to our website.`;
        }

        function displayGreeting() {
            let name = document.getElementById("nameInput").value;
            if (name.trim() === "") {
                document.getElementById("greeting").innerText = "Please enter a valid name.";
            } else {
                document.getElementById("greeting").innerText = greetUser(name);
            }
        }
    </script>
</body>
</html>


#### **Part 2: JavaScript Control Structures**

4. **If Statements**:
   - Ask the user for their age using `prompt()`. Use an `if` statement to check if they are eligible to vote (age >= 18). Display a message indicating their eligibility in an HTML element.  

5. **Loops**:
   - Write a loop to display numbers from 1 to 10 on the webpage. Use an ordered list (`<ol>`) to present the numbers.  

---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript If Statements & Loops</title>
</head>
<body>

    <h2>Check Voting Eligibility</h2>
    <button onclick="checkVotingEligibility()">Check Eligibility</button>
    <div id="votingMessage"></div>

    <h2>Numbers from 1 to 10</h2>
    <ol id="numberList"></ol>

    <script>
        function checkVotingEligibility() {
            let age = prompt("Enter your age:");
            age = Number(age); // Convert input to a number

            if (isNaN(age) || age <= 0) {
                document.getElementById("votingMessage").innerText = "Please enter a valid age.";
            } else if (age >= 18) {
                document.getElementById("votingMessage").innerText = "You are eligible to vote.";
            } else {
                document.getElementById("votingMessage").innerText = "You are not eligible to vote yet.";
            }
        }

        function displayNumbers() {
            let numberList = document.getElementById("numberList");
            for (let i = 1; i <= 10; i++) {
                let listItem = document.createElement("li");
                listItem.innerText = i;
                numberList.appendChild(listItem);
            }
        }

        displayNumbers();
    </script>

</body>
</html>


#### **Part 3: Introduction to the DOM**

6. **Creating HTML Structure**:
   - Add the following HTML elements to your webpage:
     - A heading (`<h1>`) with the text **"JavaScript Assignment"**.  
     - A paragraph (`<p>`) with the text **"Learning JavaScript is fun!"**.  
     - A `<div>` with an `id` of `dynamic-content`.  

7. **Selecting and Modifying HTML Elements**:
   - Use JavaScript to:
     - Change the text of the `<h1>` element to **"JavaScript in Action!"**.  
     - Add a new `<p>` inside the `dynamic-content` `<div>` with the text **"This content was added dynamically using JavaScript."**.  

---

### **Tips for Success:**

- Test your code frequently to catch errors early.  
- Use meaningful variable names and add comments to explain your logic.  
- Have fun and get creative!  

Happy Coding! 💻✨  
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript DOM Manipulation</title>
</head>
<body>

   
    <h1 id="main-heading">JavaScript Assignment</h1>
    <p>Learning JavaScript is fun!</p>
    <div id="dynamic-content"></div>

    <script>
      
        document.getElementById("main-heading").innerText = "JavaScript in Action!";

       <div>
        let newParagraph = document.createElement("p");
        newParagraph.innerText = "This content was added dynamically using JavaScript.";
        document.getElementById("dynamic-content").appendChild(newParagraph);
    </script>

</body>
</html>


