## 🧪 Práctica integrada 01 · Dos bóvedas HTML, dos historiales Git

### Crear un proyecto desde cero en el centro y repetirlo, con otro proyecto, en casa

> **[Módulo: SOR — Sistemas Operativos en Red · 2.º SMR]**  
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)  
> **📍 Cuándo se hace:** el proyecto del centro, después de las fases 0.3 y 0.3.b; el de casa, cuando ya esté preparado el equipo doméstico de la fase 0.5.1. Aplica el circuito completo a dos trabajos nuevos.  
> **🧭 Referencias:** [[Fase_0.1.b_El_Sistema_de_Apuntes|Plantilla de apuntes]] · [[Fase_0.3_Repo_Apuntes_y_Primera_Entrada|Primer repositorio]] · [[Fase_0.3.b_Que_No_Se_Sube_Gitignore|Qué no se sube]]

---

> [!abstract] 📋 Qué vas a demostrar
> Crear **dos bóvedas independientes de Obsidian** y, dentro de cada una, **un repositorio Git distinto**. Crear también **dos repositorios vacíos en GitHub** y conectarlos por SSH. Guardar una primera versión de una página HTML, modificarla, añadir un fichero nuevo y comprobar que el historial permite reconocer cada cambio. La práctica tiene **dos grabaciones**, una en el centro y otra en casa.

> [!note] Evaluación
> Esta práctica integrada **repasa habilidades de los prerrequisitos**. No añade un RA ni un CE propio a los ya declarados en esas fases; las evidencias concretas se indican en la lista final y en la tarea de Teams.

> [!info] 💼 El caso real
> El aula necesita publicar un aviso; en casa, alguien necesita una pequeña página para gestionar el préstamo de portátiles. Las páginas son deliberadamente sencillas: aquí no evaluamos diseño web. Lo importante es que cada cambio tenga un motivo visible y que puedas demostrar **qué había antes, qué hay ahora y cuándo se subió a GitHub**.

> [!danger] 🛑 Dos trabajos que no se mezclan
> **Centro:** `Boveda_HTML_Centro` → repo local `01_Proyecto` → GitHub `sor-web-avisos-aula`.  
> **Casa:** `Boveda_HTML_Casa` → *otro* repo local `01_Proyecto` → GitHub `sor-web-prestamo-portatiles`.  
> Son **dos bóvedas, dos carpetas `.git` y dos direcciones `origin`**. En casa vuelves a hacer `git init` porque allí creas **otro proyecto**, no porque se repita en cada commit. **No clones ni continúes el proyecto del centro.**

---

## 1 · EL MAPA DEL TRABAJO

```text
🏫 CENTRO                                  🏠 CASA
Boveda_HTML_Centro/                        Boveda_HTML_Casa/
├── .obsidian/                              ├── .obsidian/
├── 00_Grabaciones/                         ├── 00_Grabaciones/
└── 01_Proyecto/  ← Git empieza AQUÍ        └── 01_Proyecto/  ← OTRO Git empieza AQUÍ
    ├── .git/                                   ├── .git/
    ├── .gitignore                              ├── .gitignore
    ├── README.md                               ├── README.md
    ├── 00_Bitacora/                            ├── 00_Bitacora/
    │   └── b0-p01-centro-avisos-aula.md        │   └── b0-p01-casa-prestamo-portatiles.md
    └── web/                                    └── web/
        ├── index.html                             ├── index.html
        └── estilos.css  ← se añade después         └── normas.html ← se añade después
```

> [!important] 📍 La ruta manda
> La bóveda organiza el trabajo en Obsidian. **Solo `01_Proyecto` es un repositorio**; `00_Grabaciones` y `.obsidian` quedan fuera. Abre la terminal dentro de `01_Proyecto` y ejecuta `pwd` antes de `git init`, `git add`, `git commit` o `git push`. La ruta debe acabar en la bóveda correcta y en `/01_Proyecto`. No escribas una ruta del ejemplo a ciegas: la tuya puede ser distinta.

