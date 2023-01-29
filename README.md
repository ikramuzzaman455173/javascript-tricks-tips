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

