# *Getting on the Rust Train!* script

Hola a todos! Mi nombre es Anthony Suárez, soy un desarrollador de backend en
Devsu, y un partidario del open source y el software libre.

Como sabrán, el tema de esta charla será el lenguage de programación Rust.

En mi opinión, Rust es uno de los lenguages de programación que mejor permiten
al programador escribir código correcto, que sea seguro y confiable. Por esta
razón, es que lo considero mi lenguaje de programación favorito.

Con esta charla, espero que salgan todos con interés en Rust, y también con las bases
suficientes para que puedan comenzar a crear sus propios programas y aplicaciones
en este maravilloso lenguaje.

Dicho esto, bienvenidos a **Getting on the Rust Train**!

Si tienen alguna pregunta, no duden en decírmelo. Si no me equivoco, ustedes
pueden alzar la mano para prender su micrófono, no hay problema en
interrumpirme. Sino, pueden preguntarme por
el chat y responderé en cualquier momento.

## 2. What is Rust?

Entonces, qué es Rust?

Rust es un lenguage de programación de sistemas creado por Mozilla, los creadores
del navegador Mozilla Firefox, en el año 2010.

Rust, siendo un lenguage de sistemas, ofrece control de bajo nivel al igual que
C y C++, razón por la cual es común encontrar a Rust como alternativa a estos
lenguajes.

Pero, si ya tenemos lenguajes de sistemas bien establecidos como C y C++, por
qué debería importarnos Rust?

## 3. Popularity and growth

Bueno, para responder esta pregunta, miremos al paisaje actual y encontremos
el **tren de Rust**, viendo un poco de datos y estadísticas sobre el crecimiento
y popularidad de Rust.

## 4. Rust is the most loved language

Primero. Muchos de ustedes deben ya saber esto. Rust es el lenguaje de
programación más amado por la comunidad, y lo ha sido desde el 2016.

Esta información viene de las encuestas anuales de StackOverflow. Es importante
notar que Rust gana esta categoría en 2022 con un valor del 86.73% de desarrolladores
que desean seguir usando Rust para su trabajo. Esto es 10% más alto que el
segundo lenguaje más amado, que es Elixir.

## 5. High paying jobs

Segundo. Rust se mantiene entre las tecnologías mejor pagadas, según las
encuestas de StackOverflow.

Así, de acuerdo a la encuesta del 2021, los trabajos de Rust pagan un promedio
de $77,530 por año, estando entre otros lenguajes con paga alta como Go y
Scala.

## 6. Rust community is growing

Tercero. De acuerdo a la encuesta State of the Developer Nation por Slash Data,
Rust is el lenguaje con la comunidad de más rápido crecimiento. Desde 2020
hasta 2022, el número de desarrolladores se ha triplicado, teniendo alrededor
de 2.2 millones de desarrolladores, lo que significa que ahora es más grande
que Ruby en términos de comunidad.

En el mismo estudio se determinó que Rust es usado comúnmente para proyectos
de realidad virtual y aumentada y para proyecto de IoT.

## 7. Rust and WASM

Cuarto. Rust es el lenguaje #1 para WebAssembly.

Por si no sabe, WebAssembly es un nuevo target de compilación que permite a los
navegadores correr programas compilados, lo que los hace extremadamente rápidos.

WASM is una tecnología que está teniendo un gran impacto en el desarrollo web
moderno. Hay gente que incluso afirma que llegará a ser el target de compilación
por defecto del futuro, porque permite aplicaciones verdaderamente portátiles
y multiplataforma.

Volviendo a Rust, se encontró en la encuesta State of WASM 2021, que Rust es el
lenguaje más usando para WebAssembly, y que los desarrolladores que usan otros
lenguajes, desean usar Rust.

## 8. Rust and blockchain

Quinto. Rust es muy popular para tecnologías blockchain. De hecho, si es que
buscas un trabajo en Rust, es muy probable que veas que muchas posiciones
están relacionadas a blockchain.

Esta popularidad se debe en parte a frameworks como Solana, que te permite
crear smart contracts con Rust.

## 9. Rust and Linux

Sexto. Si es que eres un fanboy de Linux como yo, ya sabrás de qué va esto.

Rust es el segundo lenguaje del kernel de Linux.

Existen patches del kernel de Linux que permiten escribir el kernel con Rust.
Aunque estos patches aún no hayan sido agregados al código principal del
kernel, Linus Torvalds manifestó que es muy probable que estén en la versión
5.20 de Linux. Uno de los cambios con Rust, es la reescritura de los coreutils
de GNU en Rust, un proyecto que se nombró uutils, y que avanza rápidamente,
llegando a tener rendimiento incluso superior al de la implementación en C.

