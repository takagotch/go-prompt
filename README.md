### go-prompt
---
https://github.com/c-bata/go-prompt

```go
package main

import (
  "fmt"
  "github.com/c-bata/go-prompt"
)

func completer(d prompt.Document) []prompt.Suggest {
  s := []prompt.Suggest{
    {Text: "users", Description: "Store the username and age"},
    {Text: "articles", Description: "Store the article text posted by user"},
    {Text: "comments", Description: "Store the text commented to articles"}
  }
  return prompt.FilterHasPrefix(s, d.GetWordBeforeCursor(), true)
}

func main() {
  fmt.Println("Please select table.")
  t := prompt.Input("> ", completer)
  fmt.Println("You selected " + t)
}
```

```
kube-prompt

get deployments --all namespace
exec -it mysql-xxx-wn9b bash
logs redis-xxxx.r2mzm --timestamps | tail -n 5
```

```
```


