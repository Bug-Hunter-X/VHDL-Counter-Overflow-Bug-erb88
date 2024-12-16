# VHDL Counter Overflow Bug

This repository demonstrates a common error in VHDL: integer overflow in a counter. The `buggy_counter.vhdl` file contains a counter that increments without considering the upper limit of its range. This can lead to unexpected behavior or simulation failures.

The `buggy_counter_fixed.vhdl` file provides a corrected version of the counter that handles overflow gracefully.

## Bug Description

The original code lacks a mechanism to prevent the counter from exceeding its defined range (0 to 15). When the counter reaches 15, the next increment will result in an overflow, leading to unpredictable results.  This might manifest as unexpected counter values or simulation errors.

## Solution

The solution involves adding a modulo operation to wrap the counter value back to 0 when it reaches the upper limit.  This ensures the counter remains within the specified range.