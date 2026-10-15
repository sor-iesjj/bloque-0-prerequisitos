## 🏠 Fase 0.8 · Práctica 01 · Casa: préstamo de portátiles

### Una bóveda nueva, una página nueva y un repositorio nuevo, desde cero

> **[Módulo: SOR — Sistemas Operativos en Red · 2.º SMR]**  
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)  
> **📍 Dónde se hace:** en casa, con el equipo preparado en la Fase 0.5.1.  
> **🧭 Índice:** [Práctica 01](../00_Indice_Practica_01_Web_HTML.md) · [Fase 0.8](../../../Fase_0.8_Practicas.md)  
> **📖 Si necesitas repasar:** [estructura de la bitácora](../../../Fase_0.1.b_El_Sistema_de_Apuntes.md) · [primera conexión GitHub](../../../Fase_0.3_Repo_Apuntes_y_Primera_Entrada.md).

---

> [!abstract] 🎯 Tu misión de hoy
> Crear **desde cero** una bóveda llamada `Boveda_HTML_Casa`. Dentro crearás un proyecto HTML y **su propio repositorio Git**. Crearás **otro repositorio vacío en GitHub**, lo conectarás por SSH y guardarás tres versiones con sentido: página inicial, cambio del estado de un portátil y nueva página de normas. Grabarás **un vídeo en casa, explicando cada etapa**.

> [!danger] 🛑 Aquí no entra el trabajo del centro
> **No clones, copies, abras ni continúes** la bóveda o el repositorio del centro. El proyecto de casa usa la página de **préstamo de portátiles**, la bóveda `Boveda_HTML_Casa` y GitHub `sor-web-prestamo-portatiles-casa`. Todo se crea de nuevo. Repetirás `git init` y `git remote add origin` **porque este es otro proyecto**; dentro de este proyecto solo se hacen una vez.

### 📍 Tu mapa de carpetas

```text
Boveda_HTML_Casa/                   ← la abres en Obsidian; aquí NO haces git init
├── .obsidian/                       ← configuración de Obsidian
├── 00_Grabaciones/                  ← guarda aquí el vídeo; queda fuera de Git
└── 01_Proyecto/                     ← SOLO aquí haces git init
    ├── .gitignore
    ├── 00_Bitacora/
    │   └── b0-p01-casa-prestamo-portatiles.md
    └── web/
        ├── index.html
        └── normas.html              ← lo crearás después del segundo commit
```

> [!important] 📹 Una grabación completa, con explicación
> **Antes de grabar:** lee esta guía entera, abre OBS y prepara un editor de texto, Obsidian, Git Bash y GitHub. Comprueba que tu clave SSH **ya funciona en este equipo**; si no, vuelve a la Fase 0.5.1.  
> **Empieza a grabar antes de crear la bóveda.** Preséntate, muestra tu perfil de GitHub y explica qué vas a hacer. Mantén la grabación hasta comprobar el resultado final en GitHub. Di en voz alta qué significa cada `git status`, por qué haces cada commit y por qué este `origin` es distinto. No muestres claves privadas ni contraseñas.  
> **Título del vídeo:** `B0.P01 · Casa · Préstamo de portátiles`. **Visibilidad:** No listado. **Playlist:** `B0.P01 · Préstamo de portátiles con Git y GitHub` (igual que la tarea de Teams).

---

## 1 · PREPARA EL PROYECTO MIENTRAS GRABAS

> [!example] Paso H1 · Crea la bóveda y las carpetas
> 1. En Obsidian, crea una bóveda **nueva** llamada `Boveda_HTML_Casa`, en una ubicación local fuera de OneDrive.
> 2. Crea las carpetas del mapa: `00_Grabaciones`, `01_Proyecto`, `01_Proyecto/00_Bitacora` y `01_Proyecto/web`.
> 3. Enseña el árbol en pantalla. Explica por qué el vídeo queda **fuera** de `01_Proyecto`.

> [!example] Paso H2 · Crea los ficheros iniciales
> En `00_Bitacora/` crea `b0-p01-casa-prestamo-portatiles.md` con el encabezado y **los siete apartados de la Fase 0.1.b**. Escribe tu nombre y deja `Vídeo: pendiente` en `🔗 Enlaces`; lo completarás al subir la grabación.
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
> Abre Git Bash **dentro de `Boveda_HTML_Casa/01_Proyecto`**. No abras la terminal en la raíz de la bóveda. Ejecuta, de uno en uno:
>
> ```bash
> pwd
> git init
> git branch -M main
> git status
> ```
>
> **Por qué:** `pwd` muestra la ruta para evitar iniciar Git en la raíz de la bóveda. `git init` crea el repositorio en `01_Proyecto` y `git branch -M main` pone nombre a la rama. **Punto de control:** `pwd` termina en `Boveda_HTML_Casa/01_Proyecto`. `git status` muestra la rama `main`, que aún no hay commits y que los ficheros iniciales están *sin seguimiento*.  Si la ruta es otra, detente antes de seguir.

