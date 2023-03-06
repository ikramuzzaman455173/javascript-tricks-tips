<h1 align='center'>Simple Javascript Tips & Tricks</h1>

---

[//]: # (Table of Content)

<a name="top"></a>

## Table of Simple Javascript Tips & Tricks 🙋‍♂️ content

> Click on any topic to go there

- [Javascript Getting User Input in Node.js:)](#js-1)
- [Javascript Common Function Examples:)](#js-2)
- [Function Array Value Generate Html ListItem:)](#js-3)



***

<a name="js-1"></a>

### [One Of The Best Websit For Bd Javascript Learners:)](https://with.zonayed.me/js)


### Javascript Getting User Input in Node.js:)


![node-input](https://user-images.githubusercontent.com/106922916/215346267-98865629-610f-4cd2-8a3f-209968e76496.PNG)


```javascript
const readline = require('readline').createInterface({
  input: process.stdin,
  output: process.stdout
});

readline.question('Who are you?\n', name => {
  console.log(`Hey there ${name}!`);
  readline.close();
});
```

### Javascript Common Function Examples:)
<a name="js-2"></a>

> This Function Use For All Id Get In Javascript  😀

```js
// This Function Use For All Id Get In Javascript  😀
function getElementId(getId) {
  const elementId = document.getElementById(getId)
  return elementId
}
```

> This Function Use For All Class Get In Javascript  😀

```js
function getElementClass(getClass) {
  const elementClass = document.getElementsByClassName(getClass)
  return elementClass
}
```

> Function all text element convert in number

```js
// function all text element convert in number
function getTextElementValueById(elementId) {
  let getElement = document.getElementById(elementId)
  let getElementValue = parseInt(getElement.innerText)
  return getElement.innerText=getElementValue
}
```

> Funtion all elementIdGet & set new value 


```js
// Funtion all elementIdGet & set new value 
function setTextElementValueById(elementId, value) {
  let setElement = document.getElementById(elementId);
  setElement.innerText=value
}
```

<a name="js-3"></a>
### Function Array Value Generate Html ListItem:)

```js
// function Generate Array List Items
function operateOnArrayValues(arr) {
  let item = "";
  for (let i = 0; i < arr?.length; i++) {
    item += `<li>${arr[i]}</li>`;
  }
  return item;
}
```
