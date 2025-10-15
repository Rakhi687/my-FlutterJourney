                            DART PROGRAMES



 print("hello wolrd");

//   int firstVal=123;

//   print(firstVal.isEven);

 

//   final b=23;

//   const a=111;

//   print(a);

//   print(b);

//   b=123; main.dart:10:3: Error: Can't assign to the final variable 'b'.

//   print(b);

 

 

//    dynamic  c=123;

//   print(c);

//   print(c.runtimeType);

 

//   bool isempty=false;

//   print(isempty);

 

//   if(isempty){

//     print("hello");

 

//   }

//   else {

//     print("hii");

//   }

 

//   for(int i=0;i<10;i++){

//     if(i%2==0){

//       print(i);

//     }

//   }

 

//   int i=0;

//   while(i<=10){

//     print(i);

//     i+=1;

//   }

//   String s= 'Hello';

//   print(s.length);

//   print(s.substring(1,3));

 

//   for(int i=0;i<s.length;i++){

//     print(s\[i]);

//   }

 

//   int i=0;

//   while(i<s.length){

//     print(s\[i]);

//     i+=1;

//   }

 

//   s='${s} \\nbuddies';

//   print(s);







                          **FUNCTION**











  void main() {

 

//   var(name,age,isAdult)=printName();

//   print('name of the student:${name}');

//   print(age);

//   print(isAdult);

// String name='Rakhi';

//   printName(12,name);

//   }

 

//   void printName(){

//     print('HELLO');

//   }



// int printName(){

//   return 123;

// }



// void printName(int age,String name){

//   print(name);

//   print(age);

 }



// (String,int,bool)printName(){

//   return ("Rakhi",12,false);

// }



                  **function**



void main(){

//  printName(name:'Rakhi');

  final data=printName();

  print(data.age);

  print(data.isadult);

  print(data.name);

}





({int age,String name,bool isadult})printName(){

  return (age:12,name:'Rakhi',isadult:false);

}



          **Anonymus function**





void main(){

  final stuff=printStuff();

  stuff();



}

Function printStuff(){

  return (){

    print("hello");

  };

}







 (){

    print("hiiii");

  }();











 

                              **CLASS**







void main(){

 Cookie cookie=Cookie();

  print(Cookie().shape);

//   print(cookie.shape);

  cookie.shape='rectangle';

  cookie.baking();

print(Cookie().shape);

 

}

class Cookie{

  String shape='circle';

  double size=15.3;

  void baking(){

    print('baking is done');

  }

}



                   **constructor**





void main(){

final cookie=Cookie(shape:'circle',size:12);

  print('the shape of the cookie is ${cookie.shape}');

  print(cookie.size);

 

}

class Cookie{

 

  String shape='circle';

  double size=15.3;

 

  Cookie({ required String shape, required double size}){

    this.shape=shape;

    this.size=size;

  }

  void baking(){

    print('baking is done');

  }

}







                       \*\*LIST\*\*















void main(){

  List students=\[Student('Rakesh'),

                         Student('Rakhi'),

                "sakshi"];

//   print(students\[0].name);

 

  final student=students\[2];

  if(student is Student){

    print(student.name);

  }else{

    print("not found");

  }



}

class Student{

  final String name;

  Student(this.name);

}



**output:-not found**





void main() {

  List<Student> students = \[

    Student('Rakesh'),

    Student('Rakhi'),

    Student("sakshi")

  ];



  print(students);

}



class Student {

  final String name;

  Student(this.name);



  @override

  String toString() => 'Student(name: $name)';

}



**\[Student(name: Rakesh), Student(name: Rakhi), Student(name: sakshi)]**







print(students);

  students.add(Student("Naman"));

  students.insert(0,Student("Rivan"));

  print(students);

  students.removeAt(2);

  print(students);

print( students.length);





**\[Student(name: Rakesh), Student(name: Rakhi), Student(name: sakshi)]**

**\[Student(name: Rivan), Student(name: Rakesh), Student(name: Rakhi), Student(name: sakshi), Student(name: Naman)]**

**\[Student(name: Rivan), Student(name: Rakesh), Student(name: sakshi), Student(name: Naman)]**