> [!example] Paso H4 · Crea un repositorio vacío en GitHub
> En tu propia cuenta de GitHub crea `sor-web-prestamo-portatiles-casa`. Déjalo **vacío**: sin README, sin `.gitignore` y sin licencia generados por GitHub. Elige la visibilidad indicada en Teams. Si es privado, da acceso al profesor con la cuenta indicada allí.
>
> En la pantalla del nuevo repositorio elige **SSH** y copia **su** dirección. Debe tener esta forma: `git@github.com:TU-USUARIO/sor-web-prestamo-portatiles-casa.git`. Sustituye `TU-USUARIO` por tu usuario real, no copies el texto literalmente.
>
> En la terminal de **este proyecto**, ejecuta:
>
> ```bash
> git remote add origin git@github.com:TU-USUARIO/sor-web-prestamo-portatiles-casa.git
> git remote -v
> ```
>
> **Por qué:** `git remote add origin` guarda la dirección de GitHub; aún no sube ficheros. `git remote -v` permite comprobarla. **Punto de control:** `origin` termina en `sor-web-prestamo-portatiles-casa.git`. Si aparece otro nombre, **no hagas push**; corrige la dirección antes. `git remote add` se hace una vez en este repositorio.

---

## 3 · GUARDA TRES VERSIONES DE LA MISMA WEB

> [!info] Qué vas a mirar en Git
> `git status` indica si un fichero está sin seguimiento, modificado o preparado para el siguiente commit. `git diff -- web/index.html` muestra qué líneas cambiaron en ese HTML **desde el último commit y antes de hacer `git add`**: `-` marca la frase anterior y `+` la nueva. El `--` separa el comando del nombre del fichero. Un fichero nuevo sin seguimiento aparece en `git status`, pero aún no aparece en ese `git diff`. Si `git diff` o `git log` abre un visor, pulsa **`q`** para salir.

> [!example] Paso H5 · Versión 1: página inicial
> **Situación:** el portátil está disponible y la página ya se abre en el navegador. Vamos a guardar ese punto de partida en Git y subirlo a GitHub. Desde `01_Proyecto`, ejecuta uno a uno:
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
> El primer `status` muestra `.gitignore`, la bitácora y `web/index.html` sin seguimiento. `git add .` prepara **todos los ficheros no ignorados de `01_Proyecto`**; aquí son los del proyecto. El segundo `status` debe mostrarlos preparados. `git commit` guarda la versión 1 **en el equipo**. `git push -u origin main` la sube por primera vez y configura el seguimiento; en las siguientes subidas bastará `git push`. El último `status` debe estar limpio. Recarga GitHub y abre `web/index.html`: debe decir «disponible».

> [!example] Paso H6 · Versión 2: reserva para mantenimiento
> **Situación:** te comunican que el portátil 01 ya no se puede prestar. Vas a modificar **un fichero que Git ya conoce** y a conservar esa decisión como una versión distinta. En `web/index.html`, cambia **solo** `Equipo 01: disponible.` por `Equipo 01: reservado para mantenimiento.`. Guarda y recarga el navegador.
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
> El primer `status` debe mostrar `index.html` modificado. `git diff`, antes de `add`, permite ver exactamente la frase anterior y la nueva. Si sale vacío, comprueba que guardaste el fichero. `git add web/index.html` prepara solo ese HTML; el segundo `status` lo muestra listo. `commit` lo guarda localmente y `push` lo lleva al **mismo repositorio** GitHub. Recarga GitHub y comprueba «reservado». No repitas `git init` ni `git remote add origin`.

> [!example] Paso H7 · Versión 3: una página nueva de normas
> **Situación:** ahora se necesita publicar una norma y permitir llegar a ella desde la portada. Crearás `web/normas.html` y modificarás `web/index.html`. En el fichero nuevo escribe:
>
> ```html
> <!doctype html>
> <html lang="es">
> <head>
>   <meta charset="utf-8">
>   <title>Normas de préstamo</title>
> </head>
> <body>
>   <h1>Normas de préstamo</h1>
>   <p>Devuelve el portátil al finalizar la clase.</p>
> </body>
> </html>
> ```
>
> En `web/index.html`, antes de `</body>`, añade:
>
> ```html
> <p><a href="normas.html">Leer las normas de préstamo</a></p>
> ```
>
> Guarda ambos ficheros. Recarga `index.html` en el navegador y pulsa el enlace: debe abrir las normas. Después ejecuta:
>
> ```bash
> git status
> git diff -- web/index.html
> git add web/index.html web/normas.html
> git status
> git commit -m "Anadir normas y enlace de prestamo"
> git push
> git log --oneline
> git status
> ```
>
> El primer `status` debe mostrar `index.html` **modificado** y `normas.html` **sin seguimiento**: uno ya estaba en Git y el otro acaba de crearse. `git diff` muestra el enlace añadido al HTML conocido; no muestra el fichero nuevo. `git add` prepara **los dos** porque las normas y su enlace forman un único cambio con sentido. El segundo `status` los muestra preparados. `commit` guarda la versión 3 y `push` la sube. `git log --oneline` resume el historial; reconoce las tres versiones por sus mensajes. El `status` final debe estar limpio. Comprueba en GitHub los tres commits y `normas.html`.
>
> **Otra forma de preparar este cambio:** desde `01_Proyecto`, `git add .` añadiría los dos ficheros si **todos** los cambios visibles en `git status` son los que quieres guardar. Aquí se nombran para ver exactamente qué entra en el commit.

