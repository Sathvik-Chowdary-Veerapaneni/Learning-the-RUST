---
title: "3 : Learn by doing? "
layout: post
date: 2023-02-08
---
Draft of Blog 3

# Learn by Doing
The best way to learn a programming language is by doing implementing the learning objects by building mini projects and practicing it various times. Understanding of code How it working is an important step.

#Let’s create a simple guessing game in rust
In this blog, I am going to create a guessing game between the numbers 1-50. By the end of this blog, You will experience with 
1. how to add dependencies in rust  **cargo.toml**. 
2. how cargo build reacts to added dependencies.
3. Creating Variables and assging values with init.
4. Loop function.
5. How to take user input.
6. Building if & else statements.
7. How to add libraries into program.


You can look the main code **[Here](https://github.com/Sathvik-Chowdary-Veerapaneni/Learning-the-RUST/blob/main/Code/main.rs)**

Adding the libraries 
use rand 
use cmp::Ordering *

rand is the dependecy we are adding to cargo.toml

when we use the cmd cargo.build it will check the depencies from the cargo.toml  if it is already existed then it will skip it. it will be added to the current project by dowloading it, It will be locked in cargo.lock so,that the preivous depencies will be stored in it.

If version of dependency is changed, then it will be updated. 

#Code explanation
Our source code written in the main function for now 
println!("Guess the number!");
 prints the string
let secret_number = rand::thread_rng().gen_range(1, 51);
here the let is a predefined keyword to create a variable
secret_number is a variable , and storing a randomly generated number.
It is generated with
rand::thread_rng().gen_range(1,51);

by using the word ‘loop’ we are creating a loop function 
inside the loop
we are taking the input from user
to save it in a variable
let mut guess = String::new();
by adding mut were indicating that the variable is muttable so that it can store
