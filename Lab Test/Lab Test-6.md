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

