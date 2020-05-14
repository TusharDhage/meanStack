# Using arrow function, print factorial of a number
```
<!DOCTYPE html>
<html>
    <head>
        <title>Question 1</title>

    </head>
    <body>

        <input id="t1" type="number">
        <p id="ans"></p>
        <button onclick="myFunction()">find</button>
        <script>
            function myFunction()
            {
                var num1 = document.getElementById('t1').value;

            var factorial = (num) =>
            {
                let fact = 1;
                if(num==0)
                {
                    return fact ;
                }
                else if(num==1)
                {
                    return fact;
                }
                else
                {
                    for(let i=2;i<=num;i++)
                    {
                        fact *=i;
                    }
                    return fact;
                }
            }

            document.getElementById("ans").innerHTML = "Factorail of "+num1+" is "+factorial(num1);
        }
        </script>
    </body>
</html>
```

# Create class Account having property name, balance. Write method deposit whose job is to increase balance with the amount 
deposited by user. Create two object sand call deposit method.Write method display which will display name and balance
```
<!DOCTYPE html>
<html>
    <head>
        <title>Question 2</title>

    </head>
    <body>
        
        <header>Account Details:</header><br/>
        
        <script>

          class Account
          {
              constructor(n,b)
              {
                if(typeof(n)=="string" && typeof(b)=="number")
                {
                    this.name = n;
                  this.balance = b;
                }
                else{
                    alert("Please Enter Valid Details");
                   
                }
                  
              }

              deposite(amt)
              {
                  this.balance+=amt;
              }

              display()
              {
                  var str = "name :"+this.name+"<br/> balance :"+this.balance+"<br/><br/>";
                  document.write(str);  
              }
          }

          user1 = new Account("Tushar",50000);
          user2 = new Account("azhar",90000);
          user1.deposite(1000);
          user2.deposite(60000);
          user1.display();
          user2.display();

        </script>
    </body>
</html>
```
# >	Create class math having two static methods, cube and square, whose job is to return the square and cube of a number
```
<!DOCTYPE html>
<html>
    <head>
        <title>que 3</title>

    </head>
    <body>
        
        <label>Please enter any number:</label><br/>
        <input id="t1" type="number">
        <button onclick="myFunction()">Answer</button>
        <p id="ans1"></p>
        <p id="ans2"></p>

        <script>
             
                class Math{
                    constructor(n)
                    {
                        this.num = n;
                    }

                    static  square(n1)
                    {
                        return n1.num*n1.num;
                    }

                    static cube(n2)
                    {
                        return n2.num*n2.num*n2.num;
                    }

                }
                   
                    function myFunction()
                { 
                    var userNum1 = document.getElementById("t1").value;
                    m1 = new Math(userNum1);
                    document.getElementById("ans1").innerHTML = "Square of "+userNum1+" is "+Math.square(m1);
                    document.getElementById("ans2").innerHTML = "Cube of "+userNum1+" is "+Math.cube(m1);
                }
                

        </script>
    </body>
</html>
```

# > Create class Account having instance member name , balance . It has method deposit whose job is to increase balance.
Create a child class current account inheriting from Account class. It has method withdraw whose job is to  reduce the balance.
Create two objects of current account and call deposit and withdraw method. Child class has show method whose job is to display
name and new balance.

```
<!DOCTYPE html>
<html>
    <head>
        <title>assignment 4</title>

    </head>
    <body>
        
        <script>

               class Account{
                   constructor(n,b)
                   {
                    if(typeof(n)=="string" && typeof(b)=="number")
                {
                    this.name = n;
                  this.balance = b;
                }
                else{
                    alert("Please Enter Valid Details");
                   
                }

                   }
    
              deposite(amt)
              {
                  this.balance+=amt;
              }
            }

            class account extends Account{

                constructor(nm,bl)
                {
                    super(nm,bl);
                }

                withdraw(amt1)
                {
                    this.balance -= amt1;
                }

                show()
                {
                    var str = "name :"+this.name+"<br/> balance :"+this.balance+"<br/><br/>";
                  document.write(str); 
                }

            }

            user1 = new account("tushar",5000);
          user2 = new account("azhar",6000);
          user1.deposite(5700);
          user2.deposite(90000);
          user1.withdraw(5000);
          user2.withdraw(7890);
          user1.show();
          user2.show();

         

        </script>
    </body>
</html>
```


