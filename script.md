# *Getting on the Rust Train!* script

Hello, everyone! My name is Anthony Suárez. I'm a backend developer at Devsu
and a free and open source software advocate.

As you know, the topic of this talk is the Rust programming language, and
before starting, I would like to tell you why I chose this topic.

Aa a developer, I've always been quite **dissatisfied** with the state of
programming languages, and have always tried to find that state of
**perfection***; you know, the perfect programming language that catches all
the errors, is idiomatic, has nice tools and all of that. During this search, I
met Rust, while it's not perfect, I do think it is pretty close, and I have
grown to love it so much as to say it is my favorite programming language.

So, in this talk, I'm going to present to you an introduction to the Rust
programming language, so you can start to write fast, safe and reliable
software right away, and hopefully convince you that it's worth trying this
language.

With that said, **welcome to *Getting on the Rust Train* **!

If you have any questions, feel free to tell me. I think there is a way for you
to raise your hand and open your mic; or you can also type in the chat and I'll
be happy to answer your questions at any time.

## 2. What is Rust?

So, what is Rust? 

Rust is a systems-programming language created by Mozilla, the creators of the
Mozilla Firefox browser, in 2010.

Rust, being a system-programming language, gives you low level control over the
system, much like C and C++, which is why you'll often see Rust as an
alternative to these languages.

But, if there are languages that are well-established in software development,
like C and C++, **why should you care about Rust**?

## 3. Popularity and growth

Well, let's first look at the current landscape, and find *The Rust Train*, by
seeing some data about the **Popularity and Growth* of Rust.

## 4. Rust is the most loved language

First. Many of you may know this. Rust is the most loved programming language
of the year, and it has been since 2016.

This data is from the StackOverflow Developer Surveys, and it's worth noting
that Rust wins this category by a mindblowing value of 86.73% of developers
that want to keep using it for their job. This is almost 10% above of the
second most loved language, which is Elixir.

## 5. High paying jobs

Second. Rust has stayed among the highest paying technologies, according to the
StackOverflow Developer Surveys.

According to the 2021 survey, Rust jobs pay an average of $77,530 per year, and
is among other high-paying languages like Go and Scala.

## 6. Rust community is growing

Third. Accroding to the State of the Developer Nation study by Slash Data, Rust
is the language with the fastest growing community! Indeed, from 2020 to 2022,
the number of Rust developers has nearly tripled, and is around 2.2M developers
worldwide, which means it's now bigger than Ruby's community.

It's also worth noting that this study also found that Rust is commonly used in
AR/VR and IoT projects.

## 7. Rust and WASM

Fourth. Rust is the #1 language for WebAssembly development.

If you don't know, WebAssembly is a new compilation target that allows browsers
to run compiled programs which are extremely fast and performant.

WASM is a technology that is having a lot of impact in modern web development,
some people even claiming that it will be the default compilation target of the
future, because it allows for truly portable and cross-platform programs.

Returning to Rust, it was found in the State of WASM 2021 survey that Rust is
the most commonly used language for WebAssembly, and not only that, but Rust is
also the language that developers wish to use when working with WASM in other
languages.

## 8. Rust and blockchain

Fifth. Rust is very popular for blockchain technologies. Indeed, if you are
looking for a job with Rust, it's very probable that a lot of these jobs are
blockchain related.

This popularity is in part because the Solana framework allows you to create
smart contracts with Rust.

## 9. Rust and Linux

Sixth. If you are a Linux fanboy like me, you will already know this.

Rust is the second language of the Linux kernel.

Although the patches have not been merged to the main Linux kernel yet, it was
pointed out by Linus Torvalds that it will very likely be merged for version
5.20. One of these changes consists on a rewrite of the GNU coreutils
with a new package called `uutils`, a project that is advancing fast and is
very promising in terms of performance.

## 10. Companies using Rust

And to finish this section, here are some companies that use Rust in production.

Dropbox rewrote the core of its file-syncing engine in Rust, and in their
blogpost they explain that Rust has been a force multiplier for their team.

Coursera uses Rust for parts of their assignment grading system, and in their
blogpost they assure Rust is an excellent choice for security critical functions.