> [!tip] 🔁 El circuito que harás DOS veces, una por proyecto
> `crear bóveda → crear carpetas y ficheros → git init → git branch -M main → git status → crear repo vacío en GitHub → git remote add origin URL-SSH → git add → git commit → git push -u origin main → cambiar/añadir → git status y git diff → git add → git commit → git push → verificar en GitHub`.

> [!note] Lo que ocurre una vez y lo que se repite
> En **cada proyecto** se hacen una vez `git init`, `git branch -M main`, la creación del repo de GitHub y `git remote add origin`. En **cada cambio con sentido** se repite `git status → git diff → git add → git commit → git push`. `git push -u origin main` configura el seguimiento en la primera subida; después basta `git push`.

---

## 2 · PREPARACIÓN Y GRABACIONES

> [!important] 📹 La tarea y la playlist tienen exactamente el mismo nombre
> **Nombre de la tarea de Teams:** `B0.P01 · Dos bóvedas HTML con Git y GitHub`  
> **Nombre de la playlist de YouTube:** `B0.P01 · Dos bóvedas HTML con Git y GitHub`  
> Dentro van **dos vídeos No listados**, en este orden: `B0.P01 · Centro · Avisos del aula` y `B0.P01 · Casa · Préstamo de portátiles`. Esta playlist propia es la forma de entrega de **esta práctica integrada**; no mezcles aquí los vídeos de otras fases.

**2A · En el centro, vídeo de pantalla sin explicación oral**

- Lee la práctica y prepara OBS **antes de grabar**. Comprueba que captura la pantalla y que no mostrará contraseñas ni claves privadas.
- **Empieza a grabar antes de crear la bóveda.** En pantalla debe verse tu identidad académica o tu perfil de GitHub; no hace falta hablar. Mantén la grabación durante todo el procedimiento, incluida la comprobación final en GitHub.
- Marca las etapas con acciones visibles: enseña el árbol de Obsidian, la ruta con `pwd`, cada `git status`, el navegador antes y después de los cambios, `git log --oneline` y el repositorio remoto. Así se entiende el vídeo aunque esté en silencio.

**2B · En casa, vídeo con explicación**

- **Empieza a grabar antes de crear la segunda bóveda.** Preséntate y explica, con tus palabras, por qué este proyecto tiene otra bóveda y otro `origin`.
- Mientras trabajas, di qué muestra cada `git status`, qué entrará en el siguiente commit y por qué `git init` y `git remote add` aparecen de nuevo **solo al crear este segundo proyecto**.
- No copies los ficheros ni el repositorio del centro. El enunciado te proporciona un punto de partida distinto para que repitas el método.

**2C · Marcas de tiempo que pondrás en la descripción de CADA vídeo**

```text
00:00 Inicio e identidad
TU_TIEMPO Creación de la bóveda y carpetas
TU_TIEMPO HTML inicial y primera vista en navegador
TU_TIEMPO git init, rama main y primer git status
TU_TIEMPO Repositorio vacío en GitHub y conexión SSH
TU_TIEMPO Primer commit, primer push y comprobación
TU_TIEMPO Modificación del HTML y segundo commit
TU_TIEMPO Fichero nuevo y tercer commit
TU_TIEMPO Verificación final en GitHub y git log
```

> [!warning] Los tiempos no son los del ejemplo
> Sustituye **cada `TU_TIEMPO` por el minuto real** en formato `mm:ss` o `hh:mm:ss`. Empieza por `00:00`, pon las marcas en orden y comprueba desde la página pública del vídeo que se puede saltar a las etapas. Escribe las marcas en la **descripción**, no en un comentario.

---

## 3 · 🏫 CENTRO: «AVISOS DEL AULA»

### 3A · Crea la bóveda y sus ficheros

