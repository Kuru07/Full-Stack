[[JAVASCRIPT]]
-> In Javascript semi-colons( ';') are optional.
1) To declare a variable can use var, let, const. 
	* Var - The [****var****](https://www.geeksforgeeks.org/javascript-var/) is the oldest keyword to declare a variable in [JavaScript](https://www.geeksforgeeks.org/introduction-to-javascript/). It has the [Global scoped](https://www.geeksforgeeks.org/understanding-variable-scopes-in-javascript/#:~:text=types%20of%20scopes-,Global%20Scope,-%E2%80%93%20Scope%20outside%20the) or function scoped
	* Let - The [let keyword](https://www.geeksforgeeks.org/javascript-let/) is an improved version of the [var keyword](https://www.geeksforgeeks.org/javascript-var/). It is introduced in the ES6 or EcmaScript 2015. These variables has the [block scope](https://www.geeksforgeeks.org/what-are-block-scoped-variables-and-functions-in-es6/). It can’t be accessible outside the particular code block.
	* Const - The [const keyword](https://www.geeksforgeeks.org/javascript-const/) has all the properties that are the same as the [let keyword](https://www.geeksforgeeks.org/javascript-let/), except the user cannot update it and have to assign it with a value at the time of declaration. These variables also have the [block scope](https://www.geeksforgeeks.org/what-are-block-scoped-variables-and-functions-in-es6/). It is mainly used to create constant variables whose values can not be changed once they are initialized with a value.
2)  Commands can be given as // or /* * /
3) Print something in console 
```let xp=0;
let health=100;
let gold =50;
let currentWeapon=0;
let fighting;
let monsterHealth;
let inventory=["stick"];

const button1=document.querySelector("#button1");
const button2=document.querySelector("#button2");
const button3=document.querySelector("#button3");
const text=document.querySelector("#text");
const xpText=document.querySelector("#xpText");
const healthText=document.querySelector("#healthText");
const goldText=document.querySelector("#goldText");
const monsterStats=document.querySelector("#monsterStats");
const monsterNameText=document.querySelector("#monsterName");
const monsterHealthText=document.querySelector("#monsterHealth");

//Initialize buttons
button1.onclick=goStore;
button2.onclick=goCave;
button3.onclick=fightDragon;

function goStore()
{
  console.log("Going to Store.");
}

function goCave(){
  console.log("Going to cave.");
}

function fightDragon(){
  console.log("Fighting dragon.")
}


```
4) To set text inside a button
```
function goStore()
{
  button1.innerText="Buy 10 health (10 gold)";
  button2.innerText="Buy weapon (30 gold)";
  button3.innerText="Go to town square";
  
}


```
