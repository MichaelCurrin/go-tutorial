# Hello world steps

This covers top-level files in this project.

- [hello.go](/hello.go)
- [go.mod](/go.mod)
- [go.sum](/go.sum)

Create [hello.go](/hello.go) with an import of `quote`.

Initialize a module.

```sh
$ go mod init hello
```

That generates [go.mod](/go.mod).

Initial content:

```go
module hello

go 1.15
```

Install packages and run module.

```sh
$ go run hello.go
```

The `go.mod` now has an extra line.

```go
module hello

go 1.15

require rsc.io/quote v1.5.2
```

That generates [go.sum](/go.sum), which is used to check downloaded versions and checksums are what is expected.

This file should be versioned according to the [Wiki](https://github.com/golang/go/wiki/Modules#releasing-modules-all-versions):

> Ensure your go.sum file is committed along with your go.mod file.

If you open the `go.sum` file, you'll find the installed `quote` modules relies on this package:

- `golang.org/x/text`

That URL redirects to:

- https://pkg.go.dev/golang.org/x/text

For help on modules see

```sh
$ go help modules
```

Blog post

https://blog.golang.org/using-go-modules


For comparison, see the [go.mod](https://github.com/rsc/quote/blob/v1.5.2/go.mod) file of `quote`:

```go
module "rsc.io/quote"

require "rsc.io/sampler" v1.3.0
```
