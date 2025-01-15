# Ruby `method_missing` Bug

This repository demonstrates a potential issue with Ruby's `method_missing` method.  The `method_missing` method is powerful but can easily mask actual errors if not used correctly.  The example shows how it can intercept calls to non-existent methods, potentially hiding underlying problems. The solution shows how to add safeguards to mitigate these issues and improve error handling.

## Bug
The `bug.rb` file shows a class that uses `method_missing` to handle all method calls. This may seem convenient but makes it impossible to know if a method is actually missing or if it is being correctly handled by `method_missing` without proper debugging. 

## Solution
The `bugSolution.rb` file provides a more robust solution. It demonstrates how to include checks and logging to prevent unexpected behavior and aid in debugging.