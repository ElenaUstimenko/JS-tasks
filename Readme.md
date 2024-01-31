<h2 align="center"><img align="center" src="./image/JavaScript-logo.png" height="40" width="40"/>     Java Script задачки и вопросы</h2>
<p align="center">собираю из разных источников и тренируюсь проходить...</p2>

------ 

## ✔️ 1
_Напишите функцию, которая преобразует строку в массив слов._
```
const str = 'Быть или не быть';
function stringToArray(str) {

// Ваш код

};

const arr = stringToArray(str);

document.writeln(arr); // ['Быть','или','не','быть']
```
<details><summary><b>решение</b></summary>

<div>

```
const str = 'Быть или не быть';
function stringToArray(str) {

  return str.trim().split(" ");
}

const arr = stringToArray(str);

document.writeln(arr); // ['Быть','или','не','быть']
```

### инфо
<p>Метод trim() возвращает строку с вырезанными пробельными символами с её концов.</p>
<p>Метод split() разбивает объект String на массив строк путём разделения строки указанной подстрокой.</p>
</div>
</details>

------ 

## ✔️ 2
_Напишите функцию, которая возвращает подстроку, состоящую из указанного количества символов._
```
const str = 'Быть или не быть';
function deleteСharacters(str, length) {

// Ваш код

};

document.writeln(deleteСharacters(str, 5)); // Быть
```

<details><summary><b>решение</b></summary>

<div>

``` 
const str = 'Быть или не быть';
function deleteСharacters(str, length) {
  
  if ((str.constructor === String) && (length>0)) {
    return str.slice(0, length);
  }
};

document.writeln(deleteСharacters(str, 5)); // Быть
```

### инфо
<p>Метод slice() возвращает новый массив, содержащий копию части исходного массива.</p>
</div>
</details>

------ 

## ✔️ 3
_Напишите функцию, которая принимает строку в качестве аргумента и преобразует регистр первого символа строки из нижнего регистра в верхний._
```
const str = "string doesn`t start with a capital letter";  
 
function upperRegisterForFirstLetter(str) {

// Ваш код

}

document.writeln(upperRegisterForFirstLetter(str)); // "String doesn`t start with a capital letter"
```

<details><summary><b>решение</b></summary>

<div>

``` 
const str = "string doesn`t start with a capital letter";   
 
function upperRegisterForFirstLetter(str) {

  return str.charAt(0).toUpperCase() + str.slice(1);

}

document.writeln(upperRegisterForFirstLetter(str)); // "String doesn`t start with a capital letter"
```

### инфо
<p>Метод charAt() возвращает указанный символ из строки.</p>
<p>Метод toUpperCase() возвращает значение строки, на которой он был вызван, преобразованное в верхний регистр.</p>
<p>Метод slice() возвращает новый массив, содержащий копию части исходного массива.</p>
</div>
</details>

------ 

## ✔️ 4
_Напишите функцию, которая принимает строку str в качестве аргумента и вставляет тире (-) между словами. При этом все символы строки необходимо перевести в верхний регистр._
```
const str = "HTML CSS JavaScript React";

function addDash(str) {

// Ваш код

}

document.writeln(addDash(str)); // 'HTML-CSS-JAVASCRIPT-REACT'
```

<details><summary><b>решение</b></summary>

<div>

``` 
const str = "HTML CSS JavaScript React";

function addDash(str) {
  return str.trim().toUpperCase().replace(/[^a-zA-Z0-9 -]/, "").replace(/\s/g, "-");
};

document.writeln(addDash(str)); // 'HTML-CSS-JAVASCRIPT-REACT'
```

### инфо
<p>Метод trim() возвращает строку с вырезанными пробельными символами с её концов.</p>
<p>Метод toUpperCase() возвращает значение строки, на которой он был вызван, преобразованное в верхний регистр.</p>
<p>Метод replace() возвращает новую строку с некоторыми или всеми сопоставлениями с шаблоном, заменёнными на заменитель. Шаблон может быть строкой или регулярным выражением, а заменитель может быть строкой или функцией, вызываемой при каждом сопоставлении.</p>
<p>^ - сделать набор/диапазон исключающим, искать все символы, кроме тех, что мы перечислим; \s - искать «пустоты» в тексте: пробелы, переносы строк и табуляции; g - искать все совпадения</p>
</div>
</details>

------ 

## ✔️ 5
_Напишите функцию, которая возвращает строку, в которой каждое слово начинается с заглавной буквы._
```
const str = "популярный фреймворк для разработки серверного кода express";  
 
