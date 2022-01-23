# *var, let, const*

## Declaration
There are different ways to declare a variable in javascript:
var
let 
const 
*var* was the only way to declare variables before the introduction of let and const. It is no longer recommended in greenfield projects but can still be found in legacy code. In modern codebases *let* and *const* are the preferred ways of variable declaration
## Case Sensitivity
Variables in javascript are case sensitive. That means that the following are different:
```
let name = 'Stan Onyime';
let Name = 'Stan Onyime';
```
## Naming Conventions
Names should be descriptive. The convention in the javascript community is to use camelCase for variable names and all uppercase for constants. Names should not start with numbers and should not be any of the reserved key words. Note that unlike in other languages like Golang, javascript interpreters do not enforce the camelCase rule

## Initialization
Variables declared with *var* are initialized to *undefined* if declared without initialization. *const* and *let* are not initialized

## Assignment and Reassignment
Both *var* and *let* can be reassigned. *const* cannot be reassigned

## Scoping
*var* is function or window-scoped. *const* and *let* are lexically scoped
	
