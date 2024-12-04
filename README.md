# F# Mutable Variable Swap Bug

This example demonstrates a common pitfall when working with mutable variables in F#.  The `swap` function attempts to swap the values of two mutable variables, but due to how mutable variables are handled in F#, it doesn't work as expected.

The `bug.fs` file contains the buggy code, while `bugSolution.fs` provides a corrected version using tuples to avoid unexpected side effects.  The core issue is understanding that mutable variables in F# are passed by reference, leading to changes affecting the original variables outside the function's scope.