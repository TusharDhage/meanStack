## Create a button,  on click it should display image and if you click again it should hide image

```
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<script>
$(document).ready(function(){
  $("button").click(function(){
    $("#h").hide(1000);
  });
});
</script>
</head>
<body>

<button>Hide</button>

<img id="h" src="im.jfif">

</body>
</html>
```

## Type your name in h1 tag when you put mouse over it your name should be fade out

```
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<script>
$(document).ready(function(){
  $("#h").mouseenter(function(){
    $("#h").fadeOut("slow");   
  });
});
</script>
</head>
<body>
<h1 id="h">"Tushar"</h1>
</body>
</html>
```
## Create a button on button click your name which is written in h3 tag will slide up and then it will slide down  

```
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<script> 
$(document).ready(function(){
  $("#h").click(function(){
    $("#hh").slideToggle("slow");
  });
});
</script>

</head>
<body>
 
<button id="h">Click to slide name down or up</button>
<h3 id="hh">Tushar Dhage</h3>

</body>
</html>
```

## Create image on page on button click size of image will slowly increase

```
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<script> 
$(document).ready(function(){
  $("button").click(function(){
    $("#h1").animate({
      left: '0px',
      height: '+=150px',
      width: '+=150px'
    });
  });
});
</script> 
</head>
<body>

<button>Start Animation</button>


<img id="h1" src="im.jfif">

</body>
</html>
```

## Create a paragraph on button click it should hide once hidden it should display message done with hiding

```
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<script>
$(document).ready(function(){
  $("button").click(function(){
    $("p").hide("slow",function(){
    alert("done with hiding");
  });
});
});
</script>
</head>
<body>

<button>Hide</button>

<p>This is a paragraph with little content.</p>


</body>
</html>
```
