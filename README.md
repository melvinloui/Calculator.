# Calculator.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Scientific  Calculator</title>
</head>
<style type="text/css">
    body{
        margin: 0;
        padding: 0;
        background: radial-gradient(#1e8fa5, #08506b,black)no-repeat fixed;
    }
    button.clear{
        background: #FF5772;
        color: #fff;
    }
    table{
        background: black;
        padding: 7px 5px;
        border: 6px solid black;
        text-align: center;
        padding-bottom: 0px;
        box-shadow: 0px 0px 27px #0d5569;
        border-radius: 10px;
        margin-top: 90px;
    }
    button.equal{
        width: 88%;
        background: #210b04;
    }
    button.equal:hover{
        background: 000803;
    }
    input[type="text"]{
        width: 450px;
        height: 81px;
        border: 1px solid #000;
        padding: 10px 20px;
        font-size: 29px;
        background: black;
        font-weight: bold;
        margin-bottom: 25px;
        font-family: cursive;
        margin-top: #dedede;
        border-bottom: 2px solid #cc4014;
        color: #dedede;
    }
    button{
        padding: 10px 20px;
        width: 100px;
        height: 60px;
        margin-bottom: 20px;
        font-size: 26px;
        font-weight: bold;
        font-family: cursive;
        background: #000803;
        border: none;
        color: #d23200;

        border-radius: 6px;
        cursor: pointer;
    }
    button:hover{
        background: #210b04;
    }


</style>
<body>

    <form action="calculator">
        <table align="center"> 
            <tr>
                <td colspan="4"><input type="text" name="result" placeholder="0" 
                    style ="text-align: right;"></td>
            </tr>
            <tr>
                <td><button type="button" value="sin" onclick="sin()">sin</button>
                </td>
                <td><button type="button" value="cos" onclick="cos()">cos</button>
                </td>
                <td><button type="button" value="tan" onclick="tan()">tan</button>
                </td>
                <td colspan="2"><button type="button" onclick="remv()" 
                    class="clear">C</button></td>
            </tr>
            <tr>
                <td><button type="button" value="x^2" onclick="square()">x<sup>2</button>
                </td>
                <td><button type="button" value="x^3" onclick="qubbed()">x<sup>3</button>
                </td>
                <td><button type="button" value="sqrt2" onclick="sqrt2()">&radic;</button>
                </td>
                <td><button type="button" value="sqrt3" onclick="sqrt3()">&#8731</button>
                </td>
            </tr>
            <tr>
                <td><button type="button" value="1" onclick="number(value)">1</button>
                </td>
                <td><button type="button" value="2" onclick="number(value)">2</button>
                </td>
                <td><button type="button" value="3" onclick="number(value)">3</button>
                </td>
                <td><button type="button" value="BACKSPC" onclick="BACKSPC()"><</button>
                </td>
            </tr>
            <tr>
                <td><button type="button" value="4" onclick="number(value)">4</button>
                </td>
                <td><button type="button" value="5" onclick="number(value)">5</button>
                </td>
                <td><button type="button" value="6" onclick="number(value)">6</button>
                </td>
                <td><button type="button" value="-" onclick="number(value)">-</button>
                </td>
            </tr>
            <tr>
                <td><button type="button" value="7" onclick="number(value)">7</button>
                </td>
                <td><button type="button" value="8" onclick="number(value)">8</button>
                </td>
                <td><button type="button" value="9" onclick="number(value)">9</button>
                </td>
                <td><button type="button" value="/" onclick="number(value)">/</button>
                </td>
            </tr>
            <tr>
                <td><button type="button" value="." onclick="number(value)">.</button>
                </td>
                <td><button type="button" value="0" onclick="number(value)">0</button>
                </td>
                <td><button type="button" value="*" onclick="number(value)">*</button>
                </td>
                <td><button type="button" value="%" onclick="number(value)">%</button>
                </td>
            </tr>
            <tr>
                <td colspan="2"><button type="button" value="=" onclick="equal()">=</button>
                </td>
                <td><button type="button" value="+" onclick="number(value)">+ </button>
                </td>
            </tr>
        
        </table>
    </form>

    <script type="text/javascript">
        function sin(){
            document.calculator.result.value=math.sin(document.
            calculator.result.value);
        }
        function cos(){
            document.calculator.result.value=math.cos(document.
            calculator.result.value);
        }
        function tan(){
            document.calculator.result.value=math.tan(document.
            calculator.result.value);
        }
        function BACKSPC(){
            var a = document.calculator.result.value;
            document.calculator.result.value = a.substr(a.length-1);
        }
    function square(){
        document.calculator.result.value = math.pow(document.
        calculator.result.value, 2);
    }
    function qubbed(){
        document.calculator.result.value = math.pow(document.
        calculator.result.value, 3);
    }
    function sqrt2(){
        document.calculator.result.value = math.pow(document.
        calculator.result.value, 1/2);
    }
    function sqrt3(){
        document.calculator.result.value = math.pow(document.
        calculator.result.value, 1/3);
    }
    function number(value){
        document.calculator.result.value += value;
    }
    function remv(){
        document.calculator.result.value =" ";
    }
    function equal(){
        document.calculator.result.value = eval(document.calculator.result.value)
    }
    </script>
</body>
</html>
