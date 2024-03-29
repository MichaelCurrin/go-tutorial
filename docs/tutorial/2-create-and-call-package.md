# Create and call a package

See [create-and-call-package](/create-and-call-package).

```sh
$ cd create-and-call-package
```

This covers these two modules in this project:

- [greetings/](/create-and-call-package/greetings/)
- [hello/](/create-and-call-package/hello/)


## Create a module

```sh
$ mkdir greetings
$ cd greetings
```

Create [greetings/go.mod](/create-and-call-package/greetings/go.mod):

```sh
$ go mod init example.com/greetings
```

Create a script [greetings/greetings.go](/create-and-call-package/greetings/greetings.mod).



## Call it

From the project root:

```sh
$ mkdir hello
$ cd hello
```

Create a file [hello/hello.go](/create-and-call-package/hello/hello.go).

Create a new module.

```sh
$ go mod init hello
```

For production use, you'd publish `greetings` to a server.

And you'd reference the published module like this:

```go
require example.com/greetings v1.1.0
```

For now, we'll adapt the caller's module so it can find the greetings code on your local file system.

Update [hello/go.mod](/create-and-call-package/hello/hello.go) to end with this line:

```go
replace example.com/greetings => ../greetings
```

Now run this locate the module and add it to the `go.mod` file.

```sh
$ go build
go: found example.com/greetings in example.com/greetings v0.0.0-00010101000000-000000000000
```

That will add this line to `go.mod`:

```go
require example.com/greetings v0.0.0-00010101000000-000000000000
```

Run the executable created by the build command.

```sh
$ ./hello
```
