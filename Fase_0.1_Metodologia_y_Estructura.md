## 🧭 Fase 0.1: Metodología de Trabajo y Estructura de la Bóveda

### Cómo vamos a trabajar todo el curso (y por qué)

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> Esta fase **no** enseña redes ni servidores todavía: monta el **método** con el que trabajaremos el resto del curso. Sin esto, nada de lo que venga después se puede entregar ni corregir.
>
> **Profesor:** Pedro Navarro Miralles
> **Correo:** p.navarromiralles2@edu.gva.es
> **Centro:** IES Jorge Juan (ALICANTE)
>
> **⏱️ Tiempo estimado:** ~1,5 - 2 horas (explicación + montar el canal de vídeo + práctica grabada)
> **Requisitos:** Obsidian y OBS ya instalados en el equipo (los instala Consellería — tú no tienes permisos). Necesitarás una **cuenta de Gmail/YouTube** (la creas en el Paso previo). No hace falta Git en esta fase todavía.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin. No es un repaso al final: quiero ver **cómo lo haces tú**.
> 1. **Prepárate primero (sin grabar):** comprueba que tienes lo necesario y **léete el procedimiento entero** para no atascarte a mitad del vídeo.
> 2. **Arranca OBS y, nada más empezar, PRESÉNTATE:** *"Hola y bienvenidos. Me llamo [Nombre], soy alumno de 2.º SMR, y en este vídeo voy a explicar la Fase 0.1 — Metodología y estructura de la bóveda."* Y **muestra en pantalla algo que demuestre que eres tú** (tu **Teams** o tu **correo `@alu.edu.gva.es`** con tu nombre; cuando tengas GitHub, tu perfil). Di **qué vas a hacer**.
> 3. **Graba TODO el procedimiento**, explicando cada paso en voz alta mientras lo haces.
> 4. **Timestamps SIEMPRE** en la descripción del vídeo: `00:00 Presentación` y **uno por cada paso** (formato `mm:ss`).
> 5. **Al terminar:** nombra el vídeo con el nombre de la fase (*"Fase 0.1 — Metodología y estructura"*) y **súbelo a tu playlist de YouTube `00_Prerrequisitos`**.
> 6. **Duración:** ~5 min por vídeo. **Doble entrega:** grabas **uno en el centro** y **otro en casa** — los **dos** van a la playlist.

---

### 🎯 Objetivos de la fase

Al terminar esta fase serás capaz de:

- [ ] Explicar con tus palabras qué es una **bóveda** de Obsidian y para qué la usamos.
- [ ] Explicar la diferencia entre **tus apuntes** y las **prácticas** (Boochan), y por qué viven en carpetas separadas.
- [ ] Tener tu **canal de YouTube** con la playlist `00_Prerrequisitos` lista.
- [ ] Crear tu bóveda `Boveda_SOR` en la ruta correcta del equipo (y saber por qué **NO** va en OneDrive).
- [ ] Crear la **estructura de carpetas** exacta que usaremos todo el curso, respetándola al detalle.
- [ ] **Grabar la práctica entera con OBS**, presentándote, y subirla a tu playlist.

---

### 🎯 ¿Dónde Estamos?

> [!info] El Punto de Partida
> Este es el primer día de verdad. No vamos a tocar servidores todavía: primero vamos a montar **tu forma de trabajar conmigo durante todo el curso**. En este módulo vas a hacer **prácticas** que imitan situaciones reales de un técnico (las prácticas *Boochan*), y a la vez vas a **tomar apuntes** de todo lo que expliquemos. Las dos cosas se entregan, y las dos cosas cuentan para nota.

> [!warning] El Problema
> Un técnico no memoriza: **documenta**. Si no tienes un sitio ordenado donde anotar lo que haces, dentro de dos semanas no te acordarás de nada, no podrás repetir una práctica en casa, y yo no podré corregir tu trabajo. Por eso lo primero no es "instalar cosas", es **decidir dónde y cómo se guarda la información** — y que todos lo hagamos exactamente igual.

