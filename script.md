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

## 20. Modern tooling - Cargo

Rust has many modern tools at its disposal. For example, we got Cargo, which is
Rust's package manager, build tool, test runner and documentation generator.

Cargo is even extensible via plugins that you can install using Cargo itself.

## 21. Other tools

Other available tools are:

- Crates.io, which is Rust's package registry.
- Rustfmt, which is Rust's official formatter, ensuring for consistent style
  accross your codebase.
- Rust analyzer, which provides great IDE and editor support.
- And Rustup, which is the official installer of the Rust toolchain, allowing
  you to install all of these tools from a single place.

## 22. Learning material and community

Finally, Rust also has a big community and material for learning.

For example, you can learn Rust by reading the official Rust Book, or by following
the Rust by Example website. You can also read any library's documentation
from its automatically generated docs. Or you can ask for help from anyone in
the big community of Rustaceans around the world.

## 23. Enough talk!

But enough talk! The moment that we've all been waiting for has come.

## 24. Hands On!

It's time to write our first project in Rust!

## 25. What we're building

We will be writing a simple terminal hangman game. If you want to see the
finished project, you can go to the GitHub repo in
github.com/NeoLight1010/hangman-rs.

## 26. What we'll learn

This simple projets will expose us to multiple Rust concepts, so we will learn
things like:

- Setting up a project.
- Rust's basic syntax.
- Basic error handling.
- Enums, patter matching, traits, closures...
- Using external crates.
- Rust's module system.
- Basic unit testings.
- And more.

So, let's get started!

## [Project building]

To get started, we need to install the Rust toolchain using Rustup, so let's
go to Google and type Rustup...

[go to Google and type Rustup]

And there it is. There, we can follow the instructions depending on the opertating
system that we're using. In my case, I'm using Linux so I can run that command.
If you use Windows, you can download the installer and execute it.

[Run the command]

I recommend you follow the basic instructions for installing the stable release of
Rust. In my case, I already have Rust installed, so I wil cancel the installation.

After this, we can verify the installation by running `rustup --version` and `rustc --version`.

[Run commands]

Okay, perfect. Let's now make a directory for our project. You
can create the directory anywhere. In my case, I have a folder
specific for this lab, so I'll go in there and create the
directory.

[Create directory]

Inside this directory, we can create a new Rust file named `main.rs` in order
to create a simple Hello World.

> `touch main.rs`
> `nvim main.rs`

In my case, I will be using the NeoVim text editor, but you can use any editor
of your preference. Let's create a Hello World program like we saw before.

[Write hello world]

Perfect! Let's now compile our program using the Rust compiler.

> `rustc main.rs`
> k

If we list the contents of the directory, we can see an executable has been
generated. Let's run this executable.

> `./main`

As you can see, it prints Hello World to the console as expected. But let's stop here. Remember I told you Rust has modern tooling? This way of manually compiling everything will get really hard to manage when our project grows bigger, so let's use Cargo instead. First, let's delete everything in the directory.

> `rm main main.rs`

Now, we can run the `cargo init` command.

> `cargo init`
> `k`

If we list the contents of the directory, we can see this command generated a `Cargo.toml` file and a `src` folder. Let's see what's inside `Cargo.toml`.

[See Cargo.toml]

As you can see, it contains general information about our package, and also has
a `dependencies` section for listing external crates we might want to use. This
is really similar to a `package.json` file if you use Node.

Let's now see what's inside src.

[See src]

As you can see, it contains a single `main.rs` file. Let's look at this file.

[See main.rs]

Inside the file, we can see it contains a simple Hello World program, similar
to what we did before.

Now, let's run our program using Cargo, using the `cargo run` command.

> `cargo run`

The output tells us what happened here. First, the program was
compiled, and then it was run, all in a single step. If
instead we wished to just compile without running, we could've
used the `cargo build` command instead. Or, if we wanted to
just check the validity without generating any executables, we
could've run the `cargo check` command.

Okay, so let's start writing our game. We will start from the basics, by creating
the logic of our game first, and then translating that to the screen.

