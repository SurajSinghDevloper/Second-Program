<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Measurement</title>
    <style>
        body {
            padding: 50px 100px;
        }

        h1 {
            text-align: center;
        }

        #container {
            text-align: center;
            background-color: aqua;
            padding: 50px;
        }

        .input {
            display: inline-block;

        }

        .inp {
            padding: 5px 100px;
            margin: 10px;
            font-size: 30px;
            font-weight: bold;
            width: 250px;
            text-align: center;
        }

        label {
            font-size: 30px;
            text-align: center;

        }
    </style>
</head>

<body>
    <h1>Temperature Converter</h1>
    <div id="container">
        <div class="input">
            <label>Celsius</label><br>
            <input type="number" value="0" id="cel" class="inp">
        </div>
        <div class="input">
            <label>Fahrenheit</label><br>
            <input type="number" value="32" id="fah" class="inp">
        </div>
    </div>
    <script>
        var cell = document.getElementById("cell");
        var fah = document.getElementById("fah");

        cel.addEventListener('input', function () {
            let c = this.value;
            let f = (c * 9 / 5) + 32;
            if (!Number.isInteger(f)) {
                f = f.toFixed(4);
            }
            fah.value = f;
        });

        fah.addEventListener('input', function () {
            let f = this.value;
            let c = (f - 32) * 5 / 9;
            if (!Number.isInteger(c)) {
                c = c.toFixed(4);
            }
            cel.value = c;
        });
    </script>
</body>

</html>
