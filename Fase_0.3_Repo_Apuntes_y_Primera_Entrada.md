## 📓 Fase 0.3: Repositorio de Apuntes del Trimestre y Primera Entrada

### Tus apuntes, versionados y en la nube — y cómo se escribe una entrada

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~1,5 - 2 horas · **Requisitos:** Fases 0.1, 0.2.1 y 0.2.2 completas (bóveda + cuenta GitHub + autenticación).


> [!abstract] 📋 Qué se te evalúa en esta fase
> **RA.01**
>
> | Código | Criterio de evaluación |
> | :--- | :--- |
> | `CE.01.g` | Se han aplicado preferencias en la configuración del entorno personal. |
>
> Los criterios están tomados literalmente del **RD 1691/2007** y de la programación del módulo.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin.
> 1. **Prepárate primero (sin grabar):** comprueba lo necesario, **léete el procedimiento entero** y **crea la entrada de apuntes de esta fase** en Obsidian: fichero `b0-0.3-repo-de-apuntes.md` con la estructura del **Bloque 0 · Fase 0.1.b**, **vacía**. Rellenarla es cosa tuya, después; hoy solo tiene que existir.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a explicar la Fase 0.3 — Repositorio de apuntes y primera entrada."* Y **muestra tu perfil de GitHub** (o tu Teams/correo). Di qué vas a hacer.
> 3. **Graba TODO**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `B0.3 · Repo de apuntes y primera entrada` y súbelo a tu playlist **`B0_Prerrequisitos`** (No listado).
> 6. **~5 min.** Se graba en **🏫 el centro**.
> 7. **Al terminar esta fase toca revisar Teams**: ahí tendrás la tarea que cubre estas primeras fases.

---

### 🎯 Objetivos de la fase

- [ ] Explicar por qué usamos **un repositorio por trimestre**.
- [ ] Crear un repositorio en GitHub y conectarlo con tu carpeta `Trimestre_1`.
- [ ] Escribir la **entrada de esta fase** con el **nombre** y la **estructura** obligatorios.
- [ ] Hacer el ciclo `git add` → `commit` → `push`, con **un commit por fase** y mensajes que se entiendan.

---

### 🎯 ¿Dónde Estamos?

> [!info] El Punto de Partida
> Tienes `00_Apuntes/Trimestre_1/` en tu bóveda, pero es una carpeta normal: Git no la controla y GitHub no la conoce. Aquí le damos "vida": la convertimos en repositorio y la subimos.

> [!warning] El Problema
> No puedo esperar a final de trimestre para ver si tomas apuntes. Necesito poder decir *"enseñadme lo que lleváis"* **cualquier día**. Por eso tu repo del trimestre debe estar **siempre al día** y yo tener **tu enlace**.

---

### 📚 Fundamento Teórico

> [!info] ¿Por qué un repositorio por trimestre?
> Al cerrar cada trimestre, ese repo queda "congelado" y **te lo califico** limpio; es un enlace claro que me pasas una vez; y si algo se lía en uno, no afecta a los demás. Tendrás **tres**: `apuntes-sor-t1`, `apuntes-sor-t2`, `apuntes-sor-t3`. Montamos el primero.

> [!important] 1. Recordatorio: cómo se llama y cómo se escribe una entrada
> Esto ya lo viste en la **Fase 0.1** y hoy lo repites, porque hoy toca **la entrada de HOY**. Por si no lo tienes a mano:
>
> - **Nombre:** `material-CODIGO-titulo-corto.md`, en minúsculas y con guiones. Sin fecha: el código ya ordena. Ejemplo: `b0-0.3-repo-de-apuntes.md`
> - **Estructura:** la cabecera con tus datos y los **siete** apartados: *🎯 Qué se pedía*, *⌨️ Comandos y pasos importantes*, *🛠️ Qué he hecho*, *🚩 Qué me ha fallado*, *🤔 Respuestas a las preguntas*, *🔗 Enlaces* y *💭 Dudas / a repasar*.
>
> **La plantilla completa, para copiar y pegar, está en la [[Fase_0.1.b_El_Sistema_de_Apuntes|Bloque 0 · Fase 0.1.b]].** No la repito aquí a propósito: **una sola fuente**, para que no acaben dos versiones distintas dando vueltas.
>
> > [!tip] 💡 Hoy SÍ hay comandos que anotar
> > En la 0.1 el apartado de comandos lo dejaste vacío. Hoy no: `git init`, `git add`, `git commit`, `git push`. Anótalos **con lo que hace cada uno**, que es justo lo que se te va a olvidar en dos semanas.
>
> > [!danger] 🛑 Y hoy estrenas el apartado de fallos
> > Es tu primer `push` de verdad. **Si algo falla —y suele fallar— apunta el mensaje literal** y qué hiciste para arreglarlo. Ese apartado vale más que todos los demás juntos.

