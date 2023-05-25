```
package main

import (
	"fmt"
	"greeting"
	"log"
	"os"
)

func main() {
	// fmt.Println("hello world")

	// log.SetPrefix(">> greetings-")
	// log.SetFlags(1)
	l := log.New(os.Stderr, ">> file greetings--", 1)

	message, err := greeting.Hello("John")
	if err != nil {
		l.Fatal(err)
	}

	fmt.Println(message)
	msg1, err := greeting.Hello("")
	if err != nil {
		l.Fatal(err)
		return
	}

	fmt.Println(msg1)

}
```
