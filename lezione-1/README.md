---
title: "**Lezione 1**"
---

Argomenti trattati:
===

<!-- alignment: center -->

<!-- jump_to_middle -->

- Introduzione alla programmazione
- Sintassi
- Cosa è una IDE (e quali ci sono)
- Cosa è un progetto, e quali strumenti vengono usati

<!-- end_slide -->

Introduzione alla programmazione
===

L'arte di creare programmi, mediante un linguaggio di programmazione

Ci sono vari tipi:

**Paradigmi (modi di pensare e strutturare il codice)**:

- OOP
- Procedural Programming
- Functional Programming

**Come vengono eseguiti**:

- Interpretati (python, lua, js)
- Compilati (C, C++, Rust)
- Ibridi (C#, lua, ts, java)

**Come vengono dichiarate le variabili**:

- Scritti dinamicamente (dynamically typed)
- Scritti staticamente (statically typed)
- Strongly typed
- Weakly typed

<!-- end_slide -->

Sintassi
===

Come vengono scritti

Tanti derivano da C:

```c +line_numbers
// C
int main() {
    printf("Hello, World!");

    return 0;
}
```

```cpp +line_numbers
// C++
int main() {
    std::cout << "Hello, World!" << std::endl;

    return 0;
}
```

```csharp +line_numbers
// C#
class Program
{
    static void Main(string[] args)
    {
        Console.WriteLine("Hello, World!");
    }
}
```

<!-- end_slide -->

Altri linguaggi che hanno preso dal C sono: `lua`, `js`, `java`, `rust`

Ci sono linguaggi che non derivano da C:

```python +line_numbers
# Python
def foo():
        print("Hello, world!")

foo()
```

```go +line_numbers
// Go
func main() {
    fmt.Println("Hello, World!")
}
```

Go prende alcune cose da C, ma non tutto

<!-- end_slide -->

Cosa è una IDE
===

Un IDE è un Integrated Development Environment

Un IDE (Ambiente di sviluppo integrato) ha molte caratteristiche:

- Text editor
- Syntax highlighting
- Auto completamento
- Debugger
- Estensioni
- Terminale
- Linea dei numeri
- Linter
- Compilatore
- Intellisense
- Refactor
- Formatter

<!-- end_slide -->

**Text editor**:

È l'editor di testo

**Syntax highlighting**:

Evidenzia in modo diverso le parole del codice in base al tipo

**Auto completamento**:

Ti permette di auto completare le parole (keywords, variabili)

**Debugger**:

Strumento che ti permette di debuggare (individuare problemi nel codice e risolverli) il codice con facilità

**Estensioni**:

Ti permettono di estendere le funzionalità della IDE

**Terminale**:

Terminale integrato

<!-- end_slide -->

**Linea dei numeri**:

Ogni riga ha un numero, utile per vedere dove ci sono gli errori

**Linter**:

Ti permette di vedere gli errori nel text editor

**Compilatore**:

Compilatore integrato

**Intellisense**:

L'insieme di: syntax highlighting, auto completamento, refactor e capisce il contesto del codice

**Refactor**:

È lo strumento che ti permette di semplificare il refactoring (apportare modifiche al codice senza cambiare il comportamento)

**Formatter**:

È lo strumento che ti permette di formattare il codice

---

## Quali IDE ci sono?


- Visual Studio
- VSCode (non è proprio una IDE di definizione)
- Intellj
- Tutte le IDE di jetbrains
- Android Studio
- XCode
- NVIM o VIM con i plugins

<!-- end_slide -->

Cosa è un progetto
===

Un progetto è una cartella (o anche soluzione) che contiene uno o più programmi

I progetti (anche i programmi) possono essere multi linguaggio

---

## Quali strumenti vengono utilizzati per i progetti

- Formatter
- Linter
- Altri strumenti in base al linguaggio:
  - CMake (per C++/C)
  - Make/ninja (Per qualsiasi progetto da buildare)
  - Project managers (Conan, uv, cargo, go, npm/yarn)
- Strumento di versionamento del codice:
  - git (più famoso e de facto standard)
  - mercurial
- Compilatore se il linguaggio non è interpretato

<!-- new_line -->

**Strumento di versionamento del codice**:

È uno strumento che ti permette di versionare il codice

Di creare snapshot del codice tramite commit

<!-- new_line -->

Il codice si trova dentro dei repository (o raccolta/archivio)

Questi repo vengono caricati (hostati) su piattaforme come github
