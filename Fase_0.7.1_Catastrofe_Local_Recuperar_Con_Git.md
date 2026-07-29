## 🕐 Fase 0.7.1: He Perdido Lo Que Escribí

### Git como máquina del tiempo: recuperar sin Internet

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0.7 — parte 1 de 2]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~1 hora · **Requisitos:** Fases 0.3 a 0.6 completas. Tus entradas de apuntes commiteadas.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin.
> 1. **Prepárate primero (sin grabar):** comprueba lo necesario, **léete el procedimiento entero** y **crea la entrada de apuntes de esta fase** en Obsidian: fichero `fase-0.7.1-catastrofe-local.md` con la estructura de la Fase 0.1, **vacía**. Rellenarla es cosa tuya, después; hoy solo tiene que existir.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a explicar la Fase 0.7.1 — He perdido lo que escribí."* Y **muestra tu perfil de GitHub**. Di qué vas a hacer.
> 3. **Graba TODO**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `Fase 0.7.1 — He perdido lo que escribí` y súbelo a tu playlist **`B0_Prerrequisitos`** (No listado).
> 6. **~5 min.** Se graba en **🏫 el centro**.
> 7. **La entrega va por la TAREA de Teams.** Cuando toque, abriré una tarea que cubrirá **esta fase y otras**; te llegará notificación. Tú, hoy: graba, sube el vídeo a la playlist y **pega su enlace en tu entrada de apuntes**.
> 8. **El enlace del vídeo va DENTRO de tu entrada de apuntes**, en el apartado `Enlace al vídeo explicativo`. No lo guardes en un papel: va ahí.

---

### 🎯 Objetivos

- [ ] Explicar qué es un **commit** en términos de "punto al que puedo volver".
- [ ] Leer un `git status` y un `git diff` y decir **qué se ha perdido** antes de tocar nada.
- [ ] Recuperar **todo** el trabajo perdido con `git restore`.
- [ ] Recuperar **un solo fichero**, dejando los demás como estaban.
- [ ] Decir con precisión **qué NO recupera** este método, y por qué.

---

### 🎯 ¿Dónde Estamos?

> [!info] El Punto de Partida
> Llevas seis fases haciendo `commit` porque yo te lo he mandado. Hoy vas a descubrir **para qué servía**.

> [!warning] El Problema
> Un martes cualquiera abres Obsidian y tus apuntes están **en blanco**. Los ficheros están, con su nombre correcto, pero vacíos. ¿Qué ha pasado? Puede ser mil cosas: un plugin de Obsidian que se volvió loco, un `Ctrl+A` + `Supr` sin darte cuenta, una sincronización a medias, un compañero con tu equipo abierto. **Da igual el motivo.** Lo que importa es qué haces ahora.
>
> Sin Git, la respuesta es: reescribirlo todo. Con Git, la respuesta son **dos comandos**.

> [!success] Objetivo de esta Fase
> Provocar el desastre **a propósito**, verlo con tus propios ojos, y arreglarlo. Sin Internet, sin GitHub, sin pedirle nada a nadie: solo con lo que tu ordenador ya tiene guardado.

---

### 📚 Fundamento Teórico

> [!info] Los tres sitios donde vive tu trabajo
> Esto es lo que hay que tener claro antes de tocar nada. Cuando trabajas con Git, **el mismo fichero existe en tres estados distintos**:
>
> | Dónde | Qué es | Quién lo cambia |
> | :--- | :--- | :--- |
> | **La carpeta de trabajo** | Lo que ves en Obsidian y en el Explorador. **Lo que acabas de romper** | Tú, cada vez que escribes |
> | **El último commit** | La última foto que guardaste. Está en la carpeta oculta `.git` | Tú, al hacer `git commit` |
> | **GitHub** | La copia en Internet | Tú, al hacer `git push` |
>
> Hoy solo trabajamos con los **dos primeros**. La carpeta de trabajo está rota; el último commit está intacto. Recuperar es simplemente **copiar del segundo al primero**.

