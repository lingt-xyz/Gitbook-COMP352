# Zero values

Variables declared without an explicit initial value are given their _zero value_.

The zero value is:

* `0` for numeric types,
* `false` for the boolean type, and
* `""` \(the empty string\) for strings.

```go
package main

import "fmt"

func main() {
	var i int
	var f float64
	var b bool
	var s string
	fmt.Printf("%v %v %v %q\n", i, f, b, s)
}

// Expected results:
0 0 false ""
```

