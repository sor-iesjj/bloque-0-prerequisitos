## 📦 Fase 0.4: Bajar el Material del Curso y el Ciclo de Trabajo con Git

### Dos repositorios, dos relaciones distintas — y qué pasa cuando los borras

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~1,5 horas · **Requisitos:** Fases 0.1, 0.2.1 y 0.2.2 completas.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin.
> 1. **Prepárate primero (sin grabar):** comprueba lo necesario, **léete el procedimiento entero** y **crea la entrada de apuntes de esta fase** en Obsidian: fichero `fase-0.4-bajar-el-material.md` con la estructura de la Fase 0.1, **vacía**. Rellenarla es cosa tuya, después; hoy solo tiene que existir.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a explicar la Fase 0.4 — Bajar el material del curso con Git."* Y **muestra tu perfil de GitHub** (o tu Teams/correo). Di qué vas a hacer.
> 3. **Graba TODO**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `Fase 0.4 — Bajar el material del curso` y súbelo a tu playlist **`B0_Prerrequisitos`** (No listado).
> 6. **~9-10 min** (esta fase lleva **tres retos** al final). Se graba en **🏫 el centro**.
> 7. **La entrega va por la TAREA de Teams.** Cuando toque, abriré una tarea que cubrirá **esta fase y otras**; te llegará notificación. Tú, hoy: graba, sube el vídeo a la playlist y **pega su enlace en tu entrada de apuntes**.
> 8. **El enlace del vídeo va DENTRO de tu entrada de apuntes**, en el apartado `Enlace al vídeo explicativo`. No lo guardes en un papel: va ahí.

---

### 🎯 Objetivos de la fase

- [ ] Distinguir **material del curso** (solo lectura) de **tu copia de trabajo** (tuya, con `push`).
- [ ] Explicar qué es una **plantilla** de repositorio y qué hace "Use this template".
- [ ] **Clonar el Bloque 1** (el material de las próximas semanas) y **crear tu copia de `boochan-1`**.
- [ ] Hacer un cambio y subirlo con `git status` → `add` → `commit` → `push`.
- [ ] **Recuperar ficheros borrados** con `git restore`, sin Internet.
- [ ] **Reconstruir el repositorio entero** clonando, cuando ya no queda ni el historial.
- [ ] Explicar **por qué** el segundo caso no se arregla como el primero.
- [ ] Demostrar que **lo que escribes en material ajeno no se recupera**, y deducir dónde tienen que vivir tus apuntes.

---

### 📚 Fundamento Teórico

> [!important] 1. Hoy bajas DOS repositorios, y no son iguales
> Es lo más importante de esta fase y lo que más se confunde. Los dos vienen de mí, pero tu relación con ellos es **distinta**:
>
> | | **Bloque 1 — Entorno** | **Boochan** |
> | :--- | :--- | :--- |
> | Qué es | El material de las **próximas semanas** | La práctica grande, para más adelante |
> | Cómo lo bajas | **`git clone`** directo | **`Use this template`** y luego clonas **tu copia** |
> | ¿De quién es el repo? | **Mío.** Tú tienes una copia local | **Tuyo.** Está en tu cuenta de GitHub |
> | ¿Puedes hacer `push`? | **NO.** No eres colaborador | **SÍ.** Es tu repositorio |
> | Si escribes algo dentro | **no se guarda en ningún sitio** | se guarda al hacer `push` |
>
> **¿Por qué esta diferencia?** Porque el Bloque 1 es **documentación que yo mantengo**: si mañana corrijo una errata, quiero que la corrección sea mía y llegue a todos. Boochan es un **proyecto que tú construyes**: necesitas un sitio propio donde guardar tu trabajo.
>
> > [!danger] ⚠️ Entonces, ¿dónde escribo yo?
> > **En tu repositorio de apuntes.** Siempre. Las respuestas, las dudas, los enlaces de vídeo y tus notas van a `00_Apuntes/`, que es **tuyo** y sí se sube.
> > El material del curso **no se toca**: si crees que hay un error, dímelo y lo corrijo yo en el original. Lo de la Fase 0.1 —*"tus apuntes son tuyos, las prácticas son material del curso"*— empieza a tener sentido justo aquí.