First, we need a single entity that will hold the state of our game. For this,
we can use a struct. Let's create a Hangman struct.

[Create empty Hangman struct]

This struct will hold data about our game. A good place to start is the word that
the player has to guess, so let's add that to the struct.

[Add `word` String field]

Now, we also need a way to know what letters the player needs to guess. For this,
we can use a HashSet from Rust's standard library. Later, we will create a
constructor that will initialize this set with the letters from the word.

[Add `letters_to_guess` HashSet]

As you can see, using Rust Analyzer's autoimporting tool, I have imported the HashSet struct from
std::collections. This syntax brings HashSet to the module's namespace. If we hadn't done so, we would've needed to use the full name std::collections::Hashset for our field.

Perfect. The last thing we'll need is a way to know how many lives the player has, so let's create that.

[Add `lives` u8 field]

The type that we used here is u8, which means an 8-bit unsigned integer, which means it can hold numbers from 0 to 255, which is just what we need. If we wanted negative numbers too, we could've used the i8 type, and if we need more memory, we can use other variants like i16 and i32. For floats, you can use f32 or f64. By default, rust will use i32 for integers and f64 for floats.

Now, let's go ahead and start implementing our struct's constructor.

[Write impl and empty new -> Self]

To implement a constructor, we can create an associated
function with the name new. The truth is that Rust has no real
constructors, and it's not necessary for the function to named
`new`, but it's a convention in Rust to do so.

The function will return the type Self, which inside the impl block refers to the
Hangman struct.

Let's add a minimal implementation of our constructor.

[Add minimal Hangman return with string slice]

The editor marks an error. It says it expected a String, but found an ampersand
str instead. This is because Rust has two main String types. The ampersand str one is referred to as a "string slice", and cannot be mutated or owned by their variables, which is why they're referenced as a pointer. The String type, on the other hand, is mutable, can grow in size, is UTF-8 encoded, and can be owned by variables.

By default, simple string like the one we have here are string slices. To make
them owned Strings, we can use the `to_owned` method.

[Add to_owned to string]

Ahora, sería conveniente que la palabra por adivinar no sea constante. Por esto,
recibiremos un argumento word en la función asociada new.

> Add word &str param.

Es un patrón común en Rust que las funciones reciban como parámetro un string
slice en vez de un String, ya que por lo general es más eficiente e intuitivo
al llamar la función.

Perfect. Let's now modify our letter_to_guess so it is generated from the letters
of our word.

> Add word variable and change it in struct.
> Create letters_to_guess empty set.
> Create `for ch in word.chars()` and insert in hashet.
> Notice error, and add mut to letters_to_guess.
> Change letters_to_guess field in final return.

Aquí, hemos añadido el keyword mut al HashSet letters_to_guess. Esto es porque
en Rust, toda mutación debe ser explícita. En el loop de abajo insertamos
caracteres al HashSet; esto es considereado una mutación, por lo que debemos
declarar la variable letters_to_guess como mutable.

Ahora, crearemos una función que permita al usuario adivinar un caracter.
Esta función se llamará guess_letter. Pero antes, creemos un enum que nos
permita conocer el resultado de adivinar una letra.

> Crear GuessOutcome enum (Correct, Incorrect).

Este enum será el tipo de retorno de nuestra función, la cual definiremos
ahora mismo.

> Definir guess_letter.

Nuestra función recibe un caracter como parámetro. Implementemos esta función.

> Implementar guess_letter.

Esta función comprueba si letters_to_guess contiene la letra dada, y la remueve
y devuelve Correct si la contiene. Sino, devuelve Incorrect y disminuye la
cantidad de vidas en uno. La función std::cmp::max es utilizada para asegurarnos
que las vidas no se asignen un número negativo, ya que este campo está definido
como u8 y el programa podría crashear.

Listo, a continuación, vamos a crear un método que nos permita saber si el juego
está en progreso, o si ya se acabó. Para esto, primero crearemos un enum
que represente el estado del juego.

