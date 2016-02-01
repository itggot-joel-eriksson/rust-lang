rust-lang
==========

### [Dokumentation](https://www.rust-lang.org)

## Om Rust
Rust är ett programmeringsspråk som

## Stark eller svag typning
Rust har en stark typning. Exemplet nedan genererar ett felmeddelande vid kompilering.
#### Exempel:
```rust
//stark_svag-typning.rs
fn main() {
    let x = "20";
    let y = 10;
    let z = x + y;
}
```
#### Output:
```bash
stark_svag-typning.rs:4:13: 4:14 error: binary operation `+` cannot be applied to type `&str` [E0369]
stark_svag-typning.rs:4     let z = x + y;
                                    ^
stark_svag-typning.rs:4:13: 4:14 help: run `rustc --explain E0369` to see a detailed explanation
stark_svag-typning.rs:4:13: 4:14 note: an implementation of `std::ops::Add` might be missing for `&str`
stark_svag-typning.rs:4     let z = x + y;
                                    ^
error: aborting due to previous error
```

## Dynamiskt eller statisk typning
Rust har en statisk typning. Exemplet nedan genererar ett felmeddelande vid kompilering.
#### Exempel:
```rust
fn main() {
    let mut x = 20;
    println!("{}", x);

    x = 10;
    println!("{}", x);

    x = 13.37;
    println!("{}", x);
}
```
Rust tillåter inte heller att man byter värde på en variabel utan att använda `mut` tillsammans med `let`. `mut` står för mutable alltså att värdet för variabeln får ändras inom samma datatyp, en variabel kan alltså aldrig ändra datatyp.

#### Output:
```bash
dynamisk_statisk-typning.rs:8:9: 8:14 error: mismatched types:
 expected `_`,
    found `_`
(expected integral variable,
    found floating-point variable) [E0308]
dynamisk_statisk-typning.rs:8     x = 13.37;
                                      ^~~~~
dynamisk_statisk-typning.rs:8:9: 8:14 help: run `rustc --explain E0308` to see a detailed explanation
error: aborting due to previous error
```

## Kompilerat eller tolkat
Som nämnt är Rust ett kompilerat språk, det skulle kunna sägas att Rust är en dialekt av språket C.

## Native eller virtuell maskin
Som nämnt är Rust som en dialekt till C som är ett native-språk. En användare förväntas därför inte att ladda ner en virtuell maskin för att köra program skrivna i Rust. Det enda som krävsär att utvecklaren hämtar kompilatorn för Rust.

### Imperativt/procedurellt eller deklarativt
Rust är ett imperativt/procedurellt språk.

## Funktionellt
Rust är inte nödvändigtvis ett starkt funktionellt språk, men utan nyckelordet `mut` är Rust starkt funktionellt.

## Objektorientering
Rust har stöd för objektorienterad programmering och både klasser och objekt finns att skapa.
#### Exempel:
```rust
//Exempel på hur man skapar klasser och objekt
```

## Open eller closed source
Rust är open source och finns tillgängligt på [GitHub](https://github.com/rust-lang/rust). För [Mozilla](https://www.mozilla.org) som utvecklat Rust är open source viktigt, Rust är då licenserad under både [MIT](https://opensource.org/licenses/MIT) och [Apache 2.0](https://opensource.org/licenses/Apache-2.0).

Rust utvecklas främst av Rust Project Developers som också äger upphovsrättet till språket. Enligt det repository som finns för Rust finns det möjligheter för vem som helst bidra till utvecklingen av Rust, mer info om det finns på GitHub [CONTRIBUTE](https://github.com/rust-lang/rust/blob/master/CONTRIBUTING.md).

Enligt deras hemsida är antalet personer som är med och bidrar till utvecklingen av Rust över 1200 personer.

## Användningsområde
Rust har inget uttalat användningsområde, men det bär vara samma användningsområde som C, alltså i stort sett vad som önskas. Det finns till exempel en PlayStation emulator som skrivits i Rust med OpenGL.

Det absolut mest kända programmet som skrivits i Rust är [Mozillas Firefox](https://developer.mozilla.org/en-US/Firefox/Building_Firefox_with_Rust_code). Även om implementeringen inte är helt klar ännu så finns vissa delar klara (skrivna i Rust) i senare versioner av Firefox.

## Övriga utmärkande drag
...

## Kodexempel
Exempel skrivna i Rust finns i [examples/](examples).
