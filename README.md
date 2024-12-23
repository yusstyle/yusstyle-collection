<!DOCTYPE html>
<html>
<head>  
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>calculator app</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
     
    <style>
    * {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  background-color: #ecf0f3;
  font-family: sans-serif;
  outline: none;
}

.container {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.calculator {
  background-color: yellow;
  padding: 15px;
  border-radius: 30px;
  box-shadow: inset 5px 5px 12px #ffffff, 5px 5px 12px rgba(0, 0, 0, .16);
  display: grid;
  grid-template-columns: repeat(4, 68px);
}

input {
  grid-column: span 4;
  height: 70px;
  widows: 260px;
  background-color: skyblue;
  box-shadow: inset -5px -5px 12px #ffffff, inset 5px 5px 12px rgba(0, 0, 0, .16);
  border: none;
  border-radius: 30px;
  color: rgb(70, 70, 70);
  font-size: 50px;
  text-align: end;
  margin-top: 40px;
  margin-bottom: 30px;
  padding: 20px;
}


button {
  height: 48px;
  width: 48px;
  background-color: red;
  box-shadow: -5px -5px 12px #ffffff, 5px 5px 12px rgba(0, 0, 0, .16);
  border: none;
  border-radius: 50%;
  margin: 8px;
  font-size: 16px;
  font-weight: bold;
}


.equal {
  width: 115px;
  border-radius: 40px;
  background-color: #ecf0f3;
  box-shadow: -5px -5px 12px #ffffff, 5px 5px 12px rgba(0, 0, 0, .16);
}
h1 {
   background-color:blue;
  padding: 15px;
  border-radius: 30px;
  box-shadow: inset 5px 5px 12px #ffffff, 5px 5px 12px rgba(0, 0, 0, .16);
  display: grid;
  grid-template-columns: repeat(4, 68px);
}
</style>
</head>
<h1>Yusstyle cal</h1>

  <div class="container">
    <div class="calculator">
      <input type="text" placeholder="" id="output-screen">
      <button onclick="clr()">CL</button>
      <button onclick="del()">DEL</button>
      <button onclick="display('%')">%</button>
      <button onclick="display('/')">/</button>
      <button onclick="display('7')">7</button>
      <button onclick="display('8')">8</button>
      <button onclick="display('9')">9</button>
      <button onclick="display('*')">*</button>
      <button onclick="display('4')">4</button> 
      <button onclick="display('5')">5</button>
      <button onclick="display('6')">6</button>
      <button onclick="display('-')">-</button>
      <button onclick="display('1')">1</button>
      <button onclick="display('2')">2</button>
      <button onclick="display('3')">3</button>
      <button onclick="display('+')">+</button>
      <button onclick="display('.')">.</button>
      <button onclick="display('0')">0</button>
      <button onclick="calculate()" class="equal">=</button>
    </div>
  </div>
 <script>
     let outputscreen = document.getElementById('output-screen');


function display(num) {
  outputscreen.value += num
}


function calculate() {
  try {
    outputscreen.value = eval(outputscreen.value)
  }
  catch (err) {
    alert("yusstyleCal do not receive invalid format")
  }
}

function clr() {
  outputscreen.value = ''
}

function del() {
  outputscreen.value = outputscreen.value.slice(0, -1)
}
 </script>
</body>


</html>