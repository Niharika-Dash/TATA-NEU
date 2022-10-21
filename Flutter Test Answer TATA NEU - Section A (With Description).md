

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

