# Usage

How to run the modules which have been added to this project.


## Basic

This uses module at the top-level of this repo.

```sh
$ go run hello.go
```

```
Don't communicate by sharing memory, share memory by communicating.
```


## Advanced

Follow this pattern for these directories:

- `create-and-call-package`
- `error-handling`
- `random-greeting`

### Run

```sh
$ cd create-and-call-package/hello
```

```sh
$ go run hello.go
```

```
Don't communicate by sharing memory, share memory by communicating.
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
