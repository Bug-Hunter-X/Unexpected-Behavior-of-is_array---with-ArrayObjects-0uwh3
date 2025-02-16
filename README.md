# PHP is_array() Pitfall with ArrayObjects

This repository demonstrates a subtle bug in PHP code that arises from the `is_array()` function's behavior with `ArrayObject` instances. While `is_array()` might appear to work correctly for basic arrays, it can return `true` for objects that mimic array-like behavior, potentially leading to errors if you intend to exclusively process true arrays.

The bug is shown in the `bug.php` file.  The solution, implementing more robust type checking, is provided in `bugSolution.php`.

## How to Reproduce
1. Clone this repository.
2. Run `php bug.php`.
3. Observe the unexpected output, indicating that the `ArrayObject` was incorrectly treated as an array.
4. Run `php bugSolution.php`. This improved code correctly handles the `ArrayObject`, showing the expected error message.