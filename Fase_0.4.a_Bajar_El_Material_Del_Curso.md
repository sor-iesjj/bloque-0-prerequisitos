## 📦 Fase 0.4.a: Bajar el Material del Curso

### Tres repositorios, tres formas de bajarlos — y por qué no todas valen igual

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

- [ ] Bajar los **tres** repositorios con los que vas a trabajar el primer trimestre.
- [ ] Bajar cada uno por **una vía distinta**: **SSH**, **HTTPS** y **descarga en ZIP**.
- [ ] Explicar por qué el **ZIP no sirve** aunque los ficheros se vean igual.
- [ ] Distinguir el material que **solo lees** del material que **trabajas y entregas**, y por qué uno se **clona** y el otro se **copia con `Use this template`**.
- [ ] Hacer un cambio en tu copia y subirlo con `git status` → `add` → `commit` → `push`.

---

### 🎯 ¿Dónde Estamos?

> [!info] El Punto de Partida
> Tienes la bóveda, la cuenta de GitHub, la autenticación y tu repositorio de apuntes funcionando. Lo que **no** tienes todavía es el material del curso en tu ordenador: hasta hoy lo has leído por donde te lo he ido pasando. Hoy se baja, y se queda dentro de tu bóveda para siempre.

> [!warning] El Problema
> Bajarse ficheros de Internet sabe hacerlo cualquiera. Lo que hoy vas a aprender es que **hay varias formas de bajarse un repositorio y no dan el mismo resultado**, aunque en el Explorador se vean idénticas. La diferencia no se nota hoy: se nota el día que borras algo sin querer. *(Que es, literalmente, la fase siguiente.)*

---

### 📚 Fundamento Teórico

> [!important] 1. Hoy bajas TRES repositorios, y NO todos se bajan igual
> Estos tres:
>
> | Nº | Qué es | Carpeta en tu bóveda | Tu relación con él |
> | :---: | :--- | :--- | :--- |
> | **1** | **Prerrequisitos** — esto que estás leyendo | `B0_Prerrequisitos` | **Solo lo lees** |
> | **2** | **Bloque 1 · Entorno** — lo que viene después | `B1_Entorno` | **Solo lo lees** |
> | **3** | **Bloque 2 · Ubuntu local** — el proyecto Boochan | `B2_Ubuntu_Local` | **Trabajas dentro y me lo entregas** |
>
> Y de esa última columna sale todo lo demás. Fíjate bien, porque es la idea de la fase:
>
> | Si el material… | Qué haces | Por qué |
> | :--- | :--- | :--- |
> | **solo lo lees** *(1 y 2)* | **`git clone`** de mi repositorio | No necesitas una copia tuya en GitHub: no vas a subir nada ahí. Tus apuntes van a `apuntes-sor-t1`, como siempre |
> | **lo trabajas y lo entregas** *(3)* | **`Use this template`** y luego clonas **tu copia** | Vas a escribir dentro y hacer `push`. Para eso el repositorio tiene que ser **tuyo** |
>
> > [!success] 🔒 Y no puedes estropear mi material ni queriendo
> > **No eres colaborador de mis repositorios.** Puedes bajártelos las veces que quieras, pero un `push` contra ellos te lo rechaza GitHub con un error `403`. Trabaja tranquilo: **no hay forma de que la líes en el material del curso.**

> [!info] 2. Las tres formas de bajarse un repositorio
> Son las tres que vas a usar hoy, una por repositorio, a propósito:
>
> | Vía | Qué escribes | ¿Trae el historial? | ¿Pide identificarte? |
> | :--- | :--- | :---: | :--- |
> | **SSH** | `git clone git@github.com:…` | ✅ Sí | Sí — con **tu clave** de la Fase 0.2.2 |
> | **HTTPS** | `git clone https://github.com/…` | ✅ Sí | **Para bajar, no.** Para subir, sí |
> | **Descargar ZIP** | Botón `Code` → `Download ZIP` | ❌ **No** | No |
>
> **Las dos primeras te traen un repositorio. La tercera te trae unos ficheros sueltos.** Parecen lo mismo en el Explorador y no lo son, y lo vas a comprobar tú en el Paso 4.