> [!info] 2. Plantilla y "Use this template"
> Una **plantilla** es un repositorio pensado para sacar copias. Al pulsar **"Use this template"**, GitHub crea en **tu** cuenta un repositorio **nuevo e independiente** con el mismo contenido pero **historial propio**. No es un enlace a la plantilla del profesor: es **tuyo**.
>
> **Y por eso el Bloque 1 no lo tiene:** ese repo **no es plantilla**, así que en su página no verás ese botón. Solo `Code` → clonar.

> [!abstract] 3. Clonar vs. Push
> - **`git clone`** (GitHub → tu ordenador): **una sola vez**, para bajar el repo.
> - **`git push`** (tu ordenador → GitHub): **cada vez** que subes cambios.
> Regla: **clonas una vez**, luego trabajas con push/pull. Y al clonar, el remoto ya viene configurado (no hace falta `git init`).

---

### 🛠️ Procedimiento Práctico

> [!example] Paso 0: Prepárate (todavía SIN grabar)
> Comprueba tu bóveda y tu autenticación. **Léete el procedimiento** (tiene **10 pasos** grabados: los 6 primeros son el ciclo normal y los **tres siguientes son retos** en los que romperás lo que acabas de bajar). Ten **OBS** listo y tu **perfil de GitHub** en una pestaña.
> **Y antes de grabar: crea la entrada de apuntes de esta fase** (`fase-0.4-bajar-el-material.md`) con la estructura pegada y **vacía**. En el vídeo solo tienes que **enseñarla**, no rellenarla.

> [!example] Paso 1: Arranca la grabación y preséntate
> Inicia la grabación en **OBS**, preséntate, **enseña tu perfil de GitHub** 2-3 segundos y di qué vas a hacer.

> [!example] Paso 2: Baja el material del Bloque 1 (lo que viene ahora)
> Esto es lo que vamos a usar **las próximas semanas**, así que empieza por aquí. Es un repositorio **mío**: solo lo clonas.
>
> 1. Entra en `github.com/sor-iesjj/bloque-1-entorno` y **fíjate en el botón verde**: pone `Code`, y **no hay ningún `Use this template`**. Dilo en voz alta: *"este repositorio no es una plantilla, así que no puedo sacar una copia propia: solo puedo clonarlo."*
> 2. `Code` → pestaña **`HTTPS`** → copiar. *(Aquí sí usamos HTTPS: como no vas a subir nada, no hace falta tu clave SSH.)*
> 3. Clic derecho sobre **`01_Practicas`** → abrir la terminal ahí, y:
>    ```bash
>    pwd          # .../Boveda_SOR/01_Practicas
>    git clone https://github.com/sor-iesjj/bloque-1-entorno.git
>    cd bloque-1-entorno
>    ls
>    ```
> 4. Ábrelo en Obsidian: ya puedes leer las prácticas del Bloque 1 **dentro de tu bóveda**, sin ir al navegador.
>
> > [!warning] ⚠️ Aquí no escribas nada
> > Este material es mío y **tú no puedes subir cambios**. Si editas un fichero, ese cambio vive **solo en tu ordenador** y se pierde en cuanto pase cualquier cosa (lo comprobarás en el Reto 3). Tus notas van a `00_Apuntes/`.

> [!example] Paso 3: Crea tu copia de la plantilla Boochan en GitHub
> En `github.com/sor-iesjj/boochan-v1`, pulsa **`Use this template` → Create a new repository**: **Owner** tu usuario, **name** `boochan-1`, **Visibility** la que indique el profesor. **Create repository**. Ahora sí: pulsa el botón verde **`Code`**, pestaña **`SSH`**, y copia tu dirección (`git@github.com:TU-USUARIO/boochan-1.git`).
>
> > [!tip] 💡 ¿Ves la diferencia con la Fase 0.3?
> > En la 0.3 creaste un repositorio **vacío** y **no había botón `Code`**. Aquí sí lo hay. ¿Por qué? Porque este repo **ya tiene contenido**: lo has copiado de una plantilla que trae el manual y las fases dentro.
> > El botón `Code` sirve para **bajarse** un repositorio. En la 0.3 no había nada que bajar (tú **subías**); aquí sí lo hay (tú **bajas**). Es la misma lógica al revés, y es exactamente la diferencia entre `push` y `clone`.

