<h1 align='center'>Simple Javascript Tips & Tricks</h1>

---

### Javascript Getting User Input in Node.js:)

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