> [!example] Paso C1 — De cero en Obsidian
> 1. Inicia OBS. En Obsidian crea **una bóveda nueva** llamada `Boveda_HTML_Centro` en una carpeta local **fuera de OneDrive**. No abras `Boveda_SOR` para este ejercicio.
> 2. Dentro de la nueva bóveda crea `00_Grabaciones/` y `01_Proyecto/`. Dentro de `01_Proyecto/`, crea `00_Bitacora/` y `web/`.
> 3. En `01_Proyecto/00_Bitacora/` crea `b0-p01-centro-avisos-aula.md`. Usa los **siete apartados de la Fase 0.1.b**. Rellena el encabezado con tu nombre y deja los apartados listos para completarlos después del vídeo. En `🔗 Enlaces`, deja «Vídeo: pendiente» hasta subirlo.
> 4. En `01_Proyecto/README.md` escribe: título **Avisos del aula**, tu nombre, una frase sobre la utilidad de la página y `web/index.html` como punto de entrada.
> 5. Crea los ficheros `.html`, `.css`, `README.md` y `.gitignore` con un **editor de texto** y guárdalos en las rutas indicadas; Obsidian se usa para la bóveda y la bitácora Markdown. Comprueba en el gestor de archivos que el nombre termina en `.html` o `.css` y que no se ha añadido `.txt`.
> 6. En `01_Proyecto/.gitignore` escribe estas líneas:
>
>    ```gitignore
>    *.mp4
>    *.mkv
>    *.mov
>    .DS_Store
>    Thumbs.db
>    ```
>
>    El vídeo se guarda en `00_Grabaciones/`, **fuera** del repositorio. El `.gitignore` es una segunda barrera por si algún archivo de vídeo acaba dentro por error. No ignores `web/`, `README.md` ni `00_Bitacora/`.

En `01_Proyecto/web/index.html`, pega exactamente esta **versión inicial**:

```html
<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <title>Avisos del aula</title>
</head>
<body>
  <h1>Avisos del aula</h1>
  <p>Estado: aula disponible.</p>
</body>
</html>
```

Abre `index.html` en el navegador y **muestra que se lee «aula disponible»**. Si Obsidian trata el HTML como texto, ábrelo desde el gestor de archivos con el navegador; es normal.

### 3B · Inicializa Git y conecta GitHub

> [!example] Paso C2 — La terminal está en `01_Proyecto`
> Abre Git Bash o la terminal **en la carpeta `01_Proyecto`**, no en la raíz de la bóveda. Comprueba la ruta y ejecuta:
>
> ```bash
> pwd
> git init
> git branch -M main
> git status
> git check-ignore -v grabacion.mp4
> ```
>
> **Enséñalo:** `git status` debe indicar que estás en `main` y que los ficheros aún **no tienen seguimiento**. Git ve la bitácora, el README, el HTML y `.gitignore`; todavía no hay ningún commit. `git check-ignore -v grabacion.mp4` muestra la regla que excluiría un vídeo con ese nombre; **no crea el fichero**. Si `pwd` no termina en `Boveda_HTML_Centro/01_Proyecto`, detente y abre la terminal en la carpeta correcta.

> [!example] Paso C3 — Crea el remoto vacío, luego conéctalo
> 1. En tu cuenta de GitHub crea un repositorio nuevo llamado `sor-web-avisos-aula`. Déjalo **vacío**: no selecciones README, licencia ni `.gitignore` en GitHub, porque esos ficheros ya están en tu ordenador. Usa la visibilidad indicada por el profesor en Teams. Si es privado, asegúrate de darle acceso al profesor mediante la cuenta que indique la tarea.
> 2. En la página del repositorio vacío elige **SSH** y copia su dirección. Tendrá este patrón: `git@github.com:TU-USUARIO/sor-web-avisos-aula.git`.
> 3. En la terminal de `01_Proyecto`, pega **tu dirección real**:
>
>    ```bash
>    git remote add origin git@github.com:TU-USUARIO/sor-web-avisos-aula.git
>    git remote -v
>    ```
>
>    `origin` debe apuntar al repo **de avisos**, no al de apuntes ni a cualquier otro. No repitas `git remote add` en los commits siguientes.

