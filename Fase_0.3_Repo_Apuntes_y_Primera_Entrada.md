## 📓 Fase 0.3: Repositorio de Apuntes del Trimestre y Primera Entrada

### Tus apuntes, versionados y en la nube — y cómo se escribe una entrada

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> Ya tienes bóveda (0.1) y conexión con GitHub por SSH (0.2). Ahora vas a convertir la carpeta `Trimestre_1` en un **repositorio**, subirlo a GitHub y **darme el enlace**. Y aprenderás a escribir **la entrada del día** con el formato obligatorio.
>
> **Profesor:** Pedro Navarro Miralles
> **Correo:** p.navarromiralles2@edu.gva.es
> **Centro:** IES Jorge Juan (ALICANTE)
>
> **⏱️ Tiempo estimado:** ~2 horas (teoría + creación del repo + primera entrada + push + verificación grabada)
> **Requisitos:** Fases 0.1 y 0.2 completas. Autenticación lista: **SSH** (`ssh -T git@github.com` responde "Hi…") **o** token HTTPS.

---

### 🎯 Objetivos de la fase

Al terminar esta fase serás capaz de:

- [ ] Explicar por qué usamos **un repositorio por trimestre**.
- [ ] Crear un repositorio vacío en GitHub y conectarlo con tu carpeta `Trimestre_1`.
- [ ] Escribir la **entrada del día** respetando el **nombre de fichero** y la **estructura** obligatorios.
- [ ] Hacer el ciclo completo: `git add` → `git commit` → `git push`.
- [ ] **Darme el enlace** de tu repositorio para que pueda corregir tus apuntes.

---

### 🎯 ¿Dónde Estamos?

> [!info] El Punto de Partida
> Tienes la carpeta `00_Apuntes/Trimestre_1/` dentro de tu bóveda, pero todavía es una carpeta normal: Git no la controla y GitHub no la conoce. En esta fase le damos "vida": la convertimos en repositorio y la subimos.

> [!warning] El Problema
> Yo no me puedo esperar a final de trimestre para ver si estás tomando apuntes o no. Necesito poder decir *"enseñadme lo que lleváis"* **cualquier día** y verlo al instante. Para eso, tu repositorio del trimestre debe estar **siempre actualizado** en GitHub, y yo debo tener **tu enlace**.

> [!success] Objetivo de esta Fase
> Que tu carpeta `Trimestre_1` sea un repositorio conectado a GitHub, con **tu primera entrada** escrita y subida, y que yo tenga el enlace. A partir de aquí, **cada día de clase = una entrada nueva + un push**.

> [!tip] Hoja de Ruta
> 1. Escribir la primera entrada del día (formato obligatorio).
> 2. Convertir `Trimestre_1` en repositorio (`git init`).
> 3. Crear el repositorio vacío en GitHub.
> 4. Conectar los dos (remoto SSH) y subir (`push`).
> 5. Enviarme el enlace.
>
> **Resultado Final:** Repositorio de apuntes del Trimestre 1 vivo en GitHub, con tu primera entrada.
> **Siguiente:** Fase 0.4 — Clonar tu copia de la práctica `boochan-1` y practicar el ciclo status → commit → push.

---

### 📚 Fundamento Teórico

> [!info] ¿Por qué un repositorio por trimestre?
> Podríamos meter todo el curso en un único repo, pero separamos por trimestre porque:
> - Al cerrar cada trimestre, ese repo queda "congelado" y **te lo puedo calificar** limpio.
> - Cada trimestre es un enlace claro que me pasas una vez.
> - Si algo se lía en un trimestre, no afecta a los demás.
>
> Tendrás **tres repos de apuntes** a lo largo del curso: `apuntes-sor-t1`, `apuntes-sor-t2`, `apuntes-sor-t3`. Ahora montamos el primero.

> [!important] 1. La entrada del día: NOMBRE de fichero obligatorio
> Cada día de clase creas **un fichero nuevo** dentro del bloque que toque. El nombre **no es libre**: sigue este formato exacto, para que todos los ficheros se ordenen solos por fecha y yo pueda encontrarlos:
>
> ```
> AAAA-MM-DD_titulo-corto.md
> ```
>
> - `AAAA-MM-DD` → año-mes-día con **guiones** (ej. `2026-09-15`).
> - `_` → un guion bajo separando fecha y título.
> - `titulo-corto` → dos o tres palabras **en minúsculas y con guiones**, sin tildes ni espacios.
>
> **Ejemplos correctos:**
> - `2026-09-15_introduccion-al-modulo.md`
> - `2026-09-22_direcciones-ip.md`
>
> **Ejemplos INCORRECTOS:** `apuntes dia 1.md` ❌, `15-9.md` ❌, `Introducción.md` ❌.

