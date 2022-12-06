# OOP_calculator

# CSS part
## Create an index.css file and add the following code
html,body{<br />
padding:0;<br />
margin:0;<br />
background:whitesmoke;<br />
}<br />
<br />
.cont{<br />
position:relative;<br />
width:100%;<br />
padding:0;<br />
margin:0;<br />
text-align:center;<br />
}<br />
<br />
.calsi{<br />
width:350px;<br />
padding:0;<br />
margin:100px auto;<br />
text-align:center;<br />
background:#d82ed8;<br />
box-shadow:0px 0px 6px 0px #0006;<br />
}<br />
<br />
.calsi h1{<br />
font-size:40px;<br />
font-family:calibri;<br />
font-weight:bold;<br />
color:white;<br />
text-transform:cepitalize;<br />
padding:8px 0px;<br />
text-align:center;<br />
width:100%;<br />
background:#222;<br />
margin:0 auto;<br />
}<br />
<br />
#inp{<br />
position:relative;<br />
width:100%;<br />
padding:8px 0px;<br />
text-align:center;<br />
font-size:16px;<br />
font-family:arial;<br />
font-weight:normal;<br />
color:#222;<br />
outline:none;<br />
border:none;<br />
background:white;<br />
}<br />
<br />
.btns{<br />
position:relative;<br />
width:100%;<br />
padding:10px 0px;<br />
}<br />
<br />
.btns button{<br />
border:none;<br />
outline:none;<br />
width:50px;<br />
height:50px;<br />
font-size:30px;<br />
color:#222;<br />
vertical-align:middle;<br />
border-radius:5px;<br />
background:white;<br />
margin:10px 5px;<br />
display:inline-block;<br />
}<br />
<br />
button{<br />
border:none;<br />
outline:none;<br />
width:100px;<br />
height:50px;<br />
font-size:20px;<br />
color:#222;<br />
border-radius:5px;<br />
vertical-align:middle;<br />
background:white;<br />
margin:10px 5px;<br />
display:inline-block;<br />
}<br />
<br />

# HTML part<br />
## Create a new html file, and add the following code<br />
<svg width="100" height="100" xmlns="http://www.w3.org/2000/svg">
<div class="cont"><br />
<div class="calsi"><br />
<h1>Calculator</h1><br />
<input type="text" id="inp" placeholder="Enter Value..." readonly=""><br />
<div class="btns"><br />
<button onclick="AT_add(1)">0</button><br />
<button onclick="AT_add(1)">1</button><br />
<button onclick="AT_add(2)">2</button><br />
<button onclick="AT_add(3)">3</button><br />
<button onclick="AT_add(4)">4</button><br />
<button onclick="AT_add(5)">5</button><br />
<button onclick="AT_add(6)">6</button><br />
<button onclick="AT_add(7)">7</button><br />
<button onclick="AT_add(8)">8</button><br />
<button onclick="AT_add(9)">9</button><br />
<button onclick="AT_add('+')">+</button><br />
<button onclick="AT_add('-')">-</button><br />
<button onclick="AT_add('/')">/</button><br />
<button onclick="AT_add('*')">*</button><br />
</div><br />
<button onclick="exe()">=</button><br />
<button onclick="cancel()">⌫</button><br />
<button onclick="cls()">c</button><br />
</div><br />
</svg>

# JavaScript part<br />
## create a index.js file in the same folder with index.html and add the following code<br />
<br />
var val=document.getElementById("inp");<br />
<br />
function AT_add(v){<br />
val.value+=v;<br />
}
<br />
function cls(){<br />
val.value="";<br />
}<br />
function exe(){<br />
val.value=eval(val.value);<br />
}<br />

function cancel(){<br />
val.value=val.value.substr(0,val.value.length-1);<br />
}
<br />
