# Go

Go is an open source programming language, which is:
- statically typed
- compiled programming language

Features:
- Memory safety
- Garbage collection
- Structural typing
- CSP-style concurrency


## Good Ol Hello World

```go
package main

import "fmt"

func main() {
	fmt.PrintLn("Hi there!")
}
```

## Five essential questions

### 1. How to run go code?
We use the `go CLI` to run go code. Some commands:

- **go build** -> compile the code
- **go run** -> compile and execute the code
- **go fmt** -> format all the code in the directory
- **go install** -> compile and install a package
- **go get** -> download the raw source code of some package
- **go test** -> run tests

### 2. What is 'package main'?

- _Package_ == _Project_ == _Workspace_
- A package can have multiple files
- Each file must have `package <name>` as the first line.
- There are __two__ types of packages:
	- **Executable**
		- Packages that produce an executable upon compilation
		- `main` is a special name for executable packages
		- Must have a `func` called `main`
	- **Reusable**
		- Packages that can be used for dependencies
		- No executable file is produced on compilation
		- Can be named anything other than `main`

### 3. What is 'import "fmt"'?
### 4. What is 'func'?
### 5. How is the file organized?