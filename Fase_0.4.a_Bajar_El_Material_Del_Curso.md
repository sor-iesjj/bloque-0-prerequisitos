## 📦 Fase 0.4.a: Bajar el Material del Curso

### Tres repositorios, tres formas de bajarlos — y por qué no todas valen

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~1 - 1,5 horas · **Requisitos:** Bloque 0 · Fases 0.1 a 0.3.b completas.


> [!abstract] 📋 Qué se te evalúa en esta fase
> **RA.05**
>
> | Código | Criterio de evaluación |
> | :--- | :--- |
> | `CE.05.d` | Se han realizado tareas de mantenimiento del software instalado en el sistema. |
>
> Los criterios están tomados literalmente del **RD 1691/2007** y de la programación del módulo.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin.
> 1. **Prepárate primero (sin grabar):** comprueba lo necesario, **léete el procedimiento entero** y **crea la entrada de apuntes de esta fase** en Obsidian: fichero `b0-0.4.a-bajar-el-material.md` con la estructura del **Bloque 0 · Fase 0.1.b**, **vacía**. Rellenarla es cosa tuya, después; hoy solo tiene que existir.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a explicar la Fase 0.4.a — Bajar el material del curso."* Y **muestra tu perfil de GitHub**. Di qué vas a hacer.
> 3. **Graba TODO**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `B0.4.a · Bajar el material del curso` y súbelo a tu playlist **`B0_Prerrequisitos`** (No listado).
> 6. **~5 min.** Se graba en **🏫 el centro**.
> 7. **La entrega va por la TAREA de Teams.** Cuando toque, abriré una tarea que cubrirá **esta fase y otras**; te llegará notificación. Tú, hoy: graba, sube el vídeo a la playlist y **pega su enlace en tu entrada de apuntes**.
> 8. **El enlace del vídeo va DENTRO de tu entrada de apuntes**, en el apartado `🔗 Enlaces`. No lo guardes en un papel: va ahí.

---

### 🎯 Objetivos de la fase

- [ ] Sacar **tus copias** de los tres repositorios del trimestre y clonarlas en tu bóveda.
- [ ] Bajar cada una por **una vía distinta**: **SSH**, **HTTPS** y **descarga en ZIP**.
- [ ] Explicar por qué el **ZIP no sirve** aunque los ficheros se vean igual.
- [ ] Explicar qué hace **`Use this template`** y por qué el material tiene que ser **tuyo**.
- [ ] Hacer un cambio y subirlo con `git status` → `add` → `commit` → `push`.

---

### 🎯 ¿Dónde Estamos?

> [!info] El Punto de Partida
> Tienes la bóveda, la cuenta de GitHub, la autenticación y tu repositorio de apuntes funcionando. Lo que **no** tienes todavía es el material del curso en tu ordenador: hasta hoy lo has leído por donde te lo he ido pasando. Hoy se baja, y se queda dentro de tu bóveda para siempre.

> [!warning] El Problema
> Bajarse ficheros de Internet sabe hacerlo cualquiera. Lo que hoy vas a aprender es que **hay varias formas de bajarse un repositorio y no dan el mismo resultado**, aunque en el Explorador se vean idénticas. La diferencia no se nota hoy: se nota el día que borras algo sin querer. *(Que es, literalmente, la fase siguiente.)*

---

### 📚 Fundamento Teórico

