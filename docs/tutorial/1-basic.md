# Basic module

- [basic](/basic/)
    - [hello.go](/basic/hello.go)
    - [go.mod](/basic/go.mod)
    - [go.sum](/basic/go.sum)

Create [hello.go](/basic/hello.go) with an import of `quote`.

Initialize a module.

```sh
$ go mod init hello
```

That generates [go.mod](/basic/go.mod) module file in the root of the repo.

The initial content was:

```
module hello

go 1.15
```

Install packages and run the module.

```sh
$ go run hello.go
```

The [go.mod](/basic/go.mod) now has an extra line.

```
module hello

go 1.15

require rsc.io/quote v1.5.2
```

That generated [go.sum](/basic/go.sum), which is used to check downloaded versions and checksums are what is expected.

This file should indeed be versioned, according to the [Wiki](https://github.com/golang/go/wiki/Modules#releasing-modules-all-versions):

> Ensure your go.sum file is committed along with your go.mod file.

If you open the `go.sum` file, you'll find the installed `quote` modules relies on this package:

- `golang.org/x/text`

That URL redirects to:

- https://pkg.go.dev/golang.org/x/text

For help on modules see:

```sh
$ go help modules
```

See blog post - [Using go modules](https://blog.golang.org/using-go-modules).

For comparison, see the [go.mod](https://github.com/rsc/quote/blob/v1.5.2/go.mod) file of `quote`:

```go
module "rsc.io/quote"

require "rsc.io/sampler" v1.3.0
```
