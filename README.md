# JavaScript_intro
+ Scripts can be placed in the <body>, or in the <head> section of an HTML page, or in both.  
## JavaScript 輸出  
1.innerHTML  
2.document.write()  輸出到螢幕上  USE for test  
3.window.alert() 警報框   
4.console.log()  寫入瀏覽器console  
5.訪問HTML 元素js 可以使用document.getElementById(id)方法  id屬性定義html元素,innerHTML定義HTML內容  
## 語句  
1.let 關鍵字宣告變數 ex:let a,b,c;
2.分號";"分隔 JavaScript 語句
3.同行允許以分號隔開 a=5;b=6;c=a+b  
4.javascript 忽略多個空格 ex:let person = "Herge"; let x = y + z;  增加可讀性  
## JavaScript 代碼塊  
1.JavaScript 語句可以在大括號 {...} 內的代碼塊中組合在一起。
ex:  
```
function myFunciton(){
  document.getElementById("demo").innerHTML="Hello Dolly!";   //該語句告訴瀏覽器寫“Hello Dolly”。在 id="demo" 的 HTML 元素中：  
  document.getElementById("demo2").innerHTML=:How are you?"; 
}
```  
## 關鍵字  
## 語法  
```
//How to create variables:
var x;
let y;
//How to use variables
x=5;
y=6;
let z=x+y;
```
## 變量  
```  
//宣告或不宣告都可以  
//JavaScript 使用關鍵字var, let和const來聲明變量。  在這些示例中，使用var or let將產生相同的結果。
let x;   //var 跟 let 一樣功能都是宣告變數,let 是2015被加入到JS  
x=6;
//字串串接
"How"+"are"+"you"+"?"  
```
## 註解  
+ 使用//  
## JavaScript 美元符號 $  
```
//由於 JavaScript 將美元符號視為字母，因此包含 $ 的標識符是有效的變量名：
ex:  
let $="hello world";
let $$$ =2;
let $myMoney=5;
//使用美元符號在 JavaScript 中並不常見，但專業程序員經常將其用作 JavaScript 庫中 main 函數的別名。

例如，在 JavaScript 庫 jQuery 中，main 函數 $用於選擇 HTML 元素。在 jQuery$("p");中表示“選擇所有 p 元素”。
```  
## Let  
```
//不能重新宣告
let x="John Does:;
let x=0;
//it will cause SyntaxErrot:'x' has already been declared  
//不過var 就可以  重新宣告
var x="test string";
var x=0;
```
## Let block range 
```
//ES6 引入了兩個重要的新 JavaScript 關鍵字：let和const.
//這兩個關鍵字在 JavaScript 中提供了塊作用域。 { } 塊內聲明的變量不能從塊外訪問：
{
  let x=3;
}
//x can not be used here or access 
//但是var 可以  相比之下let 跟var 最大差別就是作用域的問題 還有redeclare -> let 比 var 嚴謹很多  
//let 要先宣告才能使用  
{
varx =3;
  }
 // x can be used here
 //var在程序的任何地方都允許重新聲明 JavaScript 變量：
 ```
 ## Let 支援度  
 + 因為比較新所以有些browser 並不支援 
 ## Const 關鍵字  
 + Cannot be Reassigned  
 + JavaScript const variables must be assigned a value when they are declared  
 + const 關鍵字有一點誤導,他事實上是定義一個reference
 ex:
 ```
 /*關鍵字const有點誤導。

它沒有定義一個常數值。它定義了對值的常量引用。

因此，您不能：

重新分配一個常數值
重新分配一個常量數組
重新分配一個常量對象
但是你可以：

改變常量數組的元素
更改常量對象的屬性
*/
// You can create a constant array:
const cars = ["Saab", "Volvo", "BMW"];

// You can change an element:
cars[0] = "Toyota";

// You can add an element:
cars.push("Audi");
但是您不能重新分配數組：    改變reference
const cars = ["Saab", "Volvo", "BMW"];

cars = ["Toyota", "Volvo", "Audi"];    // ERROR
//const不允許在同一範圍內重新分配現有變量：
const x = 2;     // Allowed
x = 2;           // Not allowed
var x = 2;       // Not allowed
let x = 2;       // Not allowed
const x = 2;     // Not allowed

{
  const x = 2;   // Allowed
  x = 2;         // Not allowed
  var x = 2;     // Not allowed
  let x = 2;     // Not allowed
  const x = 2;   // Not allowed
}
//結論是const 跟let 很像 比較嚴謹  
```
## JavaScript Arrays 陣列
+ JavaScript arrays are written with square brackets.  []  
+ Array items are separated by commas.  逗號隔開每一個item  
+ The following code declares (creates) an array called cars, containing three items (car names):
```
  const cars = ["Saab", "Volvo", "BMW"];
```
## Objects 物件  
+ JavaScript objects are written with curly braces {}.  
+ 物件的性質是 name:value  pairs  冒號隔開  
 ```
  const person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"}
  ```
## typeof Operator  
+ use the JavaScript typeof operator to find the type of a JavaScript variable.  
```
typeof ""             // Returns "string"
typeof "John"         // Returns "string"
typeof "John Doe"     // Returns "string"
typeof 0              // Returns "number"
typeof 314            // Returns "number"
typeof 3.14           // Returns "number"
typeof (3)            // Returns "number"
typeof (3 + 4)        // Returns "number"
  ```
## Functions  
+ JavaScript 函數是用function關鍵字定義的，後跟一個name，然後是括號()  
```
  function myFunction(p1,p2) {
    return p1*p2
}
  //標準長相
  function name(parameter1, parameter2, parameter3) {
  // code to be executed
}
  ```
## object 物件  
+ 物件可以想像成一台車,性質是型號,車重,顏色,而物件的方法可以是car.start(),car.drive()  
+ 物件也是一個變數,不過可以存放很多值  
```
let car = "Fiat";
const car ={type:"Fiat",model:"500",color:"white"};
//The values are written as name:value pairs (name and value separated by a colon)
object definition
const person={firstName:"John",lattName:"Doe",eyecolor:"blue"};

const person={
    firstName:"John",
    lastName:"Doe",
    age:50,
    eyeColor:"blue"
};//The name:values pairs in JavaScript objects are called properties:
```
## object method 物件方法  
```
//Objects can also have methods
//Methods are actions that can be performed on objects
//Methods are stored in properties as function definitions
 const person={
        firstName:"John",
        lastName:"Doe",
        id:5566,
        fullname:function(){
            return this.firstName+""+this.lastName  //person.firstName   person.lastName
        }
        ```
## this 關鍵字  
+ In JavaScript, the this keyword refers to an object.  關於物件  
