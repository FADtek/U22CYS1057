// create a Scanner object for user input
Scanner input = new Scanner(System.in);

// declare variables to store two digit numbers and the operator
int num1, num2;
char op;

// prompt the user to enter the first number
System.out.println("Enter the first two digit number:");
num1 = input.nextInt();

// validate the input
while (num1 < 10 || num1 > 99) {
  System.out.println("Invalid input. Enter a two digit number:");
  num1 = input.nextInt();
}

// prompt the user to enter the second number
System.out.println("Enter the second two digit number:");
num2 = input.nextInt();

// validate the input
while (num2 < 10 || num2 > 99) {
  System.out.println("Invalid input. Enter a two digit number:");
  num2 = input.nextInt();
}

// prompt the user to enter the operator
System.out.println("Enter the operator (+, -, *, /):");
op = input.next().charAt(0);

// validate the input
while (op != '+' && op != '-' && op != '*' && op != '/') {
  System.out.println("Invalid input. Enter a valid operator (+, -, *, /):");
  op = input.next().charAt(0);
}

// close the Scanner object
input.close();

// declare a variable to store the result
int result = 0;

// use a switch statement to perform the calculation based on the operator
switch (op) {
  case '+':
    result = num1 + num2;
    break;
  case '-':
    result = num1 - num2;
    break;
  case '*':
    result = num1 * num2;
    break;
  case '/':
    result = num1 / num2;
    break;
}

// display the result
System.out.println(num1 + " " + op + " " + num2 + " = " + result);