function capitalize(str) {

// Ваш код

}

document.writeln(capitalize(str)); // "Популярный Фреймворк Для Разработки Серверного Кода Express"
```

<details><summary><b>решение</b></summary>

<div>

``` 
const str = "популярный фреймворк для разработки серверного кода express";  
 
function capitalize(str) {

 return str.replace(/(^|\s)\S/g, 
 function(a) {
  return a.toUpperCase()
  })

}

document.writeln(capitalize(str)); // "Популярный Фреймворк Для Разработки Серверного Кода Express"
```

### инфо
<p>Метод toUpperCase() возвращает значение строки, на которой он был вызван, преобразованное в верхний регистр.</p>
<p>Метод replace() возвращает новую строку с некоторыми или всеми сопоставлениями с шаблоном, заменёнными на заменитель. Шаблон может быть строкой или регулярным выражением, а заменитель может быть строкой или функцией, вызываемой при каждом сопоставлении.</p>
<p>\ S - взять все символы без пробелов, ^- стоящие в начале строки \ s - или после любого символа пробела и преобразовать их в верхний регистр.</p>
</div>
</details>

------ 

## ✔️ 6
_Напишите функцию, которая возвращает строку, очищенную от всех не буквенно-цифровых символов._
```
const str = "You ., -/ do not have #! access ;: {} to $ % ^  this & * action";  
 
function removeUnnecessary(str) {
  // Ваш код
};

document.writeln(removeUnnecessary(str)); // "You do not have access to this action"
```

<details><summary><b>решение</b></summary>

<div>

``` 
const str = "You ., -/ do not have #! access ;: {} to $ % ^  this & * action";   
 
function removeUnnecessary(str) {
   let res = "";
   res = str.replace(/[^\w\s]|_/g, "")
          .replace(/\s+/g, " ");
   return res;      
}

document.writeln(removeUnnecessary(str)); // "You do not have access to this action"
```

### инфо
<p>Метод replace() возвращает новую строку с некоторыми или всеми сопоставлениями с шаблоном, заменёнными на заменитель. Шаблон может быть строкой или регулярным выражением, а заменитель может быть строкой или функцией, вызываемой при каждом сопоставлении.</p>
<p>Работает только для английского шрифта. Убрать все символы, которые не являются цифрой, буквой, пробелом ([^\w\s]), за исключением добавленных символов подчеркивания (|_). Заменить один и более пробельных символов (\s+) одиночным пробелом (" ").</p>
</div>
</details>

------ 

## ✔️ 7
_Напишите функцию, которая принимает в качестве аргумента строку и заменяет регистр каждого символа на противоположный. Например, если вводится «КаЖдЫй ОхОтНиК», то на выходе должно быть «кАжДыЙ оХоТнИк»._
```
const str = "КаЖдЫй ОхОтНиК жЕлАеТ зНаТь";  
 
function changeRegister(str) {

// Ваш код

}

document.writeln(changeRegister(str)); // "кАжДыЙ оХоТнИк ЖеЛаЕт ЗнАтЬ"
```

<details><summary><b>решение</b></summary>

<div>

``` 
const str = "КаЖдЫй ОхОтНиК жЕлАеТ зНаТь";  
 
function changeRegister(str) {
let newStr = "";
let len = str.length;
  for (let i = 0; i < len; i++) {
    if (str[i] === str[i].toLowerCase()) {
      newStr += str[i].toUpperCase();
    } else {
      newStr += str[i].toLowerCase();
    }
  }
  return newStr;
}

document.writeln(changeRegister(str)); // "кАжДыЙ оХоТнИк ЖеЛаЕт ЗнАтЬ"
```

### инфо
<p>Метод toUpperCase() возвращает значение строки, на которой он был вызван, преобразованное в верхний регистр.</p>
<p>Метод toLowerCase() возвращает значение строки, на которой он был вызван, преобразованное в нижний регистр.</p>
</div>
</details>

------ 

## ✔️ 8
_Напишите функцию, которая дополняет нулями до указаной длины числовое значение с дополнительным знаком "+" или "-" в зависимости от передаваемого аргумента._
```
function zeros (num, len, sign) {
  // Ваш код
};

document.writeln(zeros(145, 5, '-')); // -00145
document.writeln(zeros(33, 4, '+'));  // +0033 
document.writeln(zeros(33, 4));       // 0033 
```

<details><summary><b>решение</b></summary>

<div>

``` 
function zeros (number, len, sign) {
let lengthZero = len - (number + '').length, // количество нулей
numberZero = '';

for (let i = lengthZero; i < len; i++) {
  numberZero += 0;
}
    
  return (sign === undefined || sign === '') 
    ? numberZero + number + '' 
    : sign + numberZero + number + '';
}

