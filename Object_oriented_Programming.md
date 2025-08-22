# Object Oriented Programming concepts
&rarr;&nbsp; This concepts are used to represents the real world objects into a program.<br>
&rarr;&nbsp;The real world objects can be recoginzed by its properties and behaviors.<br>
&rarr;&nbsp;This properties of a **object** are represented as    **"Global variables"** and **behaviours** are represented as **"Methods"**.<br>
&rarr;&nbsp;If the properties are changing from object to object then we ha sto declared them as **"non static global variables"**, if they are common to all the objects then we have to declared them as **"static global variables"**.<br>
&rarr; If a method is using any non static property then it is recommended to declare the method as **"Non-static "** other wise it declare it as **"Static"**.<br>

---
### Real World Objects
#### Car: 
 - Properties: <br>
 &rarr;&nbsp;**Brand**<br>
 &rarr;&nbsp;**Cost**<br>
 &rarr;&nbsp;**Color**<br>
 
 - Behavior :<br>
 &rarr;&nbsp;**Start( )**<br>
 &rarr;&nbsp;**Accelerate( )**<br>
 &rarr;&nbsp;**Brake( )**<br>
 &rarr;&nbsp;**Stop( )**<br>
 &rarr;&nbsp;**Drift( )**<br>
 
 ## Program Representation  
 ```
 class Car{
                                         // Properties
    String branch;
    double cost;
    String color;

    public void Start(){                       // Behaviour
        System.out.println("Car Start");
    }
    public void Accelerate(){                 // Behaviour
        System.out.println("Car Start");
    }
    public void Break(){                     // Behaviour
        System.out.println("Car Start");
    }
    public void Stop(){                      // Behaviour
        System.out.println("Car Start");
    }
    public void Drift(){                    // Behaviour
        System.out.println("Car Start");
    }

    public static void main(String[]args){
        // First object creation

            car c1=new car();
            c1.brand="BMW";
            c1.cost=1000000;
            c1.color="black";

        // second object creation
            car c2=new car();
            c2.brand="tata";
            c2.cost=500000;
            c2.color="blue";
    }
 }

 ```

<h2>Class : </h2>

&rarr; Class is a keyword which is used to create a non premitive datatype.<br>
&rarr; Class is a logical entity which behaves as a blue print of an object.

## Object :

&rarr; Object is a huge memory block which is used to store the  non-static members.<br>
&rarr; Object is a real entity which is mirror image of a blue print class.<br>
&rarr; Object is a instance of class.<br>

#### Example program :-
#### Blueprint class : ####
```
 
class Mobile { //Blue print (or) business logic class
    String brand;
    double cost;
    String color;
    int RAM,ROM;

public void calling(){
    System.out.println("calling");
}
public void Chatting(){
    System.out.println("Chatting");
}
public void Playing(){
    System.out.println("Playing");
}
public void Watching(){
    System.out.println("Watching");
}
public void Clickingpics(){
    System.out.println("Selfies");
}
public void details(){
    System.out.println("Brand :"+Brand);
    System.out.println("Cost :"+Cost);
    System.out.println("color :"+Color);
    System.out.println("ROM :"+ROM);
    System.out.println("RAM :"+RAM);
    }
}

```
The above program is a blue print for the mobile and that can calling by the **Mobile store** class .
#### user-logic class : ####
```
class MobileStore{ //user logic (or) Control-logic class
    public static void main(String[]args){
        Mobile m1=new Mobile()
        m1.branch="Nokia";
        m1.cost=24000;
        m1.color="blue";
        m1.ROM=128;
        m1.RAM=8;
        m1.details();
        System.out.println("-----------------------")

        Mobile m2=new Mobile()
        m2.branch="realme";
        m2.cost=20000;
        m2.color="black";
        m2.ROM=256;
        m2.RAM=12;
        m2.details();
    }

}
```

