Name: Adrian Echazabal(aechazabal2018@fau.edu) <br>
Florida Atlantic University
# My Full-Stack Homework Repo
## Homework 1 <br>
Setup/Download Git and Github https://git-scm.com/download/win | https://desktop.github.com <br> 
Setup/Download Virtual Studio Code https://code.visualstudio.com/download <br>
Cloned a Calculator from https://mrbuddh4.github.io/calculator/ 
## Homework 2
### Upgraded the Calculator with 4 new Buttons
#### Square Root <br>
A Simple Square Root function that takes in the `displayValue` and then preforms/returns a `Math.sqrt()`. <br>
<img src="./Gifs/Stack Root.gif" width=400 height=600>
<br>Code: <br>
```
  function inputSquareRoot(number) {
    return displayValue = Math.sqrt(number).toFixed(9);
}
```
#### Exponents <br>
A recycled Exponent function that piggybacks the `insertOperator`function to compute and return `X ** Y`<br>
<img src="./Gifs/Stack Exponent.gif" width=400 height=600>
<br>Code: <br>
```
function inputExponent(operator) {
    if(firstOperator != null && secondOperator === null) {
        //4th click - handles input of second operator
        secondOperator = operator;
        secondOperand = displayValue;
        result = operate(Number(firstOperand), Number(secondOperand), firstOperator);
        displayValue = roundAccurately(result, 15).toString();
        firstOperand = displayValue;
        result = null;
    } else if(firstOperator != null && secondOperator != null) {
        //6th click - new secondOperator
        secondOperand = displayValue;
        result = operate(Number(firstOperand), Number(secondOperand), secondOperator);
        secondOperator = operator;
        displayValue = roundAccurately(result, 15).toString();
        firstOperand = displayValue;
        result = null;
    } else { 
        //2nd click - handles first operator input
        firstOperator = operator;
        firstOperand = displayValue;
    }
}
```
#### Factorials <br>
Another Function that preforms Factorial operation on the given `displayValue`.<br>
<img src="./Gifs/Stack Factorial.gif" width=400 height=600>
<br>Code: <br>
```
function inputFactorial(number) {
    
    factorial = 1;
    if (number < 0){
        return displayValue = 'Error';
    }
    else{
        for (num = 2; num<=number; num++){
            factorial = factorial * num
        }
    }
    return displayValue = parseFloat(factorial).toFixed(9);
}
```
#### Pi <br>
A simple function that returns the value of pi into `displayValue`.<br>
<img src="./Gifs/Stack Pi.gif" width=400 height=600>
<br> Code: <br>
```
function inputPi() {        
    return displayValue = 3.1415926;
}
```
