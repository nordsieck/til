I've never seen anyone use the preamble statement for switches:

```go
switch a:= 3; {
default:
	fmt.Println(a)
}
```

This is presumably because it's easier to just put the statement on an earlier line.