document.writeln(zeros(145, 5, '-')); // -00145
document.writeln(zeros(33, 4, '+'));  // +0033
document.writeln(zeros(33, 4));       // 0033
```

</div>
</details>

------ 

## ✔️ 9
_Напишите функцию, которая сравнивает строки без учёта регистра символов._
```
function comparison(str1, str2) {
  // Ваш код
};

document.writeln(comparison('string', 'StRiNg')); // true 
document.writeln(comparison('ABCDe', 'AbcdW'));   // false
```

<details><summary><b>решение</b></summary>

<div>

``` 
function comparison(str1, str2) {
  const res = str1.toUpperCase() === str2.toUpperCase();

  return res;
}

document.writeln(comparison('string', 'StRiNg')); // true
document.writeln(comparison('ABCDe', 'AbcdW'));   // false
```

### инфо
<p>Метод toUpperCase() возвращает значение строки, на которой он был вызван, преобразованное в верхний регистр.</p>
</div>
</details>

------ 

## ✔️ 10
_Напишите функцию, которая осуществляет поиск подстроки str2 в строке str1 без учёта регистра символов._
```
function insensitiveSearch(str1, str2) {
  // Ваш код
};

document.writeln(insensitiveSearch('Изучаю JavaScript', 'javascript')); // соответствует 
document.writeln(insensitiveSearch('Изучаю JavaScript', 'javascriptS')); // не соответствует  
```

<details><summary><b>решение</b></summary>

<div>

``` 
function insensitiveSearch(str1, str2) {
  let searchStr = new RegExp(str2, "ig");
    let result = str1.search(searchStr);

    return (result > 0) ? "соответствует" : "не соответствует";  
};

document.writeln(insensitiveSearch('Изучаю JavaScript', 'javascript')); // соответствует 
document.writeln(insensitiveSearch('Изучаю JavaScript', 'javascripttt')); // не соответствует  
```

### инфо
<p>Конструктор RegExp создаёт объект регулярного выражения для сопоставления текста с шаблоном.</p>
<p>Флаг i - не различать строчных и прописных букв. Флаг g - искать все совпадения.</p>
</div>
</details>

------ 

## ✔️ 11
_Напишите функцию, которая преобразует стиль написания составных слов строки в CamelCase._
```
str = "hEllo woRld";
function getCamelCaseText(str) {
  // Ваш код
};

document.writeln(getCamelCaseText(str)); // HelloWorld 
```

<details><summary><b>решение</b></summary>

<div>

``` 
str = "hEllo woRld";
function getCamelCaseText(str) {
  return str.toLowerCase().replace(/(?:^|\s)[a-z]/g, 
  function(m) {
    return m.toUpperCase().replace(/\s+/g, "");
  });
};

document.writeln(getCamelCaseText(str)); // HelloWorld  
```

### инфо
<p>Метод toLowerCase() возвращает значение строки, на которой он был вызван, преобразованное в нижний регистр.</p>
<p>Метод toUpperCase() возвращает значение строки, на которой он был вызван, преобразованное в верхний регистр.</p>
<p>Метод replace() возвращает новую строку с некоторыми или всеми сопоставлениями с шаблоном, заменёнными на заменитель. Шаблон может быть строкой или регулярным выражением, а заменитель может быть строкой или функцией, вызываемой при каждом сопоставлении.</p>
<p>Квантификатор ? - либо есть один символ, либо его нет вообще. Квантификатор + - искать все слова, где символ, стоящий перед +, встречается один или более раз. Спецсимвол \s ищет «пустоты» в тексте: пробелы (в том числе неразрывные), переносы строк и табуляции. Флаг g - искать все совпадения.</p>
</div>
</details>

------ 

## ❔ 12
_Что будет в консоли?_
```
function sayHello() {
  console.log(name);
  console.log(profession);
  var name = "Tom";
  let profession = "singer";
}

