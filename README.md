# Kotlin: Unexpected Behavior with removeIf on Immutable Lists

This repository demonstrates an unexpected behavior when using the `removeIf` function on immutable lists in Kotlin.  While `removeIf` works as expected on mutable lists, attempting to use it on an immutable list (created using `listOf`) will result in a compile-time error.

The `bug.kt` file shows the unexpected behavior. The `bugSolution.kt` provides a solution and best practices for working with mutable and immutable collections.

## How to Reproduce

1. Clone this repository.
2. Open `bug.kt`.
3. Uncomment the line that attempts to use `removeIf` on the immutable list and run the code.  You'll encounter a compile-time error.

## Solution

The solution involves carefully distinguishing between mutable and immutable collections.  Use `mutableListOf` when you intend to modify the list after its creation.