> [!success] Objetivo de esta Fase
> Dejar montada, en tu equipo, una **bóveda de Obsidian** llamada `Boveda_SOR` con una estructura de carpetas fija: una zona para **tus apuntes** (por trimestres) y otra para las **prácticas** (Boochan). Y entregar el **vídeo grabado** de todo el proceso en tu playlist de YouTube.

---

### 📚 Fundamento Teórico

> [!info] ¿Qué es Obsidian?
> Obsidian es un programa para **tomar notas** en formato de texto. No es como Word: cada nota es un fichero de texto simple (con extensión `.md`, llamado *Markdown*) que pesa muy poco, se lee en cualquier ordenador y se puede versionar y enviar por Internet fácilmente. Es la herramienta que usaremos para **todos tus apuntes** del módulo. Está disponible en **Windows, Linux, Mac, Android e iOS**, y como tus notas son solo ficheros de texto, **la misma bóveda funciona igual en el equipo del centro y en tu casa**.

> [!abstract] 1. Qué es una "bóveda" (vault)
> Una **bóveda** es, simplemente, **una carpeta de tu disco duro** que Obsidian abre y gestiona. Todo lo que metas dentro de esa carpeta (notas, subcarpetas, imágenes) forma parte de la bóveda. No es nada mágico ni un formato raro: es una carpeta normal. Cuando "abres una bóveda" en Obsidian, le estás diciendo: *"trabaja con todo lo que hay dentro de esta carpeta"*.
>
> Nuestra bóveda se llamará **`Boveda_SOR`** y será el **punto de referencia** de todo el curso: dentro estarán tus apuntes y las prácticas.

> [!important] 2. Apuntes vs. Prácticas: dos cosas distintas que NO se mezclan
> Dentro de la bóveda tendremos **dos zonas separadas a propósito**:
>
> | Zona | Qué es | Ejemplo |
> | :--- | :--- | :--- |
> | **`00_Apuntes/`** | **Lo que TÚ escribes**: tus notas de lo que yo explico cada día. Es tu cuaderno digital. | "Hoy hemos visto qué es una IP y para qué sirve el ping…" |
> | **`Practicas/`** | **El material que YO te doy**: las prácticas Boochan que descargarás de Internet. Tú las sigues y trabajas sobre ellas. | La práctica `boochan-1` con sus fases. |
>
> **¿Por qué separadas?** Porque tus apuntes son **tuyos** y me los entregas para que los corrija; las prácticas son material del curso. Mezclarlos sería como escribir tus apuntes encima del libro de otra persona: un lío para ti y para mí.

> [!note] 3. La metodología: una entrada por día
> Tus apuntes se organizan así, de lo más grande a lo más pequeño:
>
> **Trimestre → Bloque → Entrada del día**
>
> - **Trimestre:** primero, segundo o tercero. Cada uno en su carpeta.
> - **Bloque:** un tema grande de trabajo. El **Bloque 1 es "Introducción"** (esto que estamos haciendo ahora).
> - **Entrada del día:** **cada día de clase creas un fichero nuevo** con lo que hayas anotado ese día. No escribes todo en un único fichero gigante: un fichero por día.
>
> Las normas exactas de cómo nombrar y rellenar cada entrada las veremos en la **Fase 0.3**. Aquí solo dejamos preparadas las carpetas.

> [!warning] 4. Por qué se graba TODO (y desde el principio)
> Regla de oro del curso: **una práctica que no se graba, no cuenta.** Y se graba **de principio a fin**, no un repaso al final:
> - Grabar todo el proceso demuestra que **lo has hecho tú** y me deja ver **cómo** lo haces (dónde dudas, dónde te atascas).
> - Por eso **primero te preparas** (te lees el procedimiento) y **luego grabas** del tirón: así el vídeo sale limpio y no lleno de "espera, que no me acuerdo".
> - Habrá **dos entregas** de cada práctica, y **las dos se suben a tu playlist de YouTube**:
>   - **En el centro:** la primera toma, en clase, donde lo hacemos juntos por primera vez.
>   - **En casa:** la repites tú solo, con calma, para reforzar. **Repetir es como se aprende esto de verdad.**