sayHello();
```

<details><summary><b>ответ</b></summary>

<div>

``` undefined ``` и ``` ReferenceError ```

### инфо
<p>Внутри функции мы сначала определяем переменную name с помощью ключевого слова var. Переменная будет со значением undefined по умолчанию, до тех пор пока исполнение кода не дойдет до строчки, где определяется переменная. Мы еще не определили значение name когда пытаемся вывести её в консоль, поэтому в консоли будет undefined.</p>
<p>Доступ к переменным, определенным с помощью let/const, не возможен до тех пор, пока не выполнится строка их определения. Когда мы пытаемся обратиться к переменным до того момента как они определены, JavaScript выбрасывает исключение ReferenceError.</p>
</div>
</details>

------ 

## ❔ 13
_Что будет в консоли?_
```
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1);
}

for (let i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1);
}
```

<details><summary><b>ответ</b></summary>

<div>

``` 3 3 3 ``` и ``` 0 1 2 ```

### инфо
<p>Первый цикл: Из-за очереди событий в JavaScript, функция setTimeout вызывается после того как цикл будет завершен. Так как переменная i в первом цикле была определена с помощью var, она будет глобальной. В цикле мы каждый раз увеличиваем значение i на 1, используя унарный оператор ++. К моменту выполнения функции setTimeout значение i будет равно 3.</p>
<p>Второй цикл: Переменные, опеределённые с помощью let/const имеют область видимости внутри { }. С каждой итерацией i будет иметь новое значение, и каждое значение будет замкнуто в своей области видимости внутри цикла.</p>
</div>
</details>

------ 

## ❔ 14
_Что будет в консоли?_
```
const shape = {
  radius: 10,
  diameter() {
    return this.radius * 2;
  },
  perimeter: () => 2 * Math.PI * this.radius
};

console.log(shape.diameter());
console.log(shape.perimeter());
```

<details><summary><b>ответ</b></summary>

<div>

``` 20 ``` и ``` NaN ```

### инфо
<p>diameter это обычная функция.</p>
<p>perimeter это стрелочная функция. У неё значение this указывает на окружающую область видимости, в отличие от обычных функций, поэтому при вызове perimeter значение this у этой функции указывает не на объект shape, а на внешнюю область видимости (например, window). У этого объекта нет ключа radius, поэтому возвращается undefined.</p>
</div>
</details>

------  

## ❔ 15
_Что НЕ является валидным?_
```
const bird = {
  size: 'small'
};

const mouse = {
  name: 'Mickey',
  small: true
};

A: mouse.bird.size
B: mouse[bird.size]
C: mouse[bird["size"]]
```

<details><summary><b>ответ</b></summary>

<div>

``` mouse.bird.size ```

### инфо
<p>При использовании квадратных скобок JavaScript замечает [ и продолжает пока не встретит ]. Только после этого он вычислит то, что находится внутри скобок. mouse[bird.size]: Сперва определяется bird.size, которое равно "small". mouse["small"] возвращает true.</p>
<p>Но с записью через точку так не происходит. У mouse нет ключа bird. Таким образом, mouse.bird равно undefined. Затем мы запрашиваем ключ size: mouse.bird.size. Так как mouse.bird это undefined, мы запрашиваем undefined.size. Это не является валидным, и мы получаем ошибку типа Cannot read property "size" of undefined.</p>
</div>
</details>

------   

## ✔️ 16
_You need to swap the head and the tail of the specified array:_
_the head (the first half) of array moves to the end, the tail (the second half) moves to the start. The middle element (if it exists) leaves on the same position._

_Return new array._

_For example:_
```
[ 1, 2, 3, 4, 5 ]   =>  [ 4, 5, 3, 1, 2 ]
    \----/   \----/         
     head     tail 

   [ -1, 2 ]  => [ 2, -1 ] 
   [ 1, 2, -3, 4, 5, 6, -7, 8 ]   =>  [ 5, 6, -7, 8, 1, 2, -3, 4 ]  
