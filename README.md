# Resolutions to [StarkNet-Edu Cairo Course](https://github.com/starknet-edu) 🌱

## [StarkNet Cairo 101](https://github.com/starknet-edu/starknet-cairo-101)

**Simple tutorials to learn how to read Cairo contracts. It's a learn to earn, so each exercise completed give you tokens. As the exercises progress, the difficulty increases.**

### Ex01 - General syntax

Very simple task, just open the contract in Voyager, go to "Write Contract" and call the function "claim_points".

### Ex02 - Storage variables, getters, asserts

Here you need to first go in "Read Contract" and call "my_secret_value". Use the result in the function "claim_points" at "Write Contract".

### Ex03 - Reading and writing storage variables

Examinating the contract we can see that the value we need is 7. In "Write Contract" we have 4 functions, in order to get to 7 points we going have to call "increment_counter" 4 times, each one giving us 2 points. After that, we can call "decrement_counter" that will remove 1 point. We can check how many points we have at "Read Contract" in the "user_counters" function. With 7 points we can call the function "claim_points".

### Ex04 - Mappings

First let's get a slot, call the function "assign_user_slot" at "Write Contract" to do that. Now at "Read Contract" you can check your slot and the value mapped to that slot with the functions "user_slots" and "values_mapped", respectively.

To claim the points of this task we have to give to the function the "expected_value". Looking at the contract we see that the expected value is the value mapped minus 32. So just make the calculation and input the answer in "claim_points" to complete this exercise.

### Ex05 - Variable visibility

Similar to Ex04, we need to call the function "assign_user_slot" at "Write Contract" and then call "copy_secret_value_to_readable_mapping". The verify the value at "Read Contract" calling the "user_values" function. Then just put the output of "user_values" in "claim_points" at "Write Contract".

### Ex06 - Functions visibility

Similar to the previous, call "assign_user_slot" and then call "external_handler_for_internal_function" that takes "0" as input (we know that the "0" is the correct input by looking at the contract code). 
