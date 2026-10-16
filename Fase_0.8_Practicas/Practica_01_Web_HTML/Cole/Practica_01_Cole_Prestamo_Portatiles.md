## 🏫 Fase 0.8 · Práctica 01 · Cole: préstamo de portátiles

### Una bóveda nueva, una página nueva y un repositorio nuevo, desde cero

> **[Módulo: SOR — Sistemas Operativos en Red · 2.º SMR]**  
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)  
> **📍 Dónde se hace:** en el centro.  
> **🧭 Índice:** [Práctica 01](../00_Indice_Practica_01_Web_HTML.md) · [Fase 0.8](../../../Fase_0.8_Practicas.md)  
> **📖 Si necesitas repasar:** [estructura de la bitácora](../../../Fase_0.1.b_El_Sistema_de_Apuntes.md) · [primera conexión GitHub](../../../Fase_0.3_Repo_Apuntes_y_Primera_Entrada.md).

---

> [!abstract] 🎯 Tu misión de hoy
> Crear **desde cero** una bóveda llamada `Boveda_HTML_Centro`. Dentro crearás un proyecto HTML y **su propio repositorio Git**. Crearás **otro repositorio vacío en GitHub**, lo conectarás por SSH y guardarás tres versiones con sentido: página inicial, cambio del estado de un portátil y ampliación con normas, contacto e imagen. Después visitarás la primera entrega y regresarás a la actual. El HTML y los cambios son los mismos en Cole y Casa; repetirás el proceso en un repositorio independiente. Grabarás **un vídeo de pantalla en el centro**.

> [!danger] 🛑 Este proyecto empieza de cero
> **No abras ni continúes** una bóveda o un repositorio anteriores. El proyecto del centro usa la página de **préstamo de portátiles**, la bóveda `Boveda_HTML_Centro` y GitHub `sor-web-prestamo-portatiles-cole`. Todo se crea de nuevo. En este proyecto, `git init` y `git remote add origin` se hacen una vez; `git add`, `git commit` y `git push` se repiten al guardar cambios.

### 📍 Tu mapa de carpetas

```text
Boveda_HTML_Centro/                   ← la abres en Obsidian; aquí NO haces git init
├── .obsidian/                       ← configuración de Obsidian
├── 00_Grabaciones/                  ← guarda aquí el vídeo; queda fuera de Git
└── 01_Proyecto/                     ← SOLO aquí haces git init
    ├── .gitignore
    ├── 00_Bitacora/
    │   └── b0-p01-cole-prestamo-portatiles.md
    └── web/
        ├── index.html
        ├── normas.html              ← aparece en la tercera versión
        ├── contacto.html            ← aparece en la tercera versión
        ├── imagenes/portatil.png     ← aparece en la tercera versión
        └── videos/                  ← dos clips locales ignorados por Git
```

> [!important] 📹 Una grabación completa de pantalla
> **Antes de grabar:** ten preparada una captura PNG propia sin datos personales y dos clips MP4 propios para H7. Lee esta guía entera, abre OBS y prepara un editor de texto, Obsidian, Git Bash y GitHub. La comprobación inicial de Git, identidad y SSH se realiza en H0, antes de crear el proyecto.  
> **Empieza a grabar antes de crear la bóveda.** Muestra tu perfil de GitHub y cada etapa en pantalla. **En el centro no debes narrar:** deja cada comando y resultado visible para poder leerlo. Mantén la grabación hasta comprobar el resultado en GitHub. No muestres claves privadas ni contraseñas.  
> **Título del vídeo:** `B0.P01 · Cole · Préstamo de portátiles`. **Visibilidad:** No listado. **Playlist:** `B0.P01 · Cole · Préstamo de portátiles con Git y GitHub` (igual que la tarea de Teams).

---

## 0 · EL ENCARGO Y POR QUÉ NECESITAS VERSIONARLO

> [!abstract] Una web que una empresa necesita mantener
> Trabajas en el soporte informático de una empresa que presta portátiles a su personal. Te encargan una web interna: primero mostrará la disponibilidad; después habrá que actualizar el estado de un equipo y publicar las normas y el contacto de soporte. El responsable necesita saber qué se entregó en cada momento y recuperar una versión que funcionaba si una modificación sale mal.
>
> La web es deliberadamente pequeña, pero el trabajo es real: recibir una petición, modificar archivos, comprobar el resultado y dejar una entrega identificable. No necesitas un proyecto grande para necesitar historial.

> [!important] Los archivos evolucionan; conservar solo la última copia no basta
> En un proyecto que cambia y en el que participan varias personas necesitas control de versiones: saber qué cambió, quién lo guardó y por qué; comparar entregas y recuperar estados anteriores. Git permite hacerlo y trabajar en ramas para desarrollar cambios separados. Aquí practicarás el ciclo básico y la recuperación; la creación e integración de ramas y el trabajo simultáneo entre personas se practicarán después.
>
> **Git** conserva el historial en tu equipo. **GitHub** aloja un remoto para compartirlo y colaborar. Hacer `commit` no sube nada; hacer `push` publica tus commits en ese remoto. Tener un remoto tampoco evita por sí solo los conflictos entre cambios.

