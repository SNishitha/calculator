# calculator
.html
<!DOCTYPE html>
<html>
<head>
   <meta charset="utf-8">
   <title>SIMPLE CALCULATOR</title>
   <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.1/dist/css/bootstrap.css">
   <link rel="stylesheet" type="text/css" href="style 2.css">
</head>
<body>
   
<div class="container">
   <h1 align="center">MY CALCULATOR</h1>
   <table border="1" cellspacing="0">
      <tr>
         <td colspan="4" id="inputlabel">0</td>
      </tr>
      <tr>
         <td colspan="2"><button onclick="pushbtn(this);" style="background-color:red ;">AC</button></td>
         <td><button onclick="pushbtn(this);">DEL</button></td>
         <td><button onclick="pushbtn(this);">/</button></td>
      </tr>
      <tr>
         <td><button onclick="pushbtn(this);">7</button></td>
         <td><button onclick="pushbtn(this);">8</button></td>
         <td><button onclick="pushbtn(this);">9</button></td>
         <td><button onclick="pushbtn(this);">*</button></td>
      </tr>
      <tr>
         <td><button onclick="pushbtn(this);">4</button></td>
         <td><button onclick="pushbtn(this);">5</button></td>
         <td><button onclick="pushbtn(this);">6</button></td>
         <td><button onclick="pushbtn(this);">-</button></td>
      </tr>
      <tr>
         <td><button onclick="pushbtn(this);">1</button></td>
         <td><button onclick="pushbtn(this);">2</button></td>
         <td><button onclick="pushbtn(this);">3</button></td>
         <td><button onclick="pushbtn(this);">+</button></td>
      </tr>
      <tr>
         <td colspan="2"><button onclick="pushbtn(this);">0</button></td>
         <td><button onclick="pushbtn(this);">.</button></td>
         <td><button onclick="pushbtn(this);" style="background-color:green;">=</button></td>
      </tr>
   </table>
</div>

<script>
   var inputlabel=document.getElementById('inputlabel')

   function pushbtn(obj)
   {
      var pushed=obj.innerHTML;

      if(pushed == '=')
      {
         inputlabel.innerHTML=eval(inputlabel.innerHTML);
      }
      else if (pushed == 'AC') 
      {
         inputlabel.innerHTML = '0';
      }
      else if (pushed == 'DEL') 
      {
         inputlabel.innerHTML = inputlabel.innerHTML.slice(0,-1);
      }
      else
      {
         if (inputlabel.innerHTML == '0')
         {
            inputlabel.innerHTML = pushed;
         }
         else
         {
            inputlabel.innerHTML += pushed;
         }
      }
   }
</script>
</body>
</html>

.css
*{
         font-family: 'inconsolata',monospace;
 }
body{
   background-color: #e8e3e308;
}
.container{
   width: 700px;
   background-color: white;
   margin: 120px auto;
}
table{
   width: 100%;
   border-color: black;
}
td{
   width: 25%;
}
button{
   width: 100%;
   height: 70px;
   font-size: 24px;
   color: white;
   background-color: #332a2a;
   border: none;
}
#inputlabel{
   height: 100px;
   font-size: 30px;
   vertical-align: bottom;
   text-align: right;
   padding-right: 16px;
   background-color: #d3d3d37a;
}