> [!abstract] 3. Por qué el HTTPS no te pide contraseña para bajar
> Porque **mis repositorios del curso son públicos**: cualquiera puede leerlos, igual que cualquiera puede leer una página web sin registrarse.
>
> Identificarse hace falta para **escribir**, no para **leer**. Por eso:
>
> | Qué haces | ¿Hace falta identificarse? |
> | :--- | :--- |
> | `git clone` de un repositorio público | **No** |
> | `git push` a un repositorio, aunque sea tuyo | **Siempre** |
>
> Ahí es donde entran la clave SSH y el token de la **Bloque 0 · Fase 0.2.2**: no son para bajar cosas, **son para poder subirlas**.

> [!abstract] 4. Clonar vs. Push, y el segundo argumento
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

### 📖 Diccionario de Conceptos Clave

> [!quote] Terminología
> - **Repositorio público:** cualquiera lo lee; solo su dueño escribe. · **Plantilla:** repositorio pensado para sacar copias.
> - **`Use this template`:** crea en **tu** cuenta un repositorio **nuevo e independiente**, con el mismo contenido pero **historial propio**.
> - **`.git`:** la carpeta oculta con el historial. **Es lo que convierte una carpeta en repositorio.**
> - **Clonar:** bajar un repositorio **con su `.git` dentro**. · **Descargar ZIP:** bajar **solo los ficheros**.

---

### 🛠️ Procedimiento Práctico

> [!example] Paso 0: Prepárate (todavía SIN grabar)
> Comprueba tu bóveda y tu autenticación. **Léete el procedimiento entero** (tiene **7 pasos** grabados). Ten **OBS** listo y tu **perfil de GitHub** en una pestaña.
> **Y antes de grabar: crea la entrada de apuntes de esta fase** (`b0-0.4.a-bajar-el-material.md`) con la estructura pegada y **vacía**. En el vídeo solo tienes que **enseñarla**, no rellenarla.

> [!example] Paso 1: Arranca la grabación y preséntate
> Inicia la grabación en **OBS**, preséntate, **enseña tu perfil de GitHub** 2-3 segundos y di qué vas a hacer.

> [!example] Paso 2: Prerrequisitos, por **SSH**
> Empieza por lo que tienes delante: **este mismo material**. A partir de hoy lo lees desde tu bóveda, sin navegador.
>
> 1. Entra en **`github.com/sor-iesjj/bloque-0-prerequisitos`**.
> 2. Pulsa el botón verde **`Code`** → pestaña **`SSH`** → **icono de copiar** 📋.
> 3. **Clic derecho sobre la carpeta `01_Practicas`** de tu bóveda → `Abrir Git Bash aquí` (Windows) / `Abrir en un terminal` (Linux). Y **comprueba dónde has caído antes de tocar nada**:
>    ```bash
>    pwd          # tiene que terminar en .../Boveda_SOR/01_Practicas
>    git clone git@github.com:sor-iesjj/bloque-0-prerequisitos.git B0_Prerrequisitos
>    cd B0_Prerrequisitos
>    ls
>    ```
> 4. Ábrelo en **Obsidian**: ahí están las fases que has hecho estas semanas, dentro de tu bóveda.
>
> > [!tip] 💡 Fíjate en lo que acaba de pasar
> > **Te acabas de bajar el documento que estás leyendo.** Dilo en el vídeo, que tiene su gracia — y de paso demuestra que entiendes qué has descargado.
>
> > [!warning] ⚠️ Aquí **no** hay `Use this template`, aunque el botón esté
> > Este material **solo lo lees**: tus apuntes de estas fases ya están en `apuntes-sor-t1`, que es lo que me entregas. No necesitas una copia tuya de mi repositorio, así que **clonas el mío directamente**.
> >
> > Y ojo a un detalle que sale en el `clone`: la dirección lleva **`sor-iesjj`**, que soy yo — no tu usuario. Es la primera vez en todo el curso que clonas algo que **no es tuyo**.

