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
- [Javascript Local Stoage Use Common Function And Method:)](#js-5)
- [Javascript Simple Basics CRUD Operations:)](#js-6)




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

> Function Input Field Value Empity()

```js
// function inputValueEmpity()
function inputValueEmpity(getId) {
  let inputField = getElementId(getId)
  return inputField.value = ''
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


<a name="js-5"></a>
### Javascript Local Stoage Use Common Function And Method:)

> Product Found Or Not Found Local Storage This Function Chack:)

```js
// Product Found Or Not Found Local Storage This Function Chack
const shoppingCart = () => {
  let cart = {}
  const storeCart = localStorage.getItem('cart')
  if (storeCart) {
    cart = JSON.parse(storeCart)
  }
  return cart
}
```


> Save Product To LocalStorage Use This Function:)

```js
const saveProductToLocalStroage = (product, quantity) => {
  const cart = shoppingCart()
  cart[product] = quantity
  const stringyFi = JSON.stringify(cart)
  // console.log(stringyFi)
  localStorage.setItem('cart', stringyFi)
}
```

> Display  Product From LocalStorage Use This Function:)

```js
const displayProductFromLocalStroage = () => {
  const saveCart = shoppingCart()
  // console.log(saveCart)
  for (const product in saveCart) {
    console.log(product)
    const quantity = saveCart[product]
    console.log(`${quantity}=${saveCart[product]}`)
    displayProduct(product,quantity)
  }
}
displayProductFromLocalStroage()
```

#### [Go to top:arrow_up: ](#top)

<a name="js-6"></a>
### Javascript Simple Basics CRUD Operations:)

#### Structure Chart How To Work CRUD Operations:)

![vlsw0253j7st1ictip03](https://user-images.githubusercontent.com/106922916/224463067-51650cf8-71cd-4a7b-94e2-06332e02fdca.png)

#### Basics CRUD Operations Html Code:)

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CRUD Basics</title>
  <link rel="stylesheet" href="style.css">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css" />
</head>

<body>
  <h1>Social Media App</h1>
  <div class="container">
    <div class="left">
      <form id="form">
        <label for="">Write your post here</label>
        <br><br>
        <textarea name="" id="input" cols="30" rows="10"></textarea>
        <br><br>
        <div id="msg"></div>
        <button type="submit">Post</button>
      </form>
    </div>
    <div class="right">
      <h3>Your posts here</h3>
      <div id="posts">
        <div>
          <p>Post 1</p>
          <span class="options">
            <i onClick="editPost(this)" class="fas fa-edit"></i>
            <i onClick="deletePost(this)" class="fas fa-trash-alt"></i>
          </span>
        </div>
        <div>
          <p>Post 2</p>
          <span class="options">
            <i onClick="editPost(this)" class="fas fa-edit"></i>
            <i onClick="deletePost(this)" class="fas fa-trash-alt"></i>
          </span>
        </div>
      </div>
    </div>
  </div>
</body>
<!-- <script src="main.js"></script> -->
<script src="script.js"></script>

</html>
```

#### Basics CRUD Operations Css Code:)

```css
*{
  text-transform: capitalize;
}
body {
  font-family: sans-serif;
  margin: 0 50px;
}
button{
  width:100px;
  height:50px;
  font-size:1.2rem;
  font-weight:bold;
  background:yellow;
  cursor: pointer;
}
button:focus{
  background:tomato;
  color:#fff;
}
button:active{
  background:green;
  color:#fff;
}
.container {
  display: flex;
  gap: 50px;
}

#posts {
  width: 400px;
}

#posts div {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.options {
  display: flex;
  gap: 25px;
}

i {
  cursor: pointer;
}

#msg {
  color: red;
  margin-bottom:1rem;
  font-weight:bold;
}

textarea{
  font-size:1.5rem;
  font-weight:bold;
  color:#333;
}
```

#### Basics CRUD Operations Important Javascript Code:)

```js
const form = document.getElementById("form");
const input = document.getElementById("input");
const msg = document.getElementById("msg");
const posts = document.getElementById("posts");

// create function Click Button to formSubmit
form.addEventListener('submit', (event) => {
  event.preventDefault()
  if (input.value === '') {
    msg.innerHTML="Input Field Can Not Be Blank!"
  } else {
    acceptData()
  input.focus();
  }
})

// Global Store Data
let data = {}

// Function Accept The Data
const acceptData = () => {
  data["text"] = input.value
  posts.innerHTML += `
    <div>
          <p>${data.text}</p>
          <span class="options">
            <i onClick="editPost(this)" class="fas fa-edit"></i>
            <i onClick="deletePost(this)" class="fas fa-trash-alt"></i>
          </span>
        </div>
    `;
  input.value=''
}

// Funtion Delete The Post()
const deletePost = (e) => {
  e.parentElement.parentElement.remove()
  return
}

// Function Edit The Post()
const editPost = (e) => {
  input.value = e.parentElement.previousElementSibling.innerText;
  input.autofocus = e.parentElement.previousElementSibling.innerText;
  input.focus()
  e.parentElement.parentElement.remove()
  return
}
```

#### Demo Image:)

![screenshot-rocks](https://user-images.githubusercontent.com/106922916/224462921-ac021aa4-ee40-49c2-931e-9f281bd791ec.png)


#### [Go to top:arrow_up: ](#top)