### 📖 Diccionario de Conceptos Clave

> [!quote] Terminología
> - **`git init`:** convierte una carpeta en repositorio. · **Remoto (`origin`):** la dirección en GitHub.
> - **`git add` / `commit` / `push`:** preparar / guardar / subir. · **Entrada:** el fichero de apuntes de una fase.
> - **`git log`:** la lista de todos tus commits. Tu historial. · **Commit:** una foto guardada **y un punto al que puedes volver**.

---

### 🛠️ Procedimiento Práctico

> [!example] Paso 0: Prepárate (todavía SIN grabar)
> Comprueba que tienes la bóveda y la autenticación de la 0.2. **Léete el procedimiento** (tiene **6 pasos** grabados). Ten **OBS** listo y tu **perfil de GitHub** en una pestaña.
> **Y antes de grabar: crea la entrada de apuntes de esta fase** (`b0-0.3-repo-de-apuntes.md`) con la estructura pegada y **vacía**. En el vídeo solo tienes que **enseñarla**, no rellenarla.

> [!example] Paso 1: Arranca la grabación y preséntate
> Inicia la grabación en **OBS**, preséntate, **enseña tu perfil de GitHub** 2-3 segundos y di qué vas a hacer.

> [!example] Paso 2: Escribe la entrada de ESTA FASE en Obsidian
> En `00_Apuntes/Trimestre_1/B0_Prerrequisitos/` ya tienes las entradas de las fases anteriores. **No las toques**: esta es **otra fase**, así que va **otro fichero**.
>
> Clic derecho sobre `B0_Prerrequisitos` → **`New note`**, nómbrala `b0-0.3-repo-de-apuntes` y pega la estructura (rellena solo la cabecera). Guarda. **No te grabes redactando**: el contenido lo escribes después, a tu ritmo.
>
> Al terminar tienes **una entrada por cada fase que llevas**. Enséñalo en el vídeo: eso es la regla funcionando.
>
> > [!tip] 💡 ¿Y si esta fase nos lleva dos clases?
> > Entonces **mañana no creas otro fichero**: abres este mismo y sigues escribiendo. Una fase, una entrada — aunque dure varios días.

> [!example] Paso 3: Convierte `Trimestre_1` en repositorio
> **Primero hay que meter la terminal DENTRO de `Trimestre_1`.** No teclees la ruta: la carpeta de cada uno está en un sitio distinto (lo viste en la Fase 0.1). Haz esto, que es lo que hacemos los técnicos:
>
> 1. Abre el **Explorador/gestor de archivos** y navega hasta `Boveda_SOR/00_Apuntes/Trimestre_1`.
> 2. **Clic derecho sobre la carpeta `Trimestre_1`** (o dentro de ella, en un hueco vacío):
>    - **Windows:** `Abrir Git Bash aquí` / `Git Bash Here`. En Windows 11 puede estar dentro de **`Mostrar más opciones`**.
>    - **Linux:** `Abrir en un terminal`.
> 3. **Comprueba SIEMPRE dónde has caído** antes de tocar nada:
>    ```bash
>    pwd
>    ```
>    Tiene que terminar en `.../Boveda_SOR/00_Apuntes/Trimestre_1`. Si no, no sigas: has abierto la terminal en otro sitio.
> 4. Ahora sí:
>    ```bash
>    git init
>    git branch -M main
>    git status
>    ```
>
> > [!danger] ⚠️ `git init` **solo** dentro de `Trimestre_1`
> > Nunca en `Boveda_SOR` ni en `00_Apuntes`. Por eso el `pwd` del punto 3 no es opcional: es el seguro que evita convertir media bóveda en un repositorio. **Dilo en voz alta en el vídeo cuando lo hagas.**
>
> > [!tip] 💡 Si no te aparece la opción de clic derecho
> > Abre la terminal como sea, escribe `cd ` (con un espacio detrás) y **completa con tu ruta**, la que apuntaste en la Fase 0.1. Es una de estas cuatro:
> > ```bash
> > cd ~/Documents/SOR/Boveda_SOR/00_Apuntes/Trimestre_1     # Windows, Documentos local
> > cd ~/SOR/Boveda_SOR/00_Apuntes/Trimestre_1               # Windows, Documentos en OneDrive
> > cd ~/Documentos/SOR/Boveda_SOR/00_Apuntes/Trimestre_1    # Linux en español
> > cd ~/SOR/Boveda_SOR/00_Apuntes/Trimestre_1               # Linux sin Documentos
> > ```
> > El `~` significa "mi carpeta de usuario". Y ojo: en Linux la carpeta se llama `Documentos`, pero en Windows es `Documents` **aunque el Explorador te la enseñe traducida como "Documentos"**. Comprueba con `pwd` igualmente.

