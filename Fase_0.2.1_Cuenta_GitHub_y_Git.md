## 🔑 Fase 0.2.1: Cuenta de GitHub y Configuración de Git

### Crea tu cuenta y dile a Git quién eres

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0.2 — parte 1 de 2]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~1 - 1,5 horas · **Requisitos:** Git y OBS instalados (Consellería). Bóveda `Boveda_SOR` creada (Fase 0.1). Conexión a Internet.


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
> 1. **Prepárate primero (sin grabar):** comprueba lo necesario, **léete el procedimiento entero** y **crea la entrada de apuntes de esta fase** en Obsidian: fichero `fase-0.2.1-cuenta-github-y-git.md` con la estructura de la Fase 0.1, **vacía**. Rellenarla es cosa tuya, después; hoy solo tiene que existir.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a explicar la Fase 0.2.1 — Cuenta de GitHub y configuración de Git."* Y **muestra algo que demuestre que eres tú**: tu **Teams** o tu **correo `@alu.edu.gva.es`** (aún no tienes GitHub, lo creas ahora). Di qué vas a hacer.
> 3. **Graba TODO**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `Fase 0.2.1 — Cuenta de GitHub y Git` y súbelo a tu playlist **`B0_Prerrequisitos`** como "No listado".
> 6. **~5 min.** Se graba en **🏫 el centro** (crear la cuenta es de una sola vez; el equipo de casa se monta en la Fase 0.5.1).
> 7. **La entrega va por la TAREA de Teams.** Cuando toque, abriré una tarea que cubrirá **esta fase y otras**; te llegará notificación. Tú, hoy: graba, sube el vídeo a la playlist y **pega su enlace en tu entrada de apuntes**.
> 8. **El enlace del vídeo va DENTRO de tu entrada de apuntes**, en el apartado `Enlace al vídeo explicativo`. No lo guardes en un papel: va ahí.

---

### 🎯 Objetivos

- [ ] Explicar qué es **Git** y qué es **GitHub**, y en qué se diferencian.
- [ ] Crear tu **cuenta de GitHub** y confirmar el correo.
- [ ] Configurar Git con tu **nombre y correo** (los mismos que en GitHub).

---

### 📚 Fundamento Teórico

> [!info] Git y GitHub NO son lo mismo
> | | Qué es | Dónde vive | Analogía |
> | :--- | :--- | :--- | :--- |
> | **Git** | Un programa que guarda el **historial** de tus ficheros: cada cambio, cuándo y quién. | **En tu ordenador** (instalado). | El cuaderno de bitácora. |
> | **GitHub** | Una **web** donde subes tus proyectos Git para guardarlos en la nube y compartirlos. | **En Internet** (github.com). | La estantería en la nube. |
>
> **Git** trabaja en tu equipo; **GitHub** guarda la copia en Internet y me deja verla. Juntos me permiten corregir tus apuntes.

> [!abstract] Vocabulario mínimo (te sonará; se practica en la 0.3)
> - **Repositorio ("repo"):** una carpeta cuyo historial controla Git.
> - **Commit:** una "foto" guardada de tus cambios, con un mensaje.
> - **Push / Pull:** **subir** / **bajar** cambios entre tu ordenador y GitHub.

> [!tip] Identidad de Git ≠ cuenta de GitHub
> Configurar Git con tu nombre/correo es decirle **a Git, en tu ordenador**, cómo firmar tus commits. GitHub es la web. Conviene que el **correo coincida** en ambos.

---

### 🛠️ Procedimiento Práctico

> [!example] Paso 0: Prepárate (todavía SIN grabar)
> 1. **Comprueba Git:** abre la terminal (**Git Bash** en Windows / **Terminal** en Linux) y escribe `git --version`. Si da error, **avísame** (no lo instales tú).
> 2. **Léete el procedimiento** (pasos 1 a 4): este procedimiento tiene **4 pasos** grabados.
> 3. **Ten OBS listo** y una pestaña con tu **Teams** o tu **correo `@alu.edu.gva.es`**.
> **Y antes de grabar: crea la entrada de apuntes de esta fase** (`fase-0.2.1-cuenta-github-y-git.md`) con la estructura pegada y **vacía**. En el vídeo solo tienes que **enseñarla**, no rellenarla.