> [!example] Paso 4: Clona TU copia de Boochan dentro de `01_Practicas/`
> Igual que en la Fase 0.3: **clic derecho sobre la carpeta `01_Practicas` de tu bóveda** → `Abrir Git Bash aquí` (Windows) / `Abrir en un terminal` (Linux). Comprueba dónde estás **antes de clonar**:
> ```bash
> pwd          # tiene que terminar en .../Boveda_SOR/01_Practicas
> git clone git@github.com:TU-USUARIO/boochan-1.git
> cd boochan-1
> ls
> ```
> Debes ver los ficheros de la práctica (`Manual_BoochanV1.md`, `Fases/`…).
> > [!danger] ⚠️ Comprueba con `pwd` que clonas dentro de `.../Boveda_SOR/01_Practicas`.

> [!example] Paso 5: Ábrela en Obsidian y haz un cambio
> Como `01_Practicas/boochan-1/` está **dentro** de tu bóveda, Obsidian ya la ve (apuntes y práctica en una sola ventana). Crea ahí una nota `MIS_DATOS.md`:
> ```markdown
> # Mis datos
> - Alumno: Juan García
> - Grupo: 2º SMR
> ```
> Guarda y, en la terminal (dentro de `boochan-1`), mira el cambio:
> ```bash
> git status
> ```
> `MIS_DATOS.md` aparece como **untracked**.

> [!example] Paso 6: Sube el cambio (ciclo completo)
> ```bash
> git add .
> git commit -m "Anadir mis datos de alumno"
> git push
> ```
> Recarga tu repo `boochan-1` en GitHub: debe aparecer `MIS_DATOS.md`.

> [!example] 🔬 Paso 7 — RETO 1: bórralo y recupéralo (sin Internet)
> Ahora que tienes tu copia y ya sabes hacer `commit`, vamos a romperla a propósito. **Sigue grabando.**
>
> 1. En el Explorador, entra en `boochan-1/Fases/` y **borra TODOS los ficheros de fase**. Todos. Guarda y mira la carpeta vacía.
> 2. En la terminal, **dentro de `boochan-1`**, mira qué opina Git:
>    ```bash
>    git status
>    ```
>    Verás tus fases marcadas con **`D`** (de *deleted*). Git sabe perfectamente lo que falta.
> 3. **Piénsalo dos segundos antes de leer la solución.** ¿Necesitas Internet para recuperarlas? ¿Necesitas volver a GitHub?
>
> > [!success] ✅ Solución del Reto 1
> > **No hace falta Internet.** Un comando:
> > ```bash
> > git restore .
> > ```
> > ⚠️ **El punto no es decorativo.** Si escribes `git restore` a secas, Git responde `fatal: you must specify path(s) to restore`: no adivina qué quieres recuperar. El `.` significa *"todo lo que hay desde donde estoy hacia abajo"*.
> > Comprueba con `git status`: vuelve a decir `working tree clean`. Y las fases están otra vez ahí.
> >
> > **¿Por qué ha funcionado?** Porque al clonar te trajiste **también el historial**, que vive en la carpeta oculta `.git` dentro de `boochan-1`. Esos ficheros estaban guardados ahí, en tu propio ordenador. `git restore` los ha copiado de vuelta.
> > Dilo en voz alta en el vídeo: *"he recuperado el material sin conectarme a nada, porque el historial está en mi equipo."*

