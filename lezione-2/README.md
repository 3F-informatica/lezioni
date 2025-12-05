<div align=center>

# Lezione 2

</div>

- Version control
- Interfacce utente (GUI, TUI, CLI, Web UI)

## Version control

Serve per versionare il codice<br>
Significa: puoi cambiare il codice senza che lo stato precedente del codice non venga eliminato<br>
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

**Repository**:

Raccolta di codice, che può contenere vari branch commit e tags

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

### Github

Servizio di hosting dei repository di git, è uno strumento molto potente

[https://github.com](https://github.com)

## Interfacce utente

Strumento che ti permette di interfacciarti con il programma<br>
Ci sono 3 tipi:

- GUI (Graphical User Interface)
- TUI (Text user interface)
- CLI (Command Line Interface)
- Web UI

### GUI

È quella più diffusa e che tutti conoscono

### TUI

Vengono usate nel terminale (le più famose sono NVIM, Lazygit, Ranger)<br>
Ci sono 2 tipi di TUI:

- Interattiva
- Statica

**Interattiva**:

Dove l'utente può interagire

**Statica**:

Dove l'utente non può interagire

### CLI

Ti interfacci con il programma tramite flags, sub-commands

**Flags**:

Sono dei parametri booleani che vengono passati al programma

**Sub-commands**:

Sono simili alle flags, sono dei sotto programmi

## Web UI

È un interfaccia web