> [!danger] ⌨️ LÉEME: en la terminal, `Ctrl+C` y `Ctrl+V` NO funcionan
> Esto le pasa a todo el mundo el primer día, así que te lo aviso antes de que te bloquees. En **Git Bash** (y en las terminales de Linux) el portapapeles **no va con `Ctrl+C` / `Ctrl+V`**.
>
> **¿Por qué?** Porque en una terminal esas teclas ya significaban otra cosa desde mucho antes de que Windows las usara para copiar y pegar: **`Ctrl+C` sirve para INTERRUMPIR el programa que se está ejecutando**. Si lo pulsas esperando copiar, lo que haces es cortar lo que estuviera corriendo. No es un fallo: es que ahí esa tecla tiene otro trabajo.
>
> | Quieres… | En Git Bash (Windows) | En la terminal de Linux |
> | :--- | :--- | :--- |
> | **Pegar** (meter texto en la terminal) | **`Shift + Insert`** ← la que nunca falla · o **clic derecho** | **`Ctrl + Shift + V`** · o clic derecho → Pegar |
> | **Copiar** (sacar texto de la terminal) | **Selecciona con el ratón** y suelta: en Git Bash eso ya lo copia. Si no, `Ctrl + Insert` | **Selecciona** y `Ctrl + Shift + C` |
>
> **Regla para recordarlo:** en la terminal, las teclas de copiar y pegar llevan **`Shift`**. Así se distinguen de las de toda la vida, que ahí dentro significan otra cosa.
>
> Lo vas a necesitar ya: en la **Fase 0.2.2** tienes que **sacar** tu clave SSH de la terminal, y en la **Fase 0.3** tienes que **meter** la dirección de tu repositorio.

> [!note] 📎 Nota de referencia: cómo se instala Git (y Obsidian) por tu cuenta
> **En el centro no tienes que hacer nada de esto** — lo instala Consellería y tú no tienes permisos. Lo pongo aquí porque **en casa sí te va a tocar a ti** (Fase 0.5.1), porque en una entrevista de trabajo te lo pueden preguntar, y porque un técnico tiene que saber instalar sus propias herramientas. Léelo, no lo ejecutes en el aula.
>
> **🪟 Windows — dos caminos, el mismo resultado**
>
> *Camino A, desde la terminal* (PowerShell, y es el que usaría un técnico):
> ```powershell
> winget install --id Git.Git -e
> winget install --id Obsidian.Obsidian -e
> ```
> `winget` es el gestor de paquetes de Windows, ya viene con Windows 10 y 11. `-e` significa "coincidencia exacta del nombre", para que no te instale otra cosa parecida.
>
> *Camino B, descargando el instalador:* ve a **`git-scm.com/download/win`** y ejecuta el `.exe`. Te hará muchas preguntas: **acepta las opciones por defecto**, pero asegúrate de dejar marcadas estas tres, que son las que usamos en el curso:
>
> | Opción del instalador | Para qué la necesitas |
> | :--- | :--- |
> | *Windows Explorer integration → **Open Git Bash here*** | El clic derecho sobre una carpeta que usamos en la Fase 0.3 |
> | *Git from the command line and also from 3rd-party software* | Que `git` funcione también en PowerShell, no solo en Git Bash |
> | *Add a Git Bash Profile to Windows Terminal* | Abrir Git Bash desde la Terminal de Windows |
>
> **🐧 Linux — según tu distribución**
> ```bash
> sudo apt update && sudo apt install git      # Ubuntu, Debian, Linux Mint
> sudo dnf install git                         # Fedora
> sudo pacman -S git                           # Arch, Manjaro
> ```
> En Linux **no existe Git Bash y no hace falta**: la terminal del sistema ya es una terminal de este tipo, así que todos los comandos del curso funcionan tal cual.
> Obsidian se baja de **`obsidian.md`** (`.deb`, AppImage, o `sudo snap install obsidian --classic`).
>
> **✅ Comprobar que ha ido bien** — en cualquiera de los dos sistemas, cierra la terminal, ábrela de nuevo y escribe:
> ```bash
> git --version
> ```
> Si responde algo tipo `git version 2.53.0`, está instalado. Si dice `command not found`, **no ha funcionado**: normalmente es que no has cerrado y vuelto a abrir la terminal (el `PATH` solo se refresca al abrirla).