> [!important] 1. Hoy bajas TRES repositorios, y los tres se bajan igual
> Estos tres:
>
> | Nº | Qué es | Carpeta en tu bóveda | Cuándo lo usarás |
> | :---: | :--- | :--- | :--- |
> | **1** | **Prerrequisitos** — esto que estás leyendo | `B0_Prerrequisitos` | Ahora mismo |
> | **2** | **Bloque 1 · Entorno** | `B1_Entorno` | En cuanto acabemos los prerrequisitos |
> | **3** | **Bloque 2 · Ubuntu local** — el proyecto Boochan | `B2_Ubuntu_Local` | Después del Bloque 1 |
>
> Y el procedimiento es **idéntico** en los tres:
>
> ```
> Mi repo (plantilla)  →  Use this template  →  TU repo en tu GitHub  →  git clone  →  tu ordenador
> ```
>
> Fíjate en lo que pasa ahí: **el material deja de ser mío y pasa a ser tuyo.** A partir del segundo paso trabajas sobre **tu** repositorio, en **tu** cuenta. Puedes escribir, anotar, romper y hacer `push` sin pedirle permiso a nadie.
>
> > [!success] 🔒 Y no puedes estropear mi material ni queriendo
> > Tu copia y mi repositorio quedan **completamente separados** desde el primer segundo. **No eres colaborador de mis repos**, así que un `push` contra ellos te lo rechazaría GitHub con un error `403`.
> > Trabaja tranquilo: **no hay forma de que la líes en el material del curso.**

> [!info] 2. Qué es una plantilla, y por qué te interesa que el material sea tuyo
> Una **plantilla** es un repositorio pensado para sacar copias. Al pulsar **`Use this template`**, GitHub crea en **tu** cuenta un repositorio **nuevo e independiente**, con el mismo contenido pero **historial propio**. No es un enlace al mío: es **tuyo**.
>
> **Todos los repositorios del curso son plantilla**, así que verás ese botón en todos.
>
> ¿Y para qué lo quieres tuyo, si el material lo escribo yo? Por esto:
>
> > [!question] 🤔 Piénsalo: estás en clase, hay un paso que no te cuadra y lo anotas en el fichero
> > Si ese repositorio fuera **mío**, esa anotación se quedaría en el ordenador del aula **para siempre**: no podrías subirla, porque no tienes permiso de escritura en mis repositorios. El lunes en casa **no estaría**.
> > Siendo **tuyo**, haces `push` y la tienes en los dos sitios. **Esa es toda la razón.**

> [!info] 3. Las tres formas de bajarse un repositorio
> Son las tres que vas a usar hoy, una por repositorio, a propósito:
>
> | Vía | Qué escribes | ¿Trae el historial? | ¿Pide identificarte? |
> | :--- | :--- | :---: | :--- |
> | **SSH** | `git clone git@github.com:…` | ✅ Sí | Sí — con **tu clave** de la Fase 0.2.2 |
> | **HTTPS** | `git clone https://github.com/…` | ✅ Sí | **Para bajar, no.** Para subir, sí |
> | **Descargar ZIP** | Botón `Code` → `Download ZIP` | ❌ **No** | No |
>
> **Las dos primeras te traen un repositorio. La tercera te trae unos ficheros sueltos.** Parecen lo mismo en el Explorador y no lo son, y lo vas a comprobar tú en el Paso 5.

> [!abstract] 4. Por qué el HTTPS no te pide contraseña para bajar
> Porque los repositorios del curso son **públicos**: cualquiera puede leerlos, igual que cualquiera puede leer una página web sin registrarse.
>
> Identificarse hace falta para **escribir**, no para **leer**:
>
> | Qué haces | ¿Hace falta identificarse? |
> | :--- | :--- |
> | `git clone` de un repositorio público | **No** |
> | `git push`, aunque el repositorio sea tuyo | **Siempre** |
>
> Ahí es donde entran la clave SSH y el token de la **Bloque 0 · Fase 0.2.2**: no son para bajar cosas, **son para poder subirlas**.

