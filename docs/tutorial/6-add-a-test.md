# Add a test

- [Tutorial](https://golang.org/doc/tutorial/add-a-test)

See [random-greeting](/random-greeting/) directory.

The file [greetings_test.go](/random-greeting/greetings/greetings_test.go) is set up.

Run this:

```sh
$ cd random-greeting/greetings/
```

```console
$ go test
PASS
ok      example.com/greetings   0.160s
```

Or in verbose mode:

```console
$ go test -v
=== RUN   TestHelloName
--- PASS: TestHelloName (0.00s)
=== RUN   TestHelloEmpty
--- PASS: TestHelloEmpty (0.00s)
PASS
ok      example.com/greetings   0.154s
```
