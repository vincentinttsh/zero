# vincentinttsh/zero

[![Build Status](https://travis-ci.com/vincentinttsh/zero.svg?branch=master)](https://travis-ci.com/vincentinttsh/zero)
[![codecov](https://codecov.io/gh/vincentinttsh/zero/branch/master/graph/badge.svg?token=NATJW3S1UO)](https://codecov.io/gh/vincentinttsh/zero)
[![Go Report Card](https://goreportcard.com/badge/github.com/vincentinttsh/zero)](https://goreportcard.com/report/github.com/vincentinttsh/zero)
[![GoDoc](https://godoc.org/github.com/vincentinttsh/zero?status.svg)](https://godoc.org/github.com/vincentinttsh/zero)

Check if golang struct is empty

``` go
package main

import (
        "fmt"

        "github.com/vincentinttsh/zero"
)

type Structure struct {
        ID int
}

func ExampleStructure() {
        zeroStructure := Structure{}
        zeroStructurePointer := &zeroStructure
        nonZero := Structure{ID: 1}
        nonZeroPointer := &nonZero
        fmt.Println(zero.IsZero(zeroStructure))        // true
        fmt.Println(zero.IsZero(zeroStructurePointer)) // true
        fmt.Println(zero.IsZero(nonZero))              // false
        fmt.Println(zero.IsZero(nonZeroPointer))       // false
        // Output:
        // true
        // true
        // false
        // false
}

func main() {
        ExampleStructure()
}
```
