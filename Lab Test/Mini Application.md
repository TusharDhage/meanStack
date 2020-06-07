##  Write a script to which will take name as a input from user and display greeting message to the user according time of the day.If time is less than or equal to 12PM then Good Morning with User nameIf time is between to 12 PM to 3 PM then Good After noon with User name.And if time is greater than 3 PM then Good Evening with User name.

```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 1</title>

    </head>
    <body>
	<label>Enter Your Name</label>
        <input id="username">
        <button onclick="myFun()">Submit</button>

        <script>
            function myFun(){
                var uname = document.getElementById("username").value;
                var d = new Date();
                var time = d.getHours();
                if(time<=12){
                    document.write("Good Morning "+uname.toUpperCase());
                }else if(time>=12 && time<=15){
                    document.write("Good Afternoon "+uname.toUpperCase());
                }else if(time>15){
                    document.write("Good Evening "+uname.toUpperCase());
                }

            }
        </script>
    </body>
</html>
```

##  Generate Timer program using JavaScript where Time is decrementing from 5 mins to 0 seconds.As soon as it reaches to zero seconds we should get one alert message with message “Time out!” 

```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 2</title>
      
            <style>
                h1{
                    text-align: center;
                }
            </style>
    </head>
    <body>
        <h1>Timer</h1>
        <h1 id="t">5:00</h1>
        <script>
            var time = setInterval(myTimer,1000);
            var min = 4;
            var sec = 59;
            function myTimer(){
               
                if(sec==0 && min >=0){
                    min--;
                    sec = 59;
                }
                else {
                    sec--;
                }

                if(min==0 && sec==0){
                        clearInterval(time);
                        alert("Time Out");
                    }
                document.getElementById("t").innerHTML = min+":"+sec;
                
            }          
        </script>
    </body>
</html>
```


##  Display date on web page at right hand corner in format of Today day, month date, hours: minutes: seconds Time should move without refreshing web page

```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 6</title>
       
    </head>
    <body>
        <h3 id="t" style="text-align: right;">time</h3>
        <script>
            setInterval(myClock,1000);
            
            function myClock(){
                var dateFormat = null;
            var d = new Date();
            var dayInNumber = d.getDay();
            var day=null;
            var monthInNumber = d.getMonth()+1;
            var month = null;
            var date = ""+d.getDate();

            switch(dayInNumber){
                case 0:
                day = "Sunday";
                break;
                case 1:
                day = "Monday";
                break;
                case 2:
                day = "Tuesday";
                break;
                case 3:
                day = "Wednesday";
                break;
                case 4:
                day = "Thursday";
                break;
                case 5:
                day  = "Friday";
                break;
                case 6:
                day = "Saturday";
                break;

            }

            switch(monthInNumber){
                case 1:
                month = "January";
                break;
                case 2:
                month = "February";
                break;
                case 3:
                month = "March";
                break;
                case 4:
                month = "April";
                break;
                case 5:
                month = "May";
                break;
                case 6:
                month = "June";
                break;
                case 7:
                month = "July";
                break;
                case 8:
                month = "August";
                break;
                case 9:
                month = "September";
                break;
                case 10:
                month = "October";
                break;
                case 11:
                month = "November";
                break;
                case 12:
                month = "December";
                break;


            }



                document.getElementById("t").innerHTML ="Today- "+day+", "+month+" "+date+"/"+d.getFullYear()+", "+d.getHours()+":"+d.getMinutes()+":"+d.getSeconds();
            }
        </script>
    </body>
</html>
```

##  With the help of Regular Expressions create application form, which validate inputs like name, age, and phone no., email id If user has done any mistake show appropriate message to users 
```
<!DOCTYPE html>
<html>
    <head>
        <title>Assignment 7</title>
  
   <style>
       #nameWarning,#ageWarning,#mobileWarning,#emailWarning{
           color: red;
           display: none;
       }
   </style>
    </head>
    <body>
        <form onsubmit="return validateForm()">
            <label>Name:</label><br/>
            <input id="n" onchange="nameValidation()"><label id="nameWarning"> Please Enter Valid Name</label><br/>
            <label>Age:</label><br/>
            <input id="a" onchange="ageValidation()"><label id="ageWarning"> Please Enter Valid Age</label><br/>
            <label>Mobile Number:</label><br/>
            <input id="m" onchange="mobileValidation()"><label id="mobileWarning"> Please Enter Valid Mobile Number</label><br/>
            <label>Email:</label><br/>
            <input id="e" onchange="emailValidation()"><label id="emailWarning"> Please Enter Valid E-mail Address</label><br/><br/>
            <input type="submit">
        </form>
        <script>
            var isNameValid = false;
            var isAgeValid = false;
            var isMobileValid = false;
            var isEmailValid = false;

            function nameValidation(){
                var regForName = /^[A-Za-z]+$/;
                var name = document.getElementById("n").value.toString();
                if(name.match(regForName)){
                    isNameValid = true;
                    document.getElementById("nameWarning").style.display = "none";
                }else{
                    isNameValid = false;
                    document.getElementById("nameWarning").style.display = "block";
                }
            }


            function ageValidation(){
                var regForAge = /^[0-9]+$/;
                var age = document.getElementById("a").value.toString();
                if(age.match(regForAge)){
                    isAgeValid = true;
                    document.getElementById("ageWarning").style.display = "none";
                }else{
                    isAgeValid = false;
                    document.getElementById("ageWarning").style.display = "block";
                }
            }

            function mobileValidation(){
                var regForMobile = /^[0-9]+$/;
                var mobile = document.getElementById("m").value.toString();
                if(mobile.match(regForMobile) && mobile.length == 10 ){
                    isMobileValid = true;
                    document.getElementById("mobileWarning").style.display = "none";
                }else{
                    isMobileValid = false;
                    document.getElementById("mobileWarning").style.display = "block";
                }
            }

            function emailValidation(){
                var regForEmail = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/;
                var email = document.getElementById("e").value.toString();
                if(email.match(regForEmail)){
                    isEmailValid = true;
                    document.getElementById("emailWarning").style.display = "none";
                }else{
                    isEmailValid =false;
                    document.getElementById("emailWarning").style.display = "block";
                    
                }

            }

            

            function validateForm(){
                if(isNameValid==true && isAgeValid == true && isMobileValid == true && isEmailValid == true){
                    alert("Form Submitted Successfully");
                    return true;
                }else{
                    alert("Please Enter Required Details");
                    return false;
                }
            }
        </script>
    </body>
</html>
```