---

## 4 · CIERRA EL VÍDEO Y ENTREGA TU TRABAJO

> [!example] Paso H8 · Termina la grabación y completa la bitácora
> Enseña el resultado en GitHub, `git log --oneline`, `git remote -v` y un `git status` limpio. Detén OBS. Guarda el vídeo en `00_Grabaciones` y súbelo como **No listado** con el título y la playlist indicados al principio.
>
> En la **descripción del vídeo** escribe los minutos **reales** en que empieza cada etapa; cambia los marcadores por tiempos `mm:ss`:
>
> ```text
> 00:00 Presentación e identidad
> TU_TIEMPO Bóveda y carpetas
> TU_TIEMPO Primera página en el navegador
> TU_TIEMPO git init y git status
> TU_TIEMPO Repositorio GitHub y origin
> TU_TIEMPO Primera versión y primer push
> TU_TIEMPO Cambio del estado del equipo
> TU_TIEMPO Página nueva de normas
> TU_TIEMPO Historial y comprobación final
> ```
>
> Comprueba que las marcas llevan a las etapas correctas. Completa **tu bitácora** con los siete apartados de la Fase 0.1.b; en `🔗 Enlaces` pega el enlace de **este vídeo** y el de la playlist. Responde las preguntas del apartado 5 y anota los errores reales, si los hubo.
>
> **Ahora ya existe la URL de YouTube.** Completar la bitácora es un cierre de documentación posterior al vídeo, como en la Fase 0.3; **no es una cuarta versión de la web**. Desde `Boveda_HTML_Casa/01_Proyecto`, sube esa nota a GitHub:
>
> ```bash
> pwd
> git remote -v
> git status
> git add 00_Bitacora/b0-p01-casa-prestamo-portatiles.md
> git commit -m "Completar bitacora y enlace del video de casa"
> git push
> git status
> ```
>
> `pwd` comprueba la carpeta y el primer `status` debe mostrar la bitácora modificada. `git add` prepara solo esa nota, `commit` la guarda localmente y `push` la sube. **Este último commit no puede aparecer en el mismo vídeo**, porque la URL se obtuvo después de pararlo. Comprueba en GitHub que el enlace de la bitácora funciona. El historial tendrá tres commits de la web y uno documental.

### 📤 Entrega en Teams

La tarea se llama **`B0.P01 · Préstamo de portátiles con Git y GitHub`**, igual que la playlist. Cuando estén hechos los trabajos de **cole y casa**, pega en esa tarea **tres enlaces**: repositorio GitHub del cole, repositorio GitHub de casa y playlist con los dos vídeos. Comprueba que abren y pulsa **Entregar**. Si los repositorios son privados, el profesor necesita acceso a ambos.

---

## 5 · COMPRUEBA QUE ENTIENDES LO QUE HAS HECHO

> [!help] Preguntas críticas para la bitácora
> 1. ¿Por qué `git init` se hizo en `01_Proyecto` y no en la raíz de la bóveda?
> 2. ¿Qué mostró `git status` antes de `add`, después de `add` y después de `commit`?
> 3. ¿Por qué hubo que crear otro repositorio en GitHub y ejecutar aquí `git remote add origin`?
> 4. ¿Por qué `normas.html` aparecía en `git status` pero no en `git diff -- web/index.html`?
> 5. Si mañana corriges una errata en `normas.html`, ¿qué pasos repites y cuáles no?

> [!bug] Si algo no sale
> | Síntoma | Comprueba primero |
> | :--- | :--- |
> | `git diff` no muestra nada | ¿Guardaste `index.html`? ¿Hiciste `git add` antes del diff? |\n> | `nothing to commit` | ¿Guardaste el fichero? Mira `pwd`, `git status` y `git log --oneline`. |
> | `remote origin already exists` | Ya añadiste `origin`. Mira `git remote -v`; no repitas el alta. |
> | El enlace «Leer las normas» falla | ¿`normas.html` está junto a `index.html`? ¿Coincide el nombre en `href`? |
> | GitHub no muestra el último cambio | Revisa `git status` y si llegaste a ejecutar `git push` en **este** repo. |
> | El push apunta al repositorio del cole | **Detente.** Estás en el repo o en el remoto equivocado; comprueba `pwd` y `git remote -v` antes de tocar nada. |

> [!success] ✅ Al acabar
> - [ ] Esta bóveda y este repositorio se han creado desde cero en casa.
> - [ ] `origin` apunta a `sor-web-prestamo-portatiles-casa`.
> - [ ] El historial muestra tres versiones de la web y el cierre documental posterior.
> - [ ] El enlace a las normas funciona en el navegador.
> - [ ] El vídeo de casa explica el proceso y tiene timestamps reales.
> - [ ] La bitácora contiene el enlace del vídeo y está subida a **este** repositorio.
> - [ ] La tarea de Teams contiene los dos repositorios y la playlist.
