<h2 align="center"><img align="center" src="./image/JavaScript-logo.png" height="40" width="40"/>     Java Script задачки</h2>


------ 

## ✔️1
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

## ✔️2
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

## ✔️3
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

## ✔️4
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

## ✔️5
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

## ✔️6
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

## ✔️7
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

## ✔️8
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

## ✔️9
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

## ✔️10
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