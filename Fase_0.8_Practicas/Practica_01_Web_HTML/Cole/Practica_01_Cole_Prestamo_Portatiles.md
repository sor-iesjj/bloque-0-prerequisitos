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
> **Antes de grabar:** ten preparada una captura PNG propia sin datos personales y dos clips MP4 propios para H7. Lee esta guía entera, abre OBS y prepara un editor de texto, Obsidian, Git Bash y GitHub. Comprueba que tu clave SSH **ya funciona en este equipo**; si no, repasa la configuración de SSH de los prerrequisitos.  
> **Empieza a grabar antes de crear la bóveda.** Muestra tu perfil de GitHub y cada etapa en pantalla. **En el centro no debes narrar:** deja cada comando y resultado visible para poder leerlo. Mantén la grabación hasta comprobar el resultado en GitHub. No muestres claves privadas ni contraseñas.  
> **Título del vídeo:** `B0.P01 · Cole · Préstamo de portátiles`. **Visibilidad:** No listado. **Playlist:** `B0.P01 · Préstamo de portátiles con Git y GitHub` (igual que la tarea de Teams).

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

| Concepto | Para qué lo usas aquí |
| :--- | :--- |
| Bóveda | Carpeta que abres con Obsidian para organizar este proyecto y su bitácora. |
| Repositorio | Carpeta cuyo historial controla Git; aquí será `01_Proyecto`. |
| `git status` | Distinguir archivos nuevos, cambios sin preparar y cambios preparados. |
| Índice o área de preparación | Selección exacta del contenido que entrará en el siguiente commit. |
| `git add ruta` | Preparar el contenido actual de un archivo concreto. Si vuelves a editarlo, tendrás que preparar también ese nuevo cambio. |
| `git diff` | Comparar el trabajo con el índice. Antes de preparar cambios, si el índice coincide con el último commit, muestra las diferencias respecto a esa versión. |
| `git diff --cached` | Revisar lo que ya has preparado para el siguiente commit. |
| Commit | Versión local identificada por un código y un mensaje que explica el cambio. |
| Remoto `origin` | Dirección del repositorio de GitHub de este proyecto. |
| `.gitignore` | Reglas para excluir archivos que todavía no están bajo seguimiento. No borra ni retira archivos ya versionados. |

> [!warning] Dos prácticas independientes, no dos personas colaborando
> En este recorrido crearás tu propia bóveda y tu propio repositorio desde cero. La otra guía repite la teoría y el método para que puedas practicarlos de nuevo, sin depender de ella. Esta repetición no simula colaboración entre compañeros: demuestra que sabes iniciar y mantener un proyecto por tu cuenta.

---

## 1 · PREPARA EL PROYECTO MIENTRAS GRABAS

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
> ```bash
> pwd
> git init
> git branch -M main
> git status
> ```
>
> Antes de `git init`, ejecuta también:
>
> ```bash
> git --version
> git config user.name
> git config user.email
> ssh -T git@github.com
> ```
>
> Comprueba que la identidad de los commits es la tuya y que SSH saluda a tu usuario de GitHub. GitHub puede indicar autenticación correcta y devolver código de salida 1 porque no ofrece una shell: lee el mensaje. La clave privada permanece en este equipo; GitHub ya tiene la pública. **No generes otra pareja de claves por crear este proyecto.** Si falla, repasa la Fase 0.2.2 (centro) o la 0.5.1 (casa), antes de continuar.
>
> **Por qué:** `pwd` muestra la ruta para evitar iniciar Git en la raíz de la bóveda. `git init` crea el repositorio en `01_Proyecto` y `git branch -M main` pone nombre a la rama. **Punto de control:** `pwd` termina en `Boveda_HTML_Centro/01_Proyecto`. `git status` muestra la rama `main`, que aún no hay commits y que los ficheros iniciales están *sin seguimiento*.  Si la ruta es otra, detente antes de seguir.

