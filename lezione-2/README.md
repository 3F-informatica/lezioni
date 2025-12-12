---
title: "**Lezione 2**"
---

Argomenti trattati:
===

<!-- alignment: center -->

<!-- jump_to_middle -->

- Version control
- Interfacce utente (GUI, TUI, CLI, Web UI)

<!-- end_slide -->

Version control
===

Serve per versionare il codice

Significa: puoi cambiare il codice senza che lo stato precedente del codice venga eliminato

Serve anche per collaborare con altre persone

### I sistemi più famosi

- git (de facto standard)
- mercurial

### Features

- Repository
- Commit
- Branch
- Merge
- Tag

<!-- end_slide -->

**Repository**:

Raccolta di codice, che può contenere vari branch, commit e tags

**Commit**:

Snapshot del codice

Esempio con git:
```sh
git commit -m "<messaggio>"
```

**Branch**:

Ramo del codice

Esempio con git:
```sh
git branch [OPZIONI]
```

**Merge**:

Quando si uniscono 2 branch

Esempio con git:
```sh
git merge <nome branch> # Questo fa il merge del branch corrente con quello scelto
```

**Tag**:

Commit speciale, in genere usato per il rilascio delle versioni del programma che si sta sviluppando

Esempio con git:
```sh
git tag -a <versione> -m "<messaggio>"
```

<!-- end_slide -->

Github
===

Servizio di hosting dei repository di git, è uno strumento molto potente

[](https://github.com)

<!-- end_slide -->

Interfacce utente
===

Strumento che ti permette di interfacciarti con il programma

Ci sono 3 tipi:

- GUI (Graphical User Interface)
- TUI (Text user interface)
- CLI (Command Line Interface)
- Web UI

<!-- end_slide -->

### GUI

È quella più diffusa e che tutti conoscono

---

### TUI

Vengono usate nel terminale (le più famose sono NVIM, Lazygit, Ranger)
Ci sono 2 tipi di TUI:

- Interattiva
- Statica

**Interattiva**:

Dove l'utente può interagire

**Statica**:

Dove l'utente non può interagire

---

### CLI

Ti interfacci con il programma tramite flags, sub-commands

**Flags**:

Sono dei parametri booleani che vengono passati al programma

**Sub-commands**:

Sono simili alle flags, sono dei sotto programmi

---

### Web UI

È un interfaccia web