> [!abstract] 5. Clonar vs. Push, y el segundo argumento
> - **`git clone`** (GitHub → tu ordenador): **una sola vez**, para bajar el repositorio.
> - **`git push`** (tu ordenador → GitHub): **cada vez** que subes cambios.
>
> Y al clonar, **el remoto ya viene configurado**: no hace falta `git init` ni `git remote add`. Eso solo lo hiciste en la 0.3 porque allí la carpeta ya existía en tu ordenador y el repositorio nacía vacío.
>
> > [!danger] 🛑 El segundo argumento del `clone` NO es opcional
> > ```
> > git clone  <dirección del repositorio>  <nombre de la carpeta>
> > ```
> > **Sin él, Git le pone a la carpeta el nombre del repositorio** (`bloque-1-entorno`) y acabas con la misma cosa llamada de dos maneras. En tu bóveda las carpetas se llaman como el bloque: `B1_Entorno`.
> > Ya lo usaste en la **Bloque 0 · Fase 0.3**, cuando clonaste `apuntes-sor-t1` y le dijiste que se llamara `Trimestre_1`. Hoy lo usas **en los tres**.

> [!tip] 6. Dónde anotas: en TU fichero, no encima del mío
> Ahora que el material es tuyo puedes escribir donde quieras… pero hazte un favor y sigue esta norma:
>
> **Las dudas y anotaciones sobre una práctica van en un fichero tuyo dentro de esa carpeta, llamado `MIS_NOTAS.md`.** No encima de mi texto.
>
> ¿Por qué? Porque el día que quieras comparar tu versión con la mía —o que yo te pase una corrección— **tus cosas y las mías estarán en ficheros distintos** y no habrá nada que desenredar. Cuesta lo mismo y te ahorra líos.
>
> *(Y no confundas esto con tus **apuntes**: la entrada de cada fase, con sus respuestas y su vídeo, sigue yendo a `00_Apuntes/Trimestre_1/`. `MIS_NOTAS.md` es para el "ojo, aquí me atasqué".)*

### 📖 Diccionario de Conceptos Clave

> [!quote] Terminología
> - **Plantilla:** repositorio pensado para sacar copias. · **`Use this template`:** crea **tu** copia, con historial propio.
> - **Repositorio público:** cualquiera lo lee; solo su dueño escribe.
> - **`.git`:** la carpeta oculta con el historial. **Es lo que convierte una carpeta en repositorio.**
> - **Clonar:** bajar un repositorio **con su `.git` dentro**. · **Descargar ZIP:** bajar **solo los ficheros**.

---

### 🛠️ Procedimiento Práctico

> [!example] Paso 0: Prepárate (todavía SIN grabar)
> Comprueba tu bóveda y tu autenticación. **Léete el procedimiento entero** (tiene **7 pasos** grabados). Ten **OBS** listo y tu **perfil de GitHub** en una pestaña.
> **Y antes de grabar: crea la entrada de apuntes de esta fase** (`b0-0.4.a-bajar-el-material.md`) con la estructura pegada y **vacía**. En el vídeo solo tienes que **enseñarla**, no rellenarla.

> [!example] Paso 1: Arranca la grabación y preséntate
> Inicia la grabación en **OBS**, preséntate, **enseña tu perfil de GitHub** 2-3 segundos y di qué vas a hacer.

> [!example] Paso 2: Prerrequisitos — tu copia, y clonarla por **SSH**
> Empieza por lo que tienes delante: **este mismo material**. A partir de hoy lo lees desde tu bóveda, sin navegador.
>
> **2A · Saca tu copia**
> 1. Entra en **`github.com/sor-iesjj/bloque-0-prerequisitos`**.
> 2. Pulsa **`Use this template`** → **`Create a new repository`**:
>    - **Owner:** tu usuario · **Repository name:** `bloque-0-prerequisitos` *(déjalo igual)* · **Visibility:** **`Public`**.
>    - **`Create repository`**.
> 3. Compruébalo y **enséñalo en el vídeo**: la dirección ahora es `github.com/TU-USUARIO/bloque-0-prerequisitos`. Ese repositorio **es tuyo**.
>
> **2B · Clónalo por SSH**
> 1. **`Code`** → pestaña **`SSH`** → **icono de copiar** 📋. Fíjate en que la dirección lleva **tu usuario**.
> 2. **Clic derecho sobre la carpeta `01_Practicas`** de tu bóveda → `Abrir Git Bash aquí` (Windows) / `Abrir en un terminal` (Linux). Y **comprueba dónde has caído antes de tocar nada**:
>    ```bash
>    pwd          # tiene que terminar en .../Boveda_SOR/01_Practicas
>    git clone git@github.com:TU-USUARIO/bloque-0-prerequisitos.git B0_Prerrequisitos
>    cd B0_Prerrequisitos
>    ls
>    ```
> 3. Ábrelo en **Obsidian**: ahí están las fases que has hecho estas semanas, dentro de tu bóveda.
>
> > [!tip] 💡 Fíjate en lo que acaba de pasar
> > **Te acabas de bajar el documento que estás leyendo.** Dilo en el vídeo, que tiene su gracia — y de paso demuestra que entiendes qué has descargado.