## 10. Companies using Rust

Y para completar esta sección, aquí están algunas grandes compañías usando
Rust en producción.

Dropbox reescribió el núcleo de su motor de sincronización de archivos en Rust.
En su blog, manifiestan que Rust ha sido un multiplicador de fuerzas para su
equipo.

Coursera usa Rust en partes de su sistema de calificación de tareas, y afirman
que Rust es una excelente elección para funciones de seguridad crítica.

Figma usó Rust para reescribir su servidor multiplayer antes escrito en
Typescript. Eligieron Rust porque el sistema debe ser rápido y concurrente.
En su post, expresan que Rust combina velocidad con bajo gasto de recursos.

Entre otras compañías, están Cloudflare, Facebook, Discord, Amazon, Microsoft
(que es un miembro fundador de la Rust Foundation), Mozilla, NPM y Twitter.

Si quieren aprender más sobre estos casos de éxito, les recomiendo leer el
post de Serokell que está aquí en el pie de la diapositiva.

## 11. Rust introduction

Okay, espero que los datos y los casos de éxito les haya causado interés en 
Rust. Pero es suficiente de eso. Hablemos ahora sobre el lenguaje en sí, y
lo que lo hace increíble.

## 12. Goals of Rust

Rust fue creado por Mozilla con el siguiente objetivo: Ser un lenguaje
práctico para crear programas rápidos, seguros y concurrentes.

En las siguientes diapositivas, nos daremos cuenta que las características
de Rust giran alrededor de este objetivo principal.

## 13. The borrow checker

Hablemos sobre el borrow-checker. Este es el principal diferenciador de Rust
frente a otros lenguajes. El borrow-checker es un sistema compuesto por
simples reglas que aseguran la validez de la memoria en uso. Este funciona
en tiempo de compilación, por lo que no hace lento el programa y remueve la
necesidad de un garbage collector.

Lo que necesitamos saber sobre esto es:
1. Cada dato tiene un dueño, que es usualmente la variable a la que se asignó.
2. Se puede referenciar el valor de una varialbe mediante una referencia o
   pointer.
3. Solo puede haber uno de dos casos: Que se tenga un número indefinido de
   referencias inmutables, o que se tenga una sola referencia mutable.

## 14. Memory safety

Con estas simples reglas, el borrow-checker permite a Rust encontrar problemas
comunes como segfaults y pointers inválidos o null.

También digámosle adiós a otros problemas comunes como variables indefinidas
o excepciones no atrapadas. Más adelante veremos sobre cómo Rust resuelve estos
otros problemas.

## 15. *Fearless Concurrency*

Uno de los objetivos de Rust es ser concurrente, y de nuevo gracias al
borrow-checker, problemas comunes como race conditions o deadlocks son
imposibles en Rust.

Esto significa que podemos escribir código concurrente sin miedo, ya que
el código ni siquiera compilará si uno de estos problemas aparece. Esto
es lo opuesto a otros lenguajes, que usualmente requiren altos grados de
experiencia y cautelo para escribir programas que funcionan en múltiples
threads.

## 16. Idiomatic syntax

Siguiente. Rust tiene una sintaxis expresiva e idiomática, que nos provee
control de bajo nivel con código de alto nivel. Por ejemplo, veamos un
simple Hello World en Rust.

## 17. Hello World

En este script, vemos dos funciones definidas con el keyword fn. Una de las
funciones es la función principal, la cual define una variable greeting
y la imprime en pantalla.

Esta variable greeting no necesita un tipo explícito, ya que Rust puede inferir
el tipo de la misma.

En la función greet, vemos que se recibe un parámetro name de tipo str, y se
devuelve un String. Si se preguntan cuál es la diferencia entre un str y un
String, es que el primero, que se lo conoce como string slice, es constante y de tamaño fijo, mientras que el segundo
es mutable y puede cambiar de tamaño. Es usual en Rust ver que las funciones
reciban string slices como parámetros y devuelvan Strings. Esto es porque
cualquier string slice definido dentro de la función saldría de scope cuando
la función devuelva, por lo que el pointer se volvería inválido.

Finalmente, podemos notar que no hay ningún return en ningún lado. Esto es
porque Rust permite devolver el valor de la línea que no tenga un punto y coma
al final, haciendo nuestro código más legible.

## 18. Modern language features

Rust tiene sintaxis moderna que combina lo mejor de la programación funcional
con la programación imperativa. Algunos features incluyen:

- Pattern matching.
- Enum variants.
- Closures.
- Async/await.
- Y Macros, que son un feature avanzado de Rust que permite metaprogramming, 
  lo que hace que Rust sea extensible más allá de lo posible con la sintaxis
  regular.

## 19. Rich type system