| Concepto                     | Para qué lo usas aquí                                                                                                                                     |
| :--------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Bóveda                       | Carpeta que abres con Obsidian para organizar este proyecto y su bitácora.                                                                                |
| Repositorio                  | Carpeta cuyo historial controla Git; aquí será `01_Proyecto`.                                                                                             |
| `git status`                 | Distinguir archivos nuevos, cambios sin preparar y cambios preparados.                                                                                    |
| Índice o área de preparación | Selección exacta del contenido que entrará en el siguiente commit.                                                                                        |
| `git add ruta`               | Preparar el contenido actual de un archivo concreto. Si vuelves a editarlo, tendrás que preparar también ese nuevo cambio.                                |
| `git diff`                   | Comparar el trabajo con el índice. Antes de preparar cambios, si el índice coincide con el último commit, muestra las diferencias respecto a esa versión. |
| `git diff --cached`          | Revisar lo que ya has preparado para el siguiente commit.                                                                                                 |
| Commit                       | Versión local identificada por un código y un mensaje que explica el cambio.                                                                              |
| Remoto `origin`              | Dirección del repositorio de GitHub de este proyecto.                                                                                                     |
| `.gitignore`                 | Reglas para excluir archivos que todavía no están bajo seguimiento. No borra ni retira archivos ya versionados.                                           |

> [!warning] Dos prácticas independientes, no dos personas colaborando
> En este recorrido crearás tu propia bóveda y tu propio repositorio desde cero. La otra guía repite la teoría y el método para que puedas practicarlos de nuevo, sin depender de ella. Esta repetición no simula colaboración entre compañeros: demuestra que sabes iniciar y mantener un proyecto por tu cuenta.

---

## 1 · PREPARA EL PROYECTO MIENTRAS GRABAS

