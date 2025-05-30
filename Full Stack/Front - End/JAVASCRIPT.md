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
5) To put a quotation in string 
```
" Hllo my world \"jack\"  "

```
From this
```

button1.onclick=goStore;
button2.onclick=goCave;
button3.onclick=fightDragon;

function update(location){
  
}

function goTown(){
  button1.innerText="Go to store";
  button2.innerText="Go to town";
  button3.innerText="Go to cave";
  button1.onclick=buyHealth;
  button2.onclick=buyWeapon;
  button3.onclick=goTown;
  text.innerText="You are in the town square. You see a sign that says \"Store\".";
}

function goStore()
{
  button1.innerText="Buy 10 health (10 gold)";
  button2.innerText="Buy weapon (30 gold)";
  button3.innerText="Go to town square";
  button1.onclick=buyHealth;
  button2.onclick=buyWeapon;
  button3.onclick=goTown;
  text.innerText="You entered the store";
  
}

function goCave(){
  console.log("Going to cave.");
}

function fightDragon(){
  console.log("Fighting dragon.")
}

function buyHealth(){
  
}

function buyWeapon(){
  
}

```
To this
```
let xp=0;
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
const weapons=[
  {
    name : "stick",
    power:5
  },
  {
      name:"dagger",
      power:30
  },
  {
    name:"claw hammer",
    power:50
  },
  {
    name:"sword",
    power:100
  }
];

const monsters=[
  {
    name:"slime",
    level:2,
    health:15
  },
  {
    name:"fanged beast",
    level:8,
    health:60
  },
  {
    name:"dragon",
    level:20,
    health:300
  }
];
const locations=[
  {
    name : "town square",
    "button text":["Go to store","Go to cave","Fight dragon"],
    "button functions":[goStore,goCave,fightDragon],
    text:"You are in the town square. You see a sign that says \"Store\"."
    
  },
  {
    name : "store",
    "button text":["Buy 10 health (10 gold)","Buy weapon (30 gold)","Go to town square"],
    "button functions":[buyHealth,buyWeapon,goTown],
    text:"You enter the store."
  },
  {
    name : "cave",
    "button text":["Fight slime","Fight fanged beast","Go to town square"],
    "button functions":[fightSlime,fightBeast,goTown],
    text:"You enter the cave. You see some monsters."
  },
  {
    name:"fight",
    "button text":["Attack","Dodge","Run"],
    "button functions":[attack,dodge,goTown],
    text:"You are fighting a monster."
  },
  {
    name:"kill monster",
    "button text":["Go to town square","Go to town square","Go to town square"],
    "button functions":[goTown,goTown,easterEgg],
    text:"The monster screams \"Arg!\" as it dies. You gain experience points and find gold."
  },
  {
    name:"lose",
    "button text":["Replay?","Replay?","Replay?"],
    "button functions":[restart,restart,restart],
    text:"You die."
  },
  {
    name:"win",
    "button text":["Replay?","Replay?","Replay?"],
    "button functions":[restart,restart,restart],
    text:"You defeat the dragon! YOU WIN THE GAME!"
  },
  {
    name:"easter egg",
    "button text":["2","8","Go to town square?"],
    "button functions":[pickTwo,pickEight,goTown],
    text:"You find a secret game. Pick a number above. Ten numbers will be randomly chosen between 0 and 10. If the number choose matches one of the random numbers, you win!" 
  }
];

//Initialize buttons
button1.onclick=goStore;
button2.onclick=goCave;
button3.onclick=fightDragon;

function update(location){
  button1.innerText=location["button text"][0];
  button2.innerText=location["button text"][1];
  button3.innerText=location["button text"][2];
  button1.onclick=location["button functions"][0];
  button2.onclick=location["button functions"][1];
  button3.onclick=location["button functions"][2];
  text.innerText=location.text;
}

function goTown(){
  update(locations[0]);
}

function goStore()
{
  update(locations[1]);
}

function goCave(){
  update(locations[2]);
}

function buyHealth(){
  if(gold>=10)
  {
    gold-=10;
    health+=10;
    goldText.innerText=gold;
    healthText.innerText=health;
  }
  else{
    text.inenrText="You do not have enough gold to buy health.";
  }
}

function buyWeapon(){
  if(currentWeapon<weapons.length-1)
  {
    if(gold>=30)
    {
      gold -=30;
      currentWeapon++;
      goldText.innerText=gold;
      let newWeapon=weapons[currentWeapon].name;
      text.innerText="You now have a "+newWeapon + " .";
      inventory.push(newWeapon);
      text.innerText+="In your inventory you have: "+inventory;
  
    }
    else{
    text.innerText="You do not have enough gold to buy weapon.";
    }
  }
  else
  {
    text.innerText="You already have the most powerful weapon!";
    button2.innerText="Sell weapon for 15 gold";
    button2.onclick=sellWeapon;
  }
}

function sellWeapon()
{
  if(inventory.length>1)
  {
    gold+=15;
    goldText.innerText=gold;
    let currentWeapon=inventory.shift();
    text.innerText="You sold a "+currentWeapon+".";
    text.innerText+="In your inventory you have: "+inventory;
  }
  else
  {
    text.innerText="Don't sell your only weapon!";
  }
}

function fightSlime(){
  fighting=0;
  goFight();
}

function fightBeast(){
  fighting=1;
  goFight();
}

function fightDragon(){
  fighting=2;
  goFight();
}

function goFight(){
  update(locations[3]);
  monsterHealth=monsters[fighting].health;
  monsterStats.style.display="block"
  monsterNameText.innerText=monsters[fighting].name;
  monsterHealthText.innerText=monsterHealth;
}

function attack(){
  text.innerText="The "+ monsters[fighting].name +" attacks.";
  text.innerText+=" You attack it with your "+weapons[currentWeapon].name+" .";
  if(isMonsterHit())
  {
    health-=getMonsterAttackValue(monsters[fighting].level);
  }
  else
  {
    text.innerText="You miss.";
  }
  monsterHealth-=weapons[currentWeapon].power+Math.floor(Math.random() * xp)+1;
  healthText.innerText=health;
  monsterHealthText.innerText=monsterHealth;
  if(health<=0){
    lose();
  }
  else if(monsterHealth<=0)
  {
    fighting===2 ? winGame() : defeatMonster();
  }
  if(Math.random()<=.1 && inventory.length!==1){
    text.innerText+= "Your "+inventory.pop()+" breaks.";
    currentWeapon--;
  }
}

function dodge(){
  text.innerText="You dodge the attack from the "+ monsters[fighting].name+" .";
}

function defeatMonster(){
  gold+=Math.floor(monsters[fighting].level*6.7);
  xp+=monsters[fighting].level;
  goldText.innerText=gold;
  xpText.innerText=xp;
  update(locations[4])
  
}

function lose(){
  update(locations[5])
  
}

function winGame(){
  update(locations[6]);
}

function restart(){
  xp=0;
  health=100;
  gold=50;
  currentWeapon=0;
  inventory=["stick"];
  goldText.innerText=gold;
  healthText.innerText=health;
  xpText.innerText=xp;
  goTown();
  
}

function isMonsterHit(){
  return Math.random()>.2 || health<20;
}

function easterEgg(){
  update(locations[7]);
}

function getMonsterAttackValue(level){
  let hit=(level *5)-(Math.floor(Math.random*xp));
  console.log(hit);
  return hit;
}

function pickTwo(){
  pick(2);
}

function pickEight(){
  pick(8);
}   

function pick(guess){
  let numbers=[];
  while(numbers.length<10){
    numbers.push(Math.floor(Math.random()*11));
  }
  text.innerText="You picked "+guess+". Here are the random numbers:\n";

  for(let i=0;i<10;i++){
    text.innerText+=numbers[i]+"\n";
  }

  if(numbers.indexOf(guess) !==-1){
    text.innerText+="You win 20 gold!";
    gold+=20;
    goldText.innerText=gold;
  }
  else{
    text.innerText+="Wrong You lose 10 health!";
    health-=10;
    healthText.innerText=health;
    if(health<=0){
      lose();
    }
  }
}
```
6) ``` .shift method is used to remove the first element in array and written it
```