> [!example] 🔬 Paso 8 — RETO 2: ahora bórralo TODO (y aquí sí cambia la cosa)
> El reto anterior fue fácil. Este no se arregla igual. **Sigue grabando.**
>
> 1. Cierra Obsidian.
> 2. Borra **la carpeta `boochan-1` ENTERA**, con todo dentro. Sí, la carpeta completa.
> 3. Abre la terminal en `01_Practicas/` y prueba el truco de antes:
>    ```bash
>    git status
>    ```
>    Responde:
>    ```
>    fatal: not a git repository (or any of the parent directories): .git
>    ```
> 4. **Explica en voz alta por qué el Reto 1 ya no sirve.** Si no lo ves, la pista está en la respuesta de Git.
>
> > [!success] ✅ Solución del Reto 2
> > **Aquí Git en tu ordenador no puede hacer nada**, y la razón es esta: la carpeta oculta `.git` —tu historial, tu máquina del tiempo— **estaba DENTRO de `boochan-1`**. Al borrar la carpeta, la has borrado con ella. `git restore` no existe si no hay repositorio.
> >
> > Lo único que queda está **fuera de tu ordenador**: en GitHub. Así que se vuelve a clonar. Desde `01_Practicas/`:
> > ```bash
> > pwd          # .../Boveda_SOR/01_Practicas
> > git clone git@github.com:TU-USUARIO/boochan-1.git
> > ```
> > En segundos lo tienes todo otra vez: el manual, las fases **y tu historial completo** (`git log --oneline` lo demuestra).
> >
> > > [!important] 🔍 Fíjate en un detalle que lo explica todo
> > > **`MIS_DATOS.md` también ha vuelto.** ¿Por qué? Porque en el Paso 5 hiciste `push`. Estaba en GitHub.
> > > Si lo hubieras creado y **no** lo hubieras empujado, ahora no estaría. Se habría perdido para siempre, junto con la carpeta.
> > > **Esa es toda la lección:** lo que está en GitHub sobrevive; lo que solo está en tu ordenador, no. Por eso `push` al terminar cada sesión.
>
> > [!note] 📌 Esto lo volveremos a ver, y con calma
> > Los dos retos de hoy son un aperitivo, hechos deprisa sobre una práctica que acabas de clonar. En la **Fase 0.7** los repetiremos **sobre todo tu trabajo del curso** —apuntes incluidos—, con la teoría detrás y las comprobaciones de seguridad que hoy nos hemos saltado porque aquí no arriesgabas nada.

> [!example] 🔬 Paso 9 — RETO 3: el mismo desastre, pero con el material del Bloque 1
> Los dos retos anteriores han ido bien. Vamos a repetir **exactamente lo mismo** con la otra carpeta, la de `bloque-1-entorno`. Parece igual. **No lo es.**
>
> 1. Abre `01_Practicas/bloque-1-entorno/` en Obsidian y **escribe algo dentro**: crea un fichero `MIS_NOTAS_B1.md` con dos líneas, lo que quieras. Guarda.
> 2. Intenta subirlo, como has hecho con Boochan:
>    ```bash
>    git add .
>    git commit -m "Mis notas del bloque 1"
>    git push
>    ```
> 3. **Lee el error en voz alta.** Git te dirá algo parecido a:
>    ```
>    remote: Permission to sor-iesjj/bloque-1-entorno.git denied
>    fatal: unable to access ... 403
>    ```
> 4. Ahora **borra la carpeta `bloque-1-entorno` entera** y vuelve a clonarla:
>    ```bash
>    pwd          # .../Boveda_SOR/01_Practicas
>    git clone https://github.com/sor-iesjj/bloque-1-entorno.git
>    ```
> 5. **Busca tu `MIS_NOTAS_B1.md`.**
>
> > [!success] ✅ Solución del Reto 3 — y la conclusión de la fase
> > **El material ha vuelto entero. Tus notas, no.** Y no hay ningún comando que las traiga: no existían en ningún sitio salvo en la carpeta que acabas de borrar.
> >
> > ¿Por qué con Boochan sí y aquí no? Porque `boochan-1` **es tuyo** y pudiste hacer `push`; `bloque-1-entorno` **es mío** y el `push` te lo rechazó con un `403`. Sin `push` no hay copia fuera. Sin copia fuera, no hay recuperación.
> >
> > | | Boochan (tuyo) | Bloque 1 (mío) |
> > | :--- | :--- | :--- |
> > | Recuperas **el material** | ✅ clonando | ✅ clonando |
> > | Recuperas **lo que tú escribiste** | ✅ *si hiciste `push`* | ❌ **nunca** |
> >
> > **Por eso tus apuntes van a `00_Apuntes/`, en tu propio repositorio.** No es una manía de ordenar carpetas: es el único sitio donde lo que escribes está a salvo.
> > Escríbelo así en tu entrada de hoy, con tus palabras. Es la respuesta que más peso tiene de esta fase.

