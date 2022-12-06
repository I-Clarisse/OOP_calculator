# OBJECT-ORIENTED PROGRAMMING
Object Oriented Programming is not a language or a tool.
It’s a style of programming or programming paradigm. 
There are several programming languages that support object oriented programming: Such as javascript, Python, Ruby, Java and more.

Object-oriented programming is a very popular style of programming, and it comes up in many technical interviews.
So if you really want to be a serious developer, you need to understand object-oriented programming.

In this session, we are going to learn _OOP_ principles and how to implement them in JavaScript.

My name is [_Jeanne d’Arc NYIRAMWIZA_], I am a Backend Engineer at CoCreation Hub, and I am going to be your  instructor in this course.

## 4 Pillars of Object-Oriented Programming 

````
- Encapsulation
- Abstraction
- Inheritance
- Polymorphism
````



Let’s look at each of these concepts.
Before OOP, we had procedural programming which divides a program into a set of functions so we have data stored in a bunch of variables,and functions that operate on the data.
This style of programming is very simple and straightforward.

You may find yourself copying and pasting lines of code over and over. You make changes to one function, and other several functions break. That’s what we call spaghetti code.
![Alt text](Fig.-1.1-Structure-of-procedural-oriented-programs.png?raw=true "Procedural programming")<br/>

`There is so much interdependency between all these functions. It becomes problematic.`

Object-oriented Programming came to solve this problem. In Object Programming, we combine a group of related variables and function into a unit.We call that unit an object.We refer to these variables as properties, and functions as methods.

`Here is an example, think of a calculator`

A calculator is an object with properties, such as :
```
- make 
- model
- color
- type
```
and methods like:
- addition()
- subtraction()
- division()
- multiplication()
- clear()
- equal()

Now you might say, what Jeanne d’Arc, we don't have calculators in our programs😊, give us a real programming example. 

```Ok, think of local storage objects in your browsers. Every browser has a local storage object that allows you to store data locally. ```

```This local storage object has a property like length which returns the number of objects in the storage and methods like setItem, removeItem, getItem and more.```

```So in object-oriented programming we group related variables and functions that operate on them into objects and this is what we call [encapsulation].``` 

[Encapsulation] `reduces complexity + increase reusability`

[Abstraction]: Our calculator has a complex logic board on the inside and a few buttons on the outside that you interact with.

You simply press the addition button and you don't care what happens on the inside. All that complexity is hidden from you. This is abstract in practise. [Abstraction] `reduces complexity + isolate impact of changes`

[Inheritance]: Inheritance is a mechanism that allows you to eliminate redundant code.

[Polymorphism] means 'many shapes' or `many forms`! Each child function implements its own version of the parent's methods.


Let me show you an example of this in action:

# Object-Oriented Programming: My Calculator

## Task: Frontend 
1. Create a folder and name it My-Calculator
2. Inside your `My-Calculator`folder, create a new [index.html] file.
3. Inside your `My-Calculator`folder, create a new [index.css] file.
3. Inside your `My-Calculator`folder, create a new [index.js] file.

4. In your [index.html] head element, add your [index.css] file
5. In your [index.html] body element, add your [index.js] file path

6. Your new [index.html] file should like like this: 
```
<!DOCTYPE html>
<html>
  <head>
    <title>OOP Calculator</title>
    <link rel="stylesheet" href="./index.css" />
  </head>
  <body>
    <div class="cont">
      <div class="calsi">
        <h1>OOP Calculator</h1>
        <input type="text" id="inp" placeholder="Enter Value..." readonly="" />
        <div class="btns">
          <button onclick="AT_add(0)">0</button>
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
        <button onclick="exe()">=</button>
        <button onclick="cancel()">⌫</button>
        <button onclick="cls()">c</button>
      </div>
    </div>
    <script type="text/javascript" src="./index.js"></script>
  </body>
</html>
```

7. Your css [index.css] file should look like this: 
```
html,body{
padding:0;
margin:0;
background:whitesmoke;
}

.cont{
position:relative;
width:100%;
padding:0;
margin:0;
text-align:center;
}

.calsi{
width:350px;
padding:0;
margin:100px auto;
text-align:center;
background:#d82ed8;
box-shadow:0px 0px 6px 0px #0006;
}

.calsi h1{
font-size:40px;
font-family:calibri;
font-weight:bold;
color:white;
text-transform:cepitalize;
padding:8px 0px;
text-align:center;
width:100%;
background:#222;
margin:0 auto;
}

#inp{
position:relative;
width:100%;
padding:8px 0px;
text-align:center;
font-size:16px;
font-family:arial;
font-weight:normal;
color:#222;
outline:none;
border:none;
background:white;
}

.btns{
position:relative;
width:100%;
padding:10px 0px;
}

.btns button{
border:none;
outline:none;
width:50px;
height:50px;
font-size:30px;
color:#222;
vertical-align:middle;
border-radius:5px;
background:white;
margin:10px 5px;
display:inline-block;
}

button{
border:none;
outline:none;
width:100px;
height:50px;
font-size:20px;
color:#222;
border-radius:5px;
vertical-align:middle;
background:white;
margin:10px 5px;
display:inline-block;
}
```


8. Add the following code in your [index.js]

````
var val=document.getElementById("inp");

function AT_add(v){
val.value+=v;
}

function cls(){
val.value="";
}
function exe(){
val.value=eval(val.value);
}

function cancel(){
val.value=val.value.substr(0,val.value.length-1);
}
```

