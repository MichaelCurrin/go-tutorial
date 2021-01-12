# Random greeting

From [Random greeting](https://golang.org/doc/tutorial/random-greeting) tutorial.

See [random-greeting](/random-greeting/) directory.

```sh
$ cd random-greeting
```

Create a slice of greeting formats and choose one at random.

The `init` function is used to seed the random function with the current time.

> Go executes init functions automatically at program startup, after global variables have been initialized.

See [greetings/random.go](/greetings/random.go).

See [hello/hello.go](/hello/hello.go). This has been updated to use the script added above.

```sh
$ cd hello
$ go build

$ ./hello
```