**3**





 List<Student> filteredStudent=\[];

 

  for(int i=0;i<students.length;i++){

    if(students\[i].marks>300){

      filteredStudent.add(students\[i]);

    }

  }

  print(filteredStudent);





**\[Student(name: Maya)]**





for( final student in students){

    if(student.marks>300){

 

      filteredStudent.add(student);

    }

 

  }

   print(filteredStudent);

 }



**\[Student(name: Maya)]**







final filteredStudent=students.where((student)=>student.marks>300);

  print(filteredStudent);

  print(filteredStudent.toList());

  print(students.reversed);

  print(students.contains);

    print(students.firstWhere);





**Maya**

**(Student(name: Maya), Student(name: Maya))**

**\[Student(name: Maya), Student(name: Maya)]**

**(Student(name: Maya), Student(name: Maya), Student(name: priya), ..., Student(name: Rakhi), Student(name: Rakesh))**

**Closure: (Object?) => bool from: (...args) => context\[property](...args)**

**Closure: ((Student) => bool, {Object? orElse}) => Student from: (...args) => context\[property](...args)**





               \*\*SET\*\*







void main() {

 

  final mayastudent=Student("Maya",350) ;

  Set<Student> students = {

    Student('Rakesh',10),

    Student('Rakhi',20),

    Student("sakshi",30),

     Student('priya',120),

    mayastudent,mayastudent

    };



 final filteredStudent=students.where((student)=>student.marks>300);

 print(filteredStudent.toList());

  print(filteredStudent.toSet());



}

 



class Student {

  final String name;

######   final int marks;

  Student(this.name,this.marks);



  @override

  String toString() => 'Student(name: $name)';

}





**\[Student(name: Maya)]**

**{Student(name: Maya)}**







                      \*\*map\*\*







void main(){

  Map<String,int> marks={

    "rakhi":120,

    "Sakshi":13,

    "milan":56

  };

 

  for(int i=0;i<marks.length;i++){

    print('${marks.keys.toList()\[i]}:${marks.values.toList()\[i]}');

  }

}





**rakhi:120**

**Sakshi:13**

**milan:56**





 marks.forEach((key,val){

    print('$key : $val');

  });



**rakhi : 120**

**Sakshi : 13**

**milan : 56**



**converting from map to list**



  List<Map<String,int>> marks=\[{

    "rakhi":120,

    "Sakshi":13,

    "milan":56

 

  },{

    "rakhi":120,

    "Sakshi":13,

    "milan":56

  },

   marksA ];





marks.map((e){

  print(e);

}).toList();

}







**{rakhi: 120, Sakshi: 13, milan: 56}**

**{rakhi: 120, Sakshi: 13, milan: 56}**

**{rakhi: 120, Sakshi: 13, milan: 56}**







marks.map((e){

 e.forEach((key,val){

   print('$key:$val');

 });

}).toList();

}





rakhi:120

Sakshi:13

milan:56

rakhi:120

Sakshi:13

milan:56

rakhi:120

Sakshi:13

milan:56









                     **ENUM**



void main(){

 

  final emp1=Employee('rakhi',EmployeeType.finance);

  final emp2=Employee('Sakshi',EmployeeType.python);

  emp1.fun();

  emp2.fun();

 

}

enum EmployeeType{

  swe,finance,python

}

class Employee{

   final String name;

   final EmployeeType type;

  Employee(this.name,this.type);



  void fun(){

    switch(type){

      case EmployeeType.swe:

        print('software engineer');

      case EmployeeType.finance:

        print("finance department");

       case(EmployeeType.python):

          print('python department');

 

      default:

        print('something went wrong');

    }

  }

}







**finance department**

**python department**









&nbsp;                      \*\*Future\*\*


**void main() async{**



**print('helloooo');**

**final res= await giveResult();**

**print(res);**

**}**



**Future<String> giveResult(){**

**return Future.delayed(Duration(seconds:2),()async{**

&nbsp;   \*\*return 'hey!!!';\*\*


**});**



**}**







       helloooo(after 2sec is will print heyy)

hey!!!

