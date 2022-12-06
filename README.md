# OBJECT-ORIENTED PROGRAMMING
Object Oriented Programming is not a language or a tool.

It’s a style of programming or programming paradigm. 
There are several programming languages that support object oriented programming: Such as javascript, Python, Ruby, Java and more.

Object-oriented programming is a very popular style of programming, and it comes up in many technical interviews.
So if you really want to be a serious developer, you need to understand object-oriented programming.

In this session, we are going to learn _OOP_ principles and how to implement them in JavaScript.

My name is [_Jeanne d’Arc NYIRAMWIZA_], I am a Backend Engineer at CoCreation Hub, and I am going to be your  instructor in this course.

## 4 Pillars of Object-Oriented Programming 

- Encapsulation
- Abstraction
- Inheritance
- Polymorphism

* Let’s look at each of these concepts.
Before OOP, we had procedural programming which divides a program into a set of functions so we have data stored in a bunch of variables,and functions that operate on the data.
This style of programming is very simple and straightforward.

You may find yourself copying and pasting lines of code over and over. You make changes to one function, and other several functions break. That’s what we call spaghetti code.
![Alt text](Fig.-1.1-Structure-of-procedural-oriented-programs.png?raw=true "Procedural programming")
There is so much interdependency between all these functions. It becomes problematic.

Object-oriented Programming came to solve this problem. In Object Programming, we combine a group of related variables and function into a unit.We call that unit an object.We refer to these variables as properties, and functions as methods.

 
Here is an example, think of a calculator

A calculator is an object with properties, such as :
- make 
- model
- color
- type
and methods like:
- addition()
- subtraction()
- division()
- multiplication()
- clear()
- equal()

Now you might say, what Jeanne d’Arc, we don't have calculators in our programs😊, give us a real programming example. 

Ok, think of local storage objects in your browsers. Every browser has a local storage object that allows you to store data locally. 

This local storage object has a property like length which returns the number of objects in the storage and methods like setItem, remove item, getItem and more.

So in object-oriented programming we group related variables and functions that operate on them into objects and this is what we call [encapsulation].
[Encapsulation] reduces complexity + increase reusability

[Abstraction]: Our calculator has a complex logic board on the inside and a few buttons on the outside that you interact with.

You simply press the addition button and you don't care what happens on the inside. All that complexity is hidden from you. This is abstract in practise.

[Inheritance]: Inheritance is a mechanism that allows you to eliminate redundant code.


[Polymorphism] means 'many shapes' or `many forms`! Each child function implements its own version of the parent's methods.


Let me show you an example of this in action:
Objects are independent with specific attributes visible on the front. In contrast, certain characteristics are hidden and can only be witnessed when communicating with another object.


# OOP_calculator

# HTML part<br />
## Create a new html file, and add the following code<br />
```
<div class="cont">
<div class="calsi">
<h1>Calculator</h1>
<input type="text" id="inp" placeholder="Enter Value..." readonly="">
<div class="btns">
<button onclick="AT_add(1)">0</button>
<button onclick="AT_add(1)">1</button>
<button onclick="AT_add(2)">2</button>
<button onclick="AT_add(3)">3</button>
<button onclick="AT_add(4)">4</button>
<button onclick="AT_add(5)">5</button>
<button onclick="AT_add(6)">6</button>
<button onclick="AT_add(7)">7</button>
<button onclick="AT_add(8)">8</button>
<button onclick="AT_add(9)">9</button>
<button onclick="AT_add('+')">+</button>
<button onclick="AT_add('-')">-</button>
<button onclick="AT_add('/')">/</button>
<button onclick="AT_add('*')">*</button>
</div>
<button onclick="cls()">c</button><
</div>
```

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
