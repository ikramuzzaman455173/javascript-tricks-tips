<h1 align='center'>Simple Javascript Tips & Tricks</h1>

---

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
> This Functin Any Id Input Value Find For Working Rememeber Allso Use This getElementId () function For Use This Function 😀

```js
// This Function Get All Input Field Html
function getInputValue(id) {
  const inputField = getElementId(id)
  return inputField
}
```
