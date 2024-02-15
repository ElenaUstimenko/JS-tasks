<h2 align="center"><img align="center" src="./image/JavaScript-logo.png" height="40" width="40"/>     Java Script задачки и вопросы</h2>

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
_Что будет в консоли?_

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
_Что будет в консоли?_

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
_Какие из этих значений являются "ложными"?_

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
_Что будет в консоли?_

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

## ✔️ 47
_Write a function that takes an array of numbers and returns the sum of the numbers. The numbers can be negative or non-integer. If the array does not contain any numbers then you should return 0._

_Examples_

```
Input: [1, 5.2, 4, 0, -1]
Output: 9.2

Input: []
Output: 0

Input: [-2.398]
Output: -2.398
```
_Assumptions_
_You can assume that you are only given numbers._
_You cannot assume the size of the array._
_You can assume that you do get an array and if the array is empty, return 0._


<details><summary><b>решение</b></summary>

<div>

```
sum = function (numbers) {
  "use strict";
  return numbers.reduce(function(acc, number) {
    return acc + number;
  }, 0);
};
``` 


### инфо
<p>Метод массива reduce() позволяет превратить массив в любое другое значение с помощью переданной функции-колбэка и начального значения. Функция-колбэк будет вызвана для каждого элемента массива, и всегда должна возвращать результат.</p>
</div>
</details>

------

## ✔️ 48
_Consider an array/list of sheep where some sheep may be missing from their place. We need a function that counts the number of sheep present in the array (true means present)._

_For example,_

```
[true,  true,  true,  false,
  true,  true,  true,  true ,
  true,  false, true,  false,
  true,  false, false, true ,
  true,  true,  true,  true ,
  false, false, true,  true]
```
_The correct answer would be 17._
_Hint: Don't forget to check for bad values like null/undefined_


<details><summary><b>решение</b></summary>

<div>

```
function countSheeps(sheep) {
  return sheep.filter(Boolean).length;
}
``` 


### инфо
<p>Объект Boolean представляет значения истинности: true или false.</p>
<p>Значение, переданное первым параметром, при необходимости преобразуется в логическое значение. Если значение опущено или равно 0, -0, null, false, NaN, undefined или пустой строке (""), объект имеет начальное значение, равное false. Все остальные значения, включая любые объекты или строку "false", создают объект с начальным значением, равным true.</p>
</div>
</details>

------

## ✔️ 49
_In this little assignment you are given a string of space separated numbers, and have to return the highest and lowest number._

_Examples_

```
highAndLow("1 2 3 4 5");  // return "5 1"
highAndLow("1 2 -3 4 5"); // return "5 -3"
highAndLow("1 9 3 4 -5"); // return "9 -5"
```
_Notes_
_All numbers are valid Int32, no need to validate them._
_There will always be at least one number in the input string._
_Output string must be two numbers separated by a single space, and highest number is first._


<details><summary><b>решение</b></summary>

<div>

```
function highAndLow(numbers){
  numbers = numbers.split(' ');
  return `${Math.max(...numbers)} ${Math.min(...numbers)}`;
}
``` 


### инфо
<p>Метод split() разбивает объект String на массив строк путём разделения строки указанной подстрокой.</p>
<p>Метод Math.max() возвращает наибольшее из нуля или более чисел.</p>
<p>Метод Math.min() возвращает наименьшее из нуля или более чисел.</p>
</div>
</details>

------

## ✔️ 50
_Who remembers back to their time in the schoolyard, when girls would take a flower and tear its petals, saying each of the following phrases each time a petal was torn:_

_"I love you"_
_"a little"_
_"a lot"_
_"passionately"_
_"madly"_
_"not at all"_

_If there are more than 6 petals, you start over with "I love you" for 7 petals, "a little" for 8 petals and so on._
_When the last petal was torn there were cries of excitement, dreams, surging thoughts and emotions._
_Your goal in this kata is to determine which phrase the girls would say at the last petal for a flower of a given number of petals. The number of petals is always greater than 0._


<details><summary><b>решение</b></summary>

<div>

```
function howMuchILoveYou(nbPetals) {
  const muchLoves = [
    'I love you',
    'a little',
    'a lot',
    'passionately',
    'madly',
    'not at all'
  ];
  return muchLoves[(nbPetals - 1) % muchLoves.length];
}
``` 
</div>
</details>

