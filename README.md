# Modifying a List While Iterating in Elixir

This example demonstrates a common issue in Elixir when attempting to modify a list while iterating over it using `Enum.each`.  The code intends to remove the element `3` from the list, but due to Elixir's immutability, the original list remains unchanged. The `list = List.delete(list, x)` line creates a new list, but this new list is not assigned back to the variable used in the `Enum.each` loop.

## How to Solve the Problem
The solution demonstrates using `Enum.filter` to create a new list containing only the elements that meet a specific condition, effectively removing the undesired element.