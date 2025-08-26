# Aim
To design and develop a Simple Calculator using HTML, CSS, and JavaScript that can perform basic arithmetic operations (Addition, Subtraction, Multiplication, and Division) based on user input.

# Procedure
### Create the HTML Structure:
Add two input fields for entering numbers.
Add a dropdown list  to choose the operation (Add, Subtract, Multiply, Divide).
Add a button to perform the calculation.
### Style the Calculator with CSS:
Use basic CSS for layout, background color, button styling, and text alignment.

### Write JavaScript for Logic:

Fetch values from the input fields.
Read the selected operation from the dropdown.
Perform the calculation using a switch statement.
Display the result in the result area.
# Program :

index.html:

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simple Calculator</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="calculator">
    <h2>Simple Calculator</h2>
    <input type="number" id="num1" placeholder="Enter first number">
    <input type="number" id="num2" placeholder="Enter second number">

    <select id="operation">
      <option value="add">Add</option>
      <option value="subtract">Subtract</option>
      <option value="multiply">Multiply</option>
      <option value="divide">Divide</option>
    </select>

    <button onclick="calculate()">Calculate</button>

    <div class="result" id="result"></div>
  </div>

  <script src="script.js"></script>
</body>
</html>

```

style.css

```

body {
  font-family: Arial, sans-serif;
  background: #f4f4f4;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.calculator {
  background: #fff;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  text-align: center;
  width: 300px;
}

input, select, button {
  width: 90%;
  padding: 10px;
  margin: 10px 0;
  font-size: 16px;
  border-radius: 5px;
  border: 1px solid #ccc;
}

button {
  background-color: #007BFF;
  color: white;
  cursor: pointer;
  border: none;
}

button:hover {
  background-color: #0056b3;
}

.result {
  margin-top: 15px;
  font-size: 18px;
  font-weight: bold;
  color: #333;
}

```

script.js

```
function calculate() {
  const num1 = parseFloat(document.getElementById('num1').value);
  const num2 = parseFloat(document.getElementById('num2').value);
  const operation = document.getElementById('operation').value;
  const resultDiv = document.getElementById('result');

  if (isNaN(num1) || isNaN(num2)) {
    resultDiv.textContent = "Please enter valid numbers.";
    return;
  }

  let result;
  switch (operation) {
    case 'add':
      result = num1 + num2;
      break;
    case 'subtract':
      result = num1 - num2;
      break;
    case 'multiply':
      result = num1 * num2;
      break;
    case 'divide':
      if (num2 === 0) {
        resultDiv.textContent = "Cannot divide by zero.";
        return;
      }
      result = num1 / num2;
      break;
  }

  resultDiv.textContent = `Result: ${result}`;
}

```

# Output:

<img width="443" height="495" alt="Screenshot 2025-08-26 192335" src="https://github.com/user-attachments/assets/c3966566-356f-406f-ae6f-9149e3a99e05" />



<img width="433" height="521" alt="Screenshot 2025-08-26 192322" src="https://github.com/user-attachments/assets/8fc648bb-fcb0-4001-b500-8af5bee8cbe7" />



# Result:
The web page displays a Simple Calculator that allows the user to:Enter two numbers.Select an arithmetic operation.Click the Calculate button to display the result.
The calculator successfully performs Addition, Subtraction, Multiplication, and Division, and displays appropriate error messages for invalid inputs
