# Lecture 6
![](./%D0%91%D0%B5%D0%B7%20%D0%BD%D0%B0%D0%B7%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F%20(2).png)
># _Table of content ;_ 
## _1.Object;_
## _2.Destructuring;_
## _3.Spread;_
## _4.This;_
## _5.New Date();_
># _What is Object in JS ?_ 
![](./images%20(2).jpg)
## _Object in iak obect dorroi iakchand value va key meboshad;In JavaScript, an object is a standalone entity, with properties and type. Everything is an object in JavaScript._
># _How to make an object_ : 
![](./%D0%91%D0%B5%D0%B7%20%D0%BD%D0%B0%D0%B7%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F%20(1).png)
```
let obj = {
    name : "Bilol";
    Emai : @gmail.com,
    age : 22
}
console.log(obj) ---> output : { name : "Bilol"; Emai : @gmail.com,age 22}
```
## _3 Rohi giriftani value az object_
```
let obj = {                                     output
    name : "Bilol",
    "full name" : "Rahimov Bilol",
    Emai : @gmail.com,
    age : 22
}
console.log(obj.name);                         Bilol
console.log(obj["full name"]);                 Rahimov Bilol
va bo roho destructuring
```
># _Methods Of  Object :_
![](./images.jpg)
## _1.Object.entries()_ : - baroi nishon dodani key va valu - ho dar masivho 
```
let obj = {
    name : "Bilol",
    surName : "Rahimov",
    age : 12
}
console.log(Object.entries(obj));

output : [ [ 'name', 'Bilol' ], [ 'surName', 'Rahimov' ], [ 'age', 12 ] ]
```
## _1.Object.keys()_ : - baroi nishon dodani key (kluchho) - ho dar masiv
```
let obj = {
    name : "Bilol",
    surName : "Rahimov",
    age : 12
}
console.log(Object.keys(obj));

output : [ 'name', 'surName', 'age' ]
```
## _1.Object.values()_ : - baroi nishon dodani value (kimatho) - ho dar masiv
```
let obj = {
    name : "Bilol",
    surName : "Rahimov",
    age : 12
}
console.log(Object.values(obj));

output : [ 'Bilol', 'Rahimov', 12 ]
```
># _What is Object Destructuring and Spred;_
![](./images.png)
## _Destructuring object Milsli Array Desturucturing kor mrkunad ammo kavshoi object guzoshta meshavad Destrructuring in az object proprtihoro hamchun variable giriftan ammo az array kame tarzi giriftan fark mekunad_
```
let obj = {
    name : "Bilol",
    surName : "Rahimov",
    age : 12,
    city : {
        cityOf : "Kulob",
        village : "Ahmar"
    }
}
let {name} = obj                                   output:
console.log(name);                                 Bilol
let {name : a} = obj we can change the name of this
console.log(a);                                    Bilol
let {city : k} = obj
console.log(k);                      { cityOf: 'Kulob', village: 'Ahmar' }
let {city : { village : v }} = obj
console.log(v);                                     Ahmar
```
## _Spread inhma ba misli array kor mekunad spread dar object in propertihoro az objekt kopia karda mondan_
```
let obj = {
    name : "Bilol",
    surName : "Rahimov",
    age : 12,
}
let obj2 = {...obj}
console.log(obj2);

output : 
{ name: 'Bilol', surName: 'Rahimov', age: 12 }
```
># _What is this in js object_ 
## _this in fakat dar object kor mekunad dar  holalte ki mo dar iagon valuei properiti function menavisem this in dar returni function kor mekunad va obji blobalro mekobad_
```
let obj = {
    name : "Bilol",
    surName : "Rahimov",
    age : 12,
    fullName : function () {
        return `${this.surName} ${this.name}`
    }
}
console.log(obj.fullName());
output : 
Rahimov Bilol
```   
># _What is new Date() in js;_
![](./images%20(1).jpg)
## _new Date () in Data vremia meboshad ki mo metavone ba vositai methidho funksiaho dta vremia sozem_
>## _How to creat a new date_
## _new Date () : - Datai aini zamonro nishon medihad_ 
```
let date = new Date()
console.log(date);
output : 
2023-10-26T19:35:30.452Z
``` 
## _new Date (millisecon) mo milliseundro dobavit mekunem on az soli 1970 injonib sar kar karda millisecundhoi mori dar boli onho meguzorad_
```
let date = new Date(10000000)
console.log(date);
output : 
1970-01-01T02:46:40.000Z
```
## _new Date (sting) : in namudui date baroi sokhtani date bo string_
```
let date = new Date("2023-05-20")
console.log(date);
output :
2023-05-20T00:00:00.000Z
```
## _new Date(year,month,day,hour,minuts,secons,milliseconds) : hama namud to millisecundro bashumo nishon medihad_
```
let date = new Date(2023,04,20,16,29,1000)
console.log(date);
output : 
2023-05-20T13:45:40.000Z
```
># _Data and Time_
## _1.now() : Millisecundhoro az soli 1970 injonib sar karda nishon medihad_
```
let date = Date.now()
console.log(date);
output : 
1698349663995
```
## _getFillYear () : solro prra ba mo nishon medihad_
```
let date = new Date()
console.log(date.getFullYear());
output : returns the full Of Year with 4 digits
2023 
```
## _getMonth () : mohro nishon medihad bo raqam agar khohem ki on nomi mohro nish on dihem dar iak vriable array karda bakhshem_ 
```
// let month = ["January","Fabruaru","March","April","May","June","July","August","Seprtember","October","November","December"]
// let date = new Date()
// console.log(month[date.getMonth()]);
output : 
Otober
```
## _getDate() : baroi nishon dodani ruz_ 
```
let date = new Date()
console.log(date.getDate());
output : 
the day wich you are ///26 this is today
```
## _getDay() : baroi nishon dodani ruzhoi hafta_ 
```
// let day = ["Sun","Mon","Tuez","wed","thurth","friday","satur"]
// let date = new Date()
// console.log(day[date.getDay()]);
output : 
the day of week wich you are ///friday this is today
```
## _getHours() : baroi nishon dodani soati hamon lahza_ 
```
let date = new Date()
console.log(date.getHours());
output : 
the time wich you are ///23 this is now
```
## _getMinutes() : baroi nishon dodani soati hamon lahza daqiqa_ 
```
let date = new Date()
console.log(date.getMinures());
output : 
the time of minute wich you are ///20 this is now minute
```
>## _Also it has a second and millisecond_
## _setDate() : set the date of the day_
```
let date = new Date()
console.log(date.setDate(15));
output : show millisecond : 1697402696155
--------------------------------------------
let date = new Date()
date.setDate(15)
console.log(data);
output : 2023-10-15T20:46:08.843Z
--------------------------------------------
let date = new Date()
console.log(date.toString());
output : Mon Oct 16 2023 23:44:08 GMT+0300 (Москва, стандартное время)
--------------------------------------------
``` 
## _setMonth() : set the month of the date_
```
let date = new Date()
console.log(date.setMonth(15));
output : show millisecond : 1697402696155
--------------------------------------------
let date = new Date()
date.setMonth(0)
console.log(date);
output : 2023-01-26T20:48:24.091Z
--------------------------------------------
let date = new Date()
console.log(date.toString());
output : Mon Oct 16 2023 23:44:08 GMT+0300 (Москва, стандартное время)
--------------------------------------------
``` 
## _setFullYear() : set the year of the date_
```
let date = new Date()
date.setFullYear(0)
console.log(date);
output : 2191-08-26T21:16:05.954Z
--------------------------------------------
let date = new Date()
console.log(date.toString());
output : Fri Oct 27 2023 00:16:45 GMT+0300 (Москва, стандартное время)
--------------------------------------------
``` 