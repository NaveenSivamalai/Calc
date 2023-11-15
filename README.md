# Ex.08 Design of a Standard Calculator
## Date: 10/11/2023

## AIM:
To design a web application for a standard calculator with minimum five operations.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for creating attractive colors.

### Step 4:
Write JavaScript program for implementing five different operations.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
calc.html

<html>
<head>
    <title>Simple Calculator</title>
    <link rel="stylesheet" href="calc.css">
    <script src="calc.js"></script>
</head>
<body>
    <div id="calculator-container">
        <h1>Calculator</h1>
        <input type="text" id="display" readonly>
        <table>
            <tr>
                <td><button onclick="appendToDisplay('1')">1</button></td>
                <td><button onclick="appendToDisplay('2')">2</button></td>
                <td><button onclick="appendToDisplay('3')">3</button></td>
                <td><button data-operator="+" onclick="appendToDisplay('+')" style="color: white;">+</button></td>
            </tr>
            <tr>
                <td><button onclick="appendToDisplay('4')">4</button></td>
                <td><button onclick="appendToDisplay('5')">5</button></td>
                <td><button onclick="appendToDisplay('6')">6</button></td>
                <td><button data-operator="-" onclick="appendToDisplay('-')" style="color: white;">-</button></td>
            </tr>
            <tr>
                <td><button onclick="appendToDisplay('7')">7</button></td>
                <td><button onclick="appendToDisplay('8')">8</button></td>
                <td><button onclick="appendToDisplay('9')">9</button></td>
                <td><button data-operator="*" onclick="appendToDisplay('*')" style="color: white;">*</button></td>
            </tr>
            <tr>
                <td><button onclick="appendToDisplay('0')">0</button></td>
                <td><button data-operator="%" onclick="appendToDisplay('%')">%</button></td>
                <td><button data-operator="." onclick="appendToDisplay()">.</button></td>
                <td><button data-operator="/" onclick="appendToDisplay('/')" style="color: white;">/</button></td>
            </tr>
            <tr>
                <td colspan="3"><button onclick="clearDisplay()">C</button></td>
                <td><button onclick="calculateResult()">=</button></td>
            </tr>
        </table>
    </div>
</body>
</html>

calc.css

body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}

#calculator-container {
    background-color: gray;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(199, 20, 20, 0.2);
}

input[type="text"] {
    width: 100%;
    padding: 10px;
    margin: 5px 0;
    color: rgb(6, 96, 126); 
}

table {
    margin-top: 10px;
}

button {
    padding: 10px 20px;
    font-size: 20px;
}

/* Define colors for operators */
button[data-operator="+"] {
    background-color: black;
}

button[data-operator="-"] {
    background-color: black;
}

button[data-operator="*"] {
    background-color: black;
}

button[data-operator="/"] {
    background-color: black;
    padding: 10px 25px;
}

button[data-operator="%"] {
    background-color: black;
    color: aqua;
}

button[data-operator="."] {
    background-color: black;
    color: aqua;
}

calc.js 

function appendToDisplay(value) {
    document.getElementById('display').value += value;
}

function clearDisplay() {
    document.getElementById('display').value = '';
}

function calculateResult() {
    try {
        document.getElementById('display').value = eval(document.getElementById('display').value);
    } catch (error) {
        document.getElementById('display').value = 'Error';
    }
}

function calculateSquareRoot() {
    const inputValue = document.getElementById('display').value;
    const result = Math.sqrt(parseFloat(inputValue));
    document.getElementById('display').value = result;
}


```

## OUTPUT:

![image](https://github.com/Mithunlavanyaraj/Calc/assets/120077786/306fbe14-3eb8-4f0c-9014-8f7ca1b463c5)
![image](https://github.com/Mithunlavanyaraj/Calc/assets/120077786/1ed2c201-607f-4767-ae88-6df8919bdc7b)


## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
