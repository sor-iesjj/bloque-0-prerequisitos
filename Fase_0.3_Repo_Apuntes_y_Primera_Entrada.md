## 📓 Fase 0.3: Repositorio de Apuntes del Trimestre y Primera Entrada

### Tus apuntes, versionados y en la nube — y cómo se escribe una entrada

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~1,5 - 2 horas · **Requisitos:** Fases 0.1, 0.2.1 y 0.2.2 completas (bóveda + cuenta GitHub + autenticación).

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin.
> 1. **Prepárate primero (sin grabar):** comprueba lo necesario y **léete el procedimiento entero**.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a explicar la Fase 0.3 — Repositorio de apuntes y primera entrada."* Y **muestra tu perfil de GitHub** (o tu Teams/correo). Di qué vas a hacer.
> 3. **Graba TODO**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `Fase 0.3 — Repo de apuntes y primera entrada` y súbelo a tu playlist **`B0_Prerrequisitos`** (No listado).
> 6. **~5 min.** Se graba en **🏫 el centro**.
> 7. **Al terminar esta fase toca revisar Teams**: ahí tendrás la tarea que cubre estas primeras fases.

---

### 🎯 Objetivos de la fase

- [ ] Explicar por qué usamos **un repositorio por trimestre**.
- [ ] Crear un repositorio en GitHub y conectarlo con tu carpeta `Trimestre_1`.
- [ ] Escribir la **entrada del día** con el **nombre** y la **estructura** obligatorios.
- [ ] Hacer el ciclo `git add` → `commit` → `push` y **darme el enlace**.

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
> - **Nombre:** `MMDDAA_titulo-corto.md` — mes, día y año en dos dígitos, guion bajo, y un título corto en minúsculas sin tildes ni espacios. Ejemplo para el 16 de septiembre de 2026: `091626_fase-0.3-repo-de-apuntes.md`
> - **Estructura:** cabecera (`Fecha`, `Bloque`, `Fase / práctica`) + los cuatro apartados: *Qué hemos visto hoy*, *Conceptos clave*, *Comandos / pasos importantes*, *Dudas / a repasar en casa*.
>
> > [!tip] 💡 Hoy SÍ hay comandos que anotar
> > En la 0.1 el apartado de comandos lo dejaste vacío. Hoy no: `git init`, `git add`, `git commit`, `git push`. Anótalos **con lo que hace cada uno**, que es justo lo que se te va a olvidar en dos semanas.

### 📖 Diccionario de Conceptos Clave

> [!quote] Terminología
> - **`git init`:** convierte una carpeta en repositorio. · **Remoto (`origin`):** la dirección en GitHub.
> - **`git add` / `commit` / `push`:** preparar / guardar / subir. · **Entrada:** el fichero de apuntes de un día.

---

### 🛠️ Procedimiento Práctico

> [!example] Paso 0: Prepárate (todavía SIN grabar)
> Comprueba que tienes la bóveda y la autenticación de la 0.2. **Léete el procedimiento** (tiene **6 pasos** grabados). Ten **OBS** listo y tu **perfil de GitHub** en una pestaña.

> [!example] Paso 1: Arranca la grabación y preséntate
> Inicia la grabación en **OBS**, preséntate, **enseña tu perfil de GitHub** 2-3 segundos y di qué vas a hacer.

> [!example] Paso 2: Escribe la entrada de HOY en Obsidian
> En `00_Apuntes/Trimestre_1/B0_Prerrequisitos/` ya tienes **la entrada que escribiste en la Fase 0.1**. No la toques: hoy es otro día, así que va **otro fichero**.
>
> Clic derecho sobre `B0_Prerrequisitos` → **`New note`**, nómbrala con **la fecha de hoy** (`MMDDAA_titulo-corto`) y rellena la estructura con lo de esta sesión. Guarda.
>
> Al terminar debes tener **dos** ficheros en esa carpeta. Enséñalo en el vídeo: eso es "una entrada por día" funcionando.

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
> git add .
> git commit -m "Primera entrada: introduccion al modulo"
> git push -u origin main
> ```
> Recarga GitHub: debe verse `B0_Prerrequisitos/` con **tus dos entradas** dentro.

> [!example] Paso 6: Cierra el vídeo, complétalo todo y entrega
> 1. **Detén la grabación**, nombra el vídeo `Fase 0.3 — Repo de apuntes y primera entrada`, súbelo a la playlist `B0_Prerrequisitos` y **copia su enlace**.
> 2. **Pega ese enlace en la entrada de hoy**, en el apartado `Enlace al vídeo explicativo`. Y aprovecha para **repasar tus entradas anteriores**: la de la 0.1, la 0.2.1 y la 0.2.2 tienen que tener **su** enlace y **sus** respuestas. Donde hay vídeo, hay entrada — y donde hay entrada, hay enlace.
> 3. **Sube los cambios** (ahora ya sabes):
>    ```bash
>    git add .
>    git commit -m "Enlaces de video y respuestas de las fases 0.1 a 0.3"
>    git push
>    ```
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

> [!note] 📌 A partir de ahora, cada día de clase
> Creas la **entrada del día** (nombre + estructura) y, dentro de `Trimestre_1`: `git add .` → `git commit -m "Apuntes del ..."` → `git push`. Así el repo está siempre al día.

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | Copio la dirección y `Ctrl+V` no pega nada en la terminal. | En Git Bash `Ctrl+V` no es "pegar". | **`Shift + Insert`**, o **clic derecho**. Lo tienes explicado en la Fase 0.2.1. |
> | Pego la dirección y sale cortada o con saltos de línea. | Copiaste texto de más de la caja de GitHub. | Usa el **icono de copiar** 📋 de GitHub, no selecciones a mano. |
> | `fatal: not a git repository`. | No estás en `Trimestre_1` o no hiciste `git init`. | `pwd` para comprobar; haz `git init` ahí. |
> | `remote origin already exists`. | Ejecutaste `git remote add` dos veces. | `git remote set-url origin git@github.com:...`. |
> | `Updates were rejected`. | Creaste el repo con README (no vacío). | Recréalo vacío, o `git pull origin main --rebase` y `push`. |
> | Hice `git init` en `Boveda_SOR`. | Carpeta equivocada. | Borra ese `.git` (`rm -rf .git` en `Boveda_SOR`) y hazlo en `Trimestre_1`. |

> [!help] Preguntas Críticas
> 1. ¿Por qué un repositorio por trimestre?
> 2. Escribe el nombre de una entrada del 3 de octubre de 2026 titulada "servidor DNS".
> 3. ¿En qué carpeta EXACTA se hace `git init`?

---

### ✅ Checklist Final de la Fase 0.3

- [ ] Primera entrada en `B0_Prerrequisitos/` con nombre y estructura correctos.
- [ ] `Trimestre_1` convertido en repositorio; repo `apuntes-sor-t1` en GitHub.
- [ ] `commit` + `push` hechos; la entrada se ve en GitHub.
- [ ] Enlace enviado (y acceso concedido si es privado).
- [ ] Vídeo `Fase 0.3 — Repo de apuntes y primera entrada` subido a la playlist, con timestamps.
- [ ] **Entrega hecha en Teams**: enlace del repositorio + enlace de la playlist, y pulsado `Entregar`.
- [ ] Todas mis entradas (0.1, 0.2.1, 0.2.2, 0.3) tienen **su enlace de vídeo** y **sus respuestas**.
- [ ] Grabada **🏫 en el centro**.

> **Siguiente paso:** Fase 0.4 — Clonar tu copia de la práctica **`boochan-1`** y dominar el ciclo `status → commit → push`.