### 📖 Diccionario de Conceptos Clave

> [!quote] Terminología que usaremos todo el curso
> - **Obsidian:** programa para tomar notas en ficheros de texto (Markdown).
> - **Bóveda (vault):** la carpeta del disco que Obsidian gestiona. La nuestra: `Boveda_SOR`.
> - **Markdown (`.md`):** formato de texto simple para escribir notas con títulos, listas, etc.
> - **Apuntes:** lo que escribes tú (carpeta `00_Apuntes/`). Se corrige.
> - **Práctica:** el material Boochan que te doy y sobre el que trabajas (carpeta `Practicas/`).
> - **Bloque:** un tema grande dentro de un trimestre. El Bloque 1 es "Introducción".
> - **Entrada:** el fichero de notas de **un día concreto** de clase.
> - **OBS:** programa para **grabar la pantalla** mientras haces la práctica.
> - **Playlist:** una lista de reproducción de YouTube donde agrupas tus vídeos. La de este bloque: `00_Prerrequisitos`.
> - **Timestamp:** una marca de tiempo (`mm:ss`) en la descripción del vídeo que salta a un momento concreto (cada paso).
> - **OneDrive:** el disco en la nube de Microsoft. **Ojo:** aquí NO guardamos la bóveda (se explica abajo).

---

### 🛠️ Procedimiento Práctico

> [!danger] ⚠️ LÉEME ANTES DE EMPEZAR: la bóveda NO va en OneDrive
> Es muy tentador guardar la carpeta dentro de OneDrive "para tenerla en la nube". **No lo hagas.** Más adelante usaremos **Git** para enviar tus apuntes por Internet, y Git y OneDrive **se pelean** por los mismos ficheros: se corrompen las carpetas ocultas del control de versiones y aparecen "copias en conflicto" que lo estropean todo.
> - **La bóveda va en una carpeta LOCAL del equipo**, no dentro de OneDrive.
> - Tu "copia en la nube" será **GitHub** (lo montamos en la Fase 0.2), no OneDrive.
> - Si no sabes dónde está tu carpeta de OneDrive, pregúntame antes de crear la bóveda.

> [!example] 🎬 Paso previo (UNA sola vez, no se graba): monta tu canal de vídeo
> Necesitas un sitio donde subir todos los vídeos del curso. Esto se hace **una vez** y sirve para todas las fases:
> 1. Crea una **cuenta de Gmail** parecida a tu correo del instituto. Ejemplo: si tu correo es `luis.garcia@alu.edu.gva.es`, crea algo como `luis.garcia.smr@gmail.com` (que se te reconozca).
> 2. Con esa cuenta, entra en **YouTube** y crea tu **canal**.
> 3. Crea una **playlist** llamada exactamente **`00_Prerrequisitos`**. Ahí subirás los vídeos de las fases 0.1 a 0.6.
> 4. Sube los vídeos como **"No listado"** (unlisted): así solo quien tenga el enlace (yo) los ve, no salen en búsquedas.
>
> > [!tip] 💡 Esta cuenta te vale para todo el curso
> > Cuando más adelante hagamos el proyecto Boochan y el curso de Git, crearás **más playlists** (una por bloque) en este mismo canal. Guárdate bien el usuario y la contraseña.

