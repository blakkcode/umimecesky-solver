# umimecesky-solver
kod který napíše odpověd k dané otázce na umimecesky.cz

## kód
```js
var odpovedi = questions.find(q => q.id == window.location.pathname.split("/")[2])
var explanation = odpovedi.options.find(o => o.correct === 1)
console.log("Odpověd je: <"+explanation.option[0][1]+">")

// -> Odpověd je: <...>
```

## lepší verze
```js
var odpovedi = questions.find(q => q.id == window.location.pathname.split("/")[2])
var explanation = odpovedi.options.find(o => o.correct === 1)
var odpoved = explanation.option[0][1]
$("span:contains("+odpoved+")").click()
console.log("Odpověd je: <"+odpoved+">")
```
