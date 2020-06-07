## Write a program to display a digital clock
```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 1</title>
  
        <style>
            h1{
                text-align: center;
            }
        </style>
    </head>
    <body>
            <h1 >Digital Clock</h1>
            <h1 id="time"></h1>
       
        <script>
           // alert("hi");
            window.setInterval(digitClock,1000);
            
            function digitClock(){
                var d = new Date();
                document.getElementById("time").innerHTML = d.getHours()+":"+d.getMinutes()+":"+d.getSeconds();
               
            }
        </script>
    </body>
</html>
```

##  On loading of the page it should display height and width of a screen in h2 tag
```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 2</title>
    
    </head>
    <body onload="info()">
        <h2 id="wh"></h2>
        <script>
            function info(){
            var width = screen.width;
            var height = screen.height;
            document.getElementById("wh").innerHTML = "width = "+width+" height = "+height;
           }
        </script>
    </body>
</html>
```

##  Create a button and on click it should open a new window which shows your image
```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 3</title>
       
    </head>
    <body>
        <button onclick="myPic()">Display My Image</button>
        <script>
            function myPic(){
                open("myImageWebPage.html");
            }
        </script>
    </body>
</html>
```

## Create a text box and two buttons ‘create cookie and read cookie.'When user enters data in a text box and clicks on button create cookie it should store data in cookie.When user clicks on button read cookie it should display cookie data on the page.
```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 4</title>
      
    </head>
    <body>
        <input id="t">
        <button onclick="createMyCookie()">Create Cookie</button>
        <button onclick="readMyCookie()">Read Cookie</button>
        <script>
            function createMyCookie(){
                var text = document.getElementById("t").value.toString();
                if(text.length ==0){
                    alert("Please Enter Data");
                }else{
                    document.cookie = text;
                    alert("Cookie Created Successfully");
                }
                
            }
            function readMyCookie(){
                var cookieData = document.cookie.toString();
                if(cookieData.length==0){
                    alert("Cookie is empty!");
                }else{
                    document.write("Inside Cookie : "+cookieData);
                }

            }
        </script>
    </body>
</html>
```