```

<details><summary><b>решение</b></summary>

<div>

``` 
const swapHeadAndTail = (arr, b = arr.length / 2) => [
  ...arr.slice(-b),
  ...arr.slice(b, -b), 
  ...arr.slice(0, b)
];
```

### инфо
<p>Метод slice() возвращает новый массив, содержащий копию части исходного массива.</p>
</div>
</details>

------    

## ✔️ 17
_Sum all the numbers of a given array ( cq. list ), except the highest and the lowest element ( by value, not by index! )._

_The highest or lowest element respectively is a single element at each edge, even if there are more than one with the same value._

_Mind the input validation._

_Example:_
```
{ 6, 2, 1, 8, 10 } => 16
{ 1, 1, 11, 2, 3 } => 6
```

_Input validation_
_If an empty value ( null, None, Nothing etc. ) is given instead of an array, or the given array is an empty list or a list with only 1 element, return 0._

<details><summary><b>решение</b></summary>

<div>

``` 
function sumArray(array) {
  return Array.isArray(array) && array.length > 1
    ? array.reduce((s, n) => 
      {return s + n}, 0) 
      - Math.min(...array) 
      - Math.max(...array)
    : 0
}
```

### инфо
<p>Статический метод Array.isArray() определяет, является ли переданное значение Array.</p>
<p>Метод массива reduce() позволяет превратить массив в любое другое значение с помощью переданной функции-колбэка и начального значения. Функция-колбэк будет вызвана для каждого элемента массива, и всегда должна возвращать результат.</p>
<p>Метод Math.min() возвращает наименьшее из нуля или более чисел.</p>


</div>
</details>

------ 

## ✔️ 18
_Given two integers a and b, which can be positive or negative, find the sum of all the integers between and including them and return it. If the two numbers are equal return a or b._

_Note: a and b are not ordered!_

_Examples (a, b) --> output (explanation)_

```
(1, 0) --> 1 (1 + 0 = 1)
(1, 2) --> 3 (1 + 2 = 3)
(0, 1) --> 1 (0 + 1 = 1)
(1, 1) --> 1 (1 since both are same)
(-1, 0) --> -1 (-1 + 0 = -1)
(-1, 2) --> 2 (-1 + 0 + 1 + 2 = 2)
```
_Your function should only return a number, not the explanation about how you get that number._

<details><summary><b>решение</b></summary>

<div>

``` 
function getSum(a, b) {
  return (Math.abs(a - b) + 1) * (a + b) / 2
}
```

### инфо
<p>Метод Math.abs() возвращает абсолютное значение числа. то есть a if ≥ 0 и -a if < 0.</p>
</div>
</details>

------ 

## ✔️ 19
_Complete the solution so that it returns true if the first argument(string) passed in ends with the 2nd argument (also a string)._

_Examples:_

```
solution('abc', 'bc') // returns true
solution('abc', 'd') // returns false
```

<details><summary><b>решение</b></summary>

<div>

``` 
function solution(str, ending) {
  return str.endsWith(ending);
};
```

### инфо
<p>Метод endsWith() позволяет определить, заканчивается ли строка символами указанными в скобках, возвращая, соответственно, true или false.</p>
</div>
</details>

------ 

## ✔️ 20
_ATM machines allow 4 or 6 digit PIN codes and PIN codes cannot contain anything but exactly 4 digits or exactly 6 digits._

_If the function is passed a valid PIN string, return true, else return false._

_Examples (Input --> Output)_

```
"1234"   -->  true
"12345"  -->  false
"a234"   -->  false
```

<details><summary><b>решение</b></summary>

<div>

``` 
function validatePIN(pin) {
  return /^(\d{4}|\d{6})$/.test(pin)
}
```

### инфо
<p>Спецсимвол \d совпадает с любой цифрой.  Спецсимвол, обозначающий начало строки, ^. Символ конца строки — знак доллара $.</p>
</div>
</details>

------ 

## ❔ 21
_Каким будет результат?_

```
function sum(a, b) {
  return a + b;
}

sum(1, '2');
```

<details><summary><b>ответ</b></summary>

<div>

``` 12 ```


### инфо
<p>Во время сложения числа (1) и строки ('2') число преобразовывается к строке. Таким образом, "1" + "2" возвращает "12".</p>
</div>
</details>

------ 

## ❔ 22
_Что будет в консоли?_

```
let c = { greeting: 'Hi!' };
let d;

d = c;
c.greeting = 'Hello';
console.log(d.greeting);
```

<details><summary><b>ответ</b></summary>

<div>

``` Hello ```


### инфо
<p>Сначала переменная c указывает на объект. Затем мы указываем переменной d ссылаться на тот же объект, что и c. Когда вы изменяете один объект, то изменяются значения всех ссылок, указывающих на этот объект.</p>
</div>
</details>

------  

## ❔ 23
_Что будет в консоли?_

```
let a = 3;
let b = new Number(3);
let c = 3;