Figma used Rust to rewrite their Typescript multiplayer server, which needed
to be fast and concurrent. In their blogpost, they say they chose Rust because
it "combines best-in-class speed with low resource usage".

Among other companies using Rust in production are Cloudflare, Facebook,
Discord, Amazon, Microsoft (which is a founding member of the Rust Foundation),
Mozilla, Coursera, NPM and Twitter. About Twitter there's a really interesting
talk that I will tell you about at the end of my presentation.

If you'd like to know more about how Rust is used in production by big companies,
you can look at the Serokell blogpost in the footer.

## 11. Rust introduction

So, I hope the data and cases I gave you are compelling enough for you to be
interested in this language. But it's enough about that. Let's now talk about
Rust itself and what makes it great.

## 12. Goals of Rust

Rust was created by Mozilla with the following goal: Being a programming
language to create fast, safe, and concurrent programs **while** being practical.

You will notice that the features of Rust and the decisions made by the Rust
developers revolve around this main goal. Let's review Rust's features.

## 13. The borrow checker

First, the borrow checker. Usually, when you think of very fast languages,
you think of C and C++, which sacrifice safety and practicality for performance
and low-level control. On the other hand, when you think of practical, high-level
languages, you think of slow languages like Java, Python or Javascript, which
take away low-level control and use a garbage-collector to ensure memory
safety.

This trade-off between practicality and performance is not a problem for Rust
thanks to its borrow checker, which is a system composed of simple rules that
ensure safety when working with low-level memory constructs.

What you need to know:
1. Each variable has an owner.
2. You can reference another variable's value via a *reference*, also called a 
   pointer.
3. You may either have any number of *immutable* references, or only one
   *mutable* reference at the same time.

These rules ensure that the data you are working with is always valid, even
when working with multiple threads.

## 14. Memory safety

As I already told you, the borrow checker ensures memory-safety, so say goodbye
to segfaults and dangling pointers, which are a really common source of bugs
when working with C and C++.

Also say goodbye to other common issues like `undefined` variables or uncaught
exceptions. We will talk later about how Rust solves these issues.

## 15. *Fearless Concurrency*

As I told you, one of the main goals of Rust is being concurrent. Again, thanks
to the borrow checker, common concurrency issues like race conditions or
deadlocks are *impossible*.

This means that you can write concurrent code fearlessly, because your code
will not even compile when some of these issues arises. This is exactly the
opposite of other programming languages, where you need to be really
experienced and careful when working with multiple threads.

## 16. Idiomatic syntax

Next. Rust has a very idiomatic and expressive syntax. that gives you low-level
power, with high-level code. Let's review a simple *Hello World* program
written in Rust.

## 17. Hello World

In this script, you see two functions, defined by the `fn` keyword. The main
function creates a new variable using the `let` keyword, which is generated by
passing an argument to the `greet` function which is defined below. As you can
see, it's not necessary to define the variable type explicitly, as this is
inferred from the function call. After this, the variable is printed out
using the `println!` macro, which uses a format string similar to Python's
`f` strings.

Looking at the `greet` function, we can see it receives a `name` argument, which
is a reference to a string slice; and it returns a new string. You might be
wondering why theere are two string types, one `str` and one capitalized
`String`. The reason for this is because of partly because of how data is
dereferenced in Rust, something we will cover a bit more deeply in the hands-on.

Finally, you may have noticed that the `greet` function has no `return`
statement. This is a really nice feature of Rust that essentially makes your
functions return when a value has no semicolon, making your code less verbose.

## 18. Modern language features

Rust has a modern syntax with features from other imperative languages and from
functional languages as well. Some of these include:

- Pattern matching.
- Enum variants.
- Closures.
- Async/await.
- Macros.

Macros are an advanced feature which enables metaprogramming, allowing you
to extend Rust beyond what the common syntax lets you.

## 19. Rich type system

Rust's type system is really cool, allowing things like:

- Type aliases.
- Type inference.
- Structs (with methods).
- Enum variants.
- Traits (which are similar to Haskell typeclasses and Java interfaces).
- Genercs (not only for types, but for traits and *lifetimes* as well).

In addition, the Rust type system allows the compiler to generate helpful
error messages that guide you when your code doesn't compile.
