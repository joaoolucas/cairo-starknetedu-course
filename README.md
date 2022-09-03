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

Similar to the previous, call "assign_user_slot" and then call "external_handler_for_internal_function" that takes "0" as input (we know that the "0" is the correct input by looking at the contract code). Now go to "Read Contract" and check the correct value calling "user_values", then just put the result in "claim_points".

### Ex07 - Comparing values

For this exercise, we basically just need to look at the code of the contract. To call "claim_points" we need two values, "a_value" and "b_value". Checking the contract, we see that "a_value" has to bee a number different from 0, less than 75 and between 40 and 69. The "b_value" cannot be negative and must be less than 1. For example, a correct input would be 50 for "a_value" and 0 for "b_value".

### Ex08 - Recursions level 1

Here we're going to need to input an array at "set_user_values". Looking at the contract we find out that the array consists in a recursive function, and to call "claim_points" we need to the user_value as 10 in the slot 10. The code maps the variables recursively to set all the user_values, so at the end of the array it's start summing. In practice the values are stored in the slots every time the function is called and continuously from 0. So to make the user_value be 10 in slot 10, we will make the following input in "set_user_values": 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10

If you want to check it, call the function "user_values" in "Read Contract". Now just call "claim_points" to finish this exercise.
