In OOPs, we create classes and objects to solve real world problems.


Class - Classes are user defined data dypes, which is the blueprint or the design of an object. When we create a class we create a copy to the class.
The class contains data members(varaibles and methods) which can be either private, public or protected. The acccess modifier explains the scope of the variable or data members.
Eg-
class Student{
  public:
     int rollNumber;
     int age;
     void display(){
       cout<<age<<" "<<rollNumber;
     }
};

Once the class is designed, objects are created to use the functionality of the data the data members of the class.4
Objects can be made using various methods.
Objects are made either statically or dyanmically.
Eg-

Student s1; // creating object statically   (s1 is the object that holds properties of class Student, object s1 creates a memory block of 8 bytes)
Student *s2 = new Student;   // creating object dynamically  (*s2 is the pointer variable to a memory location which has properties of class Student, which means s2 holds adress to the object)

Getters and Setters-
In an class, a private varaible can not be accessed using the object directly which is outside the class. To access the private variable we use public function or called as getters and setters.
Eg-
class Student{
  private:
     int age;
  public:
     int rollNumber;
     void display(){
       cout<<age<<" "<<rollNumber<<endl;
     }
     int getAge(){   //Getter
       return age;  //Accessing private variable age, which can be called through object.
     }
     void setAge(int a){ //Setter
       age = a;   //Accessing private variable age, which can be called through object.
     }
};


Constructors-
Constructors is a block of code used to initialize an object. Constructor is same name as the class name. It has no return type and when constructor is not created, a default constructor is called.
A deault constructor initializes the object with default values. A contructor is invoked when an object is created.

Eg -
int main(){
   Student s1; // Student s1 object is created and it calls default constructor with the defualt values.
   Student s2(12, "Ravi");   //Student s2 object is created and it calls parametrized constructor.
}

this keyword - this holds the address of current object.

Copy Constructor - When an object is created passing an already existing object as its parameter, then all the properties of the passed object is copied to the new object.

Eg- 
Student s1(101, 10001)
Student s2(s1);  //Copy Constructor(s2 is a copy of s1)

Student *s3 = new Student(20, 200001);
Student s4(*s3); //Copy Constructor(s4 is a copy of s3)


Copy Assignment Operator - This operator copies all properties of an object to another object.

Eg - 
Student s1(101, 10001)
Student s2 = s1; //Copies all properties of s1 to s2


Destructor - It has the same name as the class name and has no return type. 
A destructor deallocates memory when it is called, but can not deallocate dynamically allocated memory.


