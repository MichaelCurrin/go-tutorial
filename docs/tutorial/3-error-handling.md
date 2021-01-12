# Error handling
> Return and handle an error

See [error-handling](/error-handling/) directory.

```sh
$ cd error-handling
```

Added the following:

- Import `errors`.
- Use error in all the return sections.
- When you need to throw an error, use `errors.New(message)`.
- Change the calling function to expect the error to be returned.


Set logging.

```go
// Set properties of the predefined Logger, including
// the log entry prefix and a flag to disable printing
// the time, source file, and line number.
log.SetPrefix("greetings: ")
log.SetFlags(0)


// If an error was returned, print it to the console and
// exit the program.
if err != nil {
    log.Fatal(err)
}
```

Then an error looks like:

```
greetings: empty name
exit status 1
```