> [!example] Paso 3: Bloque 1 · Entorno — lo mismo, pero clonando por **HTTPS**
> **Exactamente el mismo procedimiento**, cambiando el repositorio de origen y la vía. Cuéntalo así en el vídeo: *"repito los mismos pasos, porque todo el material del curso se baja igual."*
>
> 1. En **`github.com/sor-iesjj/bloque-1-entorno`**: **`Use this template`** → **`Create a new repository`** → **Owner** tu usuario, **name** `bloque-1-entorno`, **Visibility** `Public` → **`Create repository`**.
> 2. **`Code`** → pestaña **`HTTPS`** → copiar 📋. La dirección ahora **empieza por `https://`**, no por `git@`.
> 3. En la misma terminal, **vuelve a `01_Practicas`** y clona:
>    ```bash
>    cd ..
>    pwd          # .../Boveda_SOR/01_Practicas
>    git clone https://github.com/TU-USUARIO/bloque-1-entorno.git B1_Entorno
>    cd B1_Entorno
>    ls
>    ```
>
> > [!success] ✅ Y no te ha pedido ni usuario ni contraseña. **Explica por qué en el vídeo**
> > No es que se te haya olvidado configurar algo: es que **el repositorio es público y bajarlo no requiere identificarse**. La clave SSH y el token sirven para **subir**.
> > Si no lo tienes claro, vuelve al punto 4 del Fundamento antes de seguir. Es la pregunta que te voy a hacer.

> [!example] Paso 4: 🔬 Boochan **en ZIP** — y por qué no vale
> Ahora el tercero, y aquí vamos a hacerlo **mal a propósito** para que veas la diferencia con tus propios ojos.
>
> 1. Entra en **`github.com/sor-iesjj/bloque-2-ubuntu-local`**.
> 2. **`Code`** → **`Download ZIP`**. Descomprímelo dentro de `01_Practicas/` y **renombra la carpeta** a `B2_Ubuntu_Local`.
> 3. Ábrela: **están todos los ficheros**. El manual, las fases, todo. Parece que ya está.
> 4. **Piénsalo dos segundos antes de seguir.** ¿Es esto lo mismo que clonar?
> 5. Abre la terminal **dentro de `B2_Ubuntu_Local`** y pregúntaselo a Git:
>    ```bash
>    pwd          # .../01_Practicas/B2_Ubuntu_Local
>    git status
>    ```
>    Responde:
>    ```
>    fatal: not a git repository (or any of the parent directories): .git
>    ```
>
> > [!danger] 🛑 Lo que te acaba de decir Git
> > **No es un repositorio. Son ficheros.** El ZIP trae el contenido pero **no trae la carpeta oculta `.git`**, que es donde vive el historial — y sin historial no hay `git status`, ni `git log`, ni `git restore`, ni forma de subir nada.
> >
> > | Con `clone` | Con ZIP |
> > | :--- | :--- |
> > | Ficheros **+ historial completo** | **Solo** los ficheros |
> > | Puedes recuperar lo que borres | Lo que borres, borrado está |
> > | Puedes subir tu trabajo | No puedes subir nada |
> >
> > En el Explorador las dos carpetas se ven **exactamente igual**. Por eso mucha gente se baja el ZIP pensando que ha hecho lo mismo, y se entera el día que la lía. **Tú te has enterado hoy, que sale más barato.**
>
> 6. **Borra la carpeta `B2_Ubuntu_Local` entera.** No sirve. Ahora se hace bien.