> [!example] Paso 3: Bloque 1 · Entorno, por **HTTPS**
> Lo mismo, por la otra vía. Es lo que trabajaremos en cuanto acabemos los prerrequisitos.
>
> 1. Entra en **`github.com/sor-iesjj/bloque-1-entorno`**.
> 2. **`Code`** → pestaña **`HTTPS`** → **icono de copiar** 📋. Fíjate en que la dirección **empieza por `https://`**, no por `git@`.
> 3. En la misma terminal, **vuelve a `01_Practicas`** y clona:
>    ```bash
>    cd ..
>    pwd          # .../Boveda_SOR/01_Practicas
>    git clone https://github.com/sor-iesjj/bloque-1-entorno.git B1_Entorno
>    cd B1_Entorno
>    ls
>    ```
>
> > [!success] ✅ Y no te ha pedido ni usuario ni contraseña. **Explica por qué en el vídeo**
> > No es que se te haya olvidado configurar algo: es que **el repositorio es público y bajarlo no requiere identificarse**. La clave SSH y el token sirven para **subir**.
> > Si no lo tienes claro, vuelve al punto 3 del Fundamento antes de seguir. Es la pregunta que te voy a hacer.

> [!example] Paso 4: 🔬 Bloque 2 · Boochan, **en ZIP** — y por qué no vale
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

> [!example] Paso 5: Ahora sí — `Use this template` y clonar TU copia
> Este material es distinto a los dos anteriores: **vas a trabajar dentro y me lo vas a entregar.** Así que necesitas que el repositorio sea **tuyo**.
>
> 1. En **`github.com/sor-iesjj/bloque-2-ubuntu-local`**, pulsa **`Use this template`** → **`Create a new repository`**:
>    - **Owner:** tu usuario · **Repository name:** `bloque-2-ubuntu-local` · **Visibility:** la que indique el profesor.
>    - **`Create repository`**.
> 2. Compruébalo y **enséñalo en el vídeo**: la dirección ahora es `github.com/TU-USUARIO/bloque-2-ubuntu-local`. Ese repositorio **es tuyo**, con su historial propio.
> 3. **`Code`** → pestaña **`SSH`** → copiar 📋. Ahora la dirección lleva **tu usuario**, no `sor-iesjj`.
> 4. Desde `01_Practicas/`:
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

> [!example] Paso 6: Haz un cambio en TU copia y súbelo (ciclo completo)
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
> > [!question] 🤔 Y ahora la pregunta buena, para el vídeo
> > **¿Podrías hacer este mismo `push` dentro de `B1_Entorno`?** Pruébalo si quieres — Git te va a contestar con un `403`.
> > Y no es un fallo tuyo: **ese repositorio es mío.** Ahí está toda la diferencia entre clonar mi material y sacar tu copia con `Use this template`.

