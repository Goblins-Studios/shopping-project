### Features
- VueJS
- Vuetify
- Composer

# Simple Framework

**Table of Contents**

[TOCM]

[TOC]

## Guía de estilos de php

Se sigue la convención de php basada en [PSR-12](https://www.php-fig.org/psr/psr-12/ "PSR-12").


## Guía de estilos de los commits

Se sigue la siguiente convención:

1. Un encabezado con el titulo o un resumen del commit, que debe comenzar por un sustantivo, describiendo la razón del commit.

2. Un cuerpo donde se describan los cambios realizados en el commit y su función. termina en punto, pueden comenzar con un sustantivo y pueden ser varios.

3. Un pie con información extra, como por ejemplo el issue que se está resolviendo.

### Forma

```
Short (50 chars or less) summary

More detailed explanatory text. Wrap it to 72 characters. The blank
line separating the summary from the body is critical (unless you omit
the body entirely).

Write your commit message in the imperative: "Fix bug" and not "Fixed
bug" or "Fixes bug." This convention matches up with commit messages
generated by commands like git merge and git revert.

Further paragraphs come after blank lines.

- Bullet points are okay, too.
- Typically a hyphen or asterisk is used for the bullet, followed by a
  single space. Use a hanging indent.

If you use an issue tracker, put references to them at the bottom,
like this:

Resolves: #123
See also: #456, #789
```

### Ejemplos

```
Fix typo in introduction to user guide
```

```
Derezz the master control program

MCP turned out to be evil and had become intent on world domination.
This commit throws Tron's disc into MCP (causing its deresolution)
and turns it back into a chess game.
```

```
Simplify serialize.h's exception handling

Remove the 'state' and 'exceptmask' from serialize.h's stream
implementations, as well as related methods.

As exceptmask always included 'failbit', and setstate was always
called with bits = failbit, all it did was immediately raise an
exception. Get rid of those variables, and replace the setstate
with direct exception throwing (which also removes some dead
code).

As a result, good() is never reached after a failure (there are
only 2 calls, one of which is in tests), and can just be replaced
by !eof().

fail(), clear(n) and exceptions() are just never called. Delete
them.
```

### Véase también

https://gist.github.com/robertpainsi/b632364184e70900af4ab688decf6f53
https://chris.beams.io/posts/git-commit/


## Tecnologías

Clona el proyecto con las instrucciones proporcionadas por git/github.

`git clone https://github.com/Goblins-Studios/simple-framework.git`
`cd simple-framwork`

Simple Framework utiliza NodeJS y Composer para gestionar las tecnologías y dependencias de las bibliotecas utilizadas.

Realiza la instalacion de las dependencia del proyecto y compilar los archivos mediante NodeJS, los cuales se pueden encontrar las intrucciones en la documentación oficial.

`composer install`
`composer dump-autoload`
`npm install`
`npm run dev`

Para utilizar el framework se debe crear un archivo `.env`. Tiene un ejemplo de archivo `.env` llamado `.env.example`