------

## ✔️ 51
_You take your son to the forest to see the monkeys. You know that there are a certain number there (n), but your son is too young to just appreciate the full number, he has to start counting them from 1._

_As a good parent, you will sit and count with him. Given the number (n), populate an array with all numbers up to and including that number, but excluding zero._

_For example(Input --> Output):_

```
10 --> [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
 1 --> [1]
``` 

<details><summary><b>решение</b></summary>

<div>

```
function monkeyCount(n) {
  let arr = [];
  for(let i = 1; i <= n; i++) {
    arr.push(i);
  }
  return arr;
}
``` 

### инфо
<p>Метод push() добавляет один или более элементов в конец массива и возвращает новую длину массива.</p>
</div>
</details>

------

## ✔️ 52
_Given an array of integers._

_Return an array, where the first element is the count of positives numbers and the second element is sum of negative numbers. 0 is neither positive nor negative._
_If the input is an empty array or is null, return an empty array._

_Example_

```
For input [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15], you should return [10, -65].
``` 

<details><summary><b>решение</b></summary>

<div>

```
function countPositivesSumNegatives(input) {
    return input && input.length 
      ? [input.filter(p => p > 0).length, input.filter(n => n < 0).reduce((a, b) => a + b, 0)] 
      : [];
}
``` 

### инфо
<p>Метод массива reduce() позволяет превратить массив в любое другое значение с помощью переданной функции-колбэка и начального значения. Функция-колбэк будет вызвана для каждого элемента массива, и всегда должна возвращать результат.</p>
</div>
</details>

------

## ✔️ 53
_We need a function that can transform a number (integer) into a string._

_What ways of achieving this do you know?_

_Examples (input --> output):_


```
123  --> "123"
999  --> "999"
-100 --> "-100"
``` 

<details><summary><b>решение</b></summary>

<div>

```
function numberToString(num) {
  return num.toString();
}
``` 

### инфо
<p>Метод toString() возвращает строку, представляющую объект.</p>
</div>
</details>

------

## ✔️ 54
_Given an array of integers, return a new array with each value doubled._

_For example:_


```
[1, 2, 3] --> [2, 4, 6]
``` 

<details><summary><b>решение</b></summary>

<div>

```
function maps(x){
  return x.map(n => n * 2);
}
``` 

### инфо
<p>Метод map() создаёт новый массив с результатом вызова указанной функции для каждого элемента массива.</p>
</div>
</details>

------

## ✔️ 55
_You're at the zoo... all the meerkats look weird. Something has gone terribly wrong - someone has gone and switched their heads and tails around!_

_Save the animals by switching them back. You will be given an array which will have three values (tail, body, head). It is your job to re-arrange the array so that the animal is the right way round (head, body, tail)._

_Same goes for all the other arrays/lists that you will get in the tests: you have to change the element positions with the same exact logics

_Simples!_


<details><summary><b>решение</b></summary>

<div>

```
function fixTheMeerkat(arr) {
  return arr.reverse();
}
``` 

### инфо
<p>Метод reverse() на месте обращает порядок следования элементов массива. Первый элемент массива становится последним, а последний — первым.</p>
</div>
</details>

------

## ✔️ 56
_Given a non-empty array of integers, return the result of multiplying the values together in order. Example:_

```
[1, 2, 3, 4] => 1 * 2 * 3 * 4 = 24
```

<details><summary><b>решение</b></summary>

<div>

```
function grow(x){
  return x.reduce((a, b)=> a * b);
}
``` 

### инфо
<p>Метод reduce() применяет функцию reducer к каждому элементу массива (слева-направо), возвращая одно результирующее значение.</p>
</div>
</details>

------

## ✔️ 57
_In this simple exercise, you will build a program that takes a value, integer , and returns a list of its multiples up to another value, limit . If limit is a multiple of integer, it should be included as well. There will only ever be positive integers passed into the function, not consisting of 0. The limit will always be higher than the base._
_For example, if the parameters passed are (2, 6), the function should return [2, 4, 6] as 2, 4, and 6 are the multiples of 2 up to 6._


<details><summary><b>решение</b></summary>

<div>