> [!important] 2. La entrada del día: ESTRUCTURA obligatoria
> Dentro de cada entrada escribes con **esta plantilla fija**. No escribes "a lo loco": rellenas estos apartados.
>
> ```markdown
> # 2026-09-15 — Introducción al módulo
>
> **Fecha:** 2026-09-15
> **Bloque:** Bloque 1 — Introducción
>
> ## Qué hemos visto hoy
> - (con tus palabras, lo que ha explicado el profesor)
>
> ## Conceptos clave
> - **Término:** definición corta.
>
> ## Comandos / pasos importantes
> - `comando` — para qué sirve.
>
> ## Dudas / a repasar en casa
> - (lo que no te ha quedado claro)
> ```
>
> > [!tip] 💡 No copies lo que digo palabra por palabra
> > Los apuntes son para **entenderlo tú**. Escribe con tus palabras. El apartado "Dudas" es tan importante como los demás: me dice en qué reforzar.

### 📖 Diccionario de Conceptos Clave

> [!quote] Terminología
> - **`git init`:** convierte una carpeta normal en repositorio (empieza a controlar su historial).
> - **Remoto (`origin`):** la dirección en GitHub a la que está conectado tu repo local.
> - **`git add`:** marca qué cambios quieres guardar en el próximo commit.
> - **`git commit`:** guarda esos cambios con un mensaje.
> - **`git push`:** sube tus commits a GitHub.
> - **Rama `main`:** la línea principal de trabajo del repositorio.
> - **Entrada:** el fichero de apuntes de un día concreto.

---

### 🛠️ Procedimiento Práctico

> [!example] Paso 1: Escribe tu primera entrada en Obsidian
> 1. Abre la bóveda `Boveda_SOR` en Obsidian.
> 2. Ve a `00_Apuntes/Trimestre_1/Bloque_1_Introduccion/`.
> 3. Clic derecho → **`New note`** (o el icono de nueva nota) **dentro de esa carpeta**.
> 4. Nómbrala con el formato obligatorio, por ejemplo: `2026-09-15_introduccion-al-modulo`
> 5. Pega la **plantilla** del Fundamento Teórico (apartado 2) y rellénala con lo de hoy.
> 6. Guarda (Ctrl+S / Cmd+S).

> [!example] Paso 2: Convierte `Trimestre_1` en repositorio
> Abre la terminal (**Git Bash** en Windows / **Terminal** en Linux) y **entra en la carpeta del trimestre**. Ajusta la ruta a la tuya:
> ```bash
> cd ~/SOR/Boveda_SOR/00_Apuntes/Trimestre_1
> ```
> *(En Windows con Git Bash, la ruta suele ser `/c/SOR/Boveda_SOR/00_Apuntes/Trimestre_1`.)*
>
> Inicializa el repositorio:
> ```bash
> git init
> git branch -M main
> ```
> **Verificación:**
> ```bash
> git status
> ```
> Debe decir que estás en la rama `main` y listar tu entrada como fichero "sin seguimiento" (untracked).
>
> > [!danger] ⚠️ Asegúrate de estar DENTRO de `Trimestre_1`
> > No hagas `git init` en `Boveda_SOR` ni en `00_Apuntes`. **Solo dentro de `Trimestre_1`.** Comprueba con el comando `pwd` que la ruta termina en `.../Trimestre_1` antes de escribir `git init`.

> [!example] Paso 3: Crea el repositorio vacío en GitHub
> 1. En `github.com`, pulsa el **`+`** (arriba a la derecha) → **`New repository`**.
> 2. Rellena:
>    - **Repository name:** `apuntes-sor-t1`
>    - **Visibility:** **Private** (tus apuntes son tuyos; me darás acceso con el enlace).
>    - **NO** marques "Add a README", ".gitignore" ni "license" (lo dejamos vacío, ya tienes ficheros locales).
> 3. Pulsa **`Create repository`**.
> 4. GitHub te mostrará una página con instrucciones. En el botón **`Code`** tienes dos direcciones — copia la de la vía que montaste en la Fase 0.2:
>    - **SSH:** `git@github.com:TU-USUARIO/apuntes-sor-t1.git` (recomendada, sin contraseña).
>    - **HTTPS:** `https://github.com/TU-USUARIO/apuntes-sor-t1.git` (con token).

