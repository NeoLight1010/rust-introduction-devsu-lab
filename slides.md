---
title: Rust Introduction
description: A quick introduction to Rust, its history, future, and how to get started.
author: Anthony Suárez <neolight1010>
keywords: rust, introduction

theme: gaia
paginate: true
backgroundColor: #ffff
backgroundImage: url("./background.jpg")

class: lead
---

<!--
Description

Rust is one of the highest trending technologies in modern software development due to its amazing features that solves one of software's most common and old issues: memory management.. In this talk, the basics of Rust and its environment are covered, so you can start writing safe, reliable software right away!

About the speaker

Anthony Suárez is a passionate self-taught backend developer and open-source advocate. Works mainly with technologies like Python, Typescript and AWS. In his free time, he likes learning new skills like C, Rust, Haskell, and others.
-->

# Getting on the Rust train! 🦀🚂

by Anthony Suárez


![width:1em](https://cdn-icons-png.flaticon.com/512/25/25231.png) *@NeoLight1010*
![width:1em](https://cdn-icons-png.flaticon.com/512/174/174857.png) */in/neolight1010*

---

<!-- backgroundImage: url("./background-normal.jpg") -->

Rust is a systems-programming language created by Mozilla in 2010.

Having low-level capabilites, it is an alternative to languages like C and C++.

*But why should you care about Rust?*

![width:200px](https://rustacean.net/assets/cuddlyferris.png)

---

# Popularity and Growth

![width:600px](https://cdna.artstation.com/p/assets/images/images/010/103/780/large/eoin-o-broin-03.jpg?1522607778)

---

Rust has remained the most loved programming language since 2016.

![width:600px](https://rustacean.net/more-crabby-things/ferris-love.jpg)

<!--_footer: StackOverflow Survey 2016, 2017, 2018, 2019, 2020, 2021, 2022 -->

---

Rust is associated with high paying jobs.

![width:600px](https://i.imgur.com/Npho9BV.png)

<!-- Rust jobs usually have high-paying salaries averaging at around $77,530 
per year, according to the 2021 StackOverflow Survey.-->

<!-- _footer: StackOverflow Surveys -->

---

Rust has the fastest growing language community! From 2020 to 2022, the
number of Rust developers has **tripled**!

![width:600px](https://blog.knoldus.com/wp-content/uploads/2020/09/Rust-1024x381-1.jpg)

<!-- Rust is mostly popular in AR/VR and IoT. Now bigger than Ruby. -->
<!-- Rust's community had nearly 2.2M developers at the time of the survey. -->

<!-- _footer: State of the Developer Nation 2022 -->

---

Rust is the #1 language for WebAssembly development. 

![width:600px](https://www.rust-lang.org/static/images/wasm-ferris.png)

<!-- Most WASM developers either use Rust, or they want to use it. -->

<!--_footer: State of WASM 2021: https://blog.scottlogic.com/2021/06/21/state-of-wasm.html -->

---

Rust is a leader in the blockchain world.

Build smart contracts with frameworks like Solana.

![width:300px](https://s2.coinmarketcap.com/static/img/coins/200x200/5426.png)

---

Rust is the second language of the Linux kernel.


![width:600px](https://www.muylinux.com/wp-content/uploads/2021/03/RustLinux-1024x576.png)

<!--
Rust interfaces and utils (replacing GNU utils) might me merged for v5.20.
Possibly 2023.
-->

<!-- _footer: https://www.phoronix.com/scan.php?page=news_item&px=Rust-For-Linux-5.20-Possible -->

---

### Companies using Rust

- ![height:1em](https://upload.wikimedia.org/wikipedia/commons/thumb/7/78/Dropbox_Icon.svg/1101px-Dropbox_Icon.svg.png): *"Rust has been a force multiplier for our team..."*
- ![height:1em](https://cdn.iconscout.com/icon/free/png-256/coursera-3628707-3029932.png): Rust is *"an excellent choice for security critical functions."*
- ![height:1em](https://cdn-icons-png.flaticon.com/512/5968/5968705.png): Rust *"combines best-in-class speed with low resource usage."*
- Cloudflare, Facebook, Discord, Amazon, Microsoft, Mozilla,
  Coursera, NPM, Twitter.

<!-- 
Microsoft is a co-founder of The Rust Foundation.
-->

<!-- _footer: https://serokell.io/blog/rust-companies -->

---

## Quick introduction to Rust

What makes Rust great?

<!-- What makes Rust so attractive? -->

---

#### Goals

- Speed.
- Safety.
- Concurrency.
- Practicality.

![bg right 70%](https://free4kwallpapers.com/uploads/originals/2020/04/27/fast-car-wallpaper.jpg)

<!--
    - Compiled language.
    - No garbage collection.

-->

<!--
     - No `null`s.
     - No dangling pointers.
     - No *unsafe*.
-->

<!--
    - No race conditions.
    - No deadlocks.
    - *Fearless concurrency*.
-->

---

### Meet the *borrow-checker*

- Each variable has an *owner*.
- You can reference another variable's value via a *reference*.
- You may either have any number of *immutable* references, or only one
  *mutable* reference at the same time.

---

### Memory safety 

Say *Goodbye!* to memory issues and other common runtime exceptions. Never more:

- Segfaults.
- `cannot access member 'x' of undefined`.
- Invalid pointers.
- Uncaught exceptions.

---

### Fearless concurrency

The borrow-checker rules make common concurrency issues *impossible*.

**Concurrency has never been easier!**

![width:500px](https://media.istockphoto.com/illustrations/facing-the-giant-spider-robot-illustration-id1036972108?k=20&m=1036972108&s=612x612&w=0&h=TyH-jiqqjrE_oT_YxIru0J1ZEAt9TSXWLKhXMmNwKdQ=)

---

### Idiomatic syntax

Familiar, easy-to-understand syntax.

*Low-level power with high-level syntax.*

![width:400px](./hello_world.png)

---

![width:800px](./hello_world.png)

---

### Modern language features

- Pattern matching.
- Enum variants.
- Closures.
- Async/await.
- Macros!

---

### Rich type system

- Type aliases.
- Type inference.
- Structs (with methods).
- Enum variants.
- Traits (similar to Haskell *typeclasses* and OOP interfaces).
- Generics (types, traits, lifetimes).
- Helpful error messages and tips.

---

### Modern tooling

#### Cargo ![height:1em](https://user-images.githubusercontent.com/41265192/44623012-be9fcc00-a8c4-11e8-9943-646e3c682292.png)

- Build tool
- Package manager.
- Test runner.
- Docs generator.

- Extensible with *plugins*.

---

#### Crates.io ![height:1em](https://crates.io/assets/Cargo-Logo-Small.png)

Rust's crate registry.

#### Rustfmt

Awesome formatting.

#### Rust Analyzer ![height:1em](https://pbs.twimg.com/profile_images/1217461647377420289/HXHa6hZU_400x400.jpg)

Great IDE and editor support.

#### Rustup

Get all your toolchain from a single place!

---

### Great learning material and community

- Official book: *The Rust Programming Language*
- Generated crate docs.
- Growing community of *Rusteaceans*.

![width:200px](https://images-na.ssl-images-amazon.com/images/I/51fHAF3OAyL._SX376_BO1,204,203,200_.jpg)

---

# Enough talk!

![width:500px](https://i.imgur.com/rXucfA4h.jpg)

---

# Hands on!

Let's build our first application with Rust.

---

## What we're building

A terminal hangman game.

![width:400px](https://media.istockphoto.com/illustrations/simple-illustration-of-hangman-game-illustration-id1196954772?k=20&m=1196954772&s=612x612&w=0&h=nzsr9bCwxp9xW3dp-nBJeXE7TVGqnWtdJpbaXvEyl3E=)

---

## What we'll learn

- Setting up a project.
- Rust's basic syntax.
- Basic error handling.
- Enums, pattern matching, traits, closures...
- Using external *crates*.
- Rust's module system.
- Basic unit testing.

---

# Our project is finished!

Now what?

---

# Some great material

- *The Rust Programming Language* book.
- [*Let's Get Rusty*](https://www.youtube.com/c/LetsGetRusty) Youtube channel.
- [*Type-Driven API Design in Rust*](https://www.youtube.com/watch?v=bnnacleqg6k&list=PL-N92y40KxKn2wTKEB7-iJRU_IjdB7N_M&index=29&t=1964s) by Will Crichton.
- [*Whoops! I Rewrote it in Rust*](https://youtu.be/XdMgH3eV6BA) by Brian Martin.

![width:150px](https://rustacean.net/more-crabby-things/rustdocs.png)

---

# Challenges!

Some projects you can make:

- Snake game using *Piston*.
- Build a REST API using *Rocket* (web framework) and *Diesel* (ORM).
- Create a WASM web app with *Yew* (*React developers might be interested*)
- Make a cool CLI app with *tui-rs*.

The possibilites are endless!

---

# Thank you!

![width:600px](https://rustacean.net/assets/rustacean-flat-happy.png)
