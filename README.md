# fromThing
get from: token from string

I am not sure I understood the problem exactly, as this seemed to be too easy to be what you where actually asking for. But it was fun.


```
function fromTokenThing(searchString) {
  const tokens = []; // you could get an array of additional tokens as you add more...
  const fromstrMatch = searchString.match(/from:\s+/i);
  if (fromstrMatch && fromstrMatch[0]) {
    tokens.push("from");
    return {
      tokens, 
      searchString: searchString.substring(fromstrMatch[0].length),
    };
  }
}

// put that into useEffect when query string changes

//or from your input component event
function stringChangeHandler(event) {
  const [tokens, searchString] = fromTokenThing(event.target.value);
  //use searchString and tokens how you want from here
}
// -> onChange(stringChangeHandler)

```



