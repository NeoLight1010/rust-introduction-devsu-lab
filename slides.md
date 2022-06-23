---
title: Rust Introduction
description: A quick introduction to Rust, its history, future, and how to get started.
author: Anthony Suárez <neolight1010>
keywords: rust, introduction

theme: gaia
paginate: true
backgroundColor: #ffff
backgroundImage: url("../background.jpg")

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

Rust is a systems-programming language created by Mozilla in 2010.

Rust is taking over the programming world for its revolutionary features.

![width:200px](https://rustacean.net/assets/cuddlyferris.png)

---

# Popularity and Growth

![width:600px](https://cdna.artstation.com/p/assets/images/images/010/103/780/large/eoin-o-broin-03.jpg?1522607778)

---

Rust has remained the most loved programming language since 2016.

![width:600px](https://rustacean.net/more-crabby-things/ferris-love.jpg)

<!--_footer: StackOverflow Survey 2016, 2017, 2018, 2019, 2020, 2021 -->

---

Rust is associated with high paying jobs.

![width:600px](https://i.imgur.com/Npho9BV.png)

<!-- Rust jobs usually have high-paying salaries averaging at around $77,530 
per year, according to the 2021 StackOverflow Survey.-->

<!-- _footer: StackOverflow Surveys -->

---

Rust's has the fastest growing language community! From 2020 to 2022, the
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

## Quick introduction to Rust

<!-- What makes Rust so attractive? -->

---

#### Goals

- Speed.
    - Compiled language.
    - No garbage collection.
- Safety.
     - No `null`s.
     - No dangling pointers.
     - No *unsafe*.
- Concurrency.
    - No race conditions.
    - No deadlocks.
    - *Fearless concurrency*.

---

### Meet the *borrow-checker*

- Each variable has an *owner*.
- You can reference another variable's value via a *reference*.
- You may either have any number of *immutable* references, or only one
  *mutable* reference at the same time.

---

[Example here]

---

### Memory safety 

Say *Goodbye!* to memory issues. Never more:

- Segfaults.
- `cannot access member 'x' of undefined`.
- Invalid pointers.

---

### Fearless concurrency

The borrow-checker rules make common concurrency issues *impossible*.

**Concurrency has never been easier!**

---

### Idiomatic syntax

Familiar, easy-to-understand syntax.

---

### Modern language features

- Pattern matching.
- Enum variants.
- Closures (anonymous functions).
- Async/await (even before than JS!).

---

### Rich type system

- Type aliases.
- Type inference.
- Structs (with methods).
- Traits (similar to Haskell *typeclasses*).
- Generics.

- Helpful error messages and tips.

---

### Modern tooling

#### Cargo

- Build tool
- Package manager.
- Test runner.

- Extensible with *plugins*.

---

#### Rustfmt

Awesome formatting.

#### Rust Analyzer

Great IDE and editor support.

---

#### Rustup

Get all your toolchain from a single place!

---

- Doc generator.
- The Book.