El sistema de tipos de Rust da múltiples utilidades al programador, como:

- Type aliases.
- Inferencia de tipos..
- Structs (con métodos).
- Enum variants.
- Traits (similares a typeclasses de Haskell e interfaces de Java).
- Generics (no solo par tipos, sino para traits y lifetimes también).

Además, el sistema de tipos de Rust permite que el compilador genere mensajes
de error muy útiles para cuando el código no compila.

## 20. Modern tooling - Cargo

El ambiente de Rust provee muchas herramentas modernas. Por ejemplo, Cargo,
que es el package manager, build tool, test runner y generador de documentación
de Rust.

Cargo, además de proveer toda esta funcionalidad, es extensible mediante
plugins, que se pueden instalar usando Cargo mismo.

## 21. Other tools

Otras herramientas son:
- Crates.io, el registro de paquetes de Rust.
- Rustfmt, el formatter oficial de Rust.
- Rust analyzer, que permite soporte de IDEs y editores de texto para Rust.
- Y Rustup, que es el instalador oficial del toolchain the Rust.

## 22. Learning material and community

Finalmente, Rust también tiene gran material de aprendizaje y una gran comunidad.

Para aprender, hay muchas opciones, como el libro oficial, con nombre The
Rust Programming Language, o la documentación autogenerada de cada librería,
o la gran comunidad de Rusteaceans que crece cada día.

## 23. Enough talk!

Pero ya hablé suficiente. Es hora de comenzar lo que todos hemos estado esperando.

## 24. Hands On!

Es hora de escribir nuestra primera aplicación con Rust.

## 25. What we're building

Hoy escribiremos un simple juego de ahorcado con una interfaz de consola.

Si desean ver el código del producto final, con ciertas modificaciones y
uso de conceptos más avanzados a lo que veremos hoy, pueden acceder al
link del repositorio que se encuentra en esta diapositiva.

## 26. What we'll learn

Con este proyecto nos expondremos a varios conceptos de Rust. Aprenderemos:

- Cómo configurar un proyecto.
- Sintaxis básica.
- Manejo de errores básico.
- Enums y pattern matching.
- Cómo usar librerías externas.
- El sistema de módulos de Rust.
- Pruebas unitarias básicas.
- Y más.

Así que comencemos!

## [Project building]

Para comenzar, instalemos el toolchain de Rust usando Rustup. Así que vamos
a Google y buscamos Rustup...

[go to Google and type Rustup]

Ahí está. Para instalar Rust, seguimos las instrucciones de la página web,
dependiendo del sistema operativo que estemos usando. En mi caso, solo debemos
correr este comando y seguir las instrucciones.

En mi caso, ya tengo Rust instalado, entonces no voy a seguir con la
instalación.

Para comprobar que todo esté correcto, podemos correr los comandos rustup 
--version y rustc --version.

After this, we can verify the installation by running `rustup --version` and `rustc --version`.

[Run commands]

Okay, todo bien. ahora crearé un directorio para comenzar con el proyecto.

[Create directory]

Dentro de este directorio, podemos correr el comando `cargo init`, lo que
inicializará un proyecto básico con Cargo.

> `cargo init`
> `k`

Si vemos lo que está en la carpeta, veremos que se generó un archivo Cargo.toml
y una carpeta src. Veamos dentro de Cargo.toml.

[See Cargo.toml]

Dentro de este archivo se encuentra información general sobre el paquete,
incluyendo una sección de dependencias, que sirve para descargas paquetes
externos de Crates.io. Esto es bastante similar a package.json cuando se usa
Node.

Ahora, veamos dentro de src.

[See src]

Hay un archivo main.rs. Veamos dentro.

[See main.rs]

En este archivo se encuentra un simple Hello World, como el que vimos
anteriormente. para probar que todo funcione correctamente, podemos correr
el comando `cargo run`.

> `cargo run`

El output nos dice qué sucedió. Primero, el programa se compiló, y luego se
ejecutó el archivo binario generado. En caso de que queramos compilar sin
ejecutar, podemos usar `cargo build`, o también podemos usar `cargo check`
para comprobar la validez del programa sin generar ningún ejecutable.

Okay, comencemos a escribir el juego. Comenzaremos desde lo básico, creando
la lógica y luego trasladando eso a una interfaz de consola.

Primero, necesitamos una entidad que contenga el estado del juego. Para esto,
podemos usar un struct, al que llamaremos Hangman.

[Create empty Hangman struct]

Este struct mantendrá la información del juego. Por ejemplo, la palabra que
se debe adivinar.

[Add `word` String field]

También necesitamos una forma de saber qué letras quedan por adivinar. Para
esto, podemos usar el struct HashSet de la librería estándar. También necesitamos
que este HashSet se popule con los caracteres de la palabra escogida, pero
eso haremos luego.

