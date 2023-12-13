# mterm

WIP: mterm implements a virtual terminal

## Usage

```go
package main

import "github.com/stdiopt/mterm"


func main() {
    t := mterm.New(24,80)
    fmt.Fprintf(t, "\033[1;33mHello world\033[0m", "World")

    // renders the full 24x80 cells in Ansi
    output := t.GetScreenAsAnsi()

    os.Stdout.Write(output)
}
```