console.log(a == b);
console.log(a === b);
console.log(b === c);
```

<details><summary><b>ответ</b></summary>

<div>

``` true ``` ``` false ``` ``` false ```


### инфо
<p>Оператор == проверяет равенство значений, оба значения равны 3, поэтому возвращается true.</p>
<p>new Number() это встроенный конструктор функции. И хотя он выглядит как число, это не настоящее число: у него есть ряд дополнительных особенностей, и это объект.</p>
<p>При использовании оператора === значение и тип должны быть одинаковыми. Но new Number() это не число, это объект, поэтому false.</p>
</div>
</details>

------ 

## ❔ 24
_Что будет в консоли?_

```
let greeting;
greetign = {};
console.log(greetign);
```

<details><summary><b>ответ</b></summary>

<div>

``` {} ```


### инфо
<p>В консоли выведется объект, потому что мы только что создали пустой объект в глобальном объекте. Когда мы вместо greeting написали greetign, интерпретатор JS на самом деле увидел:</p>
<p>global.greetign = {} в Node.js + window.greetign = {}, frames.geetign = {} и self.greetign в браузерах + self.greetign в веб-воркерах + globalThis.greetign во всех окружениях</p>
<p>Нужно использовать "use strict", чтобы избежать такого поведения. Эта запись поможет быть уверенным в том, что переменная была определена перед тем как ей присвоили значение.</p>
</div>
</details>

------  

## ❔ 25
_Что будет в консоли?_

```
function Person(firstName, lastName) {
  this.firstName = firstName;
  this.lastName = lastName;
}

const member = new Person('Tom', 'Green');
Person.getFullName = function () {
  return `${this.firstName} ${this.lastName}`;
}

console.log(member.getFullName());
```

<details><summary><b>ответ</b></summary>

<div>

``` TypeError ```


### инфо
<p>В JavaScript функции являются объектами, поэтому метод getFullName добавляется к самому объекту функции-конструктора. По этой причине мы можем вызвать Person.getFullName(), но member.getFullName выдает TypeError.</p>
<p>Чтобы метод был доступен для всех экземпляров объекта, вы должны добавить его в свойство прототипа:</p>

```  
Person.prototype.getFullName = function () {
  return `${this.firstName} ${this.lastName}`;
}
```
</div>
</details>

------ 

## ❔ 26
_Что будет в консоли?_

```
let number = 0;
console.log(number++);
console.log(++number);
console.log(number);
```

<details><summary><b>ответ</b></summary>

<div>

``` 0 ``` ``` 2 ``` ``` 2 ```


### инфо
<p>Постфиксный унарный оператор ++: 1.Возвращает значение (0). 2.Инкрементирует значение (теперь число равно 1).</p>
<p>Префиксный унарный оператор ++: 1.Инкрементирует значение (число теперь равно 2). 2.Возвращает значение (2).</p>
</div>
</details>

------ 

## ❔ 27
_Что будет в консоли?_

```
function getAge(...args) {
  console.log(typeof args);
}

getAge(32);
```

<details><summary><b>ответ</b></summary>

<div>

``` "object" ``` 


### инфо
<p>Оператор распространения (...args) возвращает массив с аргументами. Массив это объект, поэтому typeof args возвращает "object".</p>
</div>
</details>

------ 

## ❔ 28
_Чему будет равно sum?_

```
const sum = eval('10*10+5');
```

<details><summary><b>ответ</b></summary>

<div>

``` 105 ``` 


### инфо
<p>eval выполняет код, переданный в виде строки. Если это выражение (как в данном случае), то вычисляется выражение. Выражение 10 * 10 + 5 вернет число 105.</p>
</div>
</details>

------ 

## ❔ 29
_Как долго будет доступен cool_secret?_

```
sessionStorage.setItem('cool_secret', 123);
```

<details><summary><b>ответ</b></summary>

<div>

``` Пока пользователь не закроет вкладку. ``` 


### инфо
<p>Данные, сохраненные в sessionStorage очищаются после закрытия вкладки. При использовании localStorage данные сохраняются навсегда. Очистить их можно, например, используя localStorage.clear().</p>
</div>
</details>

------ 

## ❔ 30
_Что будет в консоли?_

```
var num = 8;
var num = 10;

console.log(num);
```

<details><summary><b>ответ</b></summary>

<div>

``` 10 ``` 


### инфо
<p>С помощью ключевого слова var можно определять сколько угодно переменных с одним и тем же именем. Переменная будет хранить последнее присвоенное значение. Но такой трюк нельзя проделать с let и const, т.к. у них блочная область видимости.</p>
</div>
</details>

------ 

## ❔ 31
_Что будет в консоли?_

```
const obj = { a: 'one', b: 'two', a: 'three' };
console.log(obj);
```

<details><summary><b>ответ</b></summary>

<div>

``` { a: "three", b: "two" } ``` 


### инфо
<p>Если есть два ключа с одинаковым именем, то ключ будет перезаписан. Его позиция сохранится, но значением будет последнее указанное.</p>
</div>
</details>

------ 

## ❔ 32
_Что будет в консоли?_

```
for (let i = 1; i < 5; i++) {
  if (i === 3) continue;
  console.log(i);
}
```

<details><summary><b>ответ</b></summary>

<div>

``` 1 ``` ``` 2 ``` ``` 4 ```


### инфо
<p>Оператор continue пропускает итерацию, если условие возвращает true.</p>
</div>
</details>

------ 

## ❔ 33
_Что будет в консоли?_

```
const a = {};
const b = { key: 'b' };
const c = { key: 'c' };