> [!example] Paso 5: Boochan, ahora bien — tu copia y clonar por **SSH**
> Tercera vez el mismo procedimiento. A estas alturas deberías poder contarlo tú antes de hacerlo.
>
> 1. En **`github.com/sor-iesjj/bloque-2-ubuntu-local`**: **`Use this template`** → **Owner** tu usuario, **name** `bloque-2-ubuntu-local`, **Visibility** `Public` → **`Create repository`**.
> 2. **`Code`** → **`SSH`** → copiar 📋.
> 3. Desde `01_Practicas/`:
>    ```bash
>    cd ..
>    pwd          # .../Boveda_SOR/01_Practicas
>    git clone git@github.com:TU-USUARIO/bloque-2-ubuntu-local.git B2_Ubuntu_Local
>    cd B2_Ubuntu_Local
>    git status
>    ```
>    Ahora `git status` **sí responde**: `working tree clean`. Compáralo en voz alta con lo que salía en el Paso 4.
>
> > [!tip] 💡 ¿Ves la diferencia con la Fase 0.3?
> > En la 0.3 creaste un repositorio **vacío** y **no había botón `Code`**. Aquí sí lo hay, en los tres. ¿Por qué? Porque estos **ya tienen contenido**.
> > El botón `Code` sirve para **bajarse** un repositorio. En la 0.3 no había nada que bajar (tú **subías**); aquí sí lo hay (tú **bajas**). Es la misma lógica al revés, y es exactamente la diferencia entre `push` y `clone`.

> [!example] Paso 6: Haz un cambio y súbelo (ciclo completo)
> Como `01_Practicas/B2_Ubuntu_Local/` está **dentro** de tu bóveda, Obsidian ya la ve. Crea ahí una nota `MIS_DATOS.md`:
> ```markdown
> # Mis datos
> - Alumno: Juan García
> - Grupo: 2º SMR
> ```
> Guarda y, en la terminal (dentro de `B2_Ubuntu_Local`):
> ```bash
> git status          # MIS_DATOS.md aparece como untracked
> git add .
> git commit -m "Anadir mis datos de alumno"
> git push
> ```
> Recarga tu repositorio `bloque-2-ubuntu-local` en GitHub: debe aparecer `MIS_DATOS.md`.
>
> > [!success] ✅ Comprobación: los tres son tuyos
> > Entra en los tres y enseña la dirección en el vídeo. En las tres tiene que poner **tu usuario**, no `sor-iesjj`. Desde la terminal se ve igual de claro:
> > ```bash
> > git remote -v
> > ```
> > **Si en alguna pone `sor-iesjj`, te saltaste el `Use this template`** y clonaste el mío: bórrala y repite el paso. Ese repositorio no te dejaría hacer `push` nunca.