### Find the maximum marks in between 3 students ###
```
// Blue print class

class Students {
    int id;
    String name;    
    double marks;

    public void details() {
        System.out.println("Id: " + id);
        System.out.println("Name: " + name);
        System.out.println("Marks: " + marks);
}
	public static void main(String[]args){
	System.out.println("Hello");
	}
}

// user logic class

class School {
    public static void main(String[] args) {
        Students s1 = new Students();
        s1.id = 100;
        s1.name = "balu";
        s1.marks = 36.26;

        Students s2 = new Students();
        s2.id = 101;
        s2.name = "ramesh";
        s2.marks = 62.26;

        Students s3 = new Students();
        s3.id = 102;
        s3.name = "mahesh";
        s3.marks = 45.26;

        Students max = max(s1, s2, s3);
        max.details();
    }

    public static Students max(Students s1, Students s2, Students s3) {
        Students max;
        if (s1.marks > s2.marks && s1.marks > s3.marks)
            max = s1;
        else if (s2.marks > s3.marks)
            max = s2;
        else
            max = s3;
        return max;
    }
}
```
### Find the minimum marks in between 3 students ###
```
// Blue print class 
class Students {
    int id;
    String name;    
    double marks;

    public void details() {
        System.out.println("Id: " + id);
        System.out.println("Name: " + name);
        System.out.println("Marks: " + marks);
    }
}

// User-logic class

class School {
    public static void main(String[] args) {
        Students s1 = new Students();
        s1.id = 100;
        s1.name = "balu";
        s1.marks = 36.26;

        Students s2 = new Students();
        s2.id = 101;
        s2.name = "ramesh";
        s2.marks = 62.26;

        Students s3 = new Students();
        s3.id = 102;
        s3.name = "mahesh";
        s3.marks = 45.26;

        Students min = min(s1, s2, s3);
        min.details();
    }

    public static Students min(Students s1, Students s2, Students s3) {
        Students min;
        if (s1.marks < s2.marks && s1.marks < s3.marks)
            min = s1;
        else if (s2.marks > s3.marks)
            min = s2;
        else
            min = s3;
        return min;
    }
}
```
### Find the second maximum marks of the 3 students ###
``` 
// blue print class

class Students {
    int id;
    String name;    
    double marks;

    public void details() {
        System.out.println("Id: " + id);
        System.out.println("Name: " + name);
        System.out.println("Marks: " + marks);
    }
}

//user-logic class

class School {
    public static void main(String[] args) {
        Students s1 = new Students();
        s1.id = 100;
        s1.name = "balu";
        s1.marks = 36.26;

        Students s2 = new Students();
        s2.id = 101;
        s2.name = "ramesh";
        s2.marks = 62.26;

        Students s3 = new Students();
        s3.id = 102;
        s3.name = "mahesh";
        s3.marks = 45.26;
	Students secmax =secmax(s1,s2,s3); // second max method calling
	secmax.details(); // calling the details method in Students
	
// maxium marks method

}
   public static Students max(Students s1, Students s2, Students s3) {
        Students max=null;
        if (s1.marks > s2.marks && s1.marks > s3.marks)
            max = s1;
        else if (s2.marks > s3.marks)
            max = s2;
        else
            max = s3;
        return max;
    }

    // minimum marks method

public static Students min(Students s1, Students s2, Students s3) {
        Students min;
        if (s1.marks < s2.marks && s1.marks < s3.marks)
            min = s1;
        else if (s2.marks > s3.marks)
            min = s2;
        else
            min = s3;
        return min;
    }

// Second max method

public static Students secmax(Students s1,Students s2,Students s3){
	double secmax=(s1.marks+s2.marks+s3.marks)-(max(s1,s2,s3).marks+min(s1,s2,s3).marks);
	if(secmax==s1.marks)
		return s1;
	if(secmax==s2.marks)
		return s2;
	return s3;
	}
}
```
### Find all the employees whose salary is greater than average salary and print their details ###
```
class Employee{
	int id;
	String name;
	double salary;

	public void details(){
		System.out.println("id :"+id);
		System.out.println("Name :"+name);
		System.out.println("Salary :"+salary);
	}
}

class Office{
	public static void main(String[]args){
		Employee e1= new Employee();
		e1.id=100;
		e1.name="suresh";
		e1.salary=45000;

		Employee e2= new Employee();
		e2.id=101;
		e2.name="ramesh";
		e2.salary=37000;

		Employee e3= new Employee();
		e3.id=102;
		e3.name="raghu";
		e3.salary=28500;

		Employee e4= new Employee();
		e4.id=104;
		e4.name="jyothi";
		e4.salary=27000;

		Employee e5= new Employee();
		e5.id=104;
		e5.name="praveent";
		e5.salary=56000;
		
		AverageSalary(e1,e2,e3,e4,e5);
		
	}


	public static void AverageSalary(Employee e1,Employee e2,Employee e3,Employee e4,Employee e5){
		double avgsal=(e1.salary+e2.salary+e3.salary+e4.salary+e5.salary)/5;
			if(e1.salary>avgsal)
				e1.details();
			if(e2.salary>avgsal)
				e2.details();
			if(e3.salary>avgsal)
				e3.details();
			if(e4.salary>avgsal)
				e4.details();
			if(e5.salary>avgsal)
				e5.details();
	
	}	
}
```