> [!example] Paso 4: Crea el repositorio en GitHub y copia su dirección
> 1. En `github.com`, arriba a la derecha: **`+` → `New repository`**.
> 2. Rellena:
>    - **Repository name:** `apuntes-sor-t1` (exacto, en minúsculas)
>    - **Visibility:** **`Private`** — son tus apuntes, no tienen que verlos desconocidos.
>    - **⚠️ NO marques nada** de `Add a README file`, `Add .gitignore` ni `Choose a license`. El repositorio tiene que nacer **completamente vacío**.
> 3. Pulsa **`Create repository`**.
> 4. **Copia la dirección.** Verás una pantalla titulada **`Quick setup — if you've done this kind of thing before`**, con una caja arriba y dos pestañas: **`HTTPS`** y **`SSH`**. Pulsa **`SSH`** (es lo que configuraste en la 0.2.2) y dale al **icono de copiar** 📋 que hay al final de la caja. Copiarás algo así:
>    ```
>    git@github.com:TU-USUARIO/apuntes-sor-t1.git
>    ```
>
> > [!warning] ⚠️ Aquí NO hay botón verde `Code`. Es normal
> > Si has visto tutoriales por internet, todos dicen *"pulsa el botón `Code`"*. **En tu pantalla no está**, y no es que lo hayas hecho mal: ese botón sirve para **descargar** un repositorio, y el tuyo está vacío — no hay nada que descargar. Aparecerá solo, después del Paso 5, cuando ya tenga tus apuntes dentro.
> > Por eso el repositorio se crea **vacío**: porque tus ficheros ya existen en tu ordenador y los vas a **subir**. Si le hubieras marcado el `README`, GitHub crearía un commit por su cuenta y al hacer `push` chocarían las dos historias.
>
> > [!tip] 💡 En esa misma pantalla te regalan los comandos
> > Debajo verás dos bloques de comandos. Fíjate bien en cuál es el tuyo:
> >
> > | Bloque | ¿Es el tuyo? |
> > | :--- | :--- |
> > | *…or create a new repository on the command line* | **NO.** Lleva `git init` y tú ya lo hiciste en el Paso 3 |
> > | *…or push an existing repository from the command line* | **SÍ.** Es exactamente el Paso 5 |
> >
> > Cotéjalo con el Paso 5: son los mismos comandos. Compruébalo en voz alta en el vídeo, que es la mejor prueba de que entiendes lo que estás haciendo y no copias.

> [!example] Paso 5: Conecta y sube
> Dentro de `Trimestre_1`. Sustituye la dirección por **la tuya**, la que copiaste en el Paso 4 — y recuerda: para pegar en la terminal es **`Shift + Insert`** o **clic derecho**, `Ctrl+V` ahí no vale (Fase 0.2.1):
> ```bash
> git remote add origin git@github.com:TU-USUARIO/apuntes-sor-t1.git
> ```
> Ahora **NO subas todo de golpe**. Vas a hacer **un commit por cada entrada**, en orden. Sustituye los nombres por los de tus ficheros:
> ```bash
> git add B0_Prerrequisitos/b0-0.1-metodologia-y-estructura.md
> git commit -m "Fase 0.1: metodologia y estructura de la boveda"
>
> git add B0_Prerrequisitos/b0-0.2.1-cuenta-github-y-git.md
> git commit -m "Fase 0.2.1: cuenta de GitHub y configuracion de Git"
>
> git add B0_Prerrequisitos/b0-0.2.2-clave-ssh.md
> git commit -m "Fase 0.2.2: autenticacion con clave SSH"
>
> git add B0_Prerrequisitos/b0-0.3-repo-de-apuntes.md
> git commit -m "Fase 0.3: repositorio de apuntes"
> ```
> Y ahora sí, súbelo todo:
> ```bash
> git push -u origin main
> ```
>