```
function findMultiples(integer, limit){
  let result = []
  
  for (let i = integer; i <= limit ; i+= integer)
    result.push(i)
    
  return result;
}
``` 
</div>
</details>

------

## ❔ 58
_Каким будет результат?_

```
const firstPromise = new Promise((res, rej) => {
  setTimeout(res, 500, 'один');
});

const secondPromise = new Promise((res, rej) => {
  setTimeout(res, 100, 'два');
});

Promise.race([firstPromise, secondPromise]).then(res => console.log(res));
```


<details><summary><b>ответ</b></summary>

<div>

```"два"``` 

### инфо
<p>Когда мы передаем несколько промисов методу Promise.race, он разрешает/отклоняет первый промис, который разрешается/отклоняется. В метод setTimeout мы передаем таймер: 500 мс для первого промиса (firstPromise) и 100 мс для второго промиса (secondPromise). Это означает, что secondPromise разрешается первым со значением 'два'. res теперь содержит значение 'два', которое выводиться в консоль.</p>
</div>
</details>

------

## ✔️ 59
_Complete the function that takes a non-negative integer n as input, and returns a list of all the powers of 2 with the exponent ranging from 0 to n ( inclusive )._

_Examples_

```
n = 0  ==> [1]        # [2^0]
n = 1  ==> [1, 2]     # [2^0, 2^1]
n = 2  ==> [1, 2, 4]  # [2^0, 2^1, 2^2]
```

<details><summary><b>решение</b></summary>

<div>

```
function powersOfTwo(n){
  var result = [];
  for (var i = 0; i <= n; i++) {
    result.push(Math.pow(2, i));
  }
  return result;
}
``` 

```
function powersOfTwo(n) {
  return Array.from({length: n + 1}, (v, k) => 2 ** k);
}
```

### инфо
<p>Метод Math.pow() возвращает основание, возведённое в степень показатель, то есть, значение выражения: основание показатель.</p>
<p>Метод Array.from() создаёт новый экземпляр Array из массивоподобного или итерируемого объекта.</p>
</div>
</details>

------

## ✔️ 60
_I'm new to coding and now I want to get the sum of two arrays... Actually the sum of all their elements. I'll appreciate for your help._

_P.S. Each array includes only integer numbers. Output is a number too._


<details><summary><b>решение</b></summary>

<div>

```
function arrayPlusArray(arr1, arr2) {
  return arr1.concat(arr2).reduce((a, b) => a + b)
}
``` 

### инфо
<p>Метод concat() возвращает новый массив, состоящий из массива, на котором он был вызван, соединённого с другими массивами и/или значениями, переданными в качестве аргументов.</p>
<p>Метод reduce() применяет функцию reducer к каждому элементу массива (слева-направо), возвращая одно результирующее значение.</p>
</div>
</details>

------

## ✔️ 61
_Task_
_Create a method to see whether the string is ALL CAPS._

_Examples (input -> output)_

```
"c" -> False
"C" -> True
"hello I AM DONALD" -> False
"HELLO I AM DONALD" -> True
"ACSKLDFJSgSKLDFJSKLDFJ" -> False
"ACSKLDFJSGSKLDFJSKLDFJ" -> True
``` 

_In this Kata, a string is said to be in ALL CAPS whenever it does not contain any lowercase letter so any string containing no letters at all is trivially considered to be in ALL CAPS._

<details><summary><b>решение</b></summary>

<div>

```
String.prototype.isUpperCase=function() {
  return this==this.toUpperCase()
  }
``` 
</div>
</details>

------

## ✔️ 62
_Upon arriving at an interview, you are presented with a solid blue cube. The cube is then dipped in red paint, coating the entire surface of the cube. The interviewer then proceeds to cut through the cube in all three dimensions a certain number of times._

_Your function takes as parameter the number of times the cube has been cut. You must return the number of smaller cubes created by the cuts that have at least one red face._

_To make it clearer, the picture below represents the cube after (from left to right) 0, 1 and 2 cuts have been made._

![cube](./image/image%20for%2062.png)

``` 
Examples:
If we cut the cube 2 times, the function should return 26
If we cut the cube 4 times, the function should return 98
``` 

<details><summary><b>решение</b></summary>

<div>

```
function countSquares(cuts){
  return cuts == 0 
    ? 1 
    : 6 * cuts * cuts + 2
}
``` 
</div>
</details>