> [!example] Paso C4 — Primera fotografía y primera subida
> Antes de añadir, mira los ficheros; después añade solo los que forman el proyecto:
>
> ```bash
> git status
> git add .gitignore README.md 00_Bitacora/b0-p01-centro-avisos-aula.md web/index.html
> git status
> git diff --cached --stat
> git commit -m "Crear pagina inicial de avisos del aula"
> git push -u origin main
> git status
> ```
>
> **Enséñalo:** antes de `add` aparecen ficheros sin seguimiento; después de `add` aparecen preparados para commit; después del commit y del push, el árbol queda limpio. Actualiza GitHub y comprueba que aparece `web/index.html` con el primer commit.

### 3C · Cambia algo y añade un fichero nuevo

> [!example] Paso C5 — Un cambio en un fichero que ya existía
> Sustituye **solo** `Estado: aula disponible.` por `Estado: aula ocupada por mantenimiento.` en `web/index.html`. Guarda, actualiza el navegador y muestra la diferencia. **Antes de `git add`**, ejecuta:
>
> ```bash
> git status
> git diff -- web/index.html
> ```
>
> Ahora sí, guarda esta decisión en el historial:
>
> ```bash
> git add web/index.html
> git diff --cached -- web/index.html
> git commit -m "Actualizar estado del aula por mantenimiento"
> git push
> ```
>
> **Explica en la bitácora después:** este segundo commit modifica un fichero que Git ya conocía. En `git diff` se ve la línea anterior y la nueva. Si no hay nada en `git diff`, comprueba que guardaste el fichero en el editor.

> [!example] Paso C6 — Un fichero nuevo y el enlace que lo hace funcionar
> Crea `web/estilos.css` con este contenido:
>
> ```css
> body { font-family: sans-serif; margin: 2rem; }
> h1 { color: #174ea6; }
> ```
>
> En `web/index.html`, dentro de `<head>` y **debajo** de `<title>`, añade:
>
> ```html
> <link rel="stylesheet" href="estilos.css">
> ```
>
> Actualiza el navegador: el título debe verse azul. Comprueba los **dos estados distintos**: `web/estilos.css` es *nuevo, sin seguimiento*; `web/index.html` es *un fichero seguido y modificado*.
>
> ```bash
> git status
> git diff -- web/index.html
> git add web/estilos.css web/index.html
> git diff --cached --stat
> git commit -m "Anadir estilo azul a los avisos"
> git push
> git log --oneline
> git status
> ```
>
> En GitHub deben verse los **tres commits en orden** y los dos ficheros de `web/`. El número exacto de commits puede crecer al completar la bitácora; los tres anteriores deben seguir siendo identificables.

---

## 4 · 🏠 CASA: «PRÉSTAMO DE PORTÁTILES»

> [!important] 🔁 Empiezas desde cero otra vez
> Este apartado se realiza **en casa**, en una **bóveda nueva**. No lleves `Boveda_HTML_Centro` en un pendrive, no copies sus ficheros y no uses `git clone` aquí. Las acciones se parecen a las del centro porque el objetivo es **recordar y explicar el método**, pero el contenido y el remoto son otros.

### 4A · Nueva bóveda, otro contenido

> [!example] Paso H1 — Graba desde el nacimiento del proyecto
> Con OBS grabando y explicando lo que haces, crea `Boveda_HTML_Casa` fuera de OneDrive. Dentro crea `00_Grabaciones/` y `01_Proyecto/`. Dentro del proyecto crea `00_Bitacora/` y `web/`. En la bitácora crea `b0-p01-casa-prestamo-portatiles.md` con los **mismos siete apartados de la Fase 0.1.b** y el vídeo pendiente.
>
> Crea también `README.md` con el título **Préstamo de portátiles**, tu nombre y una frase que explique la página. Crea `.gitignore` con las mismas reglas de vídeo y archivos del sistema usadas en el centro. **Son ficheros nuevos escritos en esta segunda bóveda**, no copias del primer repositorio.

