<h2 align="center"><img align="center" src="./image/JavaScript-logo.png" height="40" width="40"/>  Java Script задачки</h2>
------ 

## ✔️1
_Напишите функцию stringToArray(str), которая преобразует строку в массив слов._
```
const str = 'Быть или не быть';
function stringToArray(str) {

// Ваш код

};

const arr = stringToArray(str);

document.writeln(arr); // ['Быть', 'или', 'не', 'быть']
```

## решение
>>>
``` 
const str = 'Быть или не быть';
function stringToArray(str) {

  return str.trim().split(" ");

}

const arr = stringToArray(str);

document.writeln(arr); // ['Быть', 'или', 'не', 'быть']

```

## инфо
<p>Метод trim() возвращает строку с вырезанными пробельными символами с её концов.</p>
<p>Метод split() разбивает объект String на массив строк путём разделения строки указанной подстрокой.</p>
<<<
------ 

## ✔️2
_Напишите функцию deleteСharacters(str, length), которая возвращает подстроку, состоящую из указанного количества символов._
```
const str = 'Быть или не быть';
function deleteСharacters(str, length) {

// Ваш код

};

document.writeln(deleteСharacters(str, 3)); // или
```

## решение

``` 
const str = 'Быть или не быть';
function deleteСharacters(str, length) {
  
  if ((str.constructor === String) && (length>0)) {
    return str.slice(0, length);
  }
};

document.writeln(deleteСharacters(str, 3)); // или
```

## инфо
<p>Метод slice() возвращает новый массив, содержащий копию части исходного массива.</p>

------ 
