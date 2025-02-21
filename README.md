# Modern Calculator Web Application

Welcome to the **Calculator Web Application**! This is a sleek, responsive, and user-friendly calculator built using **HTML**, **CSS**, and **JavaScript**. Whether you're performing simple arithmetic or complex calculations, this calculator has got you covered. With a clean design, smooth animations, and support for all basic operations, it’s the perfect tool for quick calculations on the go.

---

## 📌 **Table of Contents**
1. [Introduction](#-introduction)
2. [Features](#-features)
3. [Requirements](#-requirements)
4. [Installation](#-installation)
5. [Usage](#-usage)
6. [Code Walkthrough](#-code-walkthrough)

---

## 🚀 **Introduction**

The **Calculator Web Application** is a lightweight yet powerful tool designed to perform basic arithmetic operations like addition, subtraction, multiplication, and division. It also supports advanced operations like percentage calculations and decimal inputs. The app is built with a responsive design, ensuring it works seamlessly on both desktop and mobile devices.

---

## ✨ **Features**

- **Basic Operations**: Perform addition, subtraction, multiplication, and division.
- **Advanced Operations**: Calculate percentages and use decimal points.
- **Clear Functionality**: Clear the input with a single click.
- **Backspace Functionality**: Remove the last entered digit or operator.
- **Responsive Design**: Works flawlessly on all screen sizes.
- **Smooth Animations**: Built with **Animate.css** for a polished user experience.
- **Modern Design**: Stylish buttons and layout powered by **Bootstrap**.

---

## 📋 **Requirements**

- A modern web browser (Chrome, Firefox, Safari, Edge, etc.).
- No additional installations are required—just open the app and start calculating!

---

## 🛠️ **Installation**

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/calculator.git
   cd calculator
   ```

2. **Open the Application**:
   - Open the `index.html` file in your browser:
     ```bash
     open index.html
     ```

---

## 🖥️ **Usage**

1. **Enter Numbers**: Click the number buttons (`0-9`) to input numbers.
2. **Perform Operations**: Use the operator buttons (`+`, `-`, `*`, `/`, `%`) to perform calculations.
3. **Clear Input**: Click the `C` button to clear the input field.
4. **Backspace**: Click the backspace button (`←`) to remove the last entered digit or operator.
5. **Calculate Result**: Click the `=` button to compute and display the result.

---

## 🧑‍💻 **Code Walkthrough**

### **HTML Structure**
The `index.html` file defines the structure of the calculator, including the input field and buttons.

```html
<calculator>
    <textbox>
        <input readonly type="text" class="input" id="number" placeholder="Calculate Here">
    </textbox>
    <buttons>
        <row>
            <button type="button" class="btn btn-dark" onclick="getnumber('7')">7</button>
            <button type="button" class="btn btn-dark" onclick="getnumber('8')">8</button>
            <button type="button" class="btn btn-dark" onclick="getnumber('9')">9</button>
            <button type="button" class="btn btn-success" onclick="Clear()">C</button>
        </row>
        <!-- Additional rows for buttons -->
    </buttons>
</calculator>
```

### **CSS Styling**
The `main.css` file provides the visual styling for the calculator, including layout, colors, and responsiveness.

```css
calculator {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-top: 2em;
    border: 0px;
    padding: 3em 1em;
    border-radius: 25px;
    row-gap: 3em;
    background-color: #dadada;
}
```

### **JavaScript Functionality**
The `main.js` file handles the logic for input, calculations, and display.

```javascript
function getnumber(num) {
    let result = document.getElementById("number");
    result.value += num;
}

function Clear() {
    let result = document.getElementById("number");
    result.value = "";
}

function Result() {
    let result = document.getElementById("number");
    result.value = eval(result.value);
}

function Back() {
    var str = document.getElementById('number').value;
    str = str.substr(0, str.length - 1);
    document.getElementById('number').value = str;
}
```

---