En `01_Proyecto/web/index.html`, escribe esta versión inicial:

```html
<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <title>Préstamo de portátiles</title>
</head>
<body>
  <h1>Préstamo de portátiles</h1>
  <p>Equipo 01: disponible.</p>
</body>
</html>
```

Abre la página en el navegador. **Di en el vídeo** qué información muestra y en qué se distingue de la del centro.

### 4B · Repite la primera conexión, sin mirar el otro repositorio

> [!example] Paso H2 — Segundo `init`, segunda rama `main`, segundo `origin`
> Abre la terminal en **`Boveda_HTML_Casa/01_Proyecto`**. Antes de cada paso, predice qué debería mostrar `git status`.
>
> ```bash
> pwd
> git init
> git branch -M main
> git status
> git check-ignore -v grabacion.mp4
> ```
>
> Crea en GitHub un **nuevo repositorio vacío** llamado `sor-web-prestamo-portatiles`, con la visibilidad indicada en Teams. No generes ficheros en GitHub. Copia la dirección **SSH de este repositorio** y comprueba el enlace:
>
> ```bash
> git remote add origin git@github.com:TU-USUARIO/sor-web-prestamo-portatiles.git
> git remote -v
> ```
>
> Si `git remote -v` muestra `sor-web-avisos-aula`, **has conectado el proyecto equivocado**: para y corrige la dirección antes de subir nada. La dirección de GitHub es propia de cada proyecto.

> [!example] Paso H3 — Primera versión en GitHub
> Elige los ficheros iniciales, muéstralos con `git status`, añádelos y realiza el primer commit:
>
> ```bash
> git add .gitignore README.md 00_Bitacora/b0-p01-casa-prestamo-portatiles.md web/index.html
> git status
> git diff --cached --stat
> git commit -m "Crear pagina inicial de prestamos"
> git push -u origin main
> git status
> ```
>
> Abre **este** repositorio en GitHub y enseña que contiene la página de portátiles. Explica por qué en este momento `git push` por sí solo todavía no era el comando elegido para la primera subida.

### 4C · Dos cambios con dos motivos distintos

> [!example] Paso H4 — Cambia el estado de un equipo
> En `web/index.html` cambia `Equipo 01: disponible.` por `Equipo 01: reservado para mantenimiento.`. Muestra la nueva página en el navegador. Antes de guardar el commit, enseña el estado y la diferencia:
>
> ```bash
> git status
> git diff -- web/index.html
> git add web/index.html
> git diff --cached -- web/index.html
> git commit -m "Reservar equipo 01 para mantenimiento"
> git push
> ```
>
> **Di en voz alta:** qué línea ha cambiado y por qué este commit no requiere repetir `git init` ni `git remote add`.

> [!example] Paso H5 — Añade las normas como segundo fichero HTML
> Crea `web/normas.html` con este contenido:
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
> En `web/index.html`, antes de `</body>`, añade el enlace:
>
> ```html
> <p><a href="normas.html">Leer las normas de préstamo</a></p>
> ```
>
> Abre `index.html` en el navegador y **haz clic en el enlace**: debe abrir la página nueva. Enseña que `normas.html` es un fichero sin seguimiento y que `index.html` vuelve a estar modificado:
>
> ```bash
> git status
> git diff -- web/index.html
> git add web/index.html web/normas.html
> git diff --cached --stat
> git commit -m "Anadir normas y enlace de prestamo"
> git push
> git log --oneline
> git status
> ```
>
> En el navegador de GitHub, verifica que el repo de casa contiene `normas.html` y **no** contiene los avisos del aula. Comprueba también que el repo del centro conserva su propia historia. Son dos circuitos independientes.

---

## 5 · CIERRE, APUNTES Y ENTREGA

