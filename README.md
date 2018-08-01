# asciimatrix
`import "github.com/sh0rez/asciimatrix"`

* [Overview](#pkg-overview)
* [Index](#pkg-index)

## <a name="pkg-overview">Overview</a>
Package asciimatrix provides a utility a to entries strings at x/y coordinate described locations to be exported as a matrix.

Example:

````go
matrix := Matrix{}
matrix.Put(2, 2, "Hello") // Put "Hello" at location 2/2
matrix.Put(4, 4, "World") // Put "World" at location 4/4

fmt.Println("---")
fmt.Println(matrix) // Print the matrix
fmt.Println("---")
````

This creates the following output:

````
---

  Hello

    World
---
````



## <a name="pkg-index">Index</a>
* [type Matrix](#Matrix)
  * [func (m Matrix) Put(x, y int, text string)](#Matrix.Put)
  * [func (m Matrix) String() string](#Matrix.String)


#### <a name="pkg-files">Package files</a>
[asciimatrix.go](/asciimatrix.go) 






## <a name="Matrix">type</a> [Matrix](/asciimatrix.go?s=684:702#L29)
``` go
type Matrix column
```
A Matrix contains strings addressed by x and y coordinates. They are mutated using matrix.Put(x, y, text).










### <a name="Matrix.Put">func</a> (Matrix) [Put](/asciimatrix.go?s=888:930#L33)
``` go
func (m Matrix) Put(x, y int, text string)
```
Put sets the given string (text) at the desired x and y coordinate in the matrix. Thereby it can be used to add and
overwrite data. To remove data, overwrite it with whitespace.




### <a name="Matrix.String">func</a> (Matrix) [String](/asciimatrix.go?s=1127:1158#L43)
``` go
func (m Matrix) String() string
```
String renders the the data as a matrix. Empty addresses are filled with whitespace.
