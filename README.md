# Lua Nested Table Traversal Issue

This repository demonstrates a potential issue with using `pairs` to iterate over nested tables in Lua.  The `pairs` iterator does not guarantee a specific order, which can lead to unexpected results when recursively processing nested structures.

## Bug Description

The `bug.lua` file contains a function `foo` that recursively iterates over a nested table using `pairs`.  Due to the unordered nature of `pairs`, the order in which the nested tables are processed is not deterministic. This can lead to incorrect results in scenarios where the processing order is critical.

## Solution

The `bugSolution.lua` file presents a possible solution using a sorted table to enforce a specific iteration order.  This ensures consistent and predictable behavior.