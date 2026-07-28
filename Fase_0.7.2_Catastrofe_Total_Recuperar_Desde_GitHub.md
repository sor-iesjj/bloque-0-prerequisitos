## 🔥 Fase 0.7.2: Se Ha Llevado el Disco Por Delante

### Cuando no queda ni el historial: recuperar clonando desde GitHub

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0.7 — parte 2 de 2]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~1 - 1,5 horas · **Requisitos:** Fase 0.7.1 completa. Los **dos** repos (`apuntes-sor-t1` y `boochan-1`) subidos a GitHub.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin.
> 1. **Prepárate primero (sin grabar):** comprueba lo necesario, **léete el procedimiento entero** y **crea la entrada de apuntes de esta fase** en Obsidian: fichero `fase-0.7.2-catastrofe-total.md` con la estructura de la Fase 0.1, **vacía**. Rellenarla es cosa tuya, después; hoy solo tiene que existir.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a explicar la Fase 0.7.2 — Se ha llevado el disco por delante."* Y **muestra tu perfil de GitHub**. Di qué vas a hacer.
> 3. **Graba TODO**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `Fase 0.7.2 — Se ha llevado el disco por delante` y súbelo a tu playlist **`B0_Prerrequisitos`** (No listado).
> 6. **~5-7 min.** Se graba en **🏫 el centro**.
> 7. **La entrega va por la TAREA de Teams.** Cuando toque, abriré una tarea que cubrirá **esta fase y otras**; te llegará notificación. Tú, hoy: graba, sube el vídeo a la playlist y **pega su enlace en tu entrada de apuntes**.
> 8. **El enlace del vídeo va DENTRO de tu entrada de apuntes**, en el apartado `Enlace al vídeo explicativo`. No lo guardes en un papel: va ahí.

---

> [!danger] 🛑 ESTA PRÁCTICA DESTRUYE TRABAJO DE VERDAD
> En la 0.7.1 los ficheros seguían ahí. Hoy **no va a quedar nada**: ni carpetas, ni ficheros, ni la carpeta oculta `.git` con tu historial.
>
> Lo único que te salvará es lo que esté **en GitHub**. Por eso el Paso 0 tiene una comprobación obligatoria que **no te puedes saltar**. Si te la saltas, no estás haciendo un ejercicio: estás perdiendo tu trabajo.

---

### 🎯 Objetivos

- [ ] Explicar por qué en este desastre **Git en tu ordenador no puede hacer nada**.
- [ ] Comprobar, antes de borrar, que tus dos repos están **realmente** en GitHub.
- [ ] Reconstruir la bóveda entera **clonando** los dos repositorios.
- [ ] Clonar con el **nombre de carpeta que tú decides**, no el que trae el repo.
- [ ] Decir qué se pierde para siempre y **de qué depende** que sea mucho o poco.

---

### 🎯 ¿Dónde Estamos?

> [!info] El Punto de Partida
> En la 0.7.1 recuperaste tus apuntes **sin Internet**, porque el historial vivía en tu propio ordenador, en la carpeta oculta `.git`. Hoy se lleva por delante **también esa carpeta**.

> [!warning] El Problema
> El disco duro del aula se estropea. O reinstalan el equipo por vacaciones. O te lo formatean sin avisar. O simplemente borras la carpeta equivocada un viernes a última hora. **No queda absolutamente nada** en local.
>
> Y aquí se te va algo que no escribiste tú: en `01_Practicas/boochan-1/` está **el material del proyecto Boochan**, el manual y las fases. Eso no lo puedes reescribir de memoria. No es tuyo.
>
> Lo que hoy vas a comprobar es que **te da exactamente igual**. Que un ordenador es una herramienta reemplazable y tu trabajo no vive ahí.

> [!success] Objetivo de esta Fase
> Borrar la bóveda entera —los dos repositorios, con todo dentro— y reconstruirla desde cero **en menos de dos minutos**, clonando desde GitHub. Y saber decir con exactitud qué se ha perdido por el camino.

---

### 📚 Fundamento Teórico

> [!important] Por qué hoy `git restore` no sirve de nada
> Recuerda los tres sitios de la Fase 0.7.1:
>
> | Dónde vive | ¿Sobrevive hoy? | Por qué |
> | :--- | :--- | :--- |
> | La carpeta de trabajo | ❌ | La borras tú |
> | El último commit (carpeta `.git`) | ❌ | **`.git` está DENTRO de `Trimestre_1`.** Al borrar la carpeta, se va con ella |
> | GitHub | ✅ | Está en otro ordenador, en otro sitio, que no es el tuyo |
>
> Ese es el cambio de hoy y es todo el concepto: **la carpeta `.git` es local**. Es tu máquina del tiempo, pero vive dentro de la casa que se está quemando. `git restore` funcionaba porque `.git` existía; hoy no existe, y ningún comando de Git en tu ordenador puede inventarse un historial que ya no está.
>
> **Lo único que te salva es tener una copia FUERA.** Eso es `git push`. Eso es GitHub.