> [!example] Paso 7: Cierra el vídeo, nómbralo y súbelo
> Detén la grabación, nombra el vídeo `B0.4.a · Bajar el material del curso` y súbelo a la playlist `B0_Prerrequisitos` (No listado), **con timestamps**:
> ```
> 00:00 Presentacion
> 00:40 Paso 2 - Prerrequisitos: mi copia + clonar por SSH
> 01:40 Paso 3 - Bloque 1: clonar por HTTPS (y por que no pide token)
> 02:40 Paso 4 - Boochan en ZIP: git status falla
> 03:40 Paso 5 - Boochan bien: Use this template + SSH
> 04:30 Paso 6 - add, commit, push
> ```
> Y **pega el enlace del vídeo en tu entrada de apuntes**, en el apartado `🔗 Enlaces`.

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | `git clone` por SSH da `Permission denied (publickey)`. | Tu clave SSH no está lista en ese equipo. | Repasa la **Bloque 0 · Fase 0.2.2**. **O** clona por **HTTPS**: tus copias son públicas y no piden nada. |
> | `fatal: not a git repository` dentro de la carpeta que acabo de bajar. | La bajaste en **ZIP**: no tiene `.git`. | Bórrala y **clónala**. Es justo la lección del Paso 4. |
> | La carpeta se llama `bloque-1-entorno` en vez de `B1_Entorno`. | Se te olvidó el **segundo argumento** del `clone`. | Bórrala y vuelve a clonar con el nombre al final. |
> | Las carpetas no aparecen en Obsidian. | Las clonaste fuera de la bóveda. | `pwd`: tienen que estar dentro de `.../Boveda_SOR/01_Practicas`. |
> | `git push` da `Permission denied` o `403`. | Clonaste **mi** repositorio en vez de tu copia. | `git remote -v`: la dirección debe llevar **TU usuario**. Si pone `sor-iesjj`, te saltaste el `Use this template`. |
> | Al clonar por HTTPS me pide usuario y contraseña. | Creaste tu copia como **`Private`**. | Ponla en `Public` (`Settings → General → Danger Zone → Change visibility`), o usa el token de la 0.2.2. |
> | `destination path already exists`. | La carpeta anterior no se borró del todo. | Bórrala por completo y repite el `clone`. |
> | No veo `Use this template`. | No has iniciado sesión en GitHub. | Inicia sesión; si sigue sin salir, avísame. |
> | La pantalla se queda atascada tras `git log` o `git diff` y no puedo escribir. | Estás dentro del **paginador**, no colgado. | Pulsa **`q`**. Es la misma tecla que en `man` y en todo Linux. |

> [!help] Preguntas Críticas
> 1. ¿Qué hace `Use this template`? Después de pulsarlo, **¿sobre qué repositorio trabajas**, el mío o el tuyo?
> 2. Te has bajado el Bloque 1 por HTTPS y **no te ha pedido contraseña**. ¿Por qué? ¿Cuándo sí te la habría pedido?
> 3. En el Explorador, la carpeta del ZIP y la carpeta clonada se ven **idénticas**. ¿Qué tiene una que no tiene la otra, y qué tres cosas dejas de poder hacer sin ella?
> 4. Anotas una duda en un fichero de la práctica, en el ordenador del aula. **¿Qué tienes que hacer para encontrarla el sábado en casa?**

---

### ✅ Checklist Final de la Fase 0.4.a

- [ ] Las **tres copias** creadas en tu cuenta con `Use this template`, públicas.
- [ ] `B0_Prerrequisitos` clonado **por SSH** dentro de `01_Practicas/` y visible en Obsidian.
- [ ] `B1_Entorno` clonado **por HTTPS** dentro de `01_Practicas/` y visible en Obsidian.
- [ ] ZIP de Boochan probado, `git status` fallando **enseñado en el vídeo**, y carpeta borrada.
- [ ] `B2_Ubuntu_Local` clonado **por SSH**, con `git status` respondiendo.
- [ ] `MIS_DATOS.md` creado y subido con `add` → `commit` → `push`; visible en GitHub.
- [ ] `git remote -v` comprobado en los tres: **todos con tu usuario**.
- [ ] Las tres carpetas se llaman `B0_Prerrequisitos`, `B1_Entorno` y `B2_Ubuntu_Local` — **ninguna con el nombre del repositorio**.
- [ ] Vídeo `B0.4.a · Bajar el material del curso` subido a la playlist, con timestamps.
- [ ] **Enlace del vídeo pegado en tu entrada de apuntes** de esta fase.
- [ ] Grabada **🏫 en el centro**.

> **Siguiente paso:** Fase 0.4.b — **Tres retos**: romper lo que acabas de bajar y recuperarlo. Y descubrir qué es lo único que no vuelve.
