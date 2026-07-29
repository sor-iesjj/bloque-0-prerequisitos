## 📦 Fase 0.4: Tu Copia de la Práctica Boochan y el Ciclo de Trabajo con Git

### Descargar la práctica, hacerla tuya y subir cambios

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~1,5 horas · **Requisitos:** Fases 0.1, 0.2.1 y 0.2.2 completas.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin.
> 1. **Prepárate primero (sin grabar):** comprueba lo necesario, **léete el procedimiento entero** y **crea la entrada de apuntes de esta fase** en Obsidian: fichero `fase-0.4-clonar-boochan.md` con la estructura de la Fase 0.1, **vacía**. Rellenarla es cosa tuya, después; hoy solo tiene que existir.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a explicar la Fase 0.4 — Clonar mi copia de la práctica Boochan."* Y **muestra tu perfil de GitHub** (o tu Teams/correo). Di qué vas a hacer.
> 3. **Graba TODO**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `Fase 0.4 — Clonar la práctica Boochan` y súbelo a tu playlist **`B0_Prerrequisitos`** (No listado).
> 6. **~7-8 min** (esta fase lleva dos retos al final). Se graba en **🏫 el centro**.
> 7. **La entrega va por la TAREA de Teams.** Cuando toque, abriré una tarea que cubrirá **esta fase y otras**; te llegará notificación. Tú, hoy: graba, sube el vídeo a la playlist y **pega su enlace en tu entrada de apuntes**.
> 8. **El enlace del vídeo va DENTRO de tu entrada de apuntes**, en el apartado `Enlace al vídeo explicativo`. No lo guardes en un papel: va ahí.

---

### 🎯 Objetivos de la fase

- [ ] Explicar qué es una **plantilla** de repositorio y qué hace "Use this template".
- [ ] Crear **tu propia copia** de `boochan-1` y **clonarla** dentro de `01_Practicas/`.
- [ ] Hacer un cambio y subirlo con `git status` → `add` → `commit` → `push`.
- [ ] **Recuperar ficheros borrados** con `git restore`, sin Internet.
- [ ] **Reconstruir el repositorio entero** clonando, cuando ya no queda ni el historial.
- [ ] Explicar **por qué** el segundo caso no se arregla como el primero.

---

### 📚 Fundamento Teórico

> [!info] 1. Plantilla y "Use this template"
> Una **plantilla** es un repositorio pensado para sacar copias. Al pulsar **"Use this template"**, GitHub crea en **tu** cuenta un repositorio **nuevo e independiente** con el mismo contenido pero **historial propio**. No es un enlace a la plantilla del profesor: es **tuyo**.

> [!abstract] 2. Clonar vs. Push
> - **`git clone`** (GitHub → tu ordenador): **una sola vez**, para bajar el repo.
> - **`git push`** (tu ordenador → GitHub): **cada vez** que subes cambios.
> Regla: **clonas una vez**, luego trabajas con push/pull. Y al clonar, el remoto ya viene configurado (no hace falta `git init`).

---

### 🛠️ Procedimiento Práctico

> [!example] Paso 0: Prepárate (todavía SIN grabar)
> Comprueba tu bóveda y tu autenticación. **Léete el procedimiento** (tiene **8 pasos** grabados: los 5 primeros son el ciclo normal y los **dos últimos son retos** en los que romperás tu copia a propósito). Ten **OBS** listo y tu **perfil de GitHub** en una pestaña.
> **Y antes de grabar: crea la entrada de apuntes de esta fase** (`fase-0.4-clonar-boochan.md`) con la estructura pegada y **vacía**. En el vídeo solo tienes que **enseñarla**, no rellenarla.

> [!example] Paso 1: Arranca la grabación y preséntate
> Inicia la grabación en **OBS**, preséntate, **enseña tu perfil de GitHub** 2-3 segundos y di qué vas a hacer.

