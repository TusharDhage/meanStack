# LAB TEST-1 



> **1.Write a function whose job is to take 3 parameters and return the highest number** 

```
<!DOCTYPE html>
<html>
<body>
<p> Maximum value between three values are: </p>

<button onclick="tad()">click</button>

<p id="max"></p>

<script>
function tad() {
  document.getElementById("max").innerHTML = Math.max(456,321,568);
                }
</script>
</body>
</html>
```






> **2.On button click, display your name in browser, console and alert**

```
<!DOCTYPE html>
<html>
<head>
<title>pop up name in window</title>
</head>
<body>
<button onClick="tad()">Click Me</button>
<script>
function tad()
{
document.write("Tushar Dhage");
alert("Hello I am Tushar Dhage");

}
</script>
</body>
</html>
```

> **Print your name 5 times using h1 to h5 tag dynamically at run time**

```
<!DOCTYPE html>
<html>
<head>
<title>All size of Names</title>
</head>
<body>
<button onClick="tad()">Click Me</button>
<script>
function tad()
{
var name="Tushar";
var surname="Dhage";
document.write("<h1>"+name + "&nbsp" +surname+" </h1> "); 
document.write("<h2>"+name + "&nbsp" +surname+" </h2> ");
document.write("<h3>"+name + "&nbsp" +surname+" </h3> ");
document.write("<h4>"+name + "&nbsp" +surname+" </h4> ");
document.write("<h5>"+name + "&nbsp" +surname+" </h5> ");
}
</script>
</body>
</html>
```

















