##  write a self invoking function  whose job is to print your name.

```
<!DOCTYPE html>
<html>
<body>
<p>Que 1.self invoking function</p>
<p>Functions can be invoked automatically without being called:</p>

<p id="demo"></p>

<script>
(function () {
  document.getElementById("demo").innerHTML = "Tushar Dhage";
})();
</script>

</body>
</html>
```

## • write a self invoking function whose job is to return square of a number

```
<!DOCTYPE html>
<html>
<body>
<p>Que 2.self invoking func return square</p>
<p>Functions can be invoked automatically without being called:</p>

<p id="demo"></p>

<script>
(function () {
  var x = prompt("enter number");
  document.getElementById("demo").innerHTML =  Math.pow(x,2);
})();
</script>

</body>
</html>
```

##   write a function sum with no parameter but it will do the sum of numbers passed in function call eg sum(2,3,5), sum(2,4).So your        definition will work irrespective of the number of parameters passed
```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 1 </title>
      
    </head>
    <body>
        <script>
            function sum(){
                let addtion = 0;
                let size = arguments.length;
                for(let i=0;i<size;i++){
                    addtion += arguments[i];
                }
                return addtion;
            }

            var x = sum(1,2);
            document.write(x);
        </script>
    </body>
</html>
```