> [!important] Un commit no es "subir": es un punto de restauración
> Esto es lo que más se malentiende. **`commit` no sube nada a Internet** — eso es `push`. Un commit es una **foto de tus ficheros guardada en tu propio ordenador**, dentro de la carpeta oculta `.git` que hay en `Trimestre_1`.
>
> Y como es una foto, **puedes volver a ella**. Por eso en la Fase 0.3 te hice hacer **un commit por fase** en vez de uno gordo: cada commit es un punto de restauración distinto. Hoy vas a cobrar esa inversión.

> [!warning] El fallo nº1: tocar antes de mirar
> Cuando ves tus apuntes en blanco, el impulso es **hacer algo ya**: cerrar Obsidian, reinstalar, escribir de nuevo, buscar en Google y pegar el primer comando que salga.
>
> **Para.** Lo primero de un técnico es **diagnosticar**: `git status` y `git diff` te dicen exactamente qué ha pasado y cuánto has perdido, **sin cambiar nada**. Los dos son comandos de **solo lectura**: no pueden estropear nada. Mira primero, actúa después.

> [!danger] Lo que este método NO recupera
> Dilo en voz alta en el vídeo, porque es la mitad de la lección:
> - **Lo que nunca commiteaste no existe para Git.** Si escribiste tres párrafos y no hiciste `commit`, no hay foto de ellos. No se recuperan.
> - Recuperas hasta **el último commit**, no hasta el último segundo. Todo lo que hiciste después de ese commit se pierde.
>
> De ahí sale la norma: **commit al terminar cada sesión de trabajo**, no cuando te acuerdes. Cada commit que no haces es trabajo que estás dejando sin red.

### 📖 Diccionario de Conceptos Clave

> [!quote] Terminología
> - **Carpeta de trabajo:** los ficheros tal y como están ahora en tu disco. Lo que ves en Obsidian.
> - **`git status`:** te dice qué ficheros han cambiado respecto al último commit. **No modifica nada.**
> - **`git diff`:** te enseña **exactamente qué líneas** han cambiado. **No modifica nada.**
> - **`git restore`:** copia el contenido del último commit encima de tu carpeta de trabajo. **Sí modifica.**
> - **`git log`:** la lista de tus commits, del más nuevo al más viejo.

---

### 🛠️ Procedimiento Práctico

> [!danger] ⚠️ LÉEME ANTES DE EMPEZAR
> Vas a **borrar tu trabajo a propósito**. Antes de nada, comprueba que hay algo a lo que volver. Abre la terminal en `Trimestre_1` (clic derecho, como siempre) y ejecuta:
> ```bash
> git status
> ```
> Tiene que decir **`nothing to commit, working tree clean`**.
>
> - Si lo dice: perfecto, todo tu trabajo está commiteado. Adelante.
> - **Si NO lo dice:** tienes cambios sin guardar y **los vas a perder de verdad**. Haz `git add .` y `git commit -m "..."` **antes** de continuar. No sigas hasta que el `status` esté limpio.

> [!example] Paso 0: Prepárate (todavía SIN grabar)
> 1. **Léete el procedimiento entero** (tiene **6 pasos** grabados).
> 2. Comprueba el `git status` limpio del aviso de arriba.
> 3. Ten **OBS** listo y tu **perfil de GitHub** en una pestaña.
> **Y antes de grabar: crea la entrada de apuntes de esta fase** (`fase-0.7.1-catastrofe-local.md`) con la estructura pegada y **vacía**. En el vídeo solo tienes que **enseñarla**, no rellenarla.

> [!example] Paso 1: Arranca la grabación y preséntate
> Inicia la grabación en **OBS**, preséntate, **enseña tu perfil de GitHub** 2-3 segundos y di qué vas a hacer: *"Voy a borrar el contenido de mis apuntes a propósito y a recuperarlo solo con Git, sin usar Internet."*