[Add `letters_to_guess` HashSet]

Como pudimos ver, gracias a Rust Analyzer pude autoimportar el HashSet, el 
cual viene del crate std::collections. Si no estuviera esa importación,
tendría que llamar al HashSet con el nombre completo, o sea std::collections::HashSet.

Perfecto. Por último, añadiremos un campo con el número de vidas del jugador.

[Add `lives` u8 field]

Aquí, el tipo que hemos usado es u8, que significa un entero sin signo, o
unsigned integer, de 8 bits. Este tipo de dato puede contener números del 0 al
255. Si quisiéramos números negativos también, podemos usar variantes como i16
o i32. Para números decimales, usamos los tipos f32 o f64. Por defecto, Rust
usa i32 para enteros y f64 para floats.

Ahora que tenemos los datos del struct, implementemos el constructor.

[Write impl and empty new -> Self]

Para implementar un constructor, creamos una función asociada con el nombre
new. Esto no es requerido, ya que Rust no tiene de verdad constructores,
pero es común llamar new a las funciones asociadas que devuelven el tipo
de la implementación.

Esta función devuelve el tipo Self, que en este caso, se refiere al struct
Hangman.

Creemos una mínima implementación de esta función.

[Add minimal Hangman return with string slice]

Aquí el editor nos marca un error. Nos dice que se esperaba un String, pero
se encontró un string slice. En este caso, el error es porque los string literals
en Rust son por defecto string slices, así que para convertirlos en Strings
podemos usar el método to_owned().

[Add to_owned to string]

Ahora, sería conveniente que la palabra por adivinar no sea constante. Por esto,
recibiremos un argumento word.

> Add word &str param.

Es un patrón común en Rust que las funciones reciban como parámetro un string
slice en vez de un String, ya que por lo general es más eficiente e intuitivo
al llamar la función.

Perfecto. Ahora modifiquemos nuestro letters_to_guess, para que sea generado
de la palabra que pasamos como argumento.

> Create letters_to_guess empty set.
> Create `for ch in word.chars()` and insert in hashet.
> Notice error, and add mut to letters_to_guess.
> **Change letters_to_guess field in final return**

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
estado sea Lose si se ha adivinado incorrectamente perdiendo todas las vidas.

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

> Escribir loop { clear(); println!(guessed_word) ; println!(pic) }

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
de la misma y podrán ver una implementación más avanzada utilizando el crate
Cursive para creación de aplicaciones de consola.

## 27. Finished project

Perfecto. Hemos terminado nuestro proyecto. Y ahora qué?

Bueno, si les interesó el desarrollo con Rust, puedo recomendar material de
aprendizaje que considero muy bueno.

## 28. Some great material

Primero, el libro oficial de Rust es un grandioso lugar para comenzar a
aprender desde conceptos básicos hasta los más complejos.

Segundo, recomiendo el canal de Youtube Let's Get Rusty, que es totalmente
dedicado a Rust, y contiene guías y tutoriales de temas diversos.

También recomiendo la charla *Type-Driven API Design in Rust*, que demuestra
cómo el sistema de traits de Rust es un gran aliado para diseñar buenos APIs
en Rust.

Finalmente, otra charla que recomiendo es *Whoops! I Rewrote it in Rust*, en
la que Brian Martin muestra cómo se usó Rust para reescribir la herramienta
de caching en memoria utilizado en Twitter, llegando a tener incluso mejor
rendimiento que la implementación en C puro.

## 29. Challenges

Para ganar experiencia, también recomiendo crear tus propias aplicaciones,
así que les voy a decir algunas ideas de qué hacer.

Si les gusta los videojuegos, pueden crear un simple juego de Snake usando
el crate Piston.

Si les gusta el desarrollo web, pueden crear un REST API usando Rocket como
web framework y Diesel como ORM.

Si les gusta el frontend, y especialmente si les gusta React, les va a interesar
crear una aplciación de WebAssembly usando el crate Yew.

O, si les interesa, pueden crear una aplicación con interfaz de consola usando
librerías como Cursive o tui-rs.

La verdad es que Rust, a pesar de ser un lenguaje de sistemas, tiene una comunidad
muy grande y es ampliamente usado para otras áreas también, por lo que ahora
las posibilidades son infinitas.

Así, no me queda nada más que decir, excepto...

## 30. Thank you

...gracias por asistir a esta charla. Espero que hayan aprendido algo nuevo,
y espero que ahora se sientan interesados y listos para comenzar con Rust
y crear software rápido, seguro y confiable. Muchas gracias!

Si hay preguntas, estaré feliz de responderlas, sino, eso es todo de mi parte.
