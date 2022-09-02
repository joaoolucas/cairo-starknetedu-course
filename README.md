# Resolutions to [StarkNet-Edu Cairo Course](https://github.com/starknet-edu) 🌱

## [StarkNet Cairo 101](https://github.com/starknet-edu/starknet-cairo-101)

**Simple tutorials to learn how to read Cairo contracts. It's a learn to earn, so each exercise completed give you tokens.**

### Ex01 - General syntax

Very simple task, just open the contract in Voyager, go to "Write Contract" and call the function "claim_points".

### Ex02 - Storage variables, getters, asserts

Here you need to first go in "Read Contract" and call "my_secret_value". Use the result in the function "claim_points" at "Write Contract".

### Ex03 - Reading and writing storage variables

Examinating the contract we can see that the value we need is 7. In "Write Contract" we have 4 functions, in order to get to 7 points we going have to call "increment_counter" 4 times, each one giving us 2 points. After that, we can call "decrement_counter" that will remove 1 point. We can check how many points we have at "Read Contract" in the "user_counters" function. With 7 points we can call the function "claim_points".

### Ex04 - Reading and writing storage variables