------

## ✔️ 63
_All of the animals are having a feast! Each animal is bringing one dish. There is just one rule: the dish must start and end with the same letters as the animal's name. For example, the great blue heron is bringing garlic naan and the chickadee is bringing chocolate cake._

_Write a function feast that takes the animal's name and dish as arguments and returns true or false to indicate whether the beast is allowed to bring the dish to the feast._

_Assume that beast and dish are always lowercase strings, and that each has at least two letters. beast and dish may contain hyphens and spaces, but these will not appear at the beginning or end of the string. They will not contain numerals._

<details><summary><b>решение</b></summary>

<div>

```
function feast(beast, dish) {
	return beast[0] === dish[0] && beast[beast.length - 1] === dish[dish.length - 1]
}
``` 
</div>
</details>

------

## ✔️ 64
_If you've completed this kata already and want a bigger challenge, here's the 3D version._

_Bob is bored during his physics lessons so he's built himself a toy box to help pass the time. The box is special because it has the ability to change gravity._

There are some columns of toy cubes in the box arranged in a line. The i-th column contains a_i cubes. At first, the gravity in the box is pulling the cubes downwards. When Bob switches the gravity, it begins to pull all the cubes to a certain side of the box, d, which can be either 'L' or 'R' (left or right). Below is an example of what a box of cubes might look like before and after switching gravity.

``` 
+---+                                       +---+
|   |                                       |   |
+---+                                       +---+
+---++---+     +---+              +---++---++---+
|   ||   |     |   |   -->        |   ||   ||   |
+---++---+     +---+              +---++---++---+
+---++---++---++---+         +---++---++---++---+
|   ||   ||   ||   |         |   ||   ||   ||   |
+---++---++---++---+         +---++---++---++---+
``` 

_Given the initial configuration of the cubes in the box, find out how many cubes are in each of the n columns after Bob switches the gravity._

_Examples input -> output:_
```
* 'R', [3, 2, 1, 2]      ->  [1, 2, 2, 3]
* 'L', [1, 4, 5, 3, 5 ]  ->  [5, 5, 4, 3, 1]
```

<details><summary><b>решение</b></summary>

<div>

```
const flip=(d, a)=>{
  if(d === 'R') return a.sort((a, b) => a - b);
  if(d === 'L') return a.sort((a, b) => b - a);
}
``` 

### инфо
<p>Метод sort() на месте сортирует элементы массива и возвращает отсортированный массив.</p>
</div>
</details>

------

## ✔️ 65
_Summation_

_Write a program that finds the summation of every number from 1 to num. The number will always be a positive integer greater than 0. Your function only needs to return the result, what is shown between parentheses in the example below is how you reach that result and it's not part of it, see the sample tests._

_For example (Input -> Output):_

``` 
2 -> 3 (1 + 2)
8 -> 36 (1 + 2 + 3 + 4 + 5 + 6 + 7 + 8)
``` 

<details><summary><b>решение</b></summary>

<div>

```
var summation = function (num) {
  var sum = 0;
  for( var i = 0; i <= num; i++ ){
    sum += i
  }
  return sum;
}
``` 
</div>
</details>

------

## ✔️ 66
_For every good kata idea there seem to be quite a few bad ones!_

_In this kata you need to check the provided array (x) for good ideas 'good' and bad ideas 'bad'. If there are one or two good ideas, return 'Publish!', if there are more than 2 return 'I smell a series!'. If there are no good ideas, as is often the case, return 'Fail!'._

<details><summary><b>решение</b></summary>

<div>

```
const well = x => {
  const count = x.filter(x => x == 'good').length;
  return count < 1 ? 'Fail!' : 
         count < 3 ? 'Publish!' : 'I smell a series!';
}
``` 

### инфо
<p>Метод filter() создаёт новый массив со всеми элементами, прошедшими проверку, задаваемую в передаваемой функции.</p>
</div>
</details>

------

## ✔️ 67
_To find the volume (centimeters cubed) of a cuboid you use the formula:_

_volume = Length * Width * Height_

_But someone forgot to use proper record keeping, so we only have the volume, and the length of a single side!_

_It's up to you to find out whether the cuboid has equal sides (= is a cube)._

_Return true if the cuboid could have equal sides, return false otherwise._