> [!example] Paso 2: Enseña lo que tienes (antes del desastre)
> Para que se vea que había algo, y que se ve **de dónde** vas a recuperarlo:
> 1. En **Obsidian**, abre una de tus entradas y enséñala: tiene sus respuestas, su enlace de vídeo, su estructura.
> 2. En la terminal, dentro de `Trimestre_1`, enseña **tu historial**:
>    ```bash
>    git log --oneline
>    ```
>    Léelo en voz alta. Ahí está una línea por cada fase que has hecho. **Cada una de esas líneas es un punto al que puedes volver.**

> [!example] Paso 3: 💥 Provoca el desastre
> Explicando lo que haces y por qué:
> 1. En Obsidian, abre **cada una de tus entradas** de `B0_Prerrequisitos/`, selecciona todo el contenido (`Ctrl+A`) y **bórralo** (`Supr`). Guarda.
> 2. Los ficheros siguen ahí, con su nombre. Pero están **vacíos**. Enséñalo.
> 3. **Cierra Obsidian y reinicia el ordenador.** Sí, de verdad: quiero que compruebes que esto no es un truco de Obsidian ni algo que se deshace con `Ctrl+Z`. Cuando vuelvas, sigue roto.
> 4. Vuelve a abrir Obsidian y enseña el desastre: tus apuntes, en blanco.
>
> > [!tip] 💡 Deja de grabar mientras reinicias
> > Pausa la grabación en OBS antes de reiniciar y reanúdala al volver. No hace falta que el vídeo tenga tres minutos de arranque de Windows.

> [!example] Paso 4: Diagnostica ANTES de tocar (los dos comandos que no rompen nada)
> Abre la terminal en `Trimestre_1` y, **narrando lo que ves**:
> 1. **¿Qué ha cambiado?**
>    ```bash
>    git status
>    ```
>    Verás tus ficheros marcados como **`modified`** (modificados). Git ya sabe que están distintos de la última foto.
> 2. **¿Qué exactamente he perdido?**
>    ```bash
>    git diff
>    ```
>    Verás tus líneas antiguas precedidas de un **`-` en rojo**: eso significa *"esto estaba y ya no está"*. Si quieres solo el resumen:
>    ```bash
>    git diff --stat
>    ```
>    y te dirá cuántas líneas has perdido en cada fichero.
>
> **Di en voz alta cuántas líneas has perdido.** Ese número es la respuesta a "cuánto trabajo se ha ido".

> [!example] Paso 5: Recupera (y luego recupera solo uno)
> 1. **Recupéralo todo de golpe:**
>    ```bash
>    git restore .
>    ```
>    El punto significa *"todo lo que hay desde aquí hacia abajo"*. No dice nada al terminar: en Unix, **el silencio es buena señal**.
> 2. **Comprueba:**
>    ```bash
>    git status
>    ```
>    Debe volver a decir **`nothing to commit, working tree clean`**. Abre Obsidian y enséñalo: **todo está de vuelta**.
> 3. **Ahora la versión fina.** Vuelve a vaciar **una sola** de tus entradas, guárdala, y recupera **solo esa**:
>    ```bash
>    git restore B0_Prerrequisitos/NOMBRE-DE-TU-FICHERO.md
>    ```
>    Las demás no se tocan. **Esto es lo que te da haber hecho un commit por fase**: puedes volver atrás con precisión de cirujano en vez de a lo bruto.
>
> > [!note] 📌 `git restore` y `git checkout --`
> > Buscando por internet vas a encontrar `git checkout -- .` para esto mismo. **Hace lo mismo** y funciona: es la forma antigua. `git restore` se creó precisamente porque `git checkout` servía para demasiadas cosas distintas y confundía a todo el mundo. Usa `git restore`, pero reconoce el otro cuando lo veas.