> [!danger] ⌨️ Si la pantalla se te queda "atascada": pulsa `q`
> Te va a pasar con `git log` y con `git diff`, y la primera vez asusta: ejecutas el comando, aparece el texto, y **el terminal deja de responder**. No puedes escribir nada. Parece que se ha colgado o que te has metido en un editor.
>
> **No se ha colgado y no es un editor.** Es el **paginador**: cuando la salida no cabe en pantalla, Git te la enseña con un programa (`less`) que te deja moverte por ella tranquilamente. Se sale con **una tecla**:
>
> | Tecla | Qué hace |
> | :--- | :--- |
> | **`q`** | **SALIR** ← la que buscas |
> | `↓` `↑` o `Enter` | bajar o subir línea a línea |
> | `Espacio` | avanzar una página |
> | `/palabra` | buscar dentro del texto |
>
> Fíjate en que abajo del todo aparece un `:` o el nombre del fichero: **esa es la señal** de que estás dentro del paginador.
>
> Y no es cosa de Git: es el mismo programa que verás en las páginas de manual (`man`) y en muchas herramientas de Linux. **La tecla `q` te va a sacar de todas ellas.** Apréndetela hoy y te ahorras cerrar la terminal a lo bruto durante años.
>
> > [!important] 🕐 Por qué un commit por fase y no uno gordo
> > Podrías hacer `git add .` y un único commit con todo. **Funcionaría igual.** Pero fíjate en la diferencia cuando pides el historial:
> > ```bash
> > git log --oneline
> > ```
> > | Con un commit gordo | Con un commit por fase |
> > | :--- | :--- |
> > | `a1b2c3d Primera entrega` | `d4e5f6a Fase 0.3: repositorio de apuntes` |
> > | | `c3d4e5f Fase 0.2.2: autenticacion con clave SSH` |
> > | | `b2c3d4e Fase 0.2.1: cuenta de GitHub y Git` |
> > | | `a1b2c3d Fase 0.1: metodologia y estructura` |
> >
> > A la derecha, **el historial es un índice de lo que has hecho**. A la izquierda no es nada.
> > Y hay algo más importante que la estética: cada commit es un **punto de restauración**. Si mañana rompes la entrada de la 0.2.2, puedes volver a como estaba **esa sola**, sin tocar las demás. Con un commit gordo, o vuelves entero o no vuelves. Lo vas a comprobar tú mismo en la **Fase 0.7.1**, rompiendo tus apuntes a propósito.
> >
> > **Regla para todo el curso: un commit = un cambio con sentido propio.** Ni un commit por cada letra, ni uno cada tres semanas con todo dentro.
> Recarga GitHub: debe verse `B0_Prerrequisitos/` con **tus cuatro entradas** dentro — las de las fases 0.1, 0.2.1, 0.2.2 y 0.3.
>
> **Sí, cuatro.** Las tres primeras las escribiste en su día pero **nunca habían salido de tu ordenador**: hasta hoy no tenías repositorio. Este `push` es el que se las lleva a GitHub por primera vez.

> [!example] Paso 6: Cierra el vídeo, complétalo todo y entrega
> 1. **Detén la grabación**, nombra el vídeo `B0.3 · Repo de apuntes y primera entrada`, súbelo a la playlist `B0_Prerrequisitos` y **copia su enlace**.
> 2. **Pega ese enlace en la entrada de esta fase**, en el apartado `🔗 Enlaces`. Y aprovecha para **repasar tus entradas anteriores**: la de la 0.1, la 0.2.1 y la 0.2.2 tienen que tener **su** enlace y **sus** respuestas. Donde hay vídeo, hay entrada — y donde hay entrada, hay enlace.
> 3. **Sube los cambios.** Como antes, con mensajes que digan algo:
>    ```bash
>    git add .
>    git commit -m "Anadir enlaces de video y respuestas de las fases 0.1 a 0.3"
>    git push
>    ```
>    Aquí sí vale un `git add .`: es **un solo cambio con sentido propio** (completar los enlaces y las respuestas), aunque toque varios ficheros.
> 4. **Dame acceso al repo:** es **privado**, así que yo no lo veo. Te diré mi usuario para que me añadas en `Settings → Collaborators`. **Sin esto, tu repositorio para mí no existe.**
> 5. **Ve a Teams → `Tareas`** y mira la tarea que cubre estas fases. Pega ahí **solo dos cosas**:
>
> | Qué se entrega | Ejemplo |
> | :--- | :--- |
> | Enlace de tu **repositorio de apuntes** | `https://github.com/TU-USUARIO/apuntes-sor-t1` |
> | Enlace de tu **playlist** de YouTube | la de `B0_Prerrequisitos` |
>
> 6. **Pulsa `Entregar`.** Hasta que no pulses ese botón, para Teams no has entregado — aunque lo tengas todo pegado.
>
> > [!important] 📌 Por qué solo dos enlaces (y no uno por vídeo)
> > Porque **los vídeos ya me los has dado**: cada uno está dentro de su entrada de apuntes, en el repositorio. Al abrir tu repo veo, de un vistazo, qué fases has hecho, qué has entendido de cada una y dónde está el vídeo que lo demuestra.
> > Por eso la regla es **una entrada por fase**: si te falta una entrada, me falta una fase. No hay que buscar nada en ninguna lista.
>
> > [!tip] 💡 Tienes varios días
> > La tarea se abre con **fecha límite de varios días**, no del mismo día, y te llega **notificación** de Teams. Si algo no te ha salido, dímelo **antes** del plazo, no después.