_Return false for invalid numbers too (e.g volume or side is less than or equal to 0)._

_Note: side will be an integer_

<details><summary><b>решение</b></summary>

<div>

```
var cubeChecker = function(volume, side){
  return Math.pow(side, 3) === volume && side > 0;
};
``` 

### инфо
<p>Метод Math.pow() возвращает основание, возведённое в степень показатель, то есть, значение выражения: основаниепоказатель.</p>
</div>
</details>

------

## ✔️ 68
_Write a function that accepts an integer n and a string s as parameters, and returns a string of s repeated exactly n times._

_Examples (input -> output)_
``` 
6, "I"     -> "IIIIII"
5, "Hello" -> "HelloHelloHelloHelloHello"
``` 

<details><summary><b>решение</b></summary>

<div>

```
function repeatStr (n, s) {
  return s.repeat(n);
}
``` 

### инфо
<p>Метод repeat() конструирует и возвращает новую строку, содержащую указанное количество соединённых вместе копий строки, на которой он был вызван.</p>
</div>
</details>

------

## ✔️ 69
_In this simple assignment you are given a number and have to make it negative. But maybe the number is already negative?_

_Examples_
``` 
makeNegative(1);    // return -1
makeNegative(-5);   // return -5
makeNegative(0);    // return 0
makeNegative(0.12); // return -0.12
``` 
_Notes_
_The number can be negative already, in which case no change is required._
_Zero (0) is not checked for any specific sign. Negative zeros make no mathematical sense._


<details><summary><b>решение</b></summary>

<div>

```
function makeNegative(num) {
  if ( num > 0 ) {
    return -num;
  } else {
    return num;
  }
}
``` 
</div>
</details>

------

## ✔️ 70
_You get an array of numbers, return the sum of all of the positives ones._

Example 
```
[1,-4,7,12] => 1 + 7 + 12 = 20
```
_Note: if there is nothing to sum, the sum is default to 0._


<details><summary><b>решение</b></summary>

<div>

```
function positiveSum(arr) {
  return arr.reduce((a,b)=> a + (b > 0 ? b : 0), 0);
}
``` 

### инфо
<p>Метод reduce() применяет функцию reducer к каждому элементу массива (слева-направо), возвращая одно результирующее значение.</p>
</div>
</details>

------

## ✔️ 71
_It's the academic year's end, fateful moment of your school report. The averages must be calculated. All the students come to you and entreat you to calculate their average for them. Easy ! You just need to write a script._

_Return the average of the given array rounded down to its nearest integer._

_The array will never be empty._

<details><summary><b>решение</b></summary>

<div>

```
function getAverage(marks) {
  return Math.floor(marks.reduce((a, b) => a + b, 0) / marks.length);
}
``` 

### инфо
<p>Метод Math.floor() - округление вниз. Округляет аргумент до ближайшего меньшего целого.</p>
</div>
</details>

------

## ✔️ 72
_Complete the function which takes two arguments and returns all numbers which are divisible by the given divisor. First argument is an array of numbers and the second is the divisor._

_Example(Input1, Input2 --> Output)._
``` 
[1, 2, 3, 4, 5, 6], 2 --> [2, 4, 6]
``` 

<details><summary><b>решение</b></summary>

<div>

```
function divisibleBy(numbers, divisor) {
  return numbers.filter(n => n % divisor === 0)
}
``` 

### инфо
<p>Метод filter() создаёт новый массив со всеми элементами, прошедшими проверку, задаваемую в передаваемой функции.</p>
</div>
</details>

------

## ✔️ 73
_Description_
_An infinite number of shelves are arranged one above the other in a staggered fashion.
The cat can jump either one or three shelves at a time: from shelf i to shelf i+1 or i+3 (the cat cannot climb on the shelf directly above its head), according to the illustration:_

``` 
                 ┌────────┐
                 │-6------│
                 └────────┘
┌────────┐       
│------5-│        
└────────┘  ┌─────► OK!
            │    ┌────────┐
            │    │-4------│
            │    └────────┘
┌────────┐  │
│------3-│  │     
BANG!────┘  ├─────► OK! 
  ▲  |\_/|  │    ┌────────┐
  │ ("^-^)  │    │-2------│
  │ )   (   │    └────────┘
┌─┴─┴───┴┬──┘
│------1-│
└────────┘
``` 
_Input_
_Start and finish shelf numbers (always positive integers, finish no smaller than start)_