> [!example] Paso 6: Cierra el vídeo, nómbralo y súbelo
> 1. **Detén la grabación**, nombra el vídeo `Fase 0.7.1 — He perdido lo que escribí` y súbelo a la playlist `B0_Prerrequisitos` (No listado) con **timestamps**:
>    ```
>    00:00 Presentacion
>    00:30 Paso 2 - Lo que tenia y mi historial de commits
>    01:15 Paso 3 - Provoco el desastre
>    02:20 Paso 4 - Diagnostico con status y diff
>    03:30 Paso 5 - Recupero todo, y luego uno solo
>    04:40 Paso 6 - Repaso final
>    ```
> 2. **Escribe la entrada de esta fase**, pega ahí el enlace del vídeo y contesta las Preguntas Críticas.
> 3. **Haz commit y push** de esa entrada. Que hoy, más que nunca, tiene sentido.

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | `fatal: you must specify path(s) to restore`. | Escribiste `git restore` **sin el punto**. Git no adivina qué quieres recuperar. | `git restore .` — el punto significa *"todo lo que hay desde aquí hacia abajo"*. Si estás dentro de `Fases/` recupera solo eso; desde la raíz del repo, recupera todo. |
> | `git restore .` no recupera nada y el fichero sigue vacío. | Estás en la carpeta equivocada. | `pwd`: tienes que estar dentro de `Trimestre_1`. |
> | `git status` decía `working tree clean` **con los ficheros ya vacíos**. | Hiciste `commit` **después** de vaciarlos: guardaste una foto del desastre. | Se recupera del commit anterior: `git restore --source=HEAD~1 .` Y aprende la lección: **mira antes de commitear**. |
> | `error: pathspec ... did not match`. | Escribiste mal el nombre del fichero. | Cópialo de la salida de `git status`, no lo teclees a mano. |
> | Recuperé todo pero **falta lo último que escribí**. | Eso no estaba en ningún commit. | No hay nada que hacer: **no existía**. Es exactamente la lección de esta fase. |
> | `git: command not found`. | Abriste el `cmd` en vez de Git Bash. | Clic derecho → `Abrir Git Bash aquí` (Fase 0.3). |

> [!help] Preguntas Críticas (Autoevaluación del alumno)
> 1. Con tus palabras: ¿qué diferencia hay entre `commit` y `push`? ¿Cuál de los dos te ha salvado hoy?
> 2. ¿Por qué `git status` y `git diff` se ejecutan **antes** de `git restore` y no después?
> 3. Un compañero escribe dos horas de apuntes, no hace commit, y pierde el contenido. ¿Puede recuperarlo con lo de hoy? **Explica por qué.**
> 4. ¿Qué habrías tenido que hacer distinto en la Fase 0.3 para **no** poder recuperar una sola entrada por separado?
> 5. 🔬 **Reto:** ejecuta `git log --oneline` y cuenta tus commits. Ahora calcula: si mañana pierdes todo lo que no está commiteado, ¿cuánto trabajo pierdes? Da la respuesta en minutos.

---

### ✅ Checklist Final de la Fase 0.7.1

- [ ] `git status` limpio comprobado **antes** de provocar el desastre.
- [ ] Historial enseñado con `git log --oneline` antes de romper nada.
- [ ] Desastre provocado, equipo reiniciado y desastre confirmado tras reiniciar.
- [ ] Diagnóstico hecho con `git status` **y** `git diff`, narrando cuántas líneas se perdieron.
- [ ] Recuperación completa con `git restore .` y `status` limpio de nuevo.
- [ ] Recuperación de **un solo fichero** demostrada.
- [ ] Sabes explicar qué **no** recupera este método.
- [ ] Vídeo `Fase 0.7.1 — He perdido lo que escribí` subido a la playlist, con timestamps.
- [ ] **Enlace del vídeo pegado en tu entrada de apuntes** de esta fase, con las respuestas.
- [ ] Grabada **🏫 en el centro**.

> **Siguiente paso:** Fase 0.7.2 — Se ha llevado el disco por delante: cuando ya no queda **ni el historial**, y Git en tu ordenador no puede hacer nada.
