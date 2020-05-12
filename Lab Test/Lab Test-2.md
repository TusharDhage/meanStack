# LAB TEST - 2

> ## Create an array having 10 numbers , write a function whose  job is to return max number from the array
```
<!DOCTYPE html> 
<html> 
<head> 
	<title> Find the max element of an Array using JavaScript </title> 
</head> 
<body> 

<p>Click button to find out maximum value of the array </p> 

<p> Max number is: <span id="max"> </span></p> 
	<script>
        var maxarr = [10,20,30,40,50,60,70,80,90,100]
        document.getElementById('max').innerHTML=tad(maxarr); 

        function tad(arr)
{
        return Math.max.apply(null,arr);
}
	</script> 
</body> 
</html> 
```
___
> ## On button click print your name in P tag
```
<!DOCTYPE html> 
<html>
<body>

<p>Click the input button to display the value of its name attribute.</p>
<p id="tad">Tushar Dhage</p>
<script>
document.getElementById("tad").innerHtml;
</script>

</body>
</html>
```

___
> ## Write your name on page but keep it hidden. On button click it should unhide your name.
```
<!DOCTYPE html>
<html>

<body>
<p id='hideName' style="display:none">Tushar</p>
<button onclick="myHiddenName()" >click here</button>
        <script>
               function myHiddenName()
               {
         
               document.getElementById("hideName").style.display = "block";
                }
                </script>
  </body>
 </html>
 ```

> ## Write your name with font size 4. On button click change it to 7

___
```
<!DOCTYPE html>
<html>
<body>
<p id='size' style="size: 4;">Tushar</p>
        <button onclick="changeSize()" >click here</button>
        <script>
                  
                function changeSize()
                {
                   var name = "Tushar";
                 document.getElementById("size").innerHTML = name.fontsize(7);
                    
                }
                </script>
  </body>
 </html>
 ```
___
> ## On button click, display current date time in browser.

```
<!DOCTYPE html>
<html>
<body>
<p id="date"></p>
        <button onclick="displayDate()" >click here</button>
        <script>
                  
                function displayDate()
                {
                    var d = new Date();
                    document.getElementById("date").innerHTML = d;
                }
                </script>
  </body>
 </html>
 ```
___
> ## Create two text boxes and a button , on button click it should copy data from one text box to another.

```
<!DOCTYPE html>
<html>
<body>

            <input id="t1" placeholder="enter any word"><br/>
            <input id="t2" readonly><br/>
            <button onclick="copy()">copy</button>

        <p id='tp'></p>

        <script>
         var text = document.getElementById("t1");
         function copy()
        {
          document.getElementById("t2").value = text.value;
    
        }
      </script>
  </body>
 </html>
 ```
___
> ## Create an array having 10 numbers and display it in ascending order
```
<!DOCTYPE html>
<html>
<body>

          <p id="ascArr"></p>
        <button onclick="sortArr()">Make It In Ascending Order</button>

        <script>
        var myArr = [2,45,78, 10, 4,65, 90, 25,1, 12];
document.getElementById("ascArr").innerHTML = myArr;  

function sortArr() {
    myArr.sort(function(a, b){return a - b});
  document.getElementById("ascArr").innerHTML = myArr;
}
      </script>
  </body>
 </html>
```
___
> ## Create an array having 5 names and display it in descending order

```
<!DOCTYPE html>
<html>
<body>

         <p id ='a1'></p>
        <button onclick="desc()">sort in descending order</button>
        <p id = 'a2'></p>
        <script>
      var nameArr = ["Tushar","Azhar","Divya","Pooja","Katrina"];
document.getElementById("a1").innerHTML = nameArr;
function desc()
{
    document.getElementById("a1").innerHTML =  nameArr.reverse(nameArr.sort());
}
      </script>
  </body>
 </html>
```
___
> ## Declare a string having an email Id and check if @ is there in the string or not

```
<!DOCTYPE html>
<html>
<body>

         <p id = 's1'></p>
        <button onclick="check()">check</button>
        <p id = 'v1'></p>
        <script>
  var str = "tushar.dhage95@gmail.com";
  
  document.getElementById("s1").innerHTML = str;

function check()
{
   if(str.search("@")!=-1)
   {
    document.getElementById("v1").innerHTML = "true";
   } 
   else
   {
    document.getElementById("v1").innerHTML = "false";
   }
}
      </script>
  </body>
 </html>
 ```
___
> ## Declare a string having a 10 digit mobile number. Write a function whose job is
    to check if it has 10 digits or not

```
<!DOCTYPE html>
<html>
<body>
    
 <p id = 'm1'></p>
    <button onclick="checkmbno()">check</button>
    <p id = 'm2'></p>
        <script>
 var mobileNumber =7028303527;
var mstr = mobileNumber.toString();

document.getElementById("m1").innerHTML = mobileNumber;
function checkmbno()
{
   if(mstr.length==10)
   {
    document.getElementById("m2").innerHTML = "valid";
   }
   else
   {
    document.getElementById("m2").innerHTML = "invalid";
   }
}
      </script>
  </body>
 </html>
```
___
> ## Write a function whose  job is to return a random number
```
<!DOCTYPE html>
<html>
<body>
    
 <p id='r1'></p>
<button onclick="give()">random number</button>
        <script>
function give()
{
    var num = Math.floor(Math.random() * 10)+1;
    document.getElementById("r1").innerHTML = num;
}

      </script>
  </body>
 </html>
```
  

























 




























 
  










































