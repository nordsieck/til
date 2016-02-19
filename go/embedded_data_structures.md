It is not legal to embed either maps, slices or arrays in other types.

```go
type A struct {
     [4]bool
}

// syntax error: unexpected [, expecting field name or embedded type
```

On a practical level, this means that you can never use the `[]` operator on a struct.