# MongoDB $inc operator error with string value
This repository demonstrates a common error when using the `$inc` operator in MongoDB update operations. The `$inc` operator is used to increment a numeric field by a specified value.  However, if you attempt to increment with a string value, it will fail silently and the field will not be updated.

The `bug.js` file contains the erroneous code. The `bugSolution.js` file demonstrates the corrected code.

## Bug
The `$inc` operator in MongoDB expects a numerical value to increment the field. If you pass a string instead of a number, MongoDB won't throw an error, but it won't update the field either.  This can be very difficult to debug.

## Solution
Ensure that the value passed to the `$inc` operator is a number, not a string.