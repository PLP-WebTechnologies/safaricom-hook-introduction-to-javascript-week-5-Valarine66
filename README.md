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

3. **Functions**:
   - Create a function named `greetUser` that takes a name as a parameter and returns a greeting message. Display the message in an HTML element.  

---

#### **Part 2: JavaScript Control Structures**

4. **If Statements**:
   - Ask the user for their age using `prompt()`. Use an `if` statement to check if they are eligible to vote (age >= 18). Display a message indicating their eligibility in an HTML element.  

5. **Loops**:
   - Write a loop to display numbers from 1 to 10 on the webpage. Use an ordered list (`<ol>`) to present the numbers.  

---

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
    <title>Interactive Webpage</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
        }
        .box {
            padding: 20px;
            border: 1px solid #ccc;
            display: inline-block;
            margin-top: 20px;
        }
        button {
            margin: 10px;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1 id="title">JavaScript Interactive Webpage</h1>
    <button onclick="changeColor()">Change Text Color</button>
    
    <div class="box">
        <p>Counter: <span id="counter">0</span></p>
        <button onclick="incrementCounter()">Increase Count</button>
    </div>
    
    <div class="box">
        <p>Type something:</p>
        <input type="text" id="userInput" onkeyup="showMessage()">
        <p id="message"></p>
    </div>
    
    <script>
        function changeColor() {
            document.getElementById("title").style.color = "blue";
        }
        
        let count = 0;
        function incrementCounter() {
            count++;
            document.getElementById("counter").textContent = count;
        }
        
        function showMessage() {
            let input = document.getElementById("userInput").value;
            document.getElementById("message").textContent = "You typed: " + input;
        }
    </script>
</body>
</html>