_Task_
_Find the minimum number of jumps to go from start to finish_

_Example_
_Start 1, finish 5, then answer is 2 (1 => 4 => 5 or 1 => 2 => 5)_

_Inspirers_

![cats](./image/cats%20for%2073.jpg)

<details><summary><b>решение</b></summary>

<div>

```
function solution(start, finish) {
  return Math.floor((finish - start) / 3) + (finish - start) % 3;
}
``` 

### инфо
<p>Метод Math.floor() - округление вниз. Округляет аргумент до ближайшего меньшего целого.</p>
</div>
</details>

------

## ✔️ 74
_Sometimes, I want to quickly be able to convert miles per imperial gallon (mpg) into kilometers per liter (kpl)._

_Create an application that will display the number of kilometers per liter (output) based on the number of miles per imperial gallon (input)._

_Make sure to round off the result to two decimal points._

_Some useful associations relevant to this kata:_

_1 Imperial Gallon = 4.54609188 litres_
_1 Mile = 1.609344 kilometres_


<details><summary><b>решение</b></summary>

<div>

```
function converter(mpg) {
  return Math.round(((mpg * 1.609344) / 4.54609188) * 100) / 100;
}
``` 
```
function converter(mpg) {
  return parseFloat((1.609344 / 4.54609188 * mpg).toFixed(2));
}
``` 


### инфо
<p>Метод Math.round() возвращает число, округлённое к ближайшему целому.</p>
<p>Метод toFixed() форматирует число, используя запись с фиксированной запятой.</p>
</div>
</details>

------

## ✔️ 75
_Summation_
_Write a program that finds the summation of every number from 1 to num. The number will always be a positive integer greater than 0. Your function only needs to return the result, what is shown between parentheses in the example below is how you reach that result and it's not part of it, see the sample tests._

_For example (Input -> Output):_
```
2 -> 3 (1 + 2)
8 -> 36 (1 + 2 + 3 + 4 + 5 + 6 + 7 + 8)
```

<details><summary><b>решение</b></summary>

<div>

```
var summation = function(num) {
  let result = 0;
  for (var i = 1; i <= num; i++) {
    result += i;
  }
  
  return result;
}
``` 
</div>
</details>

------

## ✔️ 76
_Rock Paper Scissors_
_Let's play! You have to return which player won! In case of a draw return Draw!._

_Examples(Input1, Input2 --> Output):_
```
"scissors", "paper" --> "Player 1 won!"
"scissors", "rock" --> "Player 2 won!"
"paper", "paper" --> "Draw!"
```
![scissors](./image/scissors%20for%2076.png)

<details><summary><b>решение</b></summary>

<div>

```
const rps = (p1, p2) => {
  if (p1 == p2)
    return 'Draw!';
    
  if (p1 == 'rock' && p2 == 'scissors') 
    return 'Player 1 won!'
  else if (p1 == 'scissors' && p2 == 'paper') 
    return 'Player 1 won!'
  else if (p1 == 'paper' && p2 == 'rock') 
    return 'Player 1 won!'
  else
    return 'Player 2 won!';
};
``` 
</div>
</details>

------

## ✔️ 77
_In this Kata, you will be given an array of numbers in which two numbers occur once and the rest occur only twice. Your task will be to return the sum of the numbers that occur only once._

_For example,_
```
repeats([4,5,7,5,4,8]) = 15
```
_because only the numbers 7 and 8 occur once, and their sum is 15. Every other number occurs twice._

<details><summary><b>решение</b></summary>

<div>

```
function repeats(arr){
  return arr.filter(v => arr.indexOf(v) === arr.lastIndexOf(v)).reduce((a, b) => a + b, 0);
};
``` 

### инфо
<p>Метод filter() создаёт новый массив со всеми элементами, прошедшими проверку, задаваемую в передаваемой функции.</p>
<p>Метод indexOf() возвращает первый индекс, по которому данный элемент может быть найден в массиве или -1, если такого индекса нет.</p>
<p>Метод lastIndexOf() возвращает индекс последнего вхождения указанного значения в строковый объект String, на котором он был вызван, или -1, если ничего не было найдено.</p>
<p>Метод reduce() применяет функцию reducer к каждому элементу массива (слева-направо), возвращая одно результирующее значение.</p>
</div>
</details>

