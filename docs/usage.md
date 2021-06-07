# Usage

How to run the modules which have been added to this project.


## Basic

This uses the module at the top-level of this repo. It relies on an external library but does not import from any local modules.

```sh
$ go run hello.go
```

Or simply:

```sh
$ go run .
```

Sample output:

```
Don't communicate by sharing memory, share memory by communicating.
```


## Multiple modules

Follow this pattern for these directories which have multiple modules.

- `create-and-call-package`
- `error-handling`
- `random-greeting`

### Run

Navigate to the `hello` module of the [create-and-call-package](/create-and-call-package/) directory.

```sh
$ cd create-and-call-package/hello
```

```sh
$ go run hello.go
# Or
$ go run .
```

```
Don't communicate by sharing memory, share memory by communicating.
```

Note that the [greetings](/create-and-call-package/greetings/) module is at the same level as [hello](/create-and-call-package/hello/) but we are able to find `greetings` because this is set up in the `go.mod` file:

```
replace example.com/greetings => ../greetings
```

### Build and execute

```sh
$ cd create-and-call-package/hello
```

```sh
$ go build
```

```sh
$ ./hello
```
```
Hello, World!
```

The output file will be _ignored_. This is because of the rule added to [.gitignore](/.gitignore). The rule was set up _after_ the other files had been added to version control, so `hello` binaries get ignore but `hello` directories are still tracked.
