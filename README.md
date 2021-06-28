# 871865293.github.io

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>计算器实现</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }
        .title {
            padding: 10px;
            text-align: center;
            color: white;
            font-size:30px;
        }

        .xianshi {
            width: 290px;
            height: 50px;
            margin: 5px;
            font-size: 35px;
            padding: 5px;
            border: none;
            border-radius: 0.5em;
            text-align: right;
            background-color:#c7c4c4;
        }

        .main {
           
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translateX(-50%) translateY(-50%);
            background-color: white;
            border-radius: 0.5em;
        }

        html {
            background: linear-gradient(to right, #ff0052, #0072ff);
            height: 100%;
        }
        .button {
            width: 70px;
            height: 70px;
            font-size: 25px;
            margin: 2px;
            cursor: pointer;
            background:#dedddd;
            border: none;
            color: black;
            border-radius: 0.5em;
        }
        .gong {
            width: 70px;
            height: 70px;
            font-size: 25px;
            margin: 2px;
            cursor: pointer;
            background:#c4defe;
            border: none;
            color: #0e41f0;
            border-radius: 0.5em;
        }
        .deng {
            width: 70px;
            height: 70px;
            font-size: 25px;
            margin: 2px;
            cursor: pointer;
            border: none;
            color: white;
            border-radius: 0.5em;
            background-color: #0072ff;
        }
    </style>
    <script>
        let a = "1343.43245";
        let b = a.indexOf(".");
        console.log(b);
        let c = a.substring(0, b + 3);
        console.log(c);

        function insert(num) {
            document.form.xianshi.value = document.form.xianshi.value + num;
        }

        function equal() {
            let exp = document.form.xianshi.value;
            if (exp) {
                let eval1 = eval(document.form.xianshi.value);
                let number = eval1.toString().indexOf(".");
                document.form.xianshi.value = eval1;
            }
        }

        function Mclean() {
            document.form.xianshi.value = null;
        }

        function back() {
            let exp = document.form.xianshi.value;
            document.form.xianshi.value = exp.substring(0, exp.length - 1);
        }
    </script>
</head>
<body>
    <h1 class="title">
        19390241周伟豪
    </h1>
    <h2 class="title">
        <span>Welcome</span>
    </h2>
    <div class="main">
        <form name="form">
            <input class="xianshi" name="xianshi">
        </form>
        <table>
            <tr>
                <td><input type="button" class="gong" value="C" onclick="Mclean()"></td>
                <td><input type="button" class="gong" value="*" onclick="insert('*')"></td>
                <td><input type="button" class="gong" value="/" onclick="insert('/')"></td>
                <td><input type="button" class="gong" value="←" onclick="back()"></td>
            </tr>
            <tr>
                <td><input type="button" class="button" value="7" onclick="insert(7)"></td>
                <td><input type="button" class="button" value="8" onclick="insert(8)"></td>
                <td><input type="button" class="button" value="9" onclick="insert(9)"></td>
                <td><input type="button" class="gong" value="-" onclick="insert('-')"></td>
            </tr>
            <tr>
                <td><input type="button" class="button" value="4" onclick="insert(4)"></td>
                <td><input type="button" class="button" value="5" onclick="insert(5)"></td>
                <td><input type="button" class="button" value="6" onclick="insert(6)"></td>
                <td><input type="button" class="gong" value="+" onclick="insert('+')"></td>

            </tr>
            <tr>
                <td><input type="button" class="button" value="1" onclick="insert(1)"></td>
                <td><input type="button" class="button" value="2" onclick="insert(2)"></td>
                <td><input type="button" class="button" value="3" onclick="insert(3)"></td>
                <td rowspan="2" ><input style="height: 145px" type="button" class="deng" value="=" onclick="equal()"></td>

            </tr>
            <tr>
                <td colspan="2"><input style="width: 145px" type="button" class="button" value="0" onclick="insert(0)"></td>
                <td><input type="button" class="button" value="." onclick="insert('.')"></td>

            </tr>

        </table>
    </div>
</body>
</html>