> [!example] Paso H0 · Comprueba el equipo antes de crear el proyecto
> Con la grabación iniciada, abre Git Bash en tu carpeta personal, **antes de H1**. Ejecuta de uno en uno:
>
> **Objetivo del bloque:** comprobar que Git está disponible, que la identidad de los commits es la tuya y que existen las claves y funciona la autenticación SSH, antes de crear el proyecto.
>
> ```bash
> git --version
> git config --global user.name
> git config --global user.email
> ls -l ~/.ssh/id_ed25519 ~/.ssh/id_ed25519.pub
> ssh -T git@github.com
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Muestra la versión de Git instalada; no instala ni actualiza nada. |
> | 2 | Muestra el nombre global que Git usará como autor; debe ser el tuyo. |
> | 3 | Muestra el correo global del autor de los commits; debe ser el tuyo. |
> | 4 | Comprueba que existen los archivos de clave privada y pública; no muestra su contenido. |
> | 5 | Prueba la autenticación con GitHub. El saludo debe identificar tu usuario; no abre una shell ni sube archivos. |
>
> **Resultado esperado:** Git muestra su versión, nombre y correo son los tuyos, existen ambos archivos de claves y SSH saluda a tu usuario. No muestres la clave privada. GitHub puede devolver código 1 aunque la autenticación sea correcta porque no ofrece una shell: comprueba el mensaje.
>
> **Si falta algo o la identidad no es la tuya, detente aquí**, repasa Fase 0.2.1 (Git e identidad) y Fase 0.2.2 (SSH) y repite H0. No pases a H1 hasta completar estas comprobaciones. La clave privada permanece en este equipo y la pública ya debe estar registrada en GitHub: no generes otra pareja por empezar un proyecto nuevo.

> [!example] Paso H1 · Crea la bóveda y las carpetas
> 1. En Obsidian, crea una bóveda **nueva** llamada `Boveda_HTML_Centro`, en una ubicación local fuera de OneDrive.
> 2. Crea las carpetas del mapa: `00_Grabaciones`, `01_Proyecto`, `01_Proyecto/00_Bitacora` y `01_Proyecto/web`.
> 3. Las páginas de contacto y normas, la imagen y los clips se incorporan en H7; no los crees todavía.
> 4. Enseña el árbol en pantalla. El vídeo queda **fuera** de `01_Proyecto`.

> [!example] Paso H2 · Crea los ficheros iniciales
> En `00_Bitacora/` crea `b0-p01-cole-prestamo-portatiles.md` con el encabezado y **los siete apartados de la Fase 0.1.b**. Escribe tu nombre y deja `Vídeo: pendiente` en `🔗 Enlaces`; lo completarás al subir la grabación.
>
> En `01_Proyecto/.gitignore`, usando un editor de texto, escribe:
>
> ```gitignore
> *.mp4
> *.mkv
> *.mov
> .DS_Store
> Thumbs.db
> ```
>
> **Por qué creamos `.gitignore`:** indica a Git que ignore vídeos si alguno acaba por error dentro de `01_Proyecto`. `*.mp4` significa cualquier fichero terminado en .mp4. El vídeo está fuera de Git, en `00_Grabaciones`; esto añade una protección. El propio `.gitignore` sí se guarda en Git.
>
> Usa el editor de texto para los ficheros HTML. Comprueba en el gestor de archivos que se llaman `.html`, **sin `.txt` añadido**. Obsidian organiza la bóveda y la bitácora Markdown; el navegador muestra el HTML.

> [!example] Paso H2b · Escribe y abre la primera página
> En `01_Proyecto/web/index.html`, escribe esta **primera versión**:
>
> ```html
> <!doctype html>
> <html lang="es">
> <head>
>   <meta charset="utf-8">
>   <title>Préstamo de portátiles</title>
> </head>
> <body>
>   <h1>Préstamo de portátiles</h1>
>   <p>Equipo 01: disponible.</p>
> </body>
> </html>
> ```
>
> Al guardarla, ábrela en el navegador y enseña **«Equipo 01: disponible.»**. Todavía no existe `normas.html`: aparecerá en una versión posterior.

---

## 2 · CREA GIT Y LA CONEXIÓN CON GITHUB

> [!example] Paso H3 · Comprueba la ruta y haz `git init`
> Abre Git Bash **dentro de `Boveda_HTML_Centro/01_Proyecto`**. No abras la terminal en la raíz de la bóveda. Ejecuta, de uno en uno:
>
> **Objetivo del bloque:** comprobar dónde estás antes de inicializar Git; este comando no cambia nada.
>
> ```bash
> pwd
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Muestra la carpeta actual. Contrasta su ruta con la indicada en este paso antes de seguir. |
>
> **Comprueba ahora:** la ruta debe terminar en `Boveda_HTML_Centro/01_Proyecto`. Si es otra, cambia a la carpeta correcta y vuelve al bloque de comprobación anterior. **No ejecutes `git init` hasta estar en esa ruta.** Una vez comprobada, continúa:
>
> **Objetivo del bloque:** inicializar el repositorio en la ruta ya comprobada, nombrar la rama y consultar su estado inicial.
>
> ```bash
> git init
> git branch -M main
> git status
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Crea el repositorio local en la carpeta que acabas de comprobar. |
> | 2 | Establece main como nombre de la rama actual. |
> | 3 | Muestra la rama main, sin commits todavía, y los archivos iniciales sin seguimiento. |
>
> **Resultado esperado:** rama `main`, todavía sin commits y con los archivos iniciales sin seguimiento.

> [!example] Paso H4 · Crea un repositorio vacío en GitHub
> En tu propia cuenta de GitHub crea `sor-web-prestamo-portatiles-cole`. Déjalo **vacío**: sin README, sin `.gitignore` y sin licencia generados por GitHub. Elige la visibilidad indicada en Teams. Si es privado, da acceso al profesor con la cuenta indicada allí.
>
> En la pantalla del nuevo repositorio elige **SSH** y copia **su** dirección. Debe tener esta forma: `git@github.com:TU-USUARIO/sor-web-prestamo-portatiles-cole.git`. Sustituye `TU-USUARIO` por tu usuario real, no copies el texto literalmente.
>
> En la terminal de **este proyecto**, ejecuta:
>
> **Objetivo del bloque:** guardar la dirección SSH del repositorio de GitHub y comprobarla; todavía no subirás archivos.
>
> ```bash
> git remote add origin git@github.com:TU-USUARIO/sor-web-prestamo-portatiles-cole.git
> git remote -v
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Registra origin con la dirección SSH de tu repositorio vacío; todavía no envía archivos. |
> | 2 | Muestra las direcciones de lectura y envío de los remotos; origin debe ser el de este proyecto. |
>
> **Comprueba antes del primer push:** `origin` debe terminar en `sor-web-prestamo-portatiles-cole.git`. Si aparece otro repositorio, detente y corrige el remoto antes de continuar.

---

## 3 · GUARDA TRES VERSIONES DE LA MISMA WEB

> [!info] Qué vas a mirar en Git
> `git status` indica si un fichero está sin seguimiento, modificado o preparado para el siguiente commit. `git diff -- web/index.html` compara ese HTML con su versión preparada en el índice. **En este paso, antes de `git add` y sin cambios preparados, el índice coincide con el último commit**: `-` marca la frase anterior y `+` la nueva. El `--` separa el comando del nombre del fichero. Un fichero nuevo sin seguimiento aparece en `git status`, pero aún no aparece en ese `git diff`. Si `git diff` o `git log` abre un visor, pulsa **`q`** para salir.

