### Arrays

Define array:

```
> var dict = [];
```

Append dictionary to array:

```
> dict.push({
    key:   "name",
    value: "ruan"
});
```

Print the array:

```
> console.log(dict);
[ { key: 'name', value: 'ruan' } ]
```

### Read File Content:

```
> const fs = require('fs');
> const fileName = "/tmp/foo-bar";
> const myText = fs.readFileSync(fileName, "utf-8");
> console.log(myText);
hello
```
