monty: A custom bytecode interpreter

The Monty language
Monty 0.98 is a scripting language that is first compiled into Monty byte codes (Just like Python). It relies on a unique stack, with specific instructions to manipulate it. The goal of this project is to create an interpreter for Monty ByteCodes files.

The monty bytecode custom interpertor reads the codes line by line and executes each line till the last line.


Monty.c - contains main function
main - takes filename(s) as an argument

tokens.c - contains parse function
parse - parses commandline input into tokens

evaluate.c - contains eval function
eval - evaluate operation given commandline input, stack/queue mode, and line number of file
stack_functions.c - contains run function
run - runs specified command function

free.c - contains free_list function
free_list - frees a stack represented by a doubly linked list

mode.c - contains functions defining stack and queue modes
stack_mode - change to stack LIFO format
queue_mode - change to queue FIFO format

calculate.c - contains custom add, sub, mul, divide, mod functions
add - adds the top two elements of the stack
sub - subtracts the top element of the stack from the second top element of the stack
divide - divides second top element of the stack with the top element of the stack
mul - multiplies the second top element of the stack with the top element of the stack
mod - computes the rest of the division of the second top element of the stack by the top element of the stack

stack_fuctions.c - contains custom push, pop, swap, rotate left, rotate right functions
push - adds a new node at the beginning of a stack_t list, or in queue mode, add node to end
pop - remove top element of the stack
swap - swaps the top two elements of the stack
rotl - rotates the stack to the top
rotr - rotates the stack to the bottom

print.c - contains custom print functions for stack elements
pall - prints all elements of a doubly linked list
pint - prints the value at the top of the stack, followed by a new line
pchar - prints the char at the top of the stack, followed by a new line
pstr - prints the string starting at the top of the stack
nop - does not do anything

monty.h - header file