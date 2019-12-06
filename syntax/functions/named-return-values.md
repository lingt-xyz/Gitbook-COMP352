# Named return values

Go's return values may be named. If so, they are treated as variables defined at the top of the function.

 A `return` statement without arguments returns the named return values. This is known as a "naked" return.

```go
package main

import "fmt"

// named return (x, y int)
func split(sum int) (x, y int) {
	x = sum * 4 / 9
	y = sum - x
	// return x, y
	return
}

func main() {
	fmt.Println(split(17))
}

// Expected results:
7 10
```

{% hint style="warning" %}
Naked return statements should be used only in short functions, as with the example shown here. They can harm readability in longer functions.
{% endhint %}