> [!example] Paso H4 · Crea un repositorio vacío en GitHub
> En tu propia cuenta de GitHub crea `sor-web-prestamo-portatiles-cole`. Déjalo **vacío**: sin README, sin `.gitignore` y sin licencia generados por GitHub. Elige la visibilidad indicada en Teams. Si es privado, da acceso al profesor con la cuenta indicada allí.
>
> En la pantalla del nuevo repositorio elige **SSH** y copia **su** dirección. Debe tener esta forma: `git@github.com:TU-USUARIO/sor-web-prestamo-portatiles-cole.git`. Sustituye `TU-USUARIO` por tu usuario real, no copies el texto literalmente.
>
> En la terminal de **este proyecto**, ejecuta:
>
> ```bash
> git remote add origin git@github.com:TU-USUARIO/sor-web-prestamo-portatiles-cole.git
> git remote -v
> ```
>
> **Por qué:** `git remote add origin` guarda la dirección de GitHub; aún no sube ficheros. `git remote -v` permite comprobarla. **Punto de control:** `origin` termina en `sor-web-prestamo-portatiles-cole.git`. Si aparece otro nombre, **no hagas push**; corrige la dirección antes. `git remote add` se hace una vez en este repositorio.

---

## 3 · GUARDA TRES VERSIONES DE LA MISMA WEB

> [!info] Qué vas a mirar en Git
> `git status` indica si un fichero está sin seguimiento, modificado o preparado para el siguiente commit. `git diff -- web/index.html` compara ese HTML con su versión preparada en el índice. **En este paso, antes de `git add` y sin cambios preparados, el índice coincide con el último commit**: `-` marca la frase anterior y `+` la nueva. El `--` separa el comando del nombre del fichero. Un fichero nuevo sin seguimiento aparece en `git status`, pero aún no aparece en ese `git diff`. Si `git diff` o `git log` abre un visor, pulsa **`q`** para salir.

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
> El primer `status` muestra `.gitignore` y las carpetas nuevas `00_Bitacora/` y `web/` sin seguimiento. Git agrupa ahí los ficheros nuevos hasta que los añades. `git add .` prepara **todos los ficheros no ignorados de `01_Proyecto`**; aquí son los del proyecto. El segundo `status` debe mostrarlos preparados. `git commit` guarda la versión 1 **en el equipo**. `git push -u origin main` la sube por primera vez y configura el seguimiento; en las siguientes subidas bastará `git push`. El último `status` debe estar limpio. Recarga GitHub y abre `web/index.html`: debe decir «disponible».

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

> [!example] Paso H7 · Versión 3: nuevas páginas, imágenes y vídeos locales
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
> Desde `01_Proyecto`, ejecuta:
>
> ```bash
> git status --short --untracked-files=all
> git diff -- web/index.html
> git check-ignore -v web/videos/revision-01.mp4 web/videos/revision-02.mp4
> ```
>
> `--untracked-files=all` permite ver los archivos nuevos uno a uno. Deben aparecer `normas.html`, `contacto.html` y `imagenes/portatil.png` sin seguimiento, e `index.html` modificado. Los vídeos no aparecen en el estado normal: `git check-ignore -v` debe mostrar para ambos la regla `*.mp4` de `.gitignore`. Comprueba también que siguen existiendo en el gestor de archivos. **Si alguno no queda ignorado, detente antes de añadir archivos.**
>
> Prepara cada archivo por separado y observa cómo cambia su estado:
>
> ```bash
> git add web/normas.html
> git status --short --untracked-files=all
> git add web/contacto.html
> git status --short --untracked-files=all
> git add web/imagenes/portatil.png
> git status --short --untracked-files=all
> git add web/index.html
> git diff --cached --stat
> git status
> git commit -m "Anadir normas contacto e imagen de prestamos"
> git push
> git log --oneline
> git status
> ```
>
> Cada `add` prepara solo el archivo indicado; los restantes esperan. En el estado corto, `??` significa nuevo sin seguimiento, `A ` nuevo preparado, ` M` modificación sin preparar y `M ` modificación preparada. La columna izquierda corresponde al índice; la derecha, al trabajo sin preparar.
>
> Antes del commit, el resumen preparado debe incluir **cuatro archivos**: las dos páginas nuevas, la imagen y la portada modificada. Un único commit reúne esta entrega relacionada; no necesitas un commit por cada `add`. En GitHub comprueba los tres commits de la web, las páginas y la imagen, y la ausencia de los dos vídeos. `git status` debe quedar limpio aunque los vídeos ignorados sigan en el disco. Git guarda archivos: la carpeta `videos/` no aparecerá en GitHub si solo contiene archivos ignorados.

