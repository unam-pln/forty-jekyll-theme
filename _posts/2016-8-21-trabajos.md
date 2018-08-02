---
layout: post
title: Trabajos prácticos
description: Libretas a realizar fuera de curso
image: assets/images/parqueecologico.jpg
---

## Trabajos prácticos en PLN

Libretas de jupyter con los trabajos prácticos a realizar por los
participantes en el curso PLN de la MTI/UNaM. Estos trabajos tienen
como objetivo reforzar los temas vistos en el curso de PLN.

Se trato de diseñar 4 trabajos prácticos que cubrieran la mayor parte de los temas vistos
los cuales se aplican a la solución de problemas concretos en PLN. Se espera que los
participantes en el curso adquieran con las libretas a desarrollar la competencias necesarias
para poder aplicar dichas técnicas en sistemas mayores.

Si bien todo el curso (y las libretas están desarrolladas en *python*, muchas
de las herramientas se pueden aplicar en línea de comando (CLI). Por otra parte,
existen otras bibliotecas de PLN para otros lenguajes de programación, cuyas
interfases y notación son similares a esta. En particular, para JAVA
existe [CoreNLP]( http://stanfordnlp.github.io/CoreNLP/) del grupo de investigación
en PLN de Stanford.

### Descargar las libretas para desarrollarlas

Para descargar las libretas es necesario clonar el [proyecto de
github](https://github.com/unam-pln/trabajos-practicos) utilizando
de nuevo el comando

```sh
git clone https://github.com/[TU USERNAME DE GITHUB]/trabajos-practicos.git
```

Yo recomiendo que, tanto las libretas de apoyo, como estas libretas
en lugar de clonarlas simplemente, crees tu propia cuenta de
[github](github.com), y entonces, el lugar de clonarlas, primero
apliques (desde la página de github, ya dado de alta) el botón
**fork** (parte superior izquierda). De esa manera, este será un proyecto tuyo
que podrás modificar y guardar las modificaciones (y utilizarlos como evidencia
de conocimiento de PLN).

Ya habiendo aplicado el comando *fork*, entonces puedes clonar la libreta
desde tu proyecto con algo así como:

```sh
git clone https://github.com/unam-pln/trabajos-practicos.git
```

### Desarrollar las libretas

Las libretas tienen la intención de ser autocontenidas y que, con la ayuda
de las libretas vistas en el curso y un poco de investigación, las puedas
desarrollar sin mayor problema. Intenté hacerlas interesantes, a pesar que
algunas tienen unas partes tediosas que tienen como objetivo que se desarrollen
ciertas intuiciones sobre los métodos bajo estudio.

Cualquier comentario, duda, sugestión, o si encontraste un fallo, no dudes en
mandarme un correo electrónico (julio.waissman@unison.mx). Trataré de solucionar
todas las ducas (mientras no sean solucionar la libreta directamente).

Si estás desarrollando las libretas en tu propio proyecto, y no quieres
estudiar un poco más de *github*, solamente tienes que hacer lo siguiente
en la terminal (dentro de cualquier directorio del proyecto) cada
vez que quieras guardar cambios:

1. Agregar todos los cambios para ser enviados

```sh
git add -A
```

2. Comentar que cambios hiciste

```sh
git commit -m "Comentario sobre los cambios"
```

3. Enviarlos a *github*

```sh
git push -u origin master
```

Si ya sabes *git* esta explicación es innecesaria. Si no sabes, yo te
recomiendo muy encarecidamente que aprendas a utilizarlo. Este [curso
de
Udacity](https://www.udacity.com/course/how-to-use-git-and-github--ud775)
es un buen inicio.

### 3. Envio de libretas a revisión

Los trabajos prácticos los vamos a utilizar como referencia para la evaluación del
curso, por lo que es necesario que yo tenga una retroalimentación del trabajo
que realizaron.

Para simplificar el proceso. Solamente generen un archivo comprimido con las
4 libretas (archivos *.ipynb) ya resueltas (por favor, no borrar las
salidas de las celdas). El archivo comprimido no va a contener ningun otro
archivo, yo tengo los archivos necesarios y los que faltan se pueden
generar directamente al ejecutar las libretas.

Enviar el archivo comprimido a mi correo electrónico (julio.waissman@unison.mx)
con el título "libretas PLN: Nombre", donde *Nombre* es tu nombre completo.