> [!help] Preguntas críticas — responde en las dos bitácoras con tus palabras
> 1. ¿En qué carpeta exacta hiciste `git init` y qué habría pasado si lo haces en la raíz de la bóveda?
> 2. ¿Qué diferencia había entre `git status` antes de `add`, después de `add` y después de `commit`?
> 3. ¿Para qué sirve `git remote add origin`? ¿Por qué aparece **una vez en cada proyecto** y no en cada cambio?
> 4. ¿Qué mostró `git diff` al modificar el HTML? ¿Por qué el fichero nuevo apareció en `git status` aunque no saliera en ese `git diff` antes de añadirlo?
> 5. ¿Qué ganaste al hacer commits separados para la primera versión, el cambio de estado y el fichero nuevo?
> 6. Si mañana corriges una errata en `normas.html`, ¿qué pasos repites y cuáles no? ¿Qué repositorio se verá afectado?

> [!example] Paso final — Detén OBS, documenta y sube la bitácora
> 1. Detén cada grabación **después** de enseñar `git log --oneline`, `git status` y el repositorio en GitHub.
> 2. Sube los vídeos como **No listados** con los nombres de la sección 2. Agrégalos a la playlist `B0.P01 · Dos bóvedas HTML con Git y GitHub`. Añade a **cada descripción sus marcas reales** y prueba los saltos.
> 3. Completa **cada bitácora** con los siete apartados de la Fase 0.1.b. En `🔗 Enlaces` pega el enlace del vídeo correspondiente y el de la playlist. Anota las respuestas críticas y los errores reales que hayas resuelto.
> 4. Cada bitácora vive en **su propio repositorio**. Por eso debes hacer un último commit y push **en cada `01_Proyecto`**, con `pwd` y `git remote -v` delante:
>
>    ```bash
>    pwd
>    git remote -v
>    git status
>    git add 00_Bitacora/
>    git commit -m "Completar bitacora y enlace del video"
>    git push
>    git status
>    ```
>
>    Ejecuta esta secuencia una vez **en el repo del centro** y otra **en el de casa**. Si Git dice que no hay nada que commitear, revisa que hayas guardado la bitácora y añadido el enlace nuevo antes de repetir.

**5A · En Teams, en la tarea `B0.P01 · Dos bóvedas HTML con Git y GitHub`, entrega estos tres enlaces:**

| Enlace | Qué debe abrir |
| :--- | :--- |
| Repositorio `sor-web-avisos-aula` | El proyecto del centro y su bitácora |
| Repositorio `sor-web-prestamo-portatiles` | El proyecto de casa y su bitácora |
| Playlist `B0.P01 · Dos bóvedas HTML con Git y GitHub` | Los dos vídeos, en orden, con timestamps |

Si los repositorios son privados, concede al profesor acceso con la cuenta que se indique en Teams. Comprueba que los tres enlaces abren lo esperado y pulsa **Entregar**.

> [!success] ✅ Lista final
> - [ ] Hay dos bóvedas fuera de OneDrive y **ninguna** tiene `.git` en su raíz.
> - [ ] Cada `01_Proyecto` tiene su `.git` y `origin` apunta al repositorio que le corresponde.
> - [ ] En cada repo hay commits distinguibles para primera versión, cambio de estado y fichero nuevo.
> - [ ] Los dos cambios se ven en el navegador; el fichero nuevo está enlazado y funciona.
> - [ ] `git status` termina limpio en ambos repositorios y GitHub muestra la última versión.
> - [ ] Hay una bitácora por vídeo, con sus siete apartados, su enlace y las respuestas.
> - [ ] La playlist coincide **exactamente** con el nombre de la tarea; las dos descripciones tienen timestamps reales.
> - [ ] Teams contiene los dos repositorios y la playlist; has pulsado **Entregar**.

> [!summary] 🎓 Qué te llevas
> Ya has creado **dos proyectos independientes desde cero**. Cada uno tiene su bóveda para organizarse, su repositorio local para guardar versiones y su repositorio en GitHub para entregar. La próxima vez que cambies un fichero en **uno de esos proyectos**, repetirás `status → diff → add → commit → push`; no volverás a crear ese repo ni a añadir su `origin`.
