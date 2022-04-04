![image](https://user-images.githubusercontent.com/94435318/161430119-3b4a5d00-0d32-4fbf-8b6b-4979c8dfea2c.png)

# 🟥 Task-7 An Introduction to shell operators

Linux operators are a fantastic way to power up your knowledge of working with Linux. There are a few important operators that are worth noting. We'll cover the basics and break them down accordingly to bite-sized chunks.

At an overview, I'm going to be showcasing the following operators:

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161462759-93224d7c-5945-4817-8b9b-553ce9ed8005.png">
</p>

Let's cover these in a bit more detail.

## Operator "&"

This operator allows us to execute commands in the background. For example, let's say we want to copy a large file. This will obviously take quite a long time and will leave us unable to do anything else until the file successfully copies.

The "&" shell operator allows us to execute a command and have it run in the background (such as this file copy) allowing us to do other things!

## Operator "&&"

This shell operator is a bit misleading in the sense of how familiar is to its partner "&". Unlike the "&" operator, we can use "&&" to make a list of commands to run for example command1 && command2. However, it's worth noting that command2 will only run if command1 was successful.

## Operator ">"

This operator is what's known as an output redirector. What this essentially means is that we take the output from a command we run and send that output to somewhere else.

A great example of this is redirecting the output of the echo command that we learned in Task 4. Of course, running something such as echo howdy will return "howdy" back to our terminal — that isn't super useful. What we can do instead, is redirect "howdy" to something such as a new file!

Let's say we wanted to create a file named "welcome" with the message "hey". We can run echo hey > welcome where we want the file created with the contents "hey" like so:

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161462830-30c1ed8e-efcd-4c46-9606-a7f7741f7c34.png">
</p>

   *Note: If the file i.e. "welcome" already exists, the contents will be overwritten!

## Operator ">>"

This operator is also an output redirector like in the previous operator (>) we discussed. However, what makes this operator different is that rather than overwriting any contents within a file, for example, it instead just puts the output at the end.

Following on with our previous example where we have the file "welcome" that has the contents of "hey". If were to use echo to add "hello" to the file using the > operator, the file will now only have "hello" and not "hey".

The >> operator allows to append the output to the bottom of the file — rather than replacing the contents like so:

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161462993-8109929d-c465-49b7-91af-8881201904be.png">
</p>

------------------------------------------------------------------------------------------------

Answer the questions below-----------------------------------------------------------
--

### 1. If we wanted to run a command in the background, what operator would we want to use?

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161463264-aec4cbfd-c058-4556-9f9e-2fee7434c7b8.png">
</p>  

### Answer: &

### 2. If I wanted to replace the contents of a file named "passwords" with the word "password123", what would my command be? 

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161463405-52d8e227-0f5c-4501-81f5-feded1e53eea.png">
</p>

### Answer: echo password123 > passwords

### 3. Now if I wanted to add "tryhackme" to this file named "passwords" but also keep "passwords123", what would my command be

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161463469-3fede7d9-707d-4bf1-944a-d0c4fea08cb3.png">
</p>
  
### Answer: echo tryhackme >> passwords

### 4. Now use the deployed Linux machine to put these into practise

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161463550-cd7eb2d5-aa06-4be9-9e9a-566706d34efa.png">
</p>
  