> [!example] Paso 0: Prepárate (todavía SIN grabar)
> Antes de darle a grabar, deja todo listo para que el vídeo salga del tirón:
> 1. **Comprueba lo instalado:** busca **Obsidian** y **OBS Studio** en el menú de aplicaciones. Si **falta alguno**, avísame: **no intentes instalarlo tú** ni bajar versiones "portables" no autorizadas.
> 2. **Léete el procedimiento entero** (los pasos 1 a 4 de abajo): así, cuando grabes, sabrás lo que viene y no te quedarás en blanco. Este procedimiento tiene **4 pasos** que se graban.
> 3. **Ten OBS a mano** y una pestaña del navegador abierta con tu **Teams** o tu **correo `@alu.edu.gva.es`** (la usarás para presentarte).

> [!example] Paso 1: Arranca la grabación y preséntate
> 1. Abre **OBS Studio** y pulsa **"Iniciar grabación"**. A partir de aquí, **todo queda grabado**.
> 2. **Preséntate en voz alta:** *"Hola y bienvenidos. Me llamo [tu nombre], soy alumno de 2.º SMR, y en este vídeo voy a explicar la Fase 0.1 — Metodología y estructura de la bóveda."*
> 3. **Demuestra que eres tú:** cambia a la pestaña de tu **Teams** o tu **correo `@alu.edu.gva.es`** y enséñalo 2-3 segundos, para que se vea tu nombre.
> 4. Di **qué vas a hacer:** *"Voy a crear mi bóveda de Obsidian y su estructura de carpetas, siguiendo el procedimiento de esta fase."*

