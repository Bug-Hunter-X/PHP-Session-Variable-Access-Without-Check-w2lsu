# PHP Session Variable Access Without Check

This repository demonstrates a common error in PHP: accessing session variables without first checking if they are set.  This can lead to errors or unexpected behavior in your application.

The `bug.php` file shows the problematic code. The `bugSolution.php` file provides a corrected version that includes a check to prevent errors.

## Problem

Accessing a session variable that does not exist will generate an error (often a notice, but could be a warning or even a fatal error, depending on your PHP configuration). This is because PHP will attempt to perform an operation on a non-existent variable.

## Solution

The solution is to always check if a session variable exists before using it.  This can be done using `isset()` or `array_key_exists()`.