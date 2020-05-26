## Create class Employee which has instance member id, name , salary, net salary.
## Also Write getter setter for each instance member.Write calculate net salary functionwhose job is to calculate net salary after deduction of 10 % TDS. Create 2 objects of the class and call method.



```
<!DOCTYPE html>
<html>
    <head>
        <title>Object Assignment</title>
      
    </head>
    <body>

        <script>
            
            class Employee{
                constructor(i,n,s)
                {
                    if(typeof(i)=="number" && typeof(n)=="string" && typeof(s)=="number")
                     {
                         this.id = i;
                         this.name = n ;
                         this.salary = s;
                         this.netSalary = null;
                    }else{
                    alert("Please Enter Valid Details");
                    }
                }


                //getters
                get getId()
                {
                    return this.id;
                }

                get getName()
                {
                    return  this.name;
                }

                get getSalary()
                {
                   return this.salary;
                }

                get getNetSalary()
                {
                    return this.netSalary;
                }

                
                //setters
                set setId(i1)
                {
                    if(typeof(i1)=="number")
                    {
                        this.id = i1;
                    }
                    else
                    {
                        alert("please enter valid id");
                    }
                    
                }

                set setName(n1)
                {
                    if(typeof(n1)=="string")
                    {
                        this.name = n1;
                    }
                    else
                    {
                        alert("please enter valid name");
                    }
                    
                }

                set setSalary(s1)
                {
                    if(typeof(s1)=="number")
                    {
                        this.salary = s1;
                    }
                    else
                    {
                        alert("please enter valid salary");
                    }
                    
                }

                //method to calculate net salary
                calculateNetSalary()
                {
                    let TDS = 0.1;
                    this.netSalary = this.salary - (TDS*this.salary);
                }

                show()
                {
                    if(this.netSalary!=null)
                    {
                    document.write("-------Employee Details--------<br/>");
                    document.write("ID: "+this.id);
                    document.write("<br/>Name: "+this.name);
                    document.write("<br/>Salary: "+this.salary);
                    document.write("<br/>Net Salary: "+this.netSalary+"<br/><br/>");
                    }else{
                        alert("please calculate net salary of "+this.name);
                    }

                }
            }

            e1 = new Employee(1,"Tushar",15000);
            e2 = new Employee(2,"Azhar",20000);
            e1.setSalary = 18000;
            e1.calculateNetSalary();
            e1.show();
            e2.calculateNetSalary();
            e2.show();  

        </script>
    </body>
</html>
```

## Create class student which has instance member roll number, name, marks1,marks2,marks3, total, percentage.
## Write getter setter for roll number, name and marks1,marks2,marks3. Write a method to calculate total and  percentage
  
  ```
  <!DOCTYPE html>
<html>
    <head>
        <title>Assignment Que 2</title>
       
    </head>
    <body>
    
        <script>
            class Student{
                constructor(r,n,m1,m2,m3)
                {
                    if(typeof(r)=="number" && typeof(n)=="string" && typeof(m1)=="number" && typeof(m2)=="number" && typeof(m3)=="number")
                    {
                        this.rollNumber = r;
                        this.name = n;
                        this.marks1 = m1;
                        this.marks2 = m2;
                        this.marks3 = m3;
                        this.total = null;
                        this.percentage = null;
                    }else{
                        alert("please enter valid deatils");
                    }
                }
//getters
                get getRollNumber()
                {
                    return this.rollNumber;
                }

                get getName()
                {
                    return this.name;
                }

                get getMarks1()
                {
                    return this.marks1;
                }

                get getMarks2()
                {
                    return this.marks2;
                }

                get getMarks3()
                {
                    return this.marks3;
                }
//setters
                set setRollNumber(r1)
                {
                    if(typeof(r1)=="number")
                    {
                        this.rollNumber =r1;
                    }
                    else{
                        alert("please enter valid detail");
                    }
                   
                }

                set setName(n1)
                {
                    if(typeof(n1)=="string")
                    {
                        this.name=n1;
                    }
                    else{
                        alert("please enter valid detail");
                    }
                    
                }

                set setMarks1(tm1)
                {
                    
                    if(typeof(tm1)=="number")
                    {
                        this.marks1 = tm1;
                    }
                    else{
                        alert("please enter valid detail");
                    }
                }

                set setMarks2(tm2)
                {
                     
                     if(typeof(tm2)=="number")
                    {
                        this.marks2 = tm2;
                    }
                    else{
                        alert("please enter valid detail");
                    }
                }

                set setMarks3(tm3)
                {
                    if(typeof(tm3)=="number")
                    {
                        this.marks1 = tm3;
                    }
                    else{
                        alert("please enter valid detail");
                    }
                    
                }
//method to calculate total

                calculateTotalMarks()
                {
                    this.total = this.marks1 + this.marks2 + this.marks3;
                }

//method to calculate percentage
                calculatePercentage()
                {
                    if(this.total!=null)
                    {
                    this.percentage  = (this.total/300)*100;
                    }
                    else{
                        alert("Please calculate total marks")
                    }
                }
                show()
                {
                    if(this.total==null)
                    {
                        alert("Please calculate total marks of "+this.name);
                    }

                    if(this.percentage==null)
                    {
                        alert("Please calculate percentage of "+this.name);
                    }
                    document.write("-------Student Details-----");
                    document.write("<br/>Roll Number: "+this.rollNumber);
                    document.write("<br/>Name: "+this.name);
                    document.write("<br/>Marks 1: "+this.marks1);
                    document.write("<br/>Marks 2: "+this.marks2);
                    document.write("<br/>Marks 3: "+this.marks3);
                    document.write("<br/>Total Marks: "+this.total);
                    document.write("<br/>Percentage: "+this.percentage+"%<br/><br/>");
                }
            }

            s1 = new Student(1,"Tushar",81,90,78);
            s1.setName = "Tushar Dhage";
            s1.setMarks1 = 91;
            s1.calculateTotalMarks();
            s1.calculatePercentage();
            s1.show();

            s2 = new Student(2,"Azhar",66,78,89);
            s2.calculateTotalMarks();
            s2.calculatePercentage();
            s2.show();
            
        </script>
    </body>
</html>
```