> Create GameState enum (Win, Lose, Playing).

El estado Win significa que el jugador ganó, Lose significa que perdió, y
Playing significa que aún no se acaba el juego.

Ahora, definiremos nuestra función get_game_state.

> Definir tipos de get_game_state.

Podemos notar que el primer parámetro de la función es una referencia a self,
lo que significa que esta función se considerará como un método. Para implementar
esta función, utilizaremos Test Driven Development, por lo que primero escribiremos
un caso de prueba. Para hacer esto, crearemos un módulo de tests al final del
archivo.

> Definir módulo test.
> Añadir macro cfg(test).

Como podemos ver, este módulo tiene un macro cfg(test), que es utilizado por
Rust para saber que se trata de un módulo de pruebas. La primera prueba que
crearemos es asegurarnos que el juego esté en progreso si recién ha comenzado.

> Crear prueba test_playing_state.

En esta prueba, creamos una instancia de Hangman con la palabra "hello". Nuestra
prueba verificará que el estado de juego sea Playing usando un match statement.

El match statement es la forma de hacer pattern matching en Rust, y es muy
fácil de comprender. Si el estado de juego es Playing, entonces no se realiza
ninguna acción, pero si el estado es cualquier otra cosa, se ejecutará un panic
con un mensaje. Los panics en Rust son similares a las excepciones en otros
lenguajes, ya que estas causan que el programa crashee. Sin embargo, esta no
es la manera correcta de manejar errores en Rust. Veremos acerca de eso más
adelante.

Cuando el código ejecute en panic, el test fallará. Para correr nuestro test,
ejecutemos `cargo test` en la terminal.

> cargo test

Como podemos ver, nuestro código no compila ya que la función get_game_state
devuelve un unit type (similar a void en otros lenguages). Arreglemos esto
implementando lo mínimo que haga que la prueba pase.

> Retornar GameState::Playing.

Corremos nuestros tests de nuevo.

> cargo test

Nuestro test pasó. Ahora, creemos el siguiente test, que verificará que el
estado sea Lose si se ha adivinado correctamente perdiendo todas las vidas.

> Implementar test_lose_state.

Esta prueba utiliza el método guess_letter para adivinar incorrectamente hasta
que se hayan acabado las vidas. El programa entrará en pánico si el estado
del juego no es Lose. Corramos la prueba.

> cargo test

La prueba falla. Impelmentemos lo mínimo para que la prueba pase.

> Implementar self.lives == 0 -> Lose.

> cargo test

Con esta implementación, nuestra prueba pasa. Finalmente, creemos la prueba
para el estado Win.

> Impelmentar test_win_state.

En esta prueba, adivinamos correctamente todas las letras, por lo que el estado
debería ser Win. Corremos la prueba.

> cargo test

Por supuesto, la prueba falla. Implementemos esta funcionalidad.

> Implementar if letters_to_guess.is_empty -> Win;

Aquí, si ya no hay más letras por adivinar y aún tiene vidas el jugador,
retornamos Win. Corremos el test.

> cargo test

Perfecto, las pruebas pasan, y eso concluye la implementación de get_game_state.
Con este ejercicio, hemos aprendido cómo escribir pruebas en Rust y hacer
un poco de TDD. Por cuestiones de tiempo, no se escribirán pruebas para el
resto del juego, pero si están interesados pueden revisar el repositorio en
mi GitHub, que contiene todos los tests para la lógica del juego.

Perfecto. Lo que haremos a continuación es traer algunos dibujos para imprimir
en consola. Para esto, crearemos un nuevo módulo en la carpeta src, que se
llamará pics.rs.

> Crear pics.rs

Pegaré los contenidos de este archivo para no pasar mucho tiempo.

