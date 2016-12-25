---
layout: page
title: Text Editors & IDEs
---

Text editors and IDEs play a big role in developers' lives and most people are quite opinionated regarding the matter. My stance, in short, is that I want the power of an IDE but a consistent text editing experience. 

There are many advantages of IDEs that are difficult or impossible to replicate in a stand-alone text editor. For example: 

- Refactoring/renaming 
- Navigation to implementation 
- Code Generation 
- Debugging 
- Live Error Checking 
- Code Analysis 
- Tab Complete 

When you're working on a large platform with lots of libraries and APIs floating around, these features make your life a lot easier. 

That said, most languages have their own IDEs, each with their own text editor and learning all of those keymaps can be a pain. Plus, a lot of text editing takes place at the command line or over a ssh connection. In those contexts, an editor like vim or emacs is superior. I personally prefer vim for its modal editing and ubiquitousness. 

As such, my approach is to use whatever IDE is best for the language I am working in (e.g. MVS for C# or IntelliJ for Java) and swap in a vim keymap for the text editor. 

In order to ensure a consistent text-editing experience even when working on remote computers, I do not customize vim. This is because my inputs will be interpreted by the remote system which would not have my configurations and which I could not load with my configurations. 