> [!info] Copia de seguridad de verdad: la regla del "otro sitio"
> Una copia de seguridad que vive en el mismo disco que el original **no es una copia de seguridad**: es el mismo fichero dos veces esperando el mismo accidente. Para que valga, tiene que estar en **otro sitio físico**.
>
> Tú ya tienes eso montado sin habértelo planteado: tus repos están en los servidores de GitHub. Es la misma idea que verás en el proyecto Boochan cuando hablemos de servidores y de copias, solo que aquí el que se juega los apuntes eres tú.

> [!warning] El fallo nº1: confundir `commit` con `push`
> Y hoy sale carísimo. **Un commit que no has empujado sigue viviendo solo en tu ordenador**, dentro de `.git`. Si borras la carpeta, ese commit se va con ella. Estaba "guardado", sí — guardado en el sitio que acabas de destruir.
>
> Git te avisa de esto, y hasta ahora seguramente lo ignorabas. Cuando tienes commits sin empujar, `git status` te dice:
> ```
> Your branch is ahead of 'origin/main' by 2 commits.
> ```
> **`ahead` significa "vas por delante de GitHub".** Es decir: *"tienes cosas que solo están aquí"*. Traducido: *"si este ordenador se muere ahora, pierdes eso"*.

> [!danger] Lo que NO se recupera hoy, y ya no hay truco
> - Todo lo que **no habías empujado**. Commiteado o no. Se pierde para siempre.
> - Cualquier fichero de la bóveda que **no esté dentro de un repositorio**. Si tenías notas sueltas en `Boveda_SOR/` que no viven ni en `Trimestre_1` ni en `boochan-1`, **nadie las está guardando**.
>
> De aquí sale la norma que llevo repitiéndote seis fases y que hoy deja de ser una manía mía: **`push` al terminar cada sesión de trabajo.** No al final de la semana. Al terminar.

### 📖 Diccionario de Conceptos Clave

> [!quote] Terminología
> - **Repositorio local:** tu carpeta con su `.git` dentro. Vive en tu ordenador.
> - **Repositorio remoto (`origin`):** la copia en GitHub. Vive en otro sitio.
> - **`git clone`:** trae un repositorio remoto entero —ficheros **e historial**— y crea la carpeta.
> - **`ahead` / `behind`:** vas por delante de GitHub (tienes cosas sin subir) / por detrás (hay cosas sin bajar).
> - **Copia de seguridad:** una copia que está en **otro sitio**. Si está en el mismo disco, no cuenta.

---

### 🛠️ Procedimiento Práctico

> [!danger] 🛑 Paso 0: LA COMPROBACIÓN QUE NO TE PUEDES SALTAR
> **No grabes todavía.** Antes de destruir nada, hay que verificar que hay de dónde recuperar. Hazlo en **los dos repositorios**, uno detrás de otro.
>
> **En `00_Apuntes/Trimestre_1/`** (clic derecho → abrir terminal ahí):
> ```bash
> git status
> ```
> Tienen que aparecer **las dos frases**:
> - `nothing to commit, working tree clean` → no hay nada sin guardar
> - `Your branch is up to date with 'origin/main'` → **no hay nada sin subir**
>
> **Repite exactamente lo mismo en `01_Practicas/boochan-1/`.**
>
> | Lo que dice | Qué significa | Qué haces |
> | :--- | :--- | :--- |
> | `up to date with 'origin/main'` | Todo está en GitHub | ✅ Puedes seguir |
> | `Your branch is ahead by N commits` | **Tienes N commits solo aquí** | 🛑 `git push` **ahora**, y repite el `status` |
> | `Changes not staged` / `Untracked files` | Hay trabajo sin guardar | 🛑 `git add .` → `git commit` → `git push`, y repite |
>
> **Léete además el procedimiento entero** antes de grabar: tiene **6 pasos** grabados. Y **crea ya la entrada de apuntes de esta fase**: si la creas después de borrar la bóveda, tendrás que rehacerla.
>
> **Última comprobación, y esta con los ojos:** abre `github.com`, entra en tus dos repositorios y **mira que tus ficheros están ahí**. No te fíes solo del terminal. Si algo no aparece en la web, **no existe** para lo que viene ahora.

