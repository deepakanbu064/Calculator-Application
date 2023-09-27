<html>
    <head>
        <title>CALCULATOR</title>
        <style>
            input[type="button"] 
            {
                width: 50px;
                height: 50px;
                font-size: 20px;
            }
        </style>   
</head>
<body>
    <h1>Simple Calculator</h1>
    <table>
        <tr>
            <td colspan="4"><input type="text" id="result" ></td>
        </tr>
        <tr>
            <td><input type="button" value="1" onclick="deepak('1')"></td>
            <td><input type="button" value="2" onclick="deepak('2')"></td>
            <td><input type="button" value="3" onclick="deepak('3')"></td>
            <td><input type="button" value="/" onclick="deepak('/')"></td>
        </tr>
        <tr>
            <td><input type="button" value="4" onclick="deepak('4')"></td>
            <td><input type="button" value="5" onclick="deepak('5')"></td>
            <td><input type="button" value="6" onclick="deepak('6')"></td>
            <td><input type="button" value="*" onclick="deepak('*')"></td>
        </tr>
        <tr>
            <td><input type="button" value="7" onclick="deepak('7')"></td>
            <td><input type="button" value="8" onclick="deepak('8')"></td>
            <td><input type="button" value="9" onclick="deepak('9')"></td>
            <td><input type="button" value="-" onclick="deepak('-')"></td>
        </tr>
        <tr>
            <td><input type="button" value="C" onclick="cclear()"></td>
            <td><input type="button" value="0" onclick="deepak('0')"></td>
            <td><input type="button" value="=" onclick="calc()"></td>
            <td><input type="button" value="+" onclick="deepak('+')"></td>
        </tr>
    </table>
    
    <script>
        function deepak(value) 
        {
            document.getElementById('result').value += value;
        }

        function cclear() 
        {
            var x = document.getElementById('result');
            x.value='';
        }

        function calc() 
        {
            var result = eval(document.getElementById('result').value);
            if(isFinite(result))
                document.getElementById('result').value = result;
            else
                document.getElementById('result').value = 'Divide by zero error';
        }
    </script>
</body>
</html>
