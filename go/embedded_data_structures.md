It is not legal to directly embed either maps, slices or arrays in other types.

```go
type A struct {
     [4]bool
}

// syntax error: unexpected [, expecting field name or embedded type
```

However, you can embed one of these primitive types if you redefine it.

```go
type stringMap map[string]string

type A struct {
     stringMap
}
```

Even in this case, however, you can't index into the struct.