> [!example] Paso H7b · Visita la primera entrega y regresa al presente
> **Situación:** el responsable quiere comparar la entrega actual con la primera. Vas a consultar la versión antigua sin borrar commits ni modificar el historial publicado.
>
> Ejecuta `git status`: debe estar limpio. Si tienes cambios pendientes, termina de guardarlos con sentido antes de continuar. Con `git log --oneline`, localiza el código del commit **«Crear pagina inicial de prestamos»** y sustituye `CODIGO_PRIMER_COMMIT` en el siguiente comando por ese código real:
>
> ```bash
> git switch --detach CODIGO_PRIMER_COMMIT
> git status
> ```
>
> `--detach` te sitúa en un commit concreto para inspeccionarlo, fuera de una rama. Es normal que el estado indique `HEAD detached`. No edites ni crees commits aquí. Abre o recarga **`web/index.html`**: debe volver a mostrar «Equipo 01: disponible.», sin imagen ni enlaces. Las páginas nuevas y la imagen ya no están en esta versión; los vídeos locales ignorados pueden permanecer en el disco porque no pertenecen al historial.
>
> Vuelve a la última entrega:
>
> ```bash
> git switch main
> git status
> git log --oneline
> ```
>
> Recarga la portada y comprueba otra vez el estado de mantenimiento, la imagen y los dos enlaces. Debes estar en `main`, con los tres commits de la web y sin cambios pendientes. **No hagas push desde el commit antiguo:** esta consulta no crea una entrega ni necesita subir nada. Recuperar una versión para inspeccionarla es distinto de publicar una reversión; aquí no se usa `reset --hard` ni se fuerza un push.

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
> ```bash
> pwd
> git remote -v
> git status
> git add 00_Bitacora/b0-p01-cole-prestamo-portatiles.md
> git commit -m "Completar bitacora y enlace del video del centro"
> git push
> git status
> ```
>
> `pwd` comprueba la carpeta y el primer `status` debe mostrar la bitácora modificada. `git add` prepara solo esa nota, `commit` la guarda localmente y `push` la sube. **Este último commit no puede aparecer en el mismo vídeo**, porque la URL se obtuvo después de pararlo. Comprueba en GitHub que el enlace de la bitácora funciona. El historial tendrá tres commits de la web y uno documental.

### 📤 Entrega en Teams

La tarea se llama **`B0.P01 · Préstamo de portátiles con Git y GitHub`**, igual que la playlist. Cuando termines también la guía de **Casa**, pega en esa tarea **tres enlaces**: repositorio GitHub del cole, repositorio GitHub de casa y playlist con los dos vídeos. Comprueba que abren y pulsa **Entregar**. Si los repositorios son privados, el profesor necesita acceso a ambos.

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
> | Síntoma | Comprueba primero |
> | :--- | :--- |
> | `git diff` no muestra nada | ¿Guardaste `index.html`? ¿Hiciste `git add` antes del diff? |
> | `nothing to commit` | ¿Guardaste el fichero? Mira `pwd`, `git status` y `git log --oneline`. |
> | `remote origin already exists` | Ya añadiste `origin`. Mira `git remote -v`; no repitas el alta. |
> | Un enlace o la imagen falla | Comprueba que las dos páginas están junto a `index.html`, que la imagen está en `imagenes/portatil.png` y que las rutas coinciden, incluidas mayúsculas. |
> | Un vídeo aparece en `git status` | Comprueba `.gitignore`, la extensión real y `git check-ignore -v`. Si ya estaba seguido por Git, la regla no lo retirará. No lo incluyas en la entrega. |
> | Veo `HEAD detached` | Es lo esperado durante H7b. No edites; vuelve con `git switch main`. |
> | GitHub no muestra el último cambio | Revisa `git status` y si llegaste a ejecutar `git push` en **este** repo. |
> | El push apunta al repositorio de casa | **Detente.** Estás en el repo o en el remoto equivocado; comprueba `pwd` y `git remote -v` antes de tocar nada. |

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
> - [ ] Guardas los enlaces de este repositorio y vídeo para la entrega conjunta tras la guía de Casa.
