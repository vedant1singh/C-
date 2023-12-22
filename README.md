In OOPs, we carete classes and objects to solve real world problems.


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
