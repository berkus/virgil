# The Virgil Programming Language #

Virgil is a fast and light programming language which balances object-oriented, functional, and procedural programming features. It integrates classes, functions, tuples, and type parameters and offers an advanced optimizing compiler for both the JVM and native platforms.

```

def main() {
System.puts("Virgil III is fast and lightweight!\n");
}```

## Features ##

Virgil III focuses on balancing four main features in a statically-typed language:

  * Classes - for basic object-oriented programming
  * Functions - for small-scale reuse of functionality
  * Tuples - for efficient aggregation and uniform treatment of multi-argument functions
  * Type parameters - for powerful and clean abstraction over types

## Balance and Design ##

Dovetailing a small set of features into one whole is a challenging design process, both syntactically and semantically. Surprisingly, Virgil manages to do this while providing a clean syntax that C, C++ and Java programmers will find familiar. Python and Scala programmers may also find some syntactic elements reminiscent.

Despite looking syntactically similar to these popular languages, Virgil seeks not to cram more features into an ambiguous, syntactically crowded space. A large number of features have been intentionally left out!

With first-class functions and type parameters, Virgil makes it easier to write small, fast, statically-typed programs. While languages like Java, C++ and C# are struggling to bridge the gap from their object-oriented roots to increasingly popular functional styles, Virgil allows any method from any class or object to be used as a first-class function.

## Efficient Implementation ##

Virgil is well-suited to writing small and fast programs. Native binaries compiled from your programs can be as small as a few hundred bytes in size and consume just kilobytes of memory at runtime.

Virgil features a whole-program optimizing compiler that performs sophisticated dead-code elimination and data-oriented optimizations, producing efficient binaries for either a native platform or the JVM.

Large and medium-sized programs have already been built using Virgil as well. The Virgil compiler is written in Virgil, of course! That means to get started using Virgil, all that is required is a compiler executable and an appropriate computer or virtual machine. The runtime system, garbage collector, libraries, and interface to the operating system are all written in Virgil.


## Language comparisons ##

How does the Virgil language compare to...?

  * Java - it is smaller, faster, and simpler
  * C - it is strongly-typed and platform-independent
  * C++ - it is vastly simpler, strongly-typed and garbage-collected
  * Python - it is statically typed and faster
  * Go - it is more syntactically familiar and simpler

See MoreLanguageComparisons.

## Libraries ##

Virgil III is a fledgling language without many libraries. It features the bare minimum to perform IO and interact with the operating system. For example, when targeting `x86-darwin`, the compiler provides the ability to directly call the kernel's system calls, generating specialized assembly that conforms to the kernel's special calling convention. From low-level system calls it is possible to build a more useful layer with pure Virgil code. That is work in progress.

See WhySoFewLibraries for an explanation.

## Ok, let's see it! ##

Let's [get started](GettingStarted.md), and then learn how in the [tutorial](Tutorial.md).