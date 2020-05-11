# Where to?

We can write js anywhere in file but function in body tag only not in head tag.

```
<!doctype html>
<html>
<head>
<title>Lets Learn About JavaScript</title>
</head>
<body>
<h1 id="tad"></h1>
<button>Click Me</button>
<script>
document.getElementById('tad').innerHtml="hey Tad";//this function used in body tag.
</script>

</body>
</html>
```
___
# output?

we can write output by so many ways in js.

- 1.document.getElementById('tad').innerHtml="hey Tad"
- 2.document.write("hello world");
- 3.window.alert("hey");
- 4.alert("hey");
- 5.console.log("hey");

___
# inner thing in js

<script>

- document.write("5+4");//5+4

- document.write(5+4);//9

- document.write("5+4 =" 5+4);//no output

- document.write("5+4 =" +5+4);//5+4=54

- document.write("5+4 =" +(5+4));//5+4=9
___
<script>

<h1 id="result"></h1>

<script> 

- document.getElementById("result").innerHTML = 8+2;//10 without quatation mark
- document.getElementById("result").innerHTML = "8+2 =" +(8+2);//8+2=10

</script>

___
# variable

<script>

- var name="Tushar Dhage"; // for storing string we have to use quatation mark.

  - document.write(name); // Tushar Dhage

  - document.write("name"); // name

- var val1 = 56; // for storing number or value we dont have to use quotaion mark.

- var val2 = 5;

  - document.write(val1); // 56

  - document.write(val2); // 5

  - document.write(val1+val2); // 61

  - document.write(val1+"+"+val2+" = "+(val1+val2)); //this is dynamic type whatever u change value output will change

</script>


___
# comment

<!--hello bro this is comment in html-->

// this is comment in js for only single line

/*this is comment for whole paragraph in js */

___
# function

group all code and put name to that code so when u click this name this code will run for this put code in curly bracker{}

``` 
<button onClick="tad()">Click Me</button> // when we click button below code will run

<script>

// this is function syntax for putting in one double quatation we have to remove other double quoation use n single quation 

function tad()
{

var val1 = 56;

var val2 = 5;

document.write(val1+'+'+val2+' = '+(val1+val2)); 

}

</script>
```