> [!example] Paso 10: Cierra el vídeo, nómbralo y súbelo
> Detén la grabación, nombra el vídeo `Fase 0.4 — Clonar la práctica Boochan`, súbelo a la playlist `B0_Prerrequisitos` (No listado) y añade **timestamps**. Los dos retos llevan el suyo, que es lo que voy a mirar primero:
> ```
> 00:00 Presentacion
> 01:00 Paso 2 - Clonar el material del Bloque 1
> 02:00 Paso 3 - Use this template (Boochan)
> 03:00 Paso 4 - Clonar mi copia de Boochan
> 03:50 Paso 5 - MIS_DATOS.md
> 04:30 Paso 6 - add, commit, push
> 05:20 Paso 7 - RETO 1: borrar las fases y recuperarlas
> 06:40 Paso 8 - RETO 2: borrar boochan-1 entera y clonar
> 08:00 Paso 9 - RETO 3: lo mismo con el Bloque 1 (y aqui NO vuelve todo)
> 09:20 Paso 10 - Repaso final
> ```
>
> Y en tu **entrada de apuntes** de esta fase, además de las respuestas, contesta a esto con tus palabras: **¿por qué el Reto 2 no se arregla igual que el Reto 1, y por qué en el Reto 3 no vuelve todo?** Es la pregunta que resume la fase.

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | `git clone` da `Permission denied (publickey)`. | Usas SSH pero la clave no está lista. | Repasa la 0.2.2, **o** clona por HTTPS con tu token. |
> | La carpeta `boochan-1` no aparece en Obsidian. | La clonaste fuera de la bóveda. | Comprueba con `pwd`; clónala dentro de `01_Practicas/`. |
> | `git push` dice `nothing to commit`. | No hiciste `git add` o no guardaste. | Guarda en Obsidian, `git add .` y `git commit`. |
> | `fatal: you must specify path(s) to restore`. | Escribiste `git restore` **sin el punto**. Git no adivina qué quieres recuperar. | `git restore .` — el punto significa *"todo lo que hay desde aquí hacia abajo"*. Si estás dentro de `Fases/` recupera solo eso; desde la raíz del repo, recupera todo. |
> | `Permission ... denied` / `403` al hacer `push` en `bloque-1-entorno`. | **Es lo esperado**: ese repo no es tuyo. | Nada que arreglar: es justo lo que demuestra el Reto 3. Tus notas van a `00_Apuntes/`. |
> | `git restore .` no recupera nada. | No estás dentro de `boochan-1`. | `pwd`: tienes que estar dentro de la carpeta del repo, no en `01_Practicas`. |
> | Tras el Reto 2, `git clone` dice `destination path already exists`. | La carpeta no se borró del todo. | Bórrala por completo y repite. |
> | Tras el Reto 2 falta algo que yo había creado. | No le hiciste `push`. | No hay solución: no estaba en GitHub. Es justo la lección del reto. |
> | No veo "Use this template". | El repo no está como plantilla o no has iniciado sesión. | Inicia sesión; si sigue, avisa al profesor. |

> [!help] Preguntas Críticas
> 1. ¿Qué hace "Use this template"? ¿Trabajas sobre el repo del profesor o sobre tu copia?
> 2. ¿Cuántas veces se clona un repositorio? ¿Qué usas los demás días?
> 3. ¿Por qué al clonar no hace falta `git init`?

---

### ✅ Checklist Final de la Fase 0.4

- [ ] Copia de la plantilla creada (`boochan-1` en tu cuenta).
- [ ] Repo clonado dentro de `01_Practicas/boochan-1/` (se ve en Obsidian).
- [ ] `MIS_DATOS.md` creado y subido con `add` → `commit` → `push`; visible en GitHub.
- [ ] **Reto 1 resuelto:** fases borradas y recuperadas con `git restore`, explicando por qué no hizo falta Internet.
- [ ] **Reto 2 resuelto:** carpeta borrada entera y recuperada clonando, explicando por qué `git restore` ya no valía.
- [ ] **Reto 3 resuelto:** `push` rechazado con `403` en el Bloque 1, y comprobado que tus notas **no vuelven** tras clonar.
- [ ] `bloque-1-entorno` clonado dentro de `01_Practicas/` y visible en Obsidian.
- [ ] Vídeo `Fase 0.4 — Clonar la práctica Boochan` subido a la playlist, con timestamps.
- [ ] **Enlace del vídeo pegado en tu entrada de apuntes** de esta fase.
- [ ] Grabada **🏫 en el centro**.

> **Siguiente paso:** Fase 0.5 — Montar el mismo entorno **en casa** y sincronizar centro ↔ casa (va en 2 partes).
