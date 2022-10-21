

**Section A**

***1. Can we nest the Scaffold widget? Why or Why not?***

Ans – Yes, we can nest the Scaffold widget, but It’s not a good practice to do so.

Because using a single Scaffold means the parent BLoC has to have full knowledge of

child BloCs. With nested Scaffolds, each child can build its own screen. Generally, we use

a single global Scaffold in main.dart to show global snackbars.

***2. What are the different ways we can create a custom widget ?***

Ans – Custom Widget is the widget which is designed by the user according to the design

requirement. By creating Custom widget we can make it easier to add the same

functionality through out the code which also saves development time, and also testing

is made easy by using same component multiple times.

Example –

class CustomTextField extends StatelessWidget {

String text = "";

double fontSize = 0;

CustomTextField({

required this.text,

required this.fontSize,

Key? key,

}) : super(key: key);

@override

Widget build(BuildContext context) {

return TextField(

style: TextStyle(fontSize: fontSize,

fontStyle: FontStyle.italic,

color: Colors.black),

decoration: InputDecoration(

hintText: text,

hintStyle: TextStyle(fontSize: fontSize,

fontStyle: FontStyle.italic,

color: Colors.black),

),

);

}

}





This CustomTextField we can use in multiple places without rewriting the whole code

again and again.

Let’s use it inside the body of a project inside a column

body: Center(

child: Column(

mainAxisAlignment: MainAxisAlignment.center,

children: [

CustomTextField(text:"Enter email id", fontSize: 20),

CustomTextField(text:"Enter password", fontSize: 20),

],

),

),

***3. How can I access platform(iOS or Android) specific code from Flutter?***

Ans - Flutter provides a flexible system to access platform-specific features

of Android or IOS.

We can access platform-specific functionality like device information, sensors,

battery, device camera, battery level, open browser, etc using flutter platform

channels.

Flutter dart code sends messages to its host(Android or IOS) over a platform channel.

Host(Android or IOS) listens on the platform channel and receives the message. It then calls

into any number of platform-specific APIs using the native programming language and

sends a response back to the *client (Flutter dart code)*.

***4. What is BuildContext? What is its importance?***

Ans - BuildContext is a locator that is used to track each widget in a tree and locate

them and their position in the tree. The BuildContext of each widget is passed to their

build method. The build method returns the widget tree a widget renders. Each

BuildContext is unique to a widget.

**Section B**

***1. Refactor the code below so that the children will wrap to the next line***

***when the display width is small for them to fit.***

***class LongStringWidget extends StatelessWidget {***





***@override***

***Widget build(BuildContext context) {***

***return Row(***

***children: [***

***Chip(***

***label: Text(***

***'I',***

***),***

***),***

***Chip(***

***label: Text(***

***'am',***

***),***

***),Chip(***

***label: Text(***

***'looking',***

***),***

***),Chip(***

***label: Text(***

***'for',***

***),***

***),Chip(***

***label: Text(***

***'a',***

***),***

***),Chip(***

***label: Text(***

***'job',***

***),***

***),Chip(***

***label: Text(***

***'and',***

***),***

***),***

***Chip(***

***label: Text(***

***'I',***

***),***

***),Chip(***

***label: Text(***

***'need',***

***),***

***),Chip(***

***label: Text(***

***'a',***





***),***

***),***

***Chip(***

***label: Text(***

***'job',***

***),***

***),***

***],***

***);***

***}***

***}***

Ans – In this code only we need to replace the Row with Wrap, so that the children will wrap

to the next line if the display width is small for them to fit.





***2. Identify the problem in the following code block and correct it***.

***String LongOperationMethod() {***

***var counting = 0;***

***for (var i = 1; i <= 1000000000; i++) {***

***counting = i;***

***}***

***return '$counting! times I print the value! ';***

***}***

Ans – There is not any error in the above code but we should write the method name in

lower camel case i.e longOperationMethod()

String longOperationMethod() {

var counting = 0;

for (var i = 1; i <= 1000000000; i++) {

counting = i;

}

return '$counting! times I print the value!';

}





***3. In the below code, list1 declared with var, list2 with final and list3 with***

***const. What is the difference between these lists? Will the last two lines***

***compile?***

***var list1 = ['I', 'ꢀ', 'Flutter'];***

***final list2 = list1;***

***list2[2] = 'Dart';***

***const list3 = list1;***

Ans –

·

·

·

var is a keyword allowing to create a variable without specifying a type. The type

of the variable will be defined according to the initial value of the variable.

final keyword allows to create variables that can only be assigned once at

runtime so it is immutable.

const is also a keyword to create constant values and that variables are implicitly final.

The value of the variable will be known at compile time and it will be constant for the

whole application. const can’t be changed during runtime.

In the above code, list2 will compile because It’s value will be assigned at runtime, but list3

will not compile because list1’s variable is not known at compile time.