> [!example] Paso 2: Crea tu copia de la plantilla en GitHub
> En `github.com/sor-iesjj/boochan-v1`, pulsa **`Use this template` → Create a new repository**: **Owner** tu usuario, **name** `boochan-1`, **Visibility** la que indique el profesor. **Create repository**. Ahora sí: pulsa el botón verde **`Code`**, pestaña **`SSH`**, y copia tu dirección (`git@github.com:TU-USUARIO/boochan-1.git`).
>
> > [!tip] 💡 ¿Ves la diferencia con la Fase 0.3?
> > En la 0.3 creaste un repositorio **vacío** y **no había botón `Code`**. Aquí sí lo hay. ¿Por qué? Porque este repo **ya tiene contenido**: lo has copiado de una plantilla que trae el manual y las fases dentro.
> > El botón `Code` sirve para **bajarse** un repositorio. En la 0.3 no había nada que bajar (tú **subías**); aquí sí lo hay (tú **bajas**). Es la misma lógica al revés, y es exactamente la diferencia entre `push` y `clone`.

> [!example] Paso 3: Clona tu copia dentro de `01_Practicas/`
> Igual que en la Fase 0.3: **clic derecho sobre la carpeta `01_Practicas` de tu bóveda** → `Abrir Git Bash aquí` (Windows) / `Abrir en un terminal` (Linux). Comprueba dónde estás **antes de clonar**:
> ```bash
> pwd          # tiene que terminar en .../Boveda_SOR/01_Practicas
> git clone git@github.com:TU-USUARIO/boochan-1.git
> cd boochan-1
> ls
> ```
> Debes ver los ficheros de la práctica (`Manual_BoochanV1.md`, `Fases/`…).
> > [!danger] ⚠️ Comprueba con `pwd` que clonas dentro de `.../Boveda_SOR/01_Practicas`.

> [!example] Paso 4: Ábrela en Obsidian y haz un cambio
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

> [!example] Paso 5: Sube el cambio (ciclo completo)
> ```bash
> git add .
> git commit -m "Anadir mis datos de alumno"
> git push
> ```
> Recarga tu repo `boochan-1` en GitHub: debe aparecer `MIS_DATOS.md`.

> [!example] 🔬 Paso 6 — RETO 1: bórralo y recupéralo (sin Internet)
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

> [!example] 🔬 Paso 7 — RETO 2: ahora bórralo TODO (y aquí sí cambia la cosa)
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

> [!example] Paso 8: Cierra el vídeo, nómbralo y súbelo
> Detén la grabación, nombra el vídeo `Fase 0.4 — Clonar la práctica Boochan`, súbelo a la playlist `B0_Prerrequisitos` (No listado) y añade **timestamps**. Los dos retos llevan el suyo, que es lo que voy a mirar primero:
> ```
> 00:00 Presentacion
> 00:30 Paso 2 - Use this template
> 01:20 Paso 3 - Clonar dentro de 01_Practicas
> 02:10 Paso 4 - MIS_DATOS.md
> 02:50 Paso 5 - add, commit, push
> 03:40 Paso 6 - RETO 1: borrar las fases y recuperarlas
> 05:10 Paso 7 - RETO 2: borrar la carpeta entera y clonar
> 07:00 Paso 8 - Repaso final
> ```
>
> Y en tu **entrada de apuntes** de esta fase, además de las respuestas, contesta a esto con tus palabras: **¿por qué el Reto 2 no se arregla igual que el Reto 1?** Es la pregunta que resume la fase.

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | `git clone` da `Permission denied (publickey)`. | Usas SSH pero la clave no está lista. | Repasa la 0.2.2, **o** clona por HTTPS con tu token. |
> | La carpeta `boochan-1` no aparece en Obsidian. | La clonaste fuera de la bóveda. | Comprueba con `pwd`; clónala dentro de `01_Practicas/`. |
> | `git push` dice `nothing to commit`. | No hiciste `git add` o no guardaste. | Guarda en Obsidian, `git add .` y `git commit`. |
> | `fatal: you must specify path(s) to restore`. | Escribiste `git restore` **sin el punto**. Git no adivina qué quieres recuperar. | `git restore .` — el punto significa *"todo lo que hay desde aquí hacia abajo"*. Si estás dentro de `Fases/` recupera solo eso; desde la raíz del repo, recupera todo. |
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
- [ ] Vídeo `Fase 0.4 — Clonar la práctica Boochan` subido a la playlist, con timestamps.
- [ ] **Enlace del vídeo pegado en tu entrada de apuntes** de esta fase.
- [ ] Grabada **🏫 en el centro**.

> **Siguiente paso:** Fase 0.5 — Montar el mismo entorno **en casa** y sincronizar centro ↔ casa (va en 2 partes).
