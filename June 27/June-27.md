QUESTION 1
- SYNTAX: Arrow function doesn't have a curly braces around a single element/expression and it enables developers to write a concise function in javascript.

Regular Function:
let parents = (mother, father) {return mother + father};

Arrow Function:
let parents = (mother, father) => mother + father;

- ARGUMENTS OBJECTS: Regular function has arguments objects while arguments objects are not present in Arrow function.

Regular Function:
let objectArguments = {
    showArg: ()function{
        console.log(arguments);
    }
}
objectArguments.showArg(1,2,3,4,5)

Arrow Function:
let objectArguments = {
    showArg:()=>console.log(arguments)
}
objectArguments.showArg(1,2,3,4,5)

- USING A NEW KEYWORD: Regular functions are callable and constructible while Arrow functions are only callable but not constructible i.e they can not be used as a constructor function.

Regular Function:
let reg = function(a, b) {
    console.log (a + b)
}
new reg (5, 10);

Arrow Function:
let reg = (a, b) => console.log(a+b);
new reg (5, 10)

- NO DUPLICATE NAMED PARAMETERS: Arrow functions can never have duplicate named parameters, whether in strict or non-strict mode while diuplicate can be used to name parameters for regular function in non-strict mode.


QUESTION 2
A closure gives you access from an inner function scope to an outer function. Closure occurs when a Javascript function is nested inside another.
Example:
function outerFunction(){

	const outerVariable = "Outer variable";

    function innerFunction(){

    	const innerVariable = "Inner variable";

    	console.log(outerVariable);

    	console.log(innerVariable);

    }

    return innerFunction;

}

Hoising allows you to refer to Javascript function and variables before they are being created.
Example:
printHello();

function printHello(){

	console.log('Hello');

}

* Another important concept to understand with respect to variable hoisting is that it only works with the var keyword. If you attempt to hoist a variable with the const or let keyword, your browser will return an error message.(#This is not clear)

QUESTION 3
Pure function is a function that's predictable and has no side effect while an Impure function is a function that's unpredictable and has one or more side effects.


QUESTION 4
- Pure function is independent, it gives thesame output for thesame input parameters while Impure functions give different outcomes when we pass thesame arguments multiple times.
- Pure function is easy to debug while Impure function is not easy to debug.
- Pure readable and easy to understand but Impure functions can cause some confusion in more extensive systems in the form of spaghetti code.
- Pure function can execute AJAX calls or standard DOM Manipulation.

QUESTION 5 
Pure function is predictable while impure function is not.
Example of Pure function:
function add(x, y) {
    return x+y
}
console.log(add(3,2))

Example of Impure function:
function add(x, y){
    let random = Math.random()*10
    return x+y+random
}
console.log(add(2*5))

Pure function has no side effect while an Impure function has side effect.
Example of Pure function:
let globalNumber= 1
function add (x, y){
    return x + y + globalNumber
}
console.log(add(2, 2))

Example of Impure function:
let globalNum=1
function add(x, y){
    let globalNum = 0
    return x + y + globaNum
}
console.log(add(2, 3))



