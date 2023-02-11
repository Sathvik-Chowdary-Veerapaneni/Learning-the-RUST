---
title: "3 : Learn rust by doing "
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

# 2. Magic of "Cargo build"
When we executed the cargo build command, the libraries added in our toml file will be installed according to respective versions from rust offical GitHub repository. If the packages were installed already and you tried again building cargo, the cargo checks the packages with versions if already existed it will skip and will continue rest of the packages. If there is change in version of dependecy it will be updated.

# 3. Declaration of variables and assging values.
In rust, We create variable by the following statement and keywords **let variable_name = value**. </br> The variables created with "let" were immutable,so that we can't change the value in future occurences of it. </br> If we want a **muttable** variable then we need to use **let mut variable_name = value**. It will enable us a muttable variable to update and change. </br> 
            
            let apples = 5; // immutable
            let mut bananas = 5; // mutable
   
# 4. Creating a Loop
With the word loop we can start a loop between "{ }" it will continue until **break** statement is occur. And in rust you can also create a loop with **for**. similar to python. 
          
 Example for print 1 to 10 numbers using for loop.

             fn main() {
                 for i in 1..11 {
                     println!("{}", i);
                 }
             }
    
# 5. Seeking input from the User
By importing standard library **io**. we can access the read_line it is an stdin input function. 
                 
                 io::stdin().read_line(&mut variable_name);
                 
# Guessing Game Project 

You can find entire code from **[Here](https://github.com/Sathvik-Chowdary-Veerapaneni/Learning-the-RUST/blob/main/Code/main.rs)**

**Code**
           
*Importing Libraries* 
           
            use std::io;
            use std::cmp::Ordering;
            use rand::Rng;
            
*Starting the main function*
        
            fn main() {
                println!("Guess the number!");
                
*Random number generation between 0 and 50*

                let secret_number = rand::thread_rng().gen_range(1, 51);
                
*Loop Starts*
      
                loop {
                    println!("Please input your guess.");
                    
*Creating a muttable string as 'guess'*

                    let mut guess = String::new();
                    
*Input from the user*

                    io::stdin().read_line(&mut guess)
                        .expect("Failed to read line");
                        
*Matching wether the input is integer or not*

                    let guess: u32 = match guess.trim().parse() {
                        Ok(num) => num,
                        Err(_) => continue,
                    };
                    
*Matching by Compare*
   
                    println!("You guessed: {}", guess);
                    
*Returning wether the guessed number is high or low and same*

                    match guess.cmp(&secret_number) {
                        Ordering::Less => println!("Too small!"),
                        Ordering::Greater => println!("Too big!"),
                        Ordering::Equal => {
                            println!("You win!");
            break; 
            }
            }
            }
            }
                 
            
The match expression is a powerful feature in Rust that allows you to match on the value of an expression and execute different code blocks based on the variant of the value. It's similar to a switch statement in other programming languages.
