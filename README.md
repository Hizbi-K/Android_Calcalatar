# Android_Calcalatar

<p align="center">
  <img src="Images_Readme\Calcalatar_Banner.png" />
</p>

# Introduction

This is a simple calculator based upon the Windows 10 default calculator. The app is written in Java and works on devices with Android 5.0 (Lollipop) and higher.

Note: This app doesn't use parser to solve mathematical operations. Instead it takes two operands (or a single operand in case of unary operator) and an operator and performs the respective operation.

# How it works

Since their is no expressionn parsing involved, the calculation is done by manipulating the strings. The number stored in the 'Result' textView is converted aand stored in a string when the user types the number and presses an operator button. The second operand is obtained  when the user enters the number and presses the '=' button.

The two operands stored in the strings are first converted into 'Double' datatype and a 'Switch' statement is applied on the operator string. The respective operation is then performed on the operands and the result is stored in a double which is converted then converted into string to be shown in the 'Result' textView. Unary operators work similarly but require only one operand.

Division by zero (math error) is also handled and it prints a 'Toast' message to the user without crashing the app. 

The textView above the 'Result' textView shows the complete expression while 'Result' textView shows the result upto 15 digits.

# Features

1. BackSpace can be used to erase the previous digit.

2. Clear button clears all of the fields and resets the calculator. For now, Clear Entry button also does the same thing (It should actually erase the previous number entry in the expression).
3. Percentage (%) button works as in the Windows 10 calculator. Example: 9 + 8% = 9 + (8% of 9) which is the same as 9+(9*8/100). Note: Multiplication/Division is handled differently here.
4. Negation button negates the number entry, or removes the previous negation.
5. Decimal Point button inserts the decimal point and works as intented.

# ScreenShots

<p align="center">
  <img src="Images_Readme\Calcalatar_Features_Banner.png" />
</p>

<p align="center">
  Features
</p>

# Layout

<p align="center">
  <img src="Images_Readme\Calcalatar_Design_Blueprint.png" />
</p>

<p align="center">
  Constrained Layout
</p>

Constraint Layout is used throughout to design and arrange the UI elements. The buttons and textViews are chained together and then constrained to the whole screen.

This makes the layput stable from one device size to another without crafting seperate layouts for each screen size.

# onClick Funtions

The app uses separate onClick funtions for each group of buttons. The buttons are grouped as:

1. Number buttons

2. Binary Operator buttons
3. Unary Operator buttons
4. Clear/Clear Entry buttons
5. isEqualTo '=' button
6. BackSpace button
7. Decimal Point button
8. Negation button

# Improvements

The next best feature to add is the ability to parse expressions having multiple operators. This can be done either manually by using stacks and a 'PostFix' algorithm, or by using a library such as Mariusz Gromada's 'mXparser' library. 

Other features that can be added are calculation history/memory and customizable themes. 