> [!example] Paso 4: Conecta local ↔ GitHub y sube
> De vuelta en la terminal (dentro de `Trimestre_1`):
> ```bash
> git remote add origin git@github.com:TU-USUARIO/apuntes-sor-t1.git
> git add .
> git commit -m "Primera entrada: introduccion al modulo"
> git push -u origin main
> ```
> - Usa la dirección que copiaste: **SSH** (`git@github.com:...`, sin contraseña) **o** **HTTPS** (`https://github.com/...`, te pedirá el token). Las dos llegan al mismo repo.
> - Como configuraste la clave SSH en la Fase 0.2, **no te pedirá contraseña**.
>
> **Verificación:** recarga tu repositorio en GitHub. Debes ver la carpeta `Bloque_1_Introduccion/` con tu entrada dentro.

> [!example] Paso 5: Envíame el enlace
> Copia la dirección web de tu repo (la de la barra del navegador, `https://github.com/TU-USUARIO/apuntes-sor-t1`) y pásamela por **Teams**, como te indique. Con ese enlace podré revisar tus apuntes cuando quiera.
>
> > [!warning] ⚠️ Repo privado: tendrás que darme acceso
> > Al ser **privado**, además del enlace tendré que ser "colaborador". Cuando me pases el enlace te diré mi usuario de GitHub para que me añadas en `Settings → Collaborators`. (Si el profesor prefiere repos públicos, te lo indicará y te saltas esto.)

> [!example] Paso 6: El ciclo de cada día (grábalo con OBS)
> A partir de ahora, **cada día de clase**:
> 1. Creas la **entrada del día** (nombre + estructura obligatorios).
> 2. En la terminal, dentro de `Trimestre_1`:
>    ```bash
>    git add .
>    git commit -m "Apuntes del 2026-09-22"
>    git push
>    ```
> 3. Compruebas en GitHub que aparece.
>
> Graba con **OBS** este primer ciclo completo, explicándolo en voz alta. Ese vídeo es tu evidencia de la Fase 0.3.

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Tabla de Troubleshooting (¿Algo no funciona?)
> | Problema | Causa Probable | Solución Sugerida |
> | :--- | :--- | :--- |
> | `fatal: not a git repository`. | No estás dentro de `Trimestre_1`, o no hiciste `git init`. | Comprueba con `pwd` que estás en `.../Trimestre_1` y que hiciste `git init`. |
> | `remote origin already exists`. | Ejecutaste `git remote add origin` dos veces. | Usa `git remote set-url origin git@github.com:TU-USUARIO/apuntes-sor-t1.git` para corregir la dirección. |
> | `Permission denied (publickey)` al hacer push. | La clave SSH no está bien (Fase 0.2), o usaste la URL `https://` en vez de la `git@`. | Repasa la Fase 0.2 (`ssh -T git@github.com`) y usa la URL SSH `git@github.com:...`. |
> | `Updates were rejected` / `failed to push`. | El repo de GitHub no estaba vacío (marcaste README al crearlo). | Bórralo y créalo de nuevo **sin** README, o haz `git pull origin main --rebase` y vuelve a `push`. |
> | Hice `git init` en `Boveda_SOR` sin querer. | Estabas en la carpeta equivocada. | Borra la carpeta oculta `.git` que se creó ahí (`rm -rf .git` estando en `Boveda_SOR`) y hazlo bien dentro de `Trimestre_1`. Si dudas, pregúntame. |

> [!help] Preguntas Críticas (Autoevaluación del alumno)
> 1. ¿Por qué usamos un repositorio por trimestre en vez de uno para todo el curso?
> 2. Escribe, sin mirar, el formato de nombre de una entrada del día para el 3 de octubre de 2026 titulada "servidor DNS".
> 3. ¿Qué hacen, en orden, `git add`, `git commit` y `git push`?
> 4. ¿En qué carpeta EXACTA debes ejecutar `git init`? ¿Qué pasa si lo haces en `Boveda_SOR`?
> 5. 🔬 **Reto:** crea una segunda entrada de prueba (fecha de mañana), haz `git status`, y observa cómo Git detecta el fichero nuevo. Luego `add`, `commit` y `push`, y compruébalo en GitHub.

---

### ✅ Checklist Final de la Fase 0.3

- [ ] Primera entrada creada en `Bloque_1_Introduccion/` con nombre y estructura correctos.
- [ ] `Trimestre_1` convertido en repositorio (`git init`, rama `main`).
- [ ] Repositorio `apuntes-sor-t1` creado en GitHub (privado, vacío).
- [ ] Remoto conectado (`git remote add origin ...`, por SSH o HTTPS).
- [ ] Primer `commit` y `push` hechos; la entrada se ve en GitHub.
- [ ] Enlace del repositorio enviado al profesor (y acceso concedido si es privado).
- [ ] Vídeo de OBS del ciclo completo.

> **Siguiente paso:** Fase 0.4 — Clonar tu copia de la práctica **`boochan-1`** dentro de `Practicas/` y dominar el ciclo `git status` → `commit` → `push` sobre una práctica real.
