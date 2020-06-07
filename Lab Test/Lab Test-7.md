## Write your name in red colour , on a button click it should change the text colour to blue
```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 1</title>
         
       
    </head>
    <body > 
        <h1 id="myName" style="color: red;">Tushar Dhage</h1>
        <button onclick="changeColor()">change colour</button>
        <script>
           
            function changeColor()
            {
                document.getElementById("myName").style.color = "blue";
            }

        </script>
    </body>
</html>
```


## Write your name in h1 tag align it to the left, on button click it should align to right
```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 2</title>
      
       
    </head>
    <body > 
        <h1 id="myName" style="text-align: left;">Tushar Dhage</h1>
        <button onclick="changeAlignment()">change alignment</button>
        <script>
           function changeAlignment(){
               document.getElementById("myName").style.textAlign="right";
           }
        </script>
    </body>
</html>
```
##   Write your name in p tag with background colour blue and text in white colour,on button click it should reverse the colour ie Text      colour blue and background colour white
```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 3</title>
       
       <style>
           #myName{
               background-color: blue;
               color: white;
           }
       </style>
    </head>
    <body > 
        <p id="myName" >Tushar Dhage</p>
        <button onclick="myFun()">Reverse</button>
        <script>
           function myFun(){
               document.getElementById("myName").style.color = "blue";
               document.getElementById("myName").style.backgroundColor="white";

           }
        </script>
    </body>
</html>
```
## Create three radio buttons which show names of colour. Create a text bo Let user enter name in text box and select radio button,on      clicking the text in a text box should get respective colour.
```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 4</title>
        
       
    </head>
    <body > 
        <input id="myName" onfocus="changeColor()"><br/>
        <label>red</label>
        <input type="radio" name="color" value="red"><br/>
        <label>green</label>
        <input type="radio" name="color" value="green"><br/>
        <label>blue</label>
        <input type="radio" name="color" value="blue"><br/>
        
        <script>
           function changeColor(){
               
               var ele = document.getElementsByName("color");

               for(let i=0;i<ele.length;i++){
                   if(ele[i].checked){
                       document.getElementById("myName").style.color = ele[i].value;
                   }
               }
           }
        </script>
    </body>
</html>
```
##  Create a dropdown box showing the number 1 to 10.Write your name in p tag let user select option from dropdown and that font size       should be applied to the data in p tag
```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 5</title>
      
       
    </head>
    <body > 
        <p id="myName">Tushar Dhage</p>

        <select onchange="changeSize(this)">
            <option value="1" >1</option>
            <option value="2">2</option>
            <option value="3">3</option>
            <option value="4">4</option>
            <option value="5">5</option>
            <option value="6">6</option>
            <option value="7">7</option>
            <option value="8">8</option>
            <option value="9">9</option>
            <option value="10">10</option>
        </select>

       
        <script>
           function changeSize(id){
               var size = id.value;
               document.getElementById("myName").style.fontSize = size+"px";
               
               }
               
           
        </script>
    </body>
</html>
```
## Create three text boxes and two radio buttons showing value “add” and “subtract”.Let user enter number in two text boxes and as per      the selected radio button it should display result in the 3rd text box.
```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 6</title>
        

       
    </head>
    <body > 
        <label>Number 1</label><br/>
        <input type="number" id="num1"><br/><br/>
        <label>Number 2</label><br/>
        <input type="number" id="num2"><br/><br/>
        <label>Answer</label><br/>
        <input id="ans" readonly><br/><br/>
        <label>Addition</label>
        <input onchange="calculate()" type="radio" name="action" value="add"><br/>
        <label>Substraction</label>
        <input onchange="calculate()" type="radio" name="action" value="sub">
        
        <script>
        

            function calculate(){
                var n1 = Number(document.getElementById("num1").value);
                var n2 = Number(document.getElementById("num2").value);
                var operation = null;
                var ele = document.getElementsByName("action");

               for(let i=0;i<ele.length;i++){
                   if(ele[i].checked){
                       operation = ele[i].value;
                   }
               }

             
               
               if(operation=="add"){
                   document.getElementById("ans").value = n1+n2;
               }else if(operation=="sub"){
                document.getElementById("ans").value = n1-n2;
               }
            }
        </script>
    </body>
</html>
```
##  Write at least 3 paragraph about yourself.Create a button on click it should count number of p tags used in document.Also give blue     background colour to all p tags.
```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 7</title>
       
    </head>
    <body > 
        <p>My name is Tushar Dhage. I am from Hinganghat.
            I have done my B.E. from YCCE College of Engineering (Autonomous),
            Nagpur with CGPA of 7.514 in Electrical Engineering Branch.
            I have secured 81.65% in Polytechnic and 82% in SSC.
            I have also done my Job from Wipro Lightning Nagpur.</p>
            <p>I am hardworking, self-motivated, passionate about learning new things, quick learner, team player.</p>
            <p>There are  members in my family including me.
                First of my respected Father who is Government Employee. Then, my lovely mother, she is a Housewife and elder sister who is a Lecturer. </p>
            <button onclick="myFun()">click here</button>
            <h5 id="total"></h5>
        <script>
           function myFun(){
               var ele  = document.getElementsByTagName("p");
               var count = ele.length;
               for(let i=0;i<count;i++){
                    ele[i].style.background = "blue";
               }
               document.getElementById("total").innerHTML = "number of paragraph tag is "+count;
           }
        </script>
    </body>
</html>
```

