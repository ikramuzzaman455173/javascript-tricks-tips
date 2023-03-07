<h1 align='center'>Simple Javascript Tips & Tricks</h1>

---

[//]: # (Table of Content)

<a name="top"></a>

## Table of Simple Javascript Tips & Tricks 🙋‍♂️ content

> Click on any topic to go there

- [Javascript Getting User Input in Node.js:)](#js-1)
- [Javascript Common Function Examples:)](#js-2)
- [Function Array Value Generate Html ListItem:)](#js-3)
- [Simple All Important & Usefull Function:)](#js-4)




***

<a name="js-1"></a>

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

#### [Go to top:arrow_up: ](#top)

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

> Function getInputFieldValueById()

```js
// Function getInputFieldValueById()
function getInputFieldValueById(inputFieldId) {
  const inputField = document.getElementById(inputFieldId);
  const inputFieldValueString = inputField.value;
  const inputFieldValue = parseFloat(inputFieldValueString);
  return inputFieldValue;
}
```


### Function getTextElementValueById()

```js
// Function getTextElementValueById()
function getTextElementValueById(elementId) {
  const textElement = document.getElementById(elementId);
  const textElementValueString = textElement.innerText;
  // const textElementValue = textElementValueString;
  return textElementValueString;
}
```

### Function setTextElementValueById()


```js
// Function setTextElementValueById()
function setTextElementValueById(elementId, newValue) {
  const textElement = document.getElementById(elementId);
  textElement.innerText = newValue;
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


<a name="js-4"></a>

#### [Go to top:arrow_up: ](#top)

### Simple Usefull & All Important Functions:)

> Javascript Add Items:)

```js
// add item
function addItem() {
  const lastPickedColor = colorInput.value;
  const li = document.createElement("li");
  li.innerHTML = addInput.value;
  li.style.color = lastPickedColor;
  changeColor();
  itemList.appendChild(li);

  addInput.value = "";
}
```

> Javascript Remove Items:)

```js
// remove item
function removeItem() {
  let li = document.querySelector("li:last-child");
  itemList.removeChild(li);
}
```


> Javascript Change Color:)

```js
// change color
function changeColor() {
  const List = document.querySelectorAll("li");
  const lastPickedColor = colorInput.value;
  for (let i = 0; i < List.length; i++) {
    List[i].style.color = lastPickedColor;
  }
}
```

> Javascript Mouse Over Text UpperCase:)

```js
// uppercase
itemList.addEventListener("mouseover", (event) => {
  if (event.target.tagName == "LI") {
    event.target.style.textTransform = "uppercase";
  }
});
```

> Javascript Mouse Out Text UpperCase:)

```js
// lowercase
itemList.addEventListener("mouseout", (event) => {
  if (event.target.tagName == "LI") {
    event.target.style.textTransform = "lowercase";
  }
});
```

> Javascript Text Hide And Show Function:)

```js
// hide/show list
function toggleButton() {
  if (listDiv.style.display == "none") {
    listDiv.style.display = "block";
    toggle.textContent = "Hide list";
  } else {
    listDiv.style.display = "none";
    toggle.textContent = "Show list";
  }
}
```

#### [Go to top:arrow_up: ](#top)