```rust
pub const HANGMAN_PICS: &[&str] = &[
    "
  +---+
  |   |
      |
      |
      |
      |
=========",
    "
  +---+
  |   |
  O   |
      |
      |
      |
=========",
    "
  +---+
  |   |
  O   |
  |   |
      |
      |
=========",
    "
  +---+
  |   |
  O   |
 /|   |
      |
      |
=========",
    r"
  +---+
  |   |
  O   |
 /|\  |
      |
      |
=========",
    r"
  +---+
  |   |
  O   |
 /|\  |
 /    |
      |
=========",
    r"
  +---+
  |   |
  O   |
 /|\  |
 / \  |
      |
=========",
];
```

Lo que hacemos en este archivo es definir un array constante de string slices
con los dibujos que vamos a usar. El tipo del array es una referencia ya que
ninguna variable puede ser dueña de una constante; solo puede referenciarla.
La constante también tiene el keyword pub, que significa que puede ser accedida
en otros módulos.

Para poder utilizar esté módulo, el sistema de módulos de Rust requiere que
este sea declarado explícitamente en el archivo principal. Hagamos eso ahora.

> Escribir mod pics en main.

Así, ahora podremos usar nuestros dibujos en el struct. Declaremos un método
get_pic para obtener el dibujo del juego dependiendo en el número de vidas.

> Implementar get_pic.
>   i = len() as u8 - self.lives - 1

Aquí sucede algo interesante. Utilizamos el método get de los arrays para
obtener el objeto en el índice i. Pero luego usamos un método unwrap. Lo que
sucede aquí es que el método get devuelve un tipo Option, que puede ser algo
o no puede ser nada. El método unwrap devuelve lo que esté envuelto en el 
Option, y ejecutará un panic si no hay nada.

Esta es una manera de manejar errores en Rust. Ya que el índice al que llamemos
puede estar fuera de los límites del array, Rust nos permite manejar ese
caso sin crashear el programa utilizando el enum Option. En nuestro caso,
llamamos unwrap porque queremos que el programa falle, pero es mejor práctica
utilizar un match statement para manejar estos casos sin panics.

Finalmente, hagamos que nuestro constructor inicialice el número de vidas
al número de dibujos que tenemos.

> Cambiar lives = pics.len() as u8 - 1.

Por último, creemos otro método que nos devuelva un string que representará
la palabra en nuestra interfaz.

> Implementar get_guessed_word.

Esta función simplemente devolverá la palabra con guiones bajos en las letras
que faltan adivinar.

Listo. Con esto, la lógica del juego está completa. Llegó la hora de implementar
la interfaz de nuestro juego. Para esto, utilizaremos una librería externa llamada
clearscreen, que nos permite limpiar la consola en mútiples plataformas.

> Añadir clearscreen = "1.0.10" a Cargo.toml.

Con simplemente añadir esta línea, Cargo descargará la dependencia y la
compilará al construir nuestro programa. Antes de continuar, moveremos la
lógica de nuestro juego a un nuevo módulo, para limpiar un poco el archivo
main.

> Mover todo a módulo hangman.
> Añadir pub keywords.
> Cambiar import pics a crate::pics.

Listo. Hemos movido la lógica del juego a un nuevo módulo. También añadimos los
keyword pub a los structs e enums para hacerlos públicos y accesibles por otros
módulos. Y también cambiamos el import de HANGMAN_PICS usando el módulo crate,
que nos permite importar de forma relativa el archivo principal del proyecto.

Perfecto. Ahora, iremos a nuestro módulo principal, e implementaremos el juego.

Primero, crearemos una instancia de Hangman, que representará el estado del 
juego.

> Añadir mut hangman.

Ahora, entraremos en un loop infinito, en el cual imprimiremos el dibujo del
ahorcado y pediremos el input del usuario.

> Escribir loop { clear(); println!(pic) }

Aquí, llamamos a la función clear(), que viene del crate que añadimos como
dependencia, y llamamos a unwrap() ya que queremos que el programa entre en
pánico en caso de que la operación de limpiar la consola falle.

Ahora, utilizando el módulo estándar io, recibiremos input del usuario.

> io::stdin().read_line(&mut input).expect(error)