> [!example] Paso H5 · Versión 1: página inicial
> **Situación:** el portátil está disponible y la página ya se abre en el navegador. Vamos a guardar ese punto de partida en Git y subirlo a GitHub. Desde `01_Proyecto`, ejecuta uno a uno:
>
> **Objetivo del bloque:** revisar los archivos iniciales, prepararlos, guardar la primera versión y subirla a GitHub.
>
> ```bash
> git status
> git add .
> git status
> git commit -m "Crear pagina inicial de prestamos"
> git push -u origin main
> git status
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Muestra gitignore, bitácora y portada sin seguimiento; Git puede agrupar los archivos nuevos por carpeta. |
> | 2 | Prepara todos los archivos no ignorados que hay bajo esta carpeta: en esta primera entrega, gitignore, bitácora y portada. |
> | 3 | Muestra esos archivos preparados para crear el primer commit. |
> | 4 | Guarda localmente una versión con los cambios preparados y el mensaje indicado. |
> | 5 | Sube main por primera vez a origin y configura su seguimiento para las siguientes subidas. |
> | 6 | Comprueba que ya no quedan cambios pendientes y que la rama tiene seguimiento de origin/main. |
>
> **Resultado esperado:** primera versión guardada y subida; estado limpio. En GitHub, abre `web/index.html` y comprueba «disponible».


> [!example] Paso H6 · Versión 2: reserva para mantenimiento
> **Situación:** te comunican que el portátil 01 ya no se puede prestar. Vas a modificar **un fichero que Git ya conoce** y a conservar esa decisión como una versión distinta. En `web/index.html`, cambia **solo** `Equipo 01: disponible.` por `Equipo 01: reservado para mantenimiento.`. Guarda y recarga el navegador.
>
> **Objetivo del bloque:** revisar el cambio de disponibilidad de la portada, prepararlo, guardarlo y subirlo como segunda entrega.
>
> ```bash
> git status
> git diff -- web/index.html
> git add web/index.html
> git status
> git commit -m "Reservar equipo 01 para mantenimiento"
> git push
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Muestra la portada como modificada y aún sin preparar. |
> | 2 | Compara la portada del disco con el índice: antes de prepararla verás la frase anterior con - y la nueva con +. No compara dos archivos diferentes. |
> | 3 | Prepara únicamente el contenido actual del archivo indicado para el próximo commit; no sube nada. |
> | 4 | Muestra la modificación de la portada preparada para el segundo commit. |
> | 5 | Guarda localmente una versión con los cambios preparados y el mensaje indicado. |
> | 6 | Envía los commits pendientes al remoto ya configurado. Comprueba que termina sin errores. |
>
> **Resultado esperado:** antes de preparar, el diff muestra la sustitución de «disponible» por «reservado para mantenimiento». Después de subir, comprueba esa frase en GitHub. No vuelvas a inicializar el repositorio ni a registrar el remoto.


> [!example] Paso H7 · A · Construye y prueba la ampliación
> **Petición de la empresa:** publicar normas de préstamo y una vía de contacto con soporte. La portada deberá enlazar a las dos páginas. Además, recibes una imagen para la web y dos clips de vídeo para revisión interna; los clips se conservarán localmente y no se subirán por su volumen.
>
> Dentro de `web/`, crea `imagenes/` y `videos/`. Guarda en `imagenes/` una captura propia sin datos personales con el nombre `portatil.png` (formato PNG). Copia en `videos/` dos clips propios reales y renómbralos `revision-01.mp4` y `revision-02.mp4`. No basta con cambiar la extensión de otro tipo de archivo. No copies el vídeo de entrega mientras OBS lo está grabando.
>
> Crea `web/normas.html`:
>
> ```html
> <!doctype html>
> <html lang="es">
> <head><meta charset="utf-8"><title>Normas de préstamo</title></head>
> <body>
>   <h1>Normas de préstamo</h1>
>   <p>Devuelve el portátil al finalizar la jornada.</p>
>   <p><a href="index.html">Volver a la portada</a></p>
> </body>
> </html>
> ```
>
> Crea `web/contacto.html`:
>
> ```html
> <!doctype html>
> <html lang="es">
> <head><meta charset="utf-8"><title>Contacto de soporte</title></head>
> <body>
>   <h1>Contacto de soporte</h1>
>   <p>Solicita ayuda al departamento de informática.</p>
>   <p><a href="index.html">Volver a la portada</a></p>
> </body>
> </html>
> ```
>
> En `web/index.html`, antes de `</body>`, añade:
>
> ```html
> <img src="imagenes/portatil.png" alt="Portátil de préstamo" width="320">
> <p><a href="normas.html">Leer las normas de préstamo</a></p>
> <p><a href="contacto.html">Contactar con soporte</a></p>
> ```
>
> Guarda y abre la portada en el navegador. Comprueba que la imagen carga, que ambos enlaces abren su página y que puedes volver desde cada una. Las tres páginas deben funcionar **antes de guardar la entrega en Git**.
>
> [!info] Dónde ejecutar H7
> Todos los bloques de terminal de H7 se ejecutan desde `01_Proyecto`, igual que H5 y H6. Ejecuta un bloque, lee su salida y comprueba el resultado antes de pasar al siguiente.