a[b] = 123;
a[c] = 456;

console.log(a[b]);
```

<details><summary><b>ответ</b></summary>

<div>

``` 456 ```


### инфо
<p>Ключи объекта автоматически конвертируются в строки. Мы собираемся добавить объект в качестве ключа к объекту a со значением 123.</p>
<p>Тем не менее, когда мы приводим объект к строке, он становится "[object Object]". Таким образом, мы говорим, что a["object Object"] = 123. Потом мы делаем то же самое. c это другой объект, который мы неявно приводим к строке. Поэтому a["object Object"] = 456.</p>
<p>Затем, когда мы выводим a[b], мы имеем в виду a["object Object"]. Мы только что установили туда значение 456, поэтому в результате получаем 456.</p>
</div>
</details>

------ 

## ❔ 34
_Что будет в event.target после клика на кнопку?_

```
<div onclick="console.log('first div')">
  <div onclick="console.log('second div')">
    <button onclick="console.log('button')">
      Кликни!
    </button>
  </div>
</div>
```

<details><summary><b>ответ</b></summary>

<div>

``` button ```


### инфо
<p>Целью события является самый глубокий вложенный элемент. Остановить распространение событий можно с помощью event.stopPropagation</p>
</div>
</details>

------

## ❔ 35
_Что будет в консоли после клика по параграфу?_

```
<div onclick="console.log('div')">
  <p onclick="console.log('p')">
    Кликни меня!
  </p>
</div>
```

<details><summary><b>ответ</b></summary>

<div>

``` p ``` ``` div ```


### инфо
<p>После клика по p будет выведено p и div. В цикле жизни события есть три фазы: захват, цель и всплытие. По умолчанию обработчики событий выполняются на фазе всплытия (если не установлен параметр useCapture в true). Всплытие идет с самого глубокого элемента вверх.</p>
</div>
</details>

------

## ❔ 36
_Каким будет результат?_

```
function sayHi() {
  return (() => 0)();
}

console.log(typeof sayHi());
```

<details><summary><b>ответ</b></summary>

<div>

``` "number" ```


### инфо
<p>Функция sayHi возвращает значение, возвращаемое из немедленно вызываемого функционального выражения (IIFE). Результатом является 0 типа "number".</p>
</div>
</details>

------

## ❔ 37
_Что будет в консоли?_

```
console.log(typeof typeof 1);
```

<details><summary><b>ответ</b></summary>

<div>

``` "string" ```


### инфо
<p>typeof 1 возвращает "number". typeof "number" возвращает "string"</p>
</div>
</details>

------

## ❔ 38
_Что будет в консоли?_

```
const numbers = [1, 2, 3];
numbers[10] = 11;
console.log(numbers);
```

<details><summary><b>ответ</b></summary>

<div>

``` [1, 2, 3, 7 x empty, 11] ```


### инфо
<p>Когда в массив добавляется значение, которое выходит за пределы длины массива, JavaScript создает так называемые "пустые ячейки". На самом деле они имеют значения undefined, но в консоли выводятся так: [1, 2, 3, 7 x empty, 11] в зависимости от окружения (может отличаться для браузеров, Node, и т.д.).</p>
</div>
</details>

------

## ❔ 39
_Что возвращает метод setInterval в браузере?_

```
setInterval(() => console.log('Hi'), 1000);
```

<details><summary><b>ответ</b></summary>

<div>

``` уникальный id ```


### инфо
<p>Это метод возвращает уникальный id. Этот id может быть использован для очищения интервала с помощью функции clearInterval().</p>
</div>
</details>

------

## ❔ 40
_Каким будет результат?_

```
[...'JavaScript'];
```

<details><summary><b>ответ</b></summary>

<div>

``` ["J", "a", "v", "a", "S", "c", "r", "i", "p", "t"] ```


### инфо
<p>Оператор распространения преобразовывает каждый символ строки в отдельный элемент.</p>
</div>
</details>

------

## ❔ 41
_Каким будет результат?_

```
console.log(3 + 4 + '5');
```

<details><summary><b>ответ</b></summary>

<div>

``` "75" ```


### инфо
<p>Ассоциативность операторов - это порядок, в котором компилятор оценивает выражения, слева направо или справа налево. Это происходит только в том случае, если все операторы имеют одинаковый приоритет. У нас есть только один тип оператора: +. Кроме того, ассоциативность слева направо.</p>
<p>3 + 4 оценивается первым. Это приводит к числу 7. JavaScript преобразует число 7 в строку, мы можем объединить две строки, используя оператор +. "7" + "5" приводит к "75".</p>
</div>
</details>

------

## ❔ 42
_Каким будет результат?_

```
class Chameleon {
  static colorChange(newColor) {
    this.newColor = newColor;
    return this.newColor;
  }

