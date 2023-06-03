<html>
<head>
  <title>Calculator</title>
  <style>
    .container {
      width: 300px;
      margin: 0 auto;
      padding: 20px;
      border: 1px solid #ccc;
      border-radius: 5px;
      background-color: #f7f7f7;
    }

    input[type="text"] {
      width: 100%;
      padding: 10px;
      margin-bottom: 10px;
      font-size: 18px;
    }

    input[type="button"] {
      width: 48%;
      padding: 10px;
      margin-bottom: 10px;
      font-size: 18px;
    }

    .clear {
      background-color: #ff4136;
      color: #fff;
    }

    .equal {
      background-color: #0074d9;
      color: #fff;
    }
  </style>
</head>
<body>
  <div class="container">
    <input type="text" id="display" disabled>
    <input type="button" value="7" onclick="updateDisplay('7')">
    <input type="button" value="8" onclick="updateDisplay('8')">
    <input type="button" value="9" onclick="updateDisplay('9')">
    <input type="button" value="/" onclick="updateDisplay('/')">
    <input type="button" value="4" onclick="updateDisplay('4')">
    <input type="button" value="5" onclick="updateDisplay('5')">
    <input type="button" value="6" onclick="updateDisplay('6')">
    <input type="button" value="*" onclick="updateDisplay('*')">
    <input type="button" value="1" onclick="updateDisplay('1')">
    <input type="button" value="2" onclick="updateDisplay('2')">
    <input type="button" value="3" onclick="updateDisplay('3')">
    <input type="button" value="-" onclick="updateDisplay('-')">
    <input type="button" value="0" onclick="updateDisplay('0')">
    <input type="button" value="." onclick="updateDisplay('.')">
    <input type="button" value="=" onclick="calculate()">
    <input type="button" value="+" onclick="updateDisplay('+')">
    <input type="button" value="C" class="clear" onclick="clearDisplay()">
  </div>

  <script>
    function updateDisplay(value) {
      document.getElementById('display').value += value;
    }

    function calculate() {
      var expression = document.getElementById('display').value;
      var result = eval(expression);
      document.getElementById('display').value = result;
    }

    function clearDisplay() {
      document.getElementById('display').value = '';
    }
  </script>
</body>
</html>