> [!example] Paso 1: Arranca la grabación y preséntate
> Inicia la grabación en **OBS**, preséntate, **enseña tu perfil de GitHub** 2-3 segundos y di qué vas a hacer: *"Voy a borrar mi bóveda entera, incluidos los apuntes y la práctica, y a reconstruirla clonando desde GitHub."*

> [!example] Paso 2: Demuestra que tienes red debajo (grabando)
> Esto es lo que convierte el vídeo en una demostración y no en un acto de fe. Enseña, en pantalla:
> 1. El **`git status`** de los dos repos, con el `up to date` visible. Léelo en voz alta.
> 2. Los **dos repositorios en la web de GitHub**, con sus ficheros dentro.
> 3. Tu bóveda en el Explorador: `00_Apuntes/Trimestre_1/` y `01_Practicas/boochan-1/`, con todo su contenido.
>
> Di la frase: *"Todo lo que voy a borrar está en GitHub. Lo acabo de comprobar."*

> [!example] Paso 3: 💥 Provoca la catástrofe
> Ahora, sin miedo, porque acabas de comprobar que hay red:
> 1. Cierra **Obsidian** (si no, se queja de que le mueven las carpetas).
> 2. En el Explorador, borra **la carpeta `Trimestre_1` entera**. Con todo lo que hay dentro, incluida la carpeta oculta `.git`.
> 3. Borra también **`boochan-1` entera**. Sí, con mi manual y las fases del proyecto dentro.
> 4. **Reinicia el ordenador.** Que quede claro que no es un truco de Obsidian.
> 5. Al volver, abre Obsidian y **enseña el desastre**: `00_Apuntes/` vacía, `01_Practicas/` vacía. No queda nada.
>
> > [!warning] ⚠️ NO borres `Boveda_SOR` entera
> > Borra **solo esas dos carpetas**. `Boveda_SOR/` y `00_Apuntes/` se quedan (vacías, pero se quedan): son la estructura contenedor que montaste en la Fase 0.1 y que **nunca fue un repositorio**. Si las borras también, tendrás que rehacerlas a mano — no es grave, pero no es lo que toca hoy.

> [!example] Paso 4: Comprueba que Git ya no puede ayudarte
> Antes de recuperar, demuestra **por qué** hoy hace falta GitHub. Abre la terminal donde estaba `Trimestre_1` (es decir, en `00_Apuntes/`) y prueba:
> ```bash
> git status
> ```
> Responde:
> ```
> fatal: not a git repository (or any of the parent directories): .git
> ```
> **Léelo en voz alta y explícalo:** *"Git me dice que aquí no hay ningún repositorio. La carpeta `.git` con todo mi historial estaba dentro de `Trimestre_1`, y la he borrado. En la fase anterior `git restore` me salvó porque `.git` existía. Hoy no existe, así que Git en mi ordenador no puede hacer absolutamente nada."*

> [!example] Paso 5: Reconstruye clonando los dos repos
> 1. **Los apuntes.** Abre la terminal en `00_Apuntes/` y comprueba dónde estás:
>    ```bash
>    pwd          # .../Boveda_SOR/00_Apuntes
>    git clone git@github.com:TU-USUARIO/apuntes-sor-t1.git Trimestre_1
>    ```
>    > [!important] 📌 Fíjate en el `Trimestre_1` del final
>    > Ese segundo argumento **no está de adorno**. Sin él, `git clone` crea la carpeta con el nombre del repositorio: te quedaría `apuntes-sor-t1/` y tu estructura dejaría de ser la de todo el curso.
>    > **`git clone <dirección> <nombre-de-carpeta>`**: le dices cómo quieres que se llame. Con `boochan-1` no hace falta, porque el repo ya se llama así.
>
> 2. **La práctica.** Abre la terminal en `01_Practicas/`:
>    ```bash
>    pwd          # .../Boveda_SOR/01_Practicas
>    git clone git@github.com:TU-USUARIO/boochan-1.git
>    ```
>
> 3. **Comprueba que ha vuelto TODO, no solo los ficheros:**
>    ```bash
>    cd Trimestre_1        # o abre la terminal ahí
>    git log --oneline
>    git status
>    ```
>    Tu **historial completo** está de vuelta, commit a commit, con los mensajes que escribiste. Y el `status` dice `up to date with 'origin/main'`. **No has recuperado una copia: has recuperado el repositorio entero, con su memoria.**
>
> 4. Abre **Obsidian**: tus entradas están, con sus respuestas y sus enlaces. Y el material de Boochan también. Enséñalo.

