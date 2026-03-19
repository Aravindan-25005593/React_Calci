# Ex04 Simple Calculator - React Project
## Date:18.3.26

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
Calci.jsx:
```
import React, { useState } from 'react';
import Display from './Display';
import Button from './Button';
import '../Calculator.css';

const Calculator = () => {
  const [input, setInput] = useState('');
  const [result, setResult] = useState('');

  const handleClick = (value) => {
    if (value === '=') {
      try {
        setResult(eval(input).toString());
      } catch (error) {
        setResult('Error');
      }
    } else if (value === 'C') {
      setInput('');
      setResult('');
    } else {
      setInput(input + value);
    }
  };

  return (
    <div className="calculator">
      <Display input={input} result={result} />
      <div className="buttons">
        <Button onClick={handleClick} value="7" />
        <Button onClick={handleClick} value="8" />
        <Button onClick={handleClick} value="9" />
        <Button onClick={handleClick} value="/" />
        <Button onClick={handleClick} value="4" />
        <Button onClick={handleClick} value="5" />
        <Button onClick={handleClick} value="6" />
        <Button onClick={handleClick} value="*" />
        <Button onClick={handleClick} value="1" />
        <Button onClick={handleClick} value="2" />
        <Button onClick={handleClick} value="3" />
        <Button onClick={handleClick} value="-" />
        <Button onClick={handleClick} value="0" />
        <Button onClick={handleClick} value="." />
        <Button onClick={handleClick} value="=" />
        <Button onClick={handleClick} value="+" />
        <Button onClick={handleClick} value="C" />
      </div>
    </div>
  );
};

export default Calculator;
```
Calci.css:
```
body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #f0f0f0;
  margin: 0;
  font-family: 'Arial', sans-serif;
}

.calculator {
  border: 2px solid #ccc;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  width: 320px;
}

.display {
  background-color: #222;
  color: #fff;
  font-size: 2.5em;
  padding: 20px;
  text-align: right;
  min-height: 40px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
}

button {
  border: 1px solid #ccc;
  font-size: 1.5em;
  padding: 20px;
  cursor: pointer;
  background-color: #fff;
  transition: background-color 0.2s;
}

button:hover {
  background-color: #ddd;
}

.operator {
  background-color: #f9a825;
  color: #fff;
}

.operator:hover {
  background-color: #f57f17;
}

.clear {
  background-color: #d32f2f;
  color: #fff;
  grid-column: span 2;
}

.clear:hover {
  background-color: #c62828;
}

.equal {
  background-color: #4caf50;
  color: #fff;
  grid-column: span 2;
}

.equal:hover {
  background-color: #43a047;
}
```

## OUTPUT
<img width="1919" height="1199" alt="image" src="https://github.com/user-attachments/assets/ddd69206-5112-4ccb-ad81-0412547ef1a3" />

<img width="1919" height="1199" alt="image" src="https://github.com/user-attachments/assets/f07f26c4-433e-4a53-9761-c6831dfcdb65" />

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
