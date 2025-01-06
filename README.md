# Go Map Access Panic

This repository demonstrates a common error in Go: panicking due to accessing a map before checking if it's nil.  The `bug.go` file contains code that will panic at runtime.  The `bugSolution.go` file provides a corrected version.

## Problem

Attempting to access a map element (`m["a"]`) when the map is `nil` will cause a runtime panic in Go.  This can be difficult to debug, especially in larger applications.

## Solution

Always check if a map is `nil` before attempting to access its elements.  This can be done using a simple `if` statement or the `ok` idiom in a `for...range` loop.

## Additional Notes

While Go's type system helps prevent many errors, this kind of runtime panic highlights the importance of defensive programming and error handling.