<!DOCTYPE html>
<html>
<head>
    <title>Simple Calculator</title>
    <style>
        body {
            font-family: Arial;
            background-color: #f2f2f2;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .calculator {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px gray;
        }
        input {
            width: 100%;
            height: 40px;
            font-size: 18px;
            margin-bottom: 10px;
            text-align: right;
        }
        button {
            width: 60px;
            height: 40px;
            font-size: 18px;
            margin: 5px;
        }
    </style>
</head>

<body>
    <div class="calculator">
        <input type="text" id="result" disabled>

        <div>
            <button onclick="clearResult()">C</button>
            <button onclick="appendValue('/')">/</button>
            <button onclick="appendValue('*')">*</button>
            <button onclick="appendValue('-')">-</button>
        </div>

        <div>
            <button onclick="appendValue('7')">7</button>
            <button onclick="appendValue('8')">8</button>
            <button onclick="appendValue('9')">9</button>
            <button onclick="appendValue('+')">+</button>
        </div>

        <div>
            <button onclick="appendValue('4')">4</button>
            <button onclick="appendValue('5')">5</button>
            <button onclick="appendValue('6')">6</button>
            <button onclick="calculate()">=</button>
        </div>

        <div>
            <button onclick="appendValue('1')">1</button>
            <button onclick="appendValue('2')">2</button>
            <button onclick="appendValue('3')">3</button>
            <button onclick="appendValue('0')">0</button>
        </div>
    </div>

    <script>
        function appendValue(value) {
            document.getElementById("result").value += value;
        }

        function clearResult() {
            document.getElementById("result").value = "";
        }

        function calculate() {
            let res = document.getElementById("result").value;
            document.getElementById("result").value = eval(res);
        }
    </script>
</body>
</html>
# Simple-Calculator
Simple Calculator mini project
