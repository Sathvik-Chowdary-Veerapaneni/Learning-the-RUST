---
title: "2 : Basics of Rust"
layout: post
date: 2023-02-01
---
# Installing Rust in your OS?
Depending on the Operating System, the rust has Mac,Linux and Windows versions.
for Mac and linux go to this website https://www.rust-lang.org/tools/install
copy the code and paste in the terminal to install Rust.

# How to create rust program file ?
1. The source code can be written in user choice of IDE,the rust file should save '*.rs*' extension, **file_name.rs**.
2. The file name should not contain any space between the file name, you can use '_' underscore between the names </br>
   **file name.rs** not allowed. </br>
   **file_name.rs** is allowed. </br>

# How to run a rust file ?
1. Open the terminal
2. Change the directory to rust file, where it is located
3. Compile the rust file using cmd **rustc file_name.rs**
4. It will create the rust executable file
5. **./file_name** to execute the rust file

# Cargo in Rust
1. It is a Rust’s build system and package manager.
2. With this tool, you’ll get a repeatable build because it allows Rust packages to declare their dependencies in **Cargo.toml**.
3. 
4. Cargo helps to compile Rust program successfully. It downloads dependencies, compiles your packages, and uploads them to the Rust project registry, **crates.io**.
5. Cargo is installed by default with rust installation,if not we can install it later.
6. Check whether it is installed or not by entering the command **cargo** in the terminal.
   
## Example of Rust Program
Let's start with classic **Hello World**.
1. Create a rust file hello_world.rs.
2. Create the main function with rust syntax.
3. Write print statement with **println**. 
4. Save the file.
5. Open the terminal.
6. Change the directory to file location.
7. run with **rustc hello_world.rs**
8. You will find the executable **hello_world** in the same working directory.
9. Execute it with **./hello_world**
10. You will see the output in the terminal **Hello World**


It is the basic hello world programming with Rust !.