##  Write your friends name using OL tag. Create a button whose job is to delete the 1st name from the OL tag.
```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 8</title>
       
       
    </head>
    <body > 
        <ol>
            <li>Azhar</li>
            <li>Divya</li>
            <li>Mangesh</li>
        </ol>

        <button onclick="myFun()">remove</button>
        <script>
           function myFun(){
               var names = document.getElementsByTagName("li");
                names[0].remove();
           }
        </script>
    </body>
</html>
```
## Create a textbox ,and a span tag,on change event on text box it should display data entered in text box in span tag which is next to    it text box.
```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 9</title>
       
                   
    </head>
    <body > 
        <input id="t" onchange="myFun()">
        <br/><span id="d"></span>
        <script>
           function myFun(){
               var text = document.getElementById("t").value;
               document.getElementById("d").innerHTML= text;
           }
        </script>
    </body>
</html>
```
##  Create text box and a span tag , on change it should give error if user keeps text box empty. 
```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 10</title>
             
    </head>
    <body > 
       <input id="t" onchange="myFun()"><br/>
       <span id="s"></span> 
        <script>
           function myFun(){
               var text = document.getElementById("t").value;
               

               var str = text.toString();
               
               if(str.length==0){
                   document.getElementById("s").innerHTML = "Text box is empty!";
               }
           }
        </script>
    </body>
</html>
```
## Create text box and a span tag  ask user to enter password . Rule for password is

o It must have at least one capital character

o It must have at least one digit

o It must have at least 1 special symbol

## On change event it should display appropriate error message For example if user enters “Vita” error should be "please use one digit      use one symbol."

```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 11</title>
        
       
    </head>
    <body > 
        <input onchange="check(this)"><span style="color: red;" id="warning"></span>
        <script>
           function check(id)
           {
            var condition1 = false; 
            var condition2 = false;
            var condition3 = false;
            var text = id.value;
            var warn = "";


            //It must have at least one capital character
            var reg1 = /[A-Z]/g;
            if(reg1.test(text)){
                condition1 = true;
            }else{
                condition1 = false;
            }

            //It must have at least one digit
            var reg2 = /[0-9]/;
            if(reg2.test(text)){
                condition2 = true;
                
            }else{
                condition2 = false;
                
            }

            //It must have at least 1 special symbol

            var reg3 = /[ `!@#$%^&*()_+\-=\[\]{};':"\\|,.<>\/?~]/;
            
            if(reg3.test(text)){
                condition3 = true;
                
            }else{
                condition3 = false;
                
            }

            if(!condition1){
                warn += "<br/>It must have at least one capital character<br/>";
            }
            if(!condition2){
                warn += "<br/>It must have at least one digit<br/>";
            }
            if(!condition3){
                warn += "<br/>It must have at least 1 special symbol<br/>";
            }
            if(condition1 && condition2 && condition3){
                warn = "";
            }

            document.getElementById("warning").innerHTML = warn;

           }
        </script>
    </body>
</html>
```


## Create three check boxes showing book name and price.Create a text box.As per selection of check box ,text box should show total of      selected price.

```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 11</title>
         
       
    </head>
    <body > 
        <table>
            <tr>
                <th>Book Name</th>
                <th></th>
                <th>Price</th>
            </tr>
        <tr>
           <td><label>C</label></td> 
           <td><input type="checkbox" name="books" value="300" onchange="calTotal()"></td> 
           <td><label>300</label></br></td> 
            
        </tr>
        <tr>
            <td><label>C++</label></td>
            <td><input type="checkbox" name="books" value="350" onchange="calTotal()"></td>
            <td><label>350</label></br></td>
        </tr>
        <tr>
           <td><label>JAVA</label></td> 
           <td><input type="checkbox" name="books" value="400" onchange="calTotal()"></td> 
           <td><label>400</label></br></td> 
        </tr>
        <tr>
            <th>Total</th>
            
            <th id="t">0</th>
        </tr>
    </table>
        
        <script>
            
           function calTotal()
           {
            var sum = 0;
               var ele = document.getElementsByName("books");
               
               for(let i=0; i<ele.length;i++){
                   if(ele[i].checked)
                   {
                    sum += Number(ele[i].value);
                   }
                  
               }
               document.getElementById("t").innerHTML = sum;
           }
        </script>
    </body>
</html>
```