------

## ✔️ 78
_Let us begin with an example:_

_Take a number: 56789. Rotate left, you get 67895._

_Keep the first digit in place and rotate left the other digits: 68957._

_Keep the first two digits in place and rotate the other ones: 68579._

_Keep the first three digits and rotate left the rest: 68597. Now it is over since keeping the first four it remains only one digit which rotated is itself._

_You have the following sequence of numbers:_

```
56789 -> 67895 -> 68957 -> 68579 -> 68597
```

_and you must return the greatest:_ ```68957```

_Task_
_Write function max_rot(n) which given a positive integer n returns the maximum number you got doing rotations similar to the above example._

_So max_rot (or maxRot or ... depending on the language) is such as:_

_max_rot(56789) should return 68957_

_max_rot(38458215) should return 85821534_

<details><summary><b>решение</b></summary>

<div>

```
function maxRot(n){
  let max = n
  let arr = String(n).split('')
  for(let i = 0; i < arr.length; i++){
    arr.push(arr.splice(i, 1))
    const num = Number(arr.join(''))
    if(num > max) max = num
  }
  return max;
}
``` 

### инфо
<p>Метод split() разбивает объект String на массив строк путём разделения строки указанной подстрокой.</p>
<p>Метод push() добавляет один или более элементов в конец массива и возвращает новую длину массива.</p>
<p>Метод join() объединяет все элементы массива (или массивоподобного объекта) в строку.</p>
</div>
</details>

------

## ✔️ 79
_Story_
_YouTube had a like and a dislike button, which allowed users to express their opinions about particular content. It was set up in such a way that you cannot like and dislike a video at the same time. There are two other interesting rules to be noted about the interface: Pressing a button, which is already active, will undo your press. If you press the like button after pressing the dislike button, the like button overwrites the previous "Dislike" state. The same is true for the other way round._

_Task_
_Create a function that takes in a list of button inputs and returns the final state._

_Examples_

```
likeOrDislike([Dislike]) => Dislike
likeOrDislike([Like,Like]) => Nothing
likeOrDislike([Dislike,Like]) => Like
likeOrDislike([Like,Dislike,Dislike]) => Nothing
```

_Notes_
_If no button is currently active, return Nothing._
_If the list is empty, return Nothing._

<details><summary><b>решение</b></summary>

<div>

```
function likeOrDislike(buttons) {
  let state = 'Nothing';

  for (let i = 0; i < buttons.length; i++) {
    if (buttons[i] === state) {
      state = 'Nothing'
    } else {
      state = buttons[i]
    }
  }

  return state;
}
``` 
</div>
</details>

------

## ✔️ 80
_The Western Suburbs Croquet Club has two categories of membership, Senior and Open. They would like your help with an application form that will tell prospective members which category they will be placed._

_To be a senior, a member must be at least 55 years old and have a handicap greater than 7. In this croquet club, handicaps range from -2 to +26; the better the player the lower the handicap._

_Input_
_Input will consist of a list of pairs. Each pair contains information for a single potential member. Information consists of an integer for the person's age and an integer for the person's handicap._

_Output_
_Output will consist of a list of string values (in Haskell and C: Open or Senior) stating whether the respective member is to be placed in the senior or open category._

_Example_

```
input =  [[18, 20], [45, 2], [61, 12], [37, 6], [21, 21], [78, 9]]
output = ["Open", "Open", "Senior", "Open", "Open", "Senior"]
```

_Notes_
_If no button is currently active, return Nothing._
_If the list is empty, return Nothing._

<details><summary><b>решение</b></summary>

<div>

```
function openOrSenior(data){
  return data.map(([age, handicap]) => (age > 54 && handicap > 7) ? 'Senior' : 'Open');
}
``` 

### инфо
<p>Метод map() создаёт новый массив с результатом вызова указанной функции для каждого элемента массива.</p>
</div>
</details>

------

## ❔ 81
_Каким будет результат?_

```
function* generator(i) {
  yield i;
  yield i * 2;
}

const gen = generator(10);

console.log(gen.next().value);
console.log(gen.next().value);
```


<details><summary><b>ответ</b></summary>

<div>