> [!example] Paso 2: Crea la bóveda (grabando y explicando)
> Explicando en voz alta lo que haces:
> 1. Abre **Obsidian** y pulsa **`Create new vault`** (Crear nueva bóveda).
> 2. En **`Vault name`** escribe exactamente: **`Boveda_SOR`**
> 3. En **`Location`** pulsa **`Browse`** y elige una carpeta **local, fuera de OneDrive**:
>    - **Windows:** `C:\SOR\` (si no existe la carpeta `SOR`, créala primero).
>    - **Linux:** tu carpeta personal, por ejemplo `/home/tu-usuario/SOR/`.
> 4. Pulsa **`Create`**. Obsidian se abre con la bóveda vacía `Boveda_SOR`.

> [!example] Paso 3: Crea la estructura de carpetas y compruébala (grabando)
> Crea esta estructura **exacta** (nombres **sin tildes ni espacios**), explicando cada carpeta:
> ```
> Boveda_SOR/
> ├── 00_Apuntes/
> │   ├── Trimestre_1/
> │   │   └── Bloque_1_Introduccion/
> │   ├── Trimestre_2/
> │   └── Trimestre_3/
> └── Practicas/
> ```
> **Cómo:** clic derecho en el panel izquierdo → **`New folder`** → escribe el nombre **tal cual**. Para crear una carpeta **dentro** de otra, clic derecho **sobre la carpeta padre**. Créalas en este orden: `00_Apuntes` → dentro `Trimestre_1/2/3` → dentro de `Trimestre_1` la `Bloque_1_Introduccion` → y `Practicas` en la raíz.
>
> Al terminar, **recorre la estructura con el ratón** y compruébala en voz alta: *"Aquí están mis apuntes por trimestres, aquí el bloque de introducción, y aquí la carpeta de prácticas."*
>
> > [!warning] ⚠️ El nombre importa
> > No pongas `Apuntes` en vez de `00_Apuntes`, ni `Trimestre 1` con espacio, ni `Bloque1`. Si cada uno lo escribe a su manera, es imposible corregir a 20 personas. **Cópialo carácter a carácter.**

> [!example] Paso 4: Cierra el vídeo, nómbralo y súbelo a YouTube
> 1. **Detén la grabación** en OBS y localiza el archivo del vídeo.
> 2. **Nómbralo** con el nombre de la fase: `Fase 0.1 — Metodología y estructura`.
> 3. **Súbelo a YouTube**, a tu playlist **`00_Prerrequisitos`**, como **"No listado"**.
> 4. En la **descripción**, añade los **timestamps** (uno por paso). Ejemplo:
>    ```
>    00:00 Presentación
>    00:20 Paso 2 — Crear la bóveda Boveda_SOR
>    01:10 Paso 3 — Crear la estructura de carpetas
>    02:30 Paso 4 — Repaso final
>    ```
>    *(Pon los minutos:segundos reales de tu vídeo.)*
> 5. **Comprueba la duración:** debe rondar los **5 minutos**. Si se te va mucho, ve más al grano; los timestamps son obligatorios de todos modos.
>
> > [!success] ✅ La Fase 0.1 está completa cuando…
> > Tienes la bóveda `Boveda_SOR` con su estructura exacta **y** el vídeo subido a tu playlist `00_Prerrequisitos`, con presentación al principio y timestamps en la descripción. (Recuerda: **doble entrega** — repítelo en casa y sube el segundo vídeo.)

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Tabla de Troubleshooting (¿Algo no funciona?)
> | Problema | Causa Probable | Solución Sugerida |
> | :--- | :--- | :--- |
> | No encuentro Obsidian / OBS en el equipo. | No están instalados o tienen otro nombre en el menú. | Avisa al profesor. No los instales tú: dependemos de Consellería. |
> | OBS no graba / se ve la pantalla en negro. | Falta seleccionar la fuente de captura de pantalla. | En OBS, en "Fuentes" añade una **"Captura de pantalla / Display Capture"**. Si sigue en negro, avísame. |
> | No se me oye en el vídeo. | El micrófono no está como fuente de audio en OBS. | En OBS añade "Captura de entrada de audio" (micrófono) y comprueba el nivel. |
> | El vídeo se va de 5 minutos. | Te has enrollado o repites cosas. | Prepárate mejor antes de grabar (Paso 0). Los timestamps son obligatorios igualmente. |
> | No me deja crear la carpeta con ese nombre. | Has dejado un espacio al final, o un carácter raro. | Bórrala y créala de nuevo copiando el nombre exacto, sin espacios. |
> | Creé la bóveda dentro de OneDrive sin querer. | Elegiste una ruta dentro de OneDrive. | Cierra Obsidian, mueve `Boveda_SOR` a una ruta local (ej. `C:\SOR\`) y reábrela con `Open folder as vault`. Ante la duda, pregúntame. |

> [!help] Preguntas Críticas (Autoevaluación del alumno)
> 1. ¿Qué es una bóveda de Obsidian? ¿Es un formato especial o una carpeta normal?
> 2. ¿Qué diferencia hay entre la carpeta `00_Apuntes/` y la carpeta `Practicas/`?
> 3. ¿Por qué **no** guardamos la bóveda dentro de OneDrive?
> 4. ¿En qué momento del vídeo te presentas y demuestras que eres tú: al principio o al final?
> 5. 🔬 **Reto:** sin mirar la guía, dibuja en un papel el árbol de carpetas de la bóveda. Luego compáralo con Obsidian: ¿te faltaba alguna?

---

### ✅ Checklist Final de la Fase 0.1

- [ ] Canal de YouTube creado con la playlist `00_Prerrequisitos`.
- [ ] Obsidian y OBS comprobados en el equipo (instalados por Consellería).
- [ ] Bóveda `Boveda_SOR` creada en una ruta **local** (no en OneDrive).
- [ ] Estructura de carpetas exacta: `00_Apuntes/` (con `Trimestre_1/2/3` y `Bloque_1_Introduccion` en T1) + `Practicas/`.
- [ ] Vídeo grabado **de principio a fin**, con presentación e identidad al inicio.
- [ ] Vídeo nombrado `Fase 0.1 — Metodología y estructura` y subido a la playlist `00_Prerrequisitos`.
- [ ] Timestamps en la descripción (uno por paso).
- [ ] **Doble entrega:** vídeo del centro **y** vídeo de casa, los dos en la playlist.

> **Siguiente paso:** Fase 0.2 — Crear tu cuenta de **GitHub** y configurar **Git** en el equipo, para poder enviarme tus apuntes por Internet y que yo pueda corregirlos.