> [!example] Paso 1: Arranca la grabación y preséntate
> 1. En **OBS**, pulsa **"Iniciar grabación"**.
> 2. Preséntate: *"Hola, me llamo [Nombre], 2.º SMR, y en este vídeo voy a crear mi cuenta de GitHub y a configurar Git."*
> 3. **Demuestra que eres tú:** enseña 2-3 segundos tu **Teams** o tu **correo `@alu.edu.gva.es`** (que se vea tu nombre).

> [!example] Paso 2: Crea tu cuenta de GitHub
> 1. Entra en **`github.com`** y pulsa **`Sign up`**.
> 2. Rellena:
>    - **Email:** un correo al que tengas acceso. **El mismo que usarás en el Paso 3.**
>    - **Password:** segura. **Anótala.**
>    - **Username:** algo serio, tipo `nombre-apellido` (ej. `juan-garcia-smr`). **Lo veré yo.**
> 3. Completa la verificación y **confirma el correo** (te llega un email con enlace/código).
> 4. Entra en `github.com`: debes ver tu panel (dashboard) vacío.

> [!example] Paso 3: Configura Git con tu nombre y correo
> En la terminal (comandos idénticos en Git Bash y PowerShell), con **tus** datos y el **mismo correo** que en GitHub:
> ```
> git config --global user.name "Juan Garcia"
> git config --global user.email "juan.garcia@alu.edu.gva.es"
> ```
> Comprueba que se guardó:
> ```
> git config --global user.name
> git config --global user.email
> ```

> [!example] Paso 4: Cierra el vídeo, nómbralo y súbelo
> 1. **Detén la grabación** en OBS.
> 2. **Nómbralo:** `Fase 0.2.1 — Cuenta de GitHub y Git`.
> 3. **Súbelo** a tu playlist **`B0_Prerrequisitos`** (No listado).
> 4. **Timestamps** en la descripción, por ejemplo:
>    ```
>    00:00 Presentación
>    00:25 Paso 2 — Crear la cuenta de GitHub
>    02:40 Paso 3 — Configurar Git (nombre y correo)
>    03:30 Paso 4 — Repaso final
>    ```

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | `git: command not found`. | Git no instalado o abriste el cmd en vez de Git Bash. | Abre **Git Bash**. Si falla, avisa al profesor. |
> | No me llega el correo de confirmación. | Está en spam o escribiste mal el correo. | Revisa spam; reenvía desde `Settings → Emails`. |
> | Los commits saldrán con nombre raro. | `user.name/email` mal escritos. | Revísalo con `git config --list` y corrige. |

> [!help] Preguntas Críticas
> 1. Diferencia entre **Git** y **GitHub**, con tus palabras.
> 2. ¿Por qué conviene que el correo de Git coincida con el de GitHub?
> 3. ¿Qué significa `--global` en `git config`?

---

### ✅ Checklist Final de la Fase 0.2.1

- [ ] `git --version` funciona.
- [ ] Cuenta de GitHub creada y correo confirmado.
- [ ] Git configurado con `user.name` y `user.email` (mismo correo que GitHub).
- [ ] Vídeo `Fase 0.2.1 — Cuenta de GitHub y Git` subido a la playlist `B0_Prerrequisitos`, con timestamps.
- [ ] **Enlace del vídeo pegado en tu entrada de apuntes** de esta fase.
- [ ] Grabada **🏫 en el centro**.

> **Siguiente paso:** Fase 0.2.2 — Autenticación con **clave SSH** (y token HTTPS), para enviar tu trabajo sin escribir la contraseña.