```10``` ```20``` 

### инфо
<p>Обычные функции не могут быть остановлены на полпути после вызова. Однако функцию generator можно "остановить" на полпути, а затем продолжить с того места, где она остановилась. Каждый раз, когда в функции-generator встречается ключевое слово yield, функция возвращает значение, указанное после него. Функция generator в этом случае не return значение, оно yields значение.</p>
<p>Сначала мы инициализируем функцию generator с i, равным 10. Мы вызываем функцию generator, используя метод next(). Когда мы в первый раз вызываем функцию generator, i равно 10. Он встречает первое ключевое слово yield, получая значение i. Generator теперь "приостановлен", и 10 выводится в консоль.</p>
<p>Затем мы снова вызываем функцию с помощью метода next(). Она запускается с того места, где остановилась ранее, все еще с i, равным 10. Теперь он встречает следующее ключевое слово yield и возвращает i * 2. i равно 10, поэтому он возвращает 10 * 2, то есть 20. Это приводит к 10, 20.</p>
</div>
</details>

------

## ❔ 82
_Что будет на выходе?_

```
const promise1 = Promise.resolve('First')
const promise2 = Promise.resolve('Second')
const promise3 = Promise.reject('Third')
const promise4 = Promise.resolve('Fourth')

const runPromises = async () => {
	const res1 = await Promise.all([promise1, promise2])
	const res2  = await Promise.all([promise3, promise4])
	return [res1, res2]
}

runPromises()
	.then(res => console.log(res))
	.catch(err => console.log(err))
```


<details><summary><b>ответ</b></summary>

<div>

```'Third'```

### инфо
<p>Метод Promise.all выполняет переданные промисы параллельно. Если одно обещание не выполняется, метод Promise.all отклоняется со значением отклоненного обещания. В этом случае promise3 отклонен со значением "Third". Мы перехватываем отклоненное значение в цепочке методов catch при вызове runPromises, чтобы перехватывать любые ошибки внутри функции runPromises. Только "Third" регистрируется, так как promise3 отклонено с этим значением.</p>
<p>Статический Promise.resolve()метод «преобразовывает» заданное значение в файл Promise.</p>
<p>Статический Promise.reject()метод возвращает Promiseобъект, отклоненный по указанной причине.</p>
</div>
</details>

------

## ❔ 83
_Что будет на выходе?_

```
const emojis = ['🥑', ['✨', '✨', ['🍕', '🍕']]];

console.log(emojis.flat(1));
```


<details><summary><b>ответ</b></summary>

<div>

```['🥑', '✨', '✨', ['🍕', '🍕']]```

### инфо
<p>Метод flat() экземпляров Array создает новый массив со всеми элементами подмассива, рекурсивно объединенными в него до указанной глубины.</p>
<p>Глубина объединённого массива зависит от значения, которое мы передаем. В этом случае мы передали значение 1 (которое нам не нужно, это значение по умолчанию), что означает, что будут объединены только массивы на первой глубине. ['🥑'] и ['✨', '✨', ['🍕', '🍕']] в этом случае. Конкатенация этих двух массивов приводит к ['🥑', '✨', '✨', ['🍕', '🍕']].</p>
</div>
</details>

------

## ❔ 84
_Что будет на выходе?_

```
const animals = {};
let dog = { emoji: '🐶' }
let cat = { emoji: '🐈' }

animals[dog] = { ...dog, name: "Mara" }
animals[cat] = { ...cat, name: "Sara" }

console.log(animals[dog])
```


<details><summary><b>ответ</b></summary>

<div>

```{ emoji: "🐈", name: "Sara" }```

### инфо
<p>Ключи объекта преобразуются в строки.</p>
<p>Поскольку значение dog является объектом, animals[dog] на самом деле означает, что мы создаем новое свойство под названием "object Object", равное новому объекту. animals["object Object"] теперь равно { emoji: "🐶", name: "Mara"}.</p>
<p>cat также является объектом, что означает, что animals[cat] на самом деле означает, что мы перезаписываем значение animals["object Object"] новыми свойствами кота.</p>
<p>animals[dog], или фактически animals["object Object"], поскольку преобразование объекта dog в строку приводит к "object Object", возвращает { emoji: "🐈", name: " Сара"}.</p>
</div>
</details>

------