> [!example] Paso 6: Cierra el vídeo, nómbralo y súbelo
> 1. **Detén la grabación**, nombra el vídeo `Fase 0.7.2 — Se ha llevado el disco por delante` y súbelo a la playlist `B0_Prerrequisitos` (No listado) con **timestamps**:
>    ```
>    00:00 Presentacion
>    00:30 Paso 2 - Compruebo que todo esta en GitHub
>    01:40 Paso 3 - Borro la boveda entera
>    02:50 Paso 4 - Git ya no puede ayudarme
>    03:40 Paso 5 - Reconstruyo clonando los dos repos
>    05:30 Paso 6 - Repaso final
>    ```
> 2. **Escribe la entrada de esta fase**, pega el enlace del vídeo y contesta las Preguntas Críticas.
> 3. **Commit y push.** Hoy ya sabes exactamente por qué.

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | `git clone` deja la carpeta con nombre `apuntes-sor-t1`. | Olvidaste el segundo argumento. | Bórrala y repite con `... .git Trimestre_1` al final. |
> | `Permission denied (publickey)`. | El equipo ya no reconoce tu clave SSH, o estás en otro equipo. | Repasa la Fase 0.2.2, o clona por HTTPS con tu token. |
> | `Repository not found`. | Usuario mal escrito, o el repo es privado y no estás identificado. | Comprueba la dirección en la web de GitHub, botón `Code`. |
> | Ha vuelto todo **menos lo último que escribí**. | Eso estaba commiteado pero **sin `push`**. | No hay solución: se ha perdido. Es la lección de la fase. |
> | Obsidian no ve las carpetas recuperadas. | Estaba abierto mientras clonabas. | Cierra y vuelve a abrir Obsidian. |
> | `destination path already exists`. | La carpeta no se llegó a borrar del todo. | Bórrala del todo y repite el `clone`. |
> | Borré `Boveda_SOR` entera sin querer. | Te pasaste borrando. | Recréala con su estructura (Fase 0.1) y clona dentro. No se pierde nada: los repos siguen en GitHub. |

> [!help] Preguntas Críticas (Autoevaluación del alumno)
> 1. En la Fase 0.7.1 `git restore` te salvó. Hoy no sirve de nada. **¿Qué ha cambiado exactamente?**
> 2. ¿Por qué una copia de seguridad guardada en el mismo disco que el original no es una copia de seguridad?
> 3. `git status` te dice `Your branch is ahead of 'origin/main' by 3 commits`. Con tus palabras: ¿qué está pasando y **qué arriesgas** si el disco se rompe ahora?
> 4. ¿Qué hace el segundo argumento de `git clone <dirección> <carpeta>` y por qué en esta fase era imprescindible?
> 5. Un compañero guarda sus apuntes en una carpeta de la bóveda que **no** es ninguno de los dos repositorios. Le pasa lo de hoy. ¿Qué recupera? ¿Por qué?
> 6. 🔬 **Reto:** cronometra el Paso 5. ¿Cuánto has tardado en reconstruir todo tu curso? Ahora calcula cuánto habrías tardado en reescribirlo a mano.

---

### ✅ Checklist Final de la Fase 0.7.2

- [ ] `git status` comprobado en **los dos** repos, con `up to date with 'origin/main'` visible.
- [ ] Los dos repositorios comprobados **también en la web** de GitHub.
- [ ] `Trimestre_1` y `boochan-1` borradas por completo, y equipo reiniciado.
- [ ] `fatal: not a git repository` demostrado y explicado en voz alta.
- [ ] Los dos repos clonados, con `Trimestre_1` recuperando **su nombre de carpeta**.
- [ ] `git log` enseñado tras el clon: el **historial completo** ha vuelto, no solo los ficheros.
- [ ] Sabes explicar qué se pierde si hay commits sin `push`.
- [ ] Vídeo `Fase 0.7.2 — Se ha llevado el disco por delante` subido a la playlist, con timestamps.
- [ ] **Enlace del vídeo pegado en tu entrada de apuntes** de esta fase, con las respuestas.
- [ ] Grabada **🏫 en el centro**.

> [!summary] 🎓 Con esto cierras los prerrequisitos
> Ya no trabajas como alguien que guarda ficheros en un ordenador. Trabajas como un técnico: **documentas lo que haces, lo versionas y lo tienes fuera de la máquina que puede romperse.** Y lo has comprobado rompiéndolo dos veces.
>
> Todo lo que viene ahora —el proyecto Boochan, los servidores, los dominios— se apoya en esto. Un servidor se cae igual que se cae tu portátil, y la pregunta siempre es la misma: **¿dónde está la copia y cuánto tardas en volver?**

> **Siguiente paso:** empieza el proyecto **Boochan** (Fase 1). Antes, el profesor pasará la **prueba diagnóstica de redes** (ver `Prueba_Diagnostica_Inicial_SOR`).