> [!example] H7 · B · Revisa los archivos antes de prepararlos
> **Qué vas a hacer:** vas a identificar los archivos nuevos y modificados, y revisar el cambio de la portada. Estas consultas no modifican archivos ni preparan nada para el commit.
>
> ```bash
> git status --short --untracked-files=all
> git diff -- web/index.html
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Muestra el estado abreviado y enumera cada archivo sin seguimiento por su ruta completa, en lugar de agruparlos por carpetas. `--short` abrevia la salida; `--untracked-files=all` despliega los nuevos. |
> | 2 | Compara la portada guardada en disco con su versión en el índice. Como todavía no has preparado esta entrega, ves el cambio respecto al último commit: la imagen y los enlaces añadidos. No compara dos archivos diferentes ni muestra el contenido de los archivos nuevos sin seguimiento. |
>
> **Comprueba antes de continuar:** deben aparecer la portada modificada y tres archivos nuevos: normas, contacto e imagen. En el diff, `+` señala líneas añadidas y `-` líneas retiradas. Si aparece un visor, sal con la tecla `q`.

> [!info] Cómo leer el estado abreviado
> En la tabla siguiente, `[ ]` representa **un espacio**, no caracteres que tengas que escribir. Así puedes distinguir las dos columnas también en el PDF. El estado tiene dos columnas antes de la ruta: la izquierda muestra lo preparado; la derecha, los cambios del disco que aún no has preparado.
>
> | Marca | Qué significa aquí |
> | :--- | :--- |
> | `??` | Archivo nuevo que Git aún no sigue. |
> | `A[ ]` | Archivo nuevo preparado; la segunda columna es un espacio. |
> | `[ ]M` | Archivo ya seguido, modificado pero sin preparar. |
> | `M[ ]` | Modificación preparada; la segunda columna es un espacio. |
>
> En esta entrega esperas `[ ]M web/index.html` y `??` delante de cada página nueva y de la imagen. Los vídeos no deben aparecer.

> [!example] H7 · C · Comprueba por qué los vídeos quedan fuera
> **Qué vas a hacer:** vas a consultar qué regla de `.gitignore` excluye cada clip. El comando no activa la exclusión: las reglas escritas en H2 ya la aplican. Tampoco borra los vídeos.
>
> ```bash
> git check-ignore -v web/videos/revision-01.mp4 web/videos/revision-02.mp4
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Indica, para cada ruta, el archivo de reglas, su número de línea y el patrón que la ignora. `-v` pide esos detalles. |
>
> **Comprueba antes de continuar:** deben salir los dos clips asociados a `*.mp4`. Comprueba en el gestor de archivos que ambos siguen en el disco. Si falta alguno o no queda ignorado, detente antes de preparar archivos.

> [!example] H7 · D · Prepara la página de normas
> **Qué vas a hacer:** vas a seleccionar solo la página de normas para la entrega y comprobar el resultado. Los archivos que aún no hayas seleccionado siguen esperando.
>
> ```bash
> git add web/normas.html
> git status --short --untracked-files=all
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Prepara el contenido actual de `web/normas.html` para el próximo commit. No guarda todavía una versión ni sube nada. |
> | 2 | Muestra de nuevo qué está preparado y qué sigue sin preparar. Observa el archivo recién seleccionado. |
>
> **Comprueba antes de continuar:** `web/normas.html` debe tener `A[ ]`, porque es un archivo nuevo preparado.

> [!example] H7 · E · Prepara la página de contacto
> **Qué vas a hacer:** vas a seleccionar solo la página de contacto para la entrega y comprobar el resultado. Los archivos que aún no hayas seleccionado siguen esperando.
>
> ```bash
> git add web/contacto.html
> git status --short --untracked-files=all
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Prepara el contenido actual de `web/contacto.html` para el próximo commit. No guarda todavía una versión ni sube nada. |
> | 2 | Muestra de nuevo qué está preparado y qué sigue sin preparar. Observa el archivo recién seleccionado. |
>
> **Comprueba antes de continuar:** `web/contacto.html` debe tener `A[ ]`, porque es un archivo nuevo preparado.

