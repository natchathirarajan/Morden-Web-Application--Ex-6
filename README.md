# Exp-6 Create a simple calculator built with React
## Aim:
To create react app to develop a complete Simple Calculator application with all features.
## Algorithm:
### Step 1:
Create react app by npm create-react-app.
### Step 2:
Make changes to App.js where the calculator works.
### Step 3:
Include Style in the react using app.css and import it to App.js.
### Step 4:
Verify the output by running the Web-Layout in any web browser. 
## Program:
### App.css
```css
.calculator {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 2rem;
}

.input,
.result {
  width: 300px;
  height: 50px;
  background-color: #f2f2f2;
  margin-bottom: 1rem;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  padding: 0 1rem;
  font-size: 1.5rem;
  font-weight: bold;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 0.5rem;
}

button {
  width: 70px;
  height: 50px;
  background-color: #e0e0e0;
  border: none;
  border-radius: 5px;
  font-size: 1.2rem;
  cursor: pointer;
}

button:hover {
  background-color: #d3d3d3;
}
```
### App.js
```js
import React, { useState } from 'react';
import './App.css';

const App = () => {
  const [input, setInput] = useState('');
  const [result, setResult] = useState('');

  const handleClick = (value) => {
    if (value === '=') {
      try {
        setResult(eval(input));
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
      <h1>Simple Calculator</h1>
      <div className="input">{input}</div>
      <div className="result">{result}</div>
      <div className="buttons">
        <button onClick={() => handleClick('7')}>7</button>
        <button onClick={() => handleClick('8')}>8</button>
        <button onClick={() => handleClick('9')}>9</button>
        <button onClick={() => handleClick('/')}>/</button>
        <button onClick={() => handleClick('4')}>4</button>
        <button onClick={() => handleClick('5')}>5</button>
        <button onClick={() => handleClick('6')}>6</button>
        <button onClick={() => handleClick('*')}>*</button>
        <button onClick={() => handleClick('1')}>1</button>
        <button onClick={() => handleClick('2')}>2</button>
        <button onClick={() => handleClick('3')}>3</button>
        <button onClick={() => handleClick('-')}>-</button>
        <button onClick={() => handleClick('0')}>0</button>
        <button onClick={() => handleClick('.')}>.</button>
        <button onClick={() => handleClick('=')}>=</button>
        <button onClick={() => handleClick('+')}>+</button>
        <button onClick={() => handleClick('C')}>C</button>
      </div>
    </div>
  );
};

export default App;
```
### index.css
```css
body {
  margin: 0;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen',
    'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans', 'Helvetica Neue',
    sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

code {
  font-family: source-code-pro, Menlo, Monaco, Consolas, 'Courier New',
    monospace;
}
```
### index.js
```js
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';
import reportWebVitals from './reportWebVitals';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);

// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals();
```
## Output:
![image](https://github.com/Karthikeyan21001828/MERN_EX06/assets/93427303/6622c1ac-8e9c-402c-bdd1-e7def6708c12)

## Result:
React app to develop a complete Simple calculator application with all features has been created and output has been verified.
