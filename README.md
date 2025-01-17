# Unexpected Mutability Behavior in F# Function Parameters

This repository demonstrates a subtle bug related to the mutability of variables passed as parameters to functions in F#.  The `swap` function, intended to swap the values of two mutable variables, does not behave as expected. 

## The Problem
The issue arises from the way F# handles mutable variables passed as arguments.  Instead of passing the variables by reference, they're passed by value (copying the value). Changes within the function only affect the local copies, not the original variables. 

## Solution
The solution involves using references to enable modifying the original variables from within the function.