> [!example] H7 · F · Prepara la imagen
> **Qué vas a hacer:** vas a seleccionar solo la imagen para la entrega y comprobar el resultado. Los archivos que aún no hayas seleccionado siguen esperando.
>
> ```bash
> git add web/imagenes/portatil.png
> git status --short --untracked-files=all
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Prepara el contenido actual de `web/imagenes/portatil.png` para el próximo commit. No guarda todavía una versión ni sube nada. |
> | 2 | Muestra de nuevo qué está preparado y qué sigue sin preparar. Observa el archivo recién seleccionado. |
>
> **Comprueba antes de continuar:** `web/imagenes/portatil.png` debe tener `A[ ]`, porque es un archivo nuevo preparado.

> [!example] H7 · G · Prepara la portada modificada
> **Qué vas a hacer:** vas a seleccionar solo la portada modificada para la entrega y comprobar el resultado. Los archivos que aún no hayas seleccionado siguen esperando.
>
> ```bash
> git add web/index.html
> git status --short --untracked-files=all
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Prepara el contenido actual de `web/index.html` para el próximo commit. No guarda todavía una versión ni sube nada. |
> | 2 | Muestra de nuevo qué está preparado y qué sigue sin preparar. Observa el archivo recién seleccionado. |
>
> **Comprueba antes de continuar:** `web/index.html` debe tener `M[ ]`, porque es una modificación de un archivo conocido.

> [!example] H7 · H · Revisa la selección completa
> **Qué vas a hacer:** vas a comprobar qué entrará en la entrega antes de guardarla. Preparar cuatro archivos por separado no obliga a crear cuatro commits: forman una ampliación relacionada.
>
> ```bash
> git diff --cached --stat
> git status
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Resume los cambios preparados en el índice: nombres y estadísticas. `--cached` selecciona lo preparado; `--stat` pide un resumen, no todas las líneas. |
> | 2 | Muestra el estado completo, con los archivos preparados para el commit. |
>
> **Comprueba antes de continuar:** deben estar preparados exactamente cuatro archivos: portada, normas, contacto e imagen. No debe haber vídeos preparados. La carpeta de vídeos no se subirá si solo contiene archivos ignorados: Git versiona archivos, no carpetas vacías.

> [!example] H7 · I · Guarda y sube la ampliación
> **Qué vas a hacer:** vas a guardar esta entrega como la tercera versión de la web y publicarla en el mismo remoto.
>
> ```bash
> git commit -m "Anadir normas contacto e imagen de prestamos"
> git push
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Crea un commit local con los cuatro archivos preparados y un mensaje que identifica la entrega. |
> | 2 | Envía los commits pendientes a la rama remota configurada en la primera subida. |
>
> **Comprueba antes de continuar:** ambas órdenes deben terminar sin errores. Si alguna falla, no des por subida la entrega.

> [!example] H7 · J · Comprueba la entrega terminada
> **Qué vas a hacer:** vas a comprobar el historial y que no quedan cambios pendientes en los archivos del proyecto.
>
> ```bash
> git log --oneline
> git status
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Enumera los commits con código abreviado y mensaje, del más reciente al más antiguo. Sal con `q` si se abre un visor. |
> | 2 | Comprueba que estás en `main` y que el árbol de trabajo está limpio. Los vídeos ignorados pueden seguir en el disco sin aparecer aquí. |
>
> **Comprueba antes de continuar:** debe haber tres commits de la web. En GitHub comprueba las tres páginas y la imagen, y la ausencia de clips. Estar limpio no demuestra por sí solo que se haya hecho push: comprueba también el remoto.

> [!example] Paso H7b · A · Localiza la primera entrega
> **Qué vas a hacer:** el responsable quiere comparar la entrega actual con la primera. Primero vas a comprobar que no dejas trabajo pendiente.
>
> ```bash
> git status
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Consulta la rama y los cambios pendientes sin alterar el repositorio. |
>
> **Comprueba antes de continuar:** debes estar en `main` y sin cambios pendientes. Si no, detente y termina de guardar tu trabajo antes de continuar.

> [!example] H7b · B · Lee el historial
> **Qué vas a hacer:** vas a obtener el código real del primer commit para poder consultarlo; no uses un código inventado ni copies el de un compañero.
>
> ```bash
> git log --oneline
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Muestra el código abreviado y el mensaje de cada commit. Busca «Crear pagina inicial de prestamos» y copia su código. Sal del visor con `q` si se abre. |
>
> **Comprueba antes de continuar:** anota el código del commit de la página inicial. En el bloque siguiente, sustituye `CODIGO_PRIMER_COMMIT` por ese código ANTES de ejecutarlo.

> [!example] H7b · C · Abre la versión antigua
> **Qué vas a hacer:** vas a situarte temporalmente en ese commit para inspeccionarlo. No borres ni reescribas el historial y no edites archivos durante la consulta.
>
> ```bash
> git switch --detach CODIGO_PRIMER_COMMIT
> git status
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Cambia los archivos seguidos a la versión del commit indicado. `--detach` permite consultar ese commit sin situarte en una rama. |
> | 2 | Muestra el estado en ese punto: es normal ver `HEAD detached` o su traducción. |
>
> **Comprueba antes de continuar:** abre o recarga `web/index.html`: debe mostrar «Equipo 01: disponible.», sin imagen ni enlaces. Las páginas nuevas y la imagen desaparecen de esta versión; los clips ignorados pueden permanecer porque no forman parte del historial. No hagas commits ni push aquí.

> [!example] H7b · D · Regresa a la entrega actual
> **Qué vas a hacer:** vas a regresar a `main` y comprobar que recuperas la web ampliada y todo su historial. Esta consulta no crea una entrega nueva y no requiere push.
>
> ```bash
> git switch main
> git status
> git log --oneline
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Vuelve a la rama `main`, recuperando sus archivos seguidos. |
> | 2 | Comprueba que estás en `main` y sin cambios pendientes. |
> | 3 | Muestra de nuevo los tres commits de la web; ninguno se ha borrado. |
>
> **Comprueba antes de continuar:** recarga la portada: deben volver el estado de mantenimiento, la imagen y los enlaces. Comprueba ambas páginas. Sal del visor con `q` si aparece.

---

## 4 · CIERRA EL VÍDEO Y ENTREGA TU TRABAJO

> [!example] Paso H8 · Termina la grabación y completa la bitácora
> Antes de detener OBS, vas a dejar visibles el historial, el remoto de este proyecto y el estado final. Ejecuta este bloque y enseña el resultado junto a GitHub:
>
> **Objetivo del bloque:** mostrar el historial, la dirección remota y el estado final antes de cerrar la grabación.
>
> ```bash
> git log --oneline
> git remote -v
> git status
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Muestra los códigos abreviados y mensajes de los commits. Si se abre un visor, sal con q antes de la siguiente orden. |
> | 2 | Muestra las direcciones de lectura y envío de los remotos; origin debe ser el de este proyecto. |
> | 3 | Muestra qué está sin seguimiento, modificado o preparado en este punto; después de un commit sin otros cambios, debe quedar limpio. |
>
> Detén OBS. Guarda el vídeo en `00_Grabaciones` y súbelo como **No listado** con el título y la playlist indicados al principio.
>
> En la **descripción del vídeo** escribe los minutos **reales** en que empieza cada etapa; cambia los marcadores por tiempos `mm:ss`:
>
> ```text
> 00:00 Presentación e identidad
> TU_TIEMPO Comprobación inicial de Git, identidad y SSH
> TU_TIEMPO Bóveda y carpetas
> TU_TIEMPO Primera página en el navegador
> TU_TIEMPO git init y git status
> TU_TIEMPO Repositorio GitHub y origin
> TU_TIEMPO Primera versión y primer push
> TU_TIEMPO Cambio del estado del equipo
> TU_TIEMPO Páginas nuevas, imagen y vídeos ignorados
> TU_TIEMPO Preparación individual y nueva entrega
> TU_TIEMPO Primera versión y regreso a main
> TU_TIEMPO Historial y comprobación final
> ```
>
> Comprueba que las marcas llevan a las etapas correctas. Completa **tu bitácora** con los siete apartados de la Fase 0.1.b; en `🔗 Enlaces` pega el enlace de **este vídeo** y el de la playlist. Responde las preguntas del apartado 5 y anota los errores reales, si los hubo.
>
> **Ahora ya existe la URL de YouTube.** Completar la bitácora es un cierre de documentación posterior al vídeo, como en la Fase 0.3; **no es una cuarta versión de la web**. Desde `Boveda_HTML_Centro/01_Proyecto`, sube esa nota a GitHub:
>
> [!example] H8 · A · Revisa antes de guardar la bitácora
> **Qué vas a hacer:** vas a comprobar que sigues dentro del proyecto correcto y que el cambio pendiente es la nota con el enlace del vídeo.
>
> ```bash
> pwd
> git remote -v
> git status
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Muestra la carpeta actual. |
> | 2 | Muestra las direcciones de origin. |
> | 3 | Identifica los cambios pendientes; debe aparecer la bitácora modificada. |
>
> **Comprueba antes de continuar:** la ruta debe terminar en `Boveda_HTML_Centro/01_Proyecto`, origin debe corresponder a `sor-web-prestamo-portatiles-cole` y la nota debe tener el enlace real. Si no coincide, detente antes del bloque siguiente.

> [!example] H8 · B · Guarda y sube la documentación
> **Qué vas a hacer:** vas a guardar únicamente la bitácora completada y enviarla al remoto de este proyecto.
>
> ```bash
> git add 00_Bitacora/b0-p01-cole-prestamo-portatiles.md
> git commit -m "Completar bitacora y enlace del video del centro"
> git push
> git status
> ```
>
> **Qué significa cada línea:**
>
> | Línea | Significado |
> | :--- | :--- |
> | 1 | Prepara únicamente la nota de esta práctica. |
> | 2 | Crea el cuarto commit: es documental, no una cuarta versión de la web. |
> | 3 | Envía ese commit a GitHub. |
> | 4 | Comprueba que no quedan cambios pendientes. |
>
> **Comprueba antes de continuar:** abre la bitácora en GitHub y comprueba el enlace al vídeo. Este commit es posterior al vídeo y no puede aparecer en esa grabación; el historial final contiene tres commits de web y uno documental.


### 📤 Entrega en Teams

La tarea de **Cole** se llama **`B0.P01 · Cole · Préstamo de portátiles con Git y GitHub`**. La playlist de este proyecto debe llamarse **exactamente igual** y contener **un único vídeo de entrega**, el de Cole. Los dos clips MP4 de prueba de `web/videos/` son recursos locales: no son vídeos de entrega y no van a esta playlist.

Entrega en esta tarea **dos enlaces**:

1. El repositorio GitHub **de Cole**.
2. La playlist **de Cole**, que contiene su vídeo completo con las marcas de tiempo.

Comprueba que ambos enlaces abren, que el vídeo corresponde a este proyecto y pulsa **Entregar**. Si el repositorio es privado, concede acceso al profesor. **No esperes a terminar el otro trabajo ni entregues sus enlaces aquí:** Cole y Casa tienen tareas, playlists, repositorios y calificaciones independientes.

---

## 5 · COMPRUEBA QUE ENTIENDES LO QUE HAS HECHO

> [!help] Preguntas críticas para la bitácora
> 1. ¿Por qué `git init` se hizo en `01_Proyecto` y no en la raíz de la bóveda?
> 2. ¿Qué mostró `git status` antes de `add`, después de `add` y después de `commit`?
> 3. ¿Por qué creaste un repositorio de GitHub propio y lo conectaste con `git remote add origin`?
> 4. ¿Por qué las páginas nuevas aparecen en `git status` pero no en `git diff -- web/index.html`?
> 5. ¿Cómo has comprobado que los vídeos existen pero no se van a subir?
> 6. ¿Qué muestra `git diff --cached --stat` después de preparar los cuatro archivos?
> 7. ¿Qué cambia al visitar el primer commit y qué recuperas al volver a `main`?
> 8. ¿Por qué esta web necesita historial? ¿Qué aportaría GitHub si otro técnico trabajase contigo?
> 9. Si mañana corriges una errata en `normas.html`, ¿qué pasos repites y cuáles no?


> [!bug] Si algo no sale
> | Síntoma | Qué revisar y dónde volver |
> | :--- | :--- |
> | El diff sale vacío | Comprueba que guardaste la portada y si ya preparaste el cambio. Consulta H6 o H7-B para revisar antes de preparar; H7-H para revisar lo preparado. |
> | No hay nada para guardar | Comprueba que editaste el archivo correcto y lo guardaste; vuelve a la comprobación de estado de ese paso. |
> | El remoto origin ya existe | No repitas su alta. Vuelve a la comprobación del remoto en H4. |
> | Un enlace o la imagen falla | Comprueba los nombres, mayúsculas y rutas de H7-A. |
> | Un vídeo aparece entre los cambios | Revisa el patrón y extensión en H2 y la comprobación de H7-C. Si ya estaba seguido, la regla no lo retira: no sigas con la entrega. |
> | Estoy fuera de una rama | Es lo esperado durante H7b-C. No edites; vuelve mediante el bloque H7b-D. |
> | GitHub no muestra la entrega | Comprueba si terminó la subida del paso correspondiente. Estado limpio no demuestra por sí solo que se haya enviado. |
> | El remoto pertenece al otro proyecto | Detente antes de subir. Revisa la ruta y el remoto mediante H8-A. |

> [!success] ✅ Al acabar en el centro
> - [ ] Esta bóveda y este repositorio se han creado desde cero en el centro.
> - [ ] `origin` apunta a `sor-web-prestamo-portatiles-cole`.
> - [ ] El historial muestra tres versiones de la web y el cierre documental posterior.
> - [ ] La imagen y los dos enlaces funcionan, incluida la vuelta a la portada.
> - [ ] Los dos clips existen localmente, están ignorados y no aparecen en GitHub.
> - [ ] He preparado los cuatro archivos de la ampliación individualmente.
> - [ ] He visitado el primer commit y vuelto a `main` sin perder el historial.
> - [ ] El vídeo de pantalla del centro muestra el proceso y tiene timestamps reales.
> - [ ] La bitácora contiene el enlace del vídeo y está subida a **este** repositorio.
> - [ ] La tarea de Cole contiene únicamente su repositorio y su playlist con un vídeo.
