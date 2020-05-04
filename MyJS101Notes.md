# My JS101 Notes
# Metin USLU - 2020


// Create Variables
var v1 = 15;
var v2 = 30;
var v3 = 45;

alert("Sum of Variables:" + (v1 + v2 + v3));

// Create Array
var array = ["Python", "Java", "C", "C++", "GO"];

alert(array[0]);
alert(array[1]);
alert(array[2]);
alert(array[3]);
alert(array[4]);

array[5] = "Scala";
array.push("Scala")

alert(array);
alert(array.lenght);


// For Loops
for (var i=0; i<10; i++){
	console.log("i Values:" + i)
}

// While Loops
var i = 0;
while(i<=50){
	console.log("i values:" + i)
	i+2;
}

// Examples
var numbers = [32, 51, 100, -1, 13, 19]
console.log("Array Elements");
for (var i=0; i<numbers.lenght; i++){
	console.log("Element:" + numbers[i]);
}


numbers.forEach(function(number){
	console.log("Element:" + number);
});

// Conditional Statement
// If Conditional
var a = 5;
var b = 6;

if (a == b){
	console.log("Equal");
	}
	
if (a != b){
	console.log("Not Equal");
	}
	
if (2 == "2"){
	console.log("Equal");
	}
	
if (2 === "2"){
	console.log("Equal");
	}
	
if (2 == 2 && "ABC" == "ABC"){
	console.log("Equal);
	}
	
if (2 == 2 || "ABC" == "ABD"){
	console.log("Equal);
	}

if (!(4 < 3)){
	console.log("Not True");
}

// if else if
var a = 5;
var b = 15;

if (a == b){
	console.log("Equal");
}
else{
	console.log("Not Equal")
}


var operation = 2;

if (operation == 1 ){
	console.log("Operation 1");
}
else if(operation == 2){
	console.log("Operation 2");
}
else if(operation == 3){
	console.log("Operation 3");
}
else{
	console.log("Invalid Operation");
}


// Switch Case Statement
var operation = 3;

switch(operation){
	case 1:
		console.log("Operation 1");
		break;
	case 2:
		console.log("Operation 2");
		break;
		
	case 3:
		console.log("Operation 3");
		break;
	default:
		console.log("Invalid Operation")
}


// Create Function

function sayhello(){
	console.log("Hi There");
}

sayhello()


function sayhello(name){
	console.log("Hi " + name);
}

sayhello("Metin USLU");


function sum_numbers(a, b, c){
	console.log("Sum of Values: " + (a+b+c))
}

sum(3,4,5)


function sum_numbers(a,b,c){
	return a+b+c;
}

var sum = sum_numbers(3,4,5)

console.log("Sum of Numbers:" + sum)


// Object Based

var employee = {
	name:"Metin",
	surname:"Uslu",
	number:123456,
	prog_lang:["Php", "Java", "C++"]
};

console.log(employee.name);
console.log(employee.surname);
console.log(employee.prog_lang);



var employee = {
	name:"Metin",
	surname:"Uslu",
	number:123456,
	prog_lang:["Php", "Java", "C++"],
	address:{
		street:"Eryaman",
		neighborhood:"1453"
	}
};

console.log(employee.address);
console.log(employee.address.street);
console.log(employee.address.neighborhood);



var employee = {
	name:"Metin",
	surname:"Uslu",
	number:123456,
	prog_lang:["Php", "Java", "C++"],
	address:{
		street:"Eryaman",
		neighborhood:"1453"
	},
	personInfo:function(){
		return "Person Name: " + this.name + "Person Surname: " + this.surname
		}
	
};

console.log(employee.personInfo());



var employee = new Object();

employee.name="Metin";
employee.surname="Uslu";

employee.personInfo=function(){
return this.name + this.surname
};


console.log(employee.name);
console.log(employee.surname);
console.log(employee.personInfo());


function Employees(name, surname, pid){
	this.name = name;
	this.surname = surname;
	this.pid = pid;
	this.showInfo = function(){
		return "Name:" + this.name + "\nSurname:" + this.surname + "\nPersonId:" + this.pid;
	}
}

var employee1 = new Employees("Metin", "Uslu", 1234567);

var employee2 = new Employees("Ali", "Karaca", 987654);

console.log(employee1)

console.log(employee2)