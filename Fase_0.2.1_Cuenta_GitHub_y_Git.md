## 🔑 Fase 0.2.1: Cuenta de GitHub y Configuración de Git

### Crea tu cuenta y dile a Git quién eres

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0.2 — parte 1 de 2]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~1 - 1,5 horas · **Requisitos:** Git y OBS instalados (Consellería). Bóveda `Boveda_SOR` creada (Fase 0.1). Conexión a Internet.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin.
> 1. **Prepárate primero (sin grabar):** comprueba lo necesario y **léete el procedimiento entero**.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a explicar la Fase 0.2.1 — Cuenta de GitHub y configuración de Git."* Y **muestra algo que demuestre que eres tú**: tu **Teams** o tu **correo `@alu.edu.gva.es`** (aún no tienes GitHub, lo creas ahora). Di qué vas a hacer.
> 3. **Graba TODO**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `Fase 0.2.1 — Cuenta de GitHub y Git (centro)` [o `(casa)`] y súbelo a tu playlist **`00_Prerrequisitos`** como "No listado".
> 6. **~5 min.** **Doble entrega:** uno en el centro y otro en casa, los dos a la playlist.

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
> 3. **Súbelo** a tu playlist **`00_Prerrequisitos`** (No listado).
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
- [ ] Vídeo `Fase 0.2.1 — Cuenta de GitHub y Git` subido a la playlist `00_Prerrequisitos`, con timestamps.
- [ ] **Doble entrega:** vídeo del centro **y** de casa.

> **Siguiente paso:** Fase 0.2.2 — Autenticación con **clave SSH** (y token HTTPS), para enviar tu trabajo sin escribir la contraseña.