Aquí, creamos una variable mutable input, y la pasamos como referencia mutable
al método read_line. En este caso, en vez de llamar unwrap, llamamos expect,
el cual tiene la misma funcionalidad de unwrap, con la diferencia de que
se imprimirá un mensaje de error.

Si corremos nuestro programa ahora, veremos que podemos ingresar nuestro input
y la consola se limpiará al dar Enter. Para terminar el programa, podemos usar

> cargo run
> Podemos usar Ctrl + C para terminar la ejecución.

Perfecto. Ahora, para no complicar la implementación, supondremos que el primer
caracter del input es la letra por adivinar.

> Definir guess_letter input.trim().chars().nth(0);

Aquí, usamos el iterador del string para obtener el primer caracter. Como podemos
ver, el resutado es un Option, por lo que es posible que el elemento no exista.
Usaremos un match statement para manejar este caso sin problemas.

> match Some => (), None => print!("Enter char"); sleep(1 sec);

Aquí, lo que hacemos es imprimir un mensaje en caso de que no haya ningún input.
Luego, se utiliza la funcińo sleep, del módulo std::thread, para para la ejecución por un segundo antes de continuar.

Aún no hemos implementado la lógica en caso de que si haya un caracter. Hagámoslo
ahora.

> match Some => hangman.guess_letter().

Perfecto. Corramos nuestro programa y veamos qué sucede.

> cargo run.
> [Enter sin nada].
> Si no ingresamos nada, nos sale el mensaje de error y espera un segundo hasta
ejecutar lo siguiente.
> [Letra incorrecta].
> Y cuando escribimos una letra incorrecta, vemos que el dibujo cambia.

Ahora, implementemos lógica para mostrar distintos mensajes si se gana o se
pierde el juego.

> Impelmentar if game_state => print(); break;

Listo. Con esto, el juego mostrará un mensaje si es que se ganó o perdió; y,
además, se saldrá del loop, efectivamente terminando el programa.

Probemos nuestro juego:

> cargo run
> Vamos a ganar.
> Salió del juego con un mensaje de feliciationes.
> Vamos a perder.
> Salió del juego con un mensaje distinto.

Perfecto. Felicitaciones! Hemos creado nuestra primera aplicación en Rust!
Si es que desean profundizar un poco más esta aplicación, pueden ir al repositorio
de la misma y podrán ver una implementación más avanzada utilizando un crate
de creación de aplicaciones de consola.

## 27. Finished project

So, we've finished our project. Now what?

Well, if you're interested in learning more about Rust, I can recommend some
material that you can use.

## 28. Some great material

First, The Rust Programming Language book is a great place to start to learn
Rust, from its basic usage, to the more advanced topics.

Second, I recommend the *Let's Get Rusty* Youtube channel, which is a channel
all dedicated to Rust where you will find guides for diverse topics about the
language.

I also recommend the talk *Type-Driven API Design in Rust*; an amazing talk
that showcases how Rust's trait system can be a powerful tool for designing
good APIs in Rust.

Another talk that I highly recommend is *Whoops! I Rewrote it in Rust* by
Brian Martin, in which Martin showcases how Rust was used at Twitter for
rewriting an open source memory-caching tool, achieving even better results
than with the pure C implementation.

## 29. Challenges

Finally, if you like learning by doing, I can recommend some challenges
that will help you get hands-on experience working with Rust.

You can create a simple Snake game using the Piston game engine; or, you can
build a REST API using the Rocket web framework and the Diesel ORM; or, if you
are a React developer, you might be interested in creating a WebAssembly web
app using Yew; or you can create a cool CLI application using a crate like
Cursive or tui-rs.

The possibilities with Rust are endless! Because, although Rust's initial scope was
systems programming, its amazing features has allowed it to be an excellent
language for many other areas.

With that, I have nothing else to say but...

## 30. Thank you

... thank you for attending this talk. I hope you have learned something new
and I hope you now feel ready to jump into Rust and start creating
amazing, fast, safe and reliable software. Thank you!

So, if there are any questions, I'll be happy to answer them.