> [!note] 📌 A partir de ahora, en cada fase
> **Al empezar la fase** creas su entrada (nombre + estructura, vacía). **Durante la fase** la vas rellenando a tu ritmo, sin grabar. **Al acabar cada día**, dentro de `Trimestre_1`: `git add .` → `git commit -m "Fase 0.X: ..."` → `git push`. Así el repo está siempre al día y nunca pierdes más de una sesión.

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | Copio la dirección y `Ctrl+V` no pega nada en la terminal. | En Git Bash `Ctrl+V` no es "pegar". | **`Shift + Insert`**, o **clic derecho**. Lo tienes explicado en la Fase 0.2.1. |
> | Pego la dirección y sale cortada o con saltos de línea. | Copiaste texto de más de la caja de GitHub. | Usa el **icono de copiar** 📋 de GitHub, no selecciones a mano. |
> | La pantalla se queda atascada tras `git log` o `git diff` y no puedo escribir. | Estás dentro del **paginador**, no en un editor ni colgado. | Pulsa **`q`**. Es la misma tecla que en `man` y en todo Linux. |
> | `fatal: not a git repository`. | No estás en `Trimestre_1` o no hiciste `git init`. | `pwd` para comprobar; haz `git init` ahí. |
> | `remote origin already exists`. | Ejecutaste `git remote add` dos veces. | `git remote set-url origin git@github.com:...`. |
> | `Updates were rejected`. | Creaste el repo con README (no vacío). | Recréalo vacío, o `git pull origin main --rebase` y `push`. |
> | Hice `git init` en `Boveda_SOR`. | Carpeta equivocada. | Borra ese `.git` (`rm -rf .git` en `Boveda_SOR`) y hazlo en `Trimestre_1`. |

> [!help] Preguntas Críticas
> 1. ¿Por qué un repositorio por trimestre?
> 2. Un día damos **teoría suelta**, que no pertenece a ninguna fase. ¿Cómo se llamaría esa entrada, y **por qué esa sí lleva la fecha** cuando las de fase no la llevan? *(La convención está en el **Bloque 0 · Fase 0.1.b**.)*
> 3. ¿En qué carpeta EXACTA se hace `git init`?

---

### ✅ Checklist Final de la Fase 0.3

- [ ] Primera entrada en `B0_Prerrequisitos/` con nombre y estructura correctos.
- [ ] `Trimestre_1` convertido en repositorio; repo `apuntes-sor-t1` en GitHub.
- [ ] `commit` + `push` hechos; la entrada se ve en GitHub.
- [ ] Enlace enviado (y acceso concedido si es privado).
- [ ] Vídeo `B0.3 · Repo de apuntes y primera entrada` subido a la playlist, con timestamps.
- [ ] **Entrega hecha en Teams**: enlace del repositorio + enlace de la playlist, y pulsado `Entregar`.
- [ ] Todas mis entradas (0.1, 0.2.1, 0.2.2, 0.3) tienen **su enlace de vídeo** y **sus respuestas**.
- [ ] Grabada **🏫 en el centro**.

> **Siguiente paso:** Fase 0.3.b — **Qué NO se sube**: el `.gitignore`. Antes de meter nada más en el repo, hay que decidir qué debe quedarse fuera.

> *(Y después, Fase 0.4 — Bajar el material del curso: tus copias del Bloque 1 y de Boochan.)*
