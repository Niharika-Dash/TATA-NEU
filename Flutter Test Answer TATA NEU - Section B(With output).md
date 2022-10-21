

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

***var list1 = ['I', '*** ***', 'Flutter'];***

***final list2 = list1;***

***list2[2] = 'Dart';***

***const list3 = list1;***

Ans –

•

•

•

var is a keyword allowing to create a variable without specifying a type. The type

of the variable will be defined according to the initial value of the variable.

final keyword allows to create variables that can only be assigned once at

runtime so it is immutable.

const is also a keyword to create constant values and that variables are implicitly final.

The value of the variable will be known at compile time and it will be constant for the

whole application. const can’t be changed during runtime.

In the above code, list2 will compile because It’s value will be assigned at runtime, but list3

will not compile because list1’s variable is not known at compile time.