> [!example] Paso 7: Cierra el vídeo, nómbralo y súbelo
> Detén la grabación, nombra el vídeo `B0.4.a · Bajar el material del curso` y súbelo a la playlist `B0_Prerrequisitos` (No listado), **con timestamps**:
> ```
> 00:00 Presentacion
> 00:40 Paso 2 - Prerrequisitos por SSH
> 01:40 Paso 3 - Bloque 1 por HTTPS (y por que no pide token)
> 02:40 Paso 4 - Boochan en ZIP: git status falla
> 03:40 Paso 5 - Use this template + clonar mi copia
> 04:30 Paso 6 - add, commit, push
> ```
> Y **pega el enlace del vídeo en tu entrada de apuntes**, en el apartado `🔗 Enlaces`.

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | `git clone` por SSH da `Permission denied (publickey)`. | Tu clave SSH no está lista en ese equipo. | Repasa la **Bloque 0 · Fase 0.2.2**. **O** clona ese repositorio por **HTTPS**: es público y no pide nada. |
> | `fatal: not a git repository` dentro de la carpeta que acabo de bajar. | La bajaste en **ZIP**: no tiene `.git`. | Bórrala y **clónala**. Es justo la lección del Paso 4. |
> | La carpeta se llama `bloque-1-entorno` en vez de `B1_Entorno`. | Se te olvidó el **segundo argumento** del `clone`. | Bórrala y vuelve a clonar con el nombre al final. |
> | Las carpetas no aparecen en Obsidian. | Las clonaste fuera de la bóveda. | `pwd`: tienen que estar dentro de `.../Boveda_SOR/01_Practicas`. |
> | `git push` da `Permission denied` o `403` en `B0_Prerrequisitos` o `B1_Entorno`. | **Son míos.** Tú no escribes ahí. | No es un error a arreglar: es así a propósito. Tu trabajo va a `apuntes-sor-t1`. |
> | `git push` da `403` en `B2_Ubuntu_Local`. | Clonaste **mi** repositorio en vez de tu copia. | `git remote -v`: la dirección debe llevar **TU usuario**. Si pone `sor-iesjj`, te saltaste el `Use this template`. |
> | `destination path already exists`. | La carpeta anterior no se borró del todo. | Bórrala por completo y repite el `clone`. |
> | No veo `Use this template`. | No has iniciado sesión en GitHub. | Inicia sesión; si sigue sin salir, avísame. |
> | La pantalla se queda atascada tras `git log` o `git diff` y no puedo escribir. | Estás dentro del **paginador**, no colgado. | Pulsa **`q`**. Es la misma tecla que en `man` y en todo Linux. |

> [!help] Preguntas Críticas
> 1. Te has bajado el Bloque 1 por HTTPS y **no te ha pedido contraseña**. ¿Por qué? ¿Cuándo sí te la habría pedido?
> 2. En el Explorador, la carpeta del ZIP y la carpeta clonada se ven **idénticas**. ¿Qué tiene una que no tiene la otra, y qué tres cosas dejas de poder hacer sin ella?
> 3. ¿Por qué de los tres repositorios solo uno lleva `Use this template`? Contéstalo mirando **qué haces tú** con cada uno.

---

### ✅ Checklist Final de la Fase 0.4.a

- [ ] `B0_Prerrequisitos` clonado **por SSH** dentro de `01_Practicas/` y visible en Obsidian.
- [ ] `B1_Entorno` clonado **por HTTPS** dentro de `01_Practicas/` y visible en Obsidian.
- [ ] ZIP de Boochan probado, `git status` fallando **enseñado en el vídeo**, y carpeta borrada.
- [ ] Copia de la plantilla creada (`bloque-2-ubuntu-local` **en tu cuenta**).
- [ ] `B2_Ubuntu_Local` clonado **por SSH desde tu copia**, con `git status` respondiendo.
- [ ] `MIS_DATOS.md` creado y subido con `add` → `commit` → `push`; visible en GitHub.
- [ ] Las tres carpetas se llaman `B0_Prerrequisitos`, `B1_Entorno` y `B2_Ubuntu_Local` — **ninguna con el nombre del repositorio**.
- [ ] Vídeo `B0.4.a · Bajar el material del curso` subido a la playlist, con timestamps.
- [ ] **Enlace del vídeo pegado en tu entrada de apuntes** de esta fase.
- [ ] Grabada **🏫 en el centro**.

> **Siguiente paso:** Fase 0.4.b — **Tres retos**: romper lo que acabas de bajar y recuperarlo. Y descubrir qué es lo único que no vuelve.
