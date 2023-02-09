---
title: "3 : Learn by doing? "
layout: post
date: 2023-02-08
---
# Draft of Blog 3

# Learn rust by doing
The best way to learn a programming language is by doing implementing the learning objects by building mini projects and practicing it various times. Understanding of code How it working is an important step.

# Let’s create a simple guessing game in rust
In this blog, I am going to create a guessing game between the numbers 1-50. By the end of this blog, You will experience with 
1. how to add dependencies in rust  **cargo.toml**. 
2. how cargo build reacts to added dependencies.
3. Creating Variables and assging values with init.
4. Loop function.
5. How to take user input.
6. Building if & else statements.
7. How to add libraries into program.


You can look the main code **[Here](https://github.com/Sathvik-Chowdary-Veerapaneni/Learning-the-RUST/blob/main/Code/main.rs)**

# 1. Addig Dependency in Rust
Similar to other programming languages you can install dependencies from the their source platform. But in rust, while we building cargo project, it creates a file called **cargo.toml** where we can add dependencies over there, we need to add the list of libraries and versions. but here the dependiences were installed from rust git repo.

# 2. magic of "Cargo build"
When we executed the cargo build command, the libraries added in our toml file will be installed according to respective versions from rust offical GitHub repository. If the packages were installed already and you tried again building cargo, the cargo checks the packages with versions if already existed it will skip and will continue rest of the packages. If there is change in version of dependecy it will be updated.

# 3 Declaration of variables and assging values.
In rust, We create variable by the following statement and keywords **let variable_name = value**. </br> The variables created with "let" were immutable,so that we can't change the value in future occurences of it. </br> If we want a **muttable** variable then we need to use **let mut variable_name = value**. It will enable us a muttable variable to update and change. </br> 
            
            let apples = 5; // immutable
            let mut bananas = 5; // mutable
   
# 4 Creating a Loop
With the word loop we can start a loop between "{ }" it will continue until **break** statement is occur. And in rust you can also create a loop with **for**. similar to python. 
          
 Example for print 1 to 10 numbers using for loop.

             fn main() {
                 for i in 1..11 {
                     println!("{}", i);
                 }
             }
    