  constructor({ newColor = 'green' } = {}) {
    this.newColor = newColor;
  }
}

const freddie = new Chameleon({ newColor: 'purple' });
freddie.colorChange('orange');
```

<details><summary><b>ответ</b></summary>

<div>

``` TypeError ```


### инфо
<p>Функция colorChange является статической. Статические методы предназначены для работы только в конструкторе, в котором они созданы, и не могут передаваться каким-либо дочерним элементам или вызываться в экземплярах класса. Так как freddie является экземпляром класса Chameleon, функция не может быть вызвана для него. Будет выдана ошибка TypeError.</p>
</div>
</details>

------

## ❔ 43
_ Что будет в консоли?_

```
function Person(firstName, lastName) {
  this.firstName = firstName;
  this.lastName = lastName;
}

const tom = new Person('Tom', 'Green');
const marta = Person('Marta', 'Black');

console.log(tom);
console.log(marta);
```

<details><summary><b>ответ</b></summary>

<div>

``` Person {firstName: "Tom", lastName: "Green"} ``` и ``` undefined ```


### инфо
<p>Для marta мы не использовали ключевое слово new. Использование new приводит к созданию нового объекта. Но без new он указывает на глобальный объект.</p>
<p>Мы указали, что this.firstName равно "Marta" и this.lastName равно "Black". На самом деле мы определили global.firstName = 'Marta' и global.lastName = 'Black'. marta осталась undefined, поскольку мы не возвращаем значение из функции Person.</p>
</div>
</details>

------

## ❔ 44
_ Что будет в консоли?_

```
function getPersonInfo(one, two, three) {
  console.log(one);
  console.log(two);
  console.log(three);
}

const person = 'Sara';
const age = 30;

getPersonInfo`${person} is ${age} years old`;
```

<details><summary><b>ответ</b></summary>

<div>

``` ["", " is ", " years old"] ``` ``` "Sara" ``` ``` 30 ```


### инфо
<p>При использовании шаблонных строк первым аргументом всегда будет массив строковых значений. Оставшимися аргументами будут значения переданных выражений.</p>
</div>
</details>

------

## ❔ 45
_ Какие из этих значений являются "ложными"?_

```
0;
new Number(0);
("");
(" ");
new Boolean(false);
undefined;
```

<details><summary><b>ответ</b></summary>

<div>

``` 0 ``` ``` '' ``` ``` undefined ```


### инфо
<p>Есть только 8 "ложных" значений:</p>
<p>undefined</p>
<p>null</p>
<p>NaN</p>
<p>false</p>
<p>'' (пустая строка)</p>
<p>0</p>
<p>-0</p>
<p>0n</p>
<p>Конструкторы функций, такие как new Number и new Boolean являются "истинными".</p>
</div>
</details>

------

## ❔ 46
_ Что будет в консоли?_

```
(() => {
  let x, y;
  try {
    throw new Error();
  } catch (x) {
    (x = 1), (y = 2);
    console.log(x);
  }
  console.log(x);
  console.log(y);
})();
```

<details><summary><b>ответ</b></summary>

<div>

``` 1 ``` ``` undefined ``` ``` 2 ```


### инфо
<p>Блок catch получает аргумент x. Это не тот же x, который определен в качестве переменной let x, y;</p>
<p>Затем мы присваиваем этому аргументу значение 1 и устанавливаем значение для переменной y. Потом выводим в консоль значение аргумента x, которое равно 1.</p>
<p>За пределами блока catch переменная x все еще undefined, а y равно 2. Когда мы вызываем console.log(x) за пределами блока catch, этот вызов возвращает undefined, а y возвращает 2.</p>
</div>
</details>

------