Types and consts can be declared in any block scope, not just the package scope.

```go

func main() {
	{
		const c = 1
		type f int
		_ = f(c) // good
	}
	_ = f(c) // f & c undefined
}
```
