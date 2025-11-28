<div align=center>

# Lezione 1

</div>

- Introduzione alla programmazione;
- Sintassi;
- Cosa è una IDE (e quali ci sono);
- Cosa è un progetto, e quali strumenti vengono usati;

## Introduzione alla programmazione

L'arte di creare programmi, medianti un linguaggio di programmazione;

Ci sono vari tipi:

**Paradigmi (modi di pensare e strutturare il codice)**:

- OOP;
- Procedural Programming;
- Functional Programming;

**Come vengono eseguiti**:

- Interpretati (python, lua, js);
- Compilati (C, C++, Rust);
- Ibridi (C#, lua, ts, java);

**Come vengono dichiarate le variabili**:

- Scritti dinamicamente (dynamically typed);
- Scritti staticamente (statically typed);
- Strongly typed;
- Weakly typed;

## Sintassi

Come vengono scritti<br>
Tanti derivati da C

```c
// C
int main() {
  printf("Hello, World");

  return 0;
}
```

```cpp
// C++
int main() {
  std::cout << "Hello, World" << std::endl;

  return 0;
}
```

```cs
// C#
public class Program {
  public void Program() {
    Console.WriteLine("Hello, World");
  }
}
```

Altri linguaggi che hanno preso dal C sono: lua, js, java, rust;

Ci sono linguaggi che non derivano da C:

```py
# Python
def foo():
        print("Hello, world")

foo()
```

```go
// Go
func main() {
  fmt.Println("Hello, World")
}
```

## Cosa è una IDE

Un IDE è un Integrated Development Environment

Un IDE (Ambiente di sviluppo integrato) ha molte caratteristiche:

- Text editor;
- Syntax highlighting;
- Auto completamento;
- Debugger;
- Estensioni;
- Terminale;
- Linea dei numeri;
- Linter;
- Compilatore;
- Intellisense;
- Refactor;
- Formatter;

**Text editor**:

è l'editor di testo;

**Syntax highlighting**:

Evidenzia in modo diverso le parole del codice in base al tipo;

**Auto completamento**:

Ti permette di auto completare le parole (keywords, variabili);

**Debugger**:

Strumento che ti permette di debuggare (individuare problemi nel codice e risolverli) il codice con facilità;

**Estensioni**:

Ti permettono di estendere le funzionalità della IDE;

**Terminale**:

Ha un terminale integrato;

**Linea dei numeri**:

Ogni riga ha un numero, utile per vedere dove ci sono gli errori;

**Linter**:

Ti permette di vedere gli errori nel text editor;

**Compilatore**:

Ha un compilatore integrato;

**Intellisense**:

L'insieme di: Syntax highlighting, auto completamento, refactor  e capisce il contesto del codice;

**Refactor**:

è lo strumento che ti permette di semplificare il refactoring (apportare modifiche al codice senza cambiare il comportamento);

**Formatter**:

è lo strumento che ti permette di formattare il codice;

### Quali IDE ci sono?

- Visual Studio;
- VSCode (non è proprio una IDE di definizione);
- Intellj;
- Tutte le IDE di jetbrains;
- Android Studio;
- XCode;
- NVIM o VIM con i plugins;

## Cosa è un progetto

Un progetto è una cartella (o anche soluzione) che contiene uno o più programmi; <br>
I progetti (anche i programmi) possono essere multi linguaggio;

### Quali strumenti vengono utilizzati per i progetti

- Formatter;
- Linter;
- Altri strumenti in base al linguaggio:
  - CMake (per C++/C);
  - Make/ninja (Per qualsiasi progetto da buildare);
  - Project managers (Conan, uv, cargo, go, npm/yarn);
- Strumento di versionamento del codice:
  - git (più famoso e de facto standard);
  - mercurial;
- Compilatore se il linguaggio non è interpretato;

**Strumento di versionamento del codice**:

è uno strumento che ti permette di versionare il codice;<br>
Di creare snapshot del codice tramite commit;

Il codice si trova dentro dei repository (o raccolta/archivio)<br>
Questi repo vengono caricati (hostati) su piattaforme come github;
