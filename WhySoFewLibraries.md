# Why are there so few libraries? #

So far the focus of Virgil has been getting the language right. To that end, only the bare minimum of library support has been supplied so that programs like compilers and benchmarks can run and do IO.

## Why separate language and library? ##

Virgil has very consciously opposed entangling libraries, such as common data structures, IO and threads, from the language itself. A clear boundary between language and library means that the job of the compiler is clearer to both programmers and compiler developers. Primitive types are the only types built into the language, while arrays, tuples, classes, and functions offer programmers type _constructors_ to build their own types. There aren't hidden calls to mysterious library functions introduced by the compiler when it generates code for your program.

This means that the goal of "pay for what you use", often touted in C++, is even more strongly adhered to in Virgil. Virgil programs start with _nothing_. An empty program generates essentially an empty binary, and the code size scales up with your program. This is only possible with a very careful separation of language and library.

## Rebuilding Userspace ##

Most languages that target native platforms require low-level code written in another language in order to get going. With few exceptions this code is written in C. For a language that is supposed to be useful as a systems language, this is basically an admission of failure. Worse, a whole host of problems ensues with interfacing code in the new language with code in C, such as catering to the memory layout, process model, threading model, address space layout, and calling conventions of C.

Virgil takes a different approach. It makes no attempt to play nice with C. It needs no other language underneath. It simply starts over from scratch. The Virgil compiler generates statically-linked binaries that contain only machine code produced by the compiler. The source code of your program is compiled together with the source code of a small runtime system (also written in Virgil), and a single, complete binary is produced.

## Liberation ##

The seduction of tapping into a large amount of C and C++ libraries, as well as other languages, is that a lot of functionality can be had for little cost. This is not really the goal of Virgil. For now, it is more important to build small, fast, and clean programs. Replacement libraries will be developed over time.