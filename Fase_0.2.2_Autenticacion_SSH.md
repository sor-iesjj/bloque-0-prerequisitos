## 🔐 Fase 0.2.2: Autenticación — Clave SSH (y token HTTPS)

### Conecta tu equipo con GitHub sin escribir la contraseña

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0.2 — parte 2 de 2]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~1 - 1,5 horas · **Requisitos:** Fase 0.2.1 completa (cuenta de GitHub + Git configurado).


> [!abstract] 📋 Qué se te evalúa en esta fase
> **RA.04**
>
> | Código | Criterio de evaluación |
> | :--- | :--- |
> | `CE.04.f` | Se han establecido niveles de seguridad para controlar el acceso del cliente a los recursos compartidos. |
>
> Los criterios están tomados literalmente del **RD 1691/2007** y de la programación del módulo.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin.
> 1. **Prepárate primero (sin grabar):** comprueba lo necesario, **léete el procedimiento entero** y **crea la entrada de apuntes de esta fase** en Obsidian: fichero `b0-0.2.2-clave-ssh.md` con la estructura del **Bloque 0 · Fase 0.1.b**, **vacía**. Rellenarla es cosa tuya, después; hoy solo tiene que existir.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a explicar la Fase 0.2.2 — Autenticación con clave SSH."* Y **muestra algo que demuestre que eres tú**: ya tienes GitHub, así que enseña **tu perfil de GitHub** (o tu Teams/correo). Di qué vas a hacer.
> 3. **Graba TODO**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Paso 1 — Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `B0.2.2 · Autenticación SSH` y súbelo a tu playlist **`B0_Prerrequisitos`** como "No listado".
> 6. **~5 min.** Se graba en **🏫 el centro** (la clave SSH de casa se genera en la Fase 0.5.1).
> 7. **La entrega va por la TAREA de Teams.** Cuando toque, abriré una tarea que cubrirá **esta fase y otras**; te llegará notificación. Tú, hoy: graba, sube el vídeo a la playlist y **pega su enlace en tu entrada de apuntes**.
> 8. **El enlace del vídeo va DENTRO de tu entrada de apuntes**, en el apartado `🔗 Enlaces`. No lo guardes en un papel: va ahí.

> [!danger] ⚠️ LÉEME: la clave privada no se comparte JAMÁS
> Vas a generar una **pareja de claves**. Comparte **solo la PÚBLICA** (el fichero que termina en **`.pub`**). La **privada** se queda en tu equipo y no se sube, ni se pega en un chat, ni se enseña con detalle en el vídeo. Si alguien te la pide: **NO**.

---

### 🎯 Objetivos

- [ ] Explicar qué es una **clave SSH** (pública/privada) y por qué se usa en vez de la contraseña.
- [ ] Generar tu clave y **añadir la pública** a GitHub.
- [ ] **Verificar** con un comando que tu equipo y GitHub se reconocen.
- [ ] Conocer la vía alternativa **HTTPS + token**.

---

### 📚 Fundamento Teórico

> [!info] Por qué NO usamos la contraseña
> Escribir la contraseña en cada envío es incómodo y, además, GitHub ya **no** la admite para esto. La vía profesional es una **clave SSH**: un candado que dejas puesto una vez y no molesta más.

> [!important] Qué es una clave SSH (candado y llave)
> Es una **pareja de ficheros**:
> - **Clave privada:** se queda **siempre** en tu ordenador. **NUNCA se comparte.** Es la llave.
> - **Clave pública:** se puede compartir. Es el candado que pegas en GitHub.
>
> Cuando envías cambios, GitHub comprueba que tu llave privada encaja con el candado público — y te deja pasar **sin contraseña**.

> [!warning] Una clave por equipo
> La clave privada no se copia. Generarás **una en el centro y otra en casa**, y añadirás **las dos** a tu cuenta de GitHub. Es normal tener varias claves (una por dispositivo).

> [!tip] Alternativa: HTTPS + token
> GitHub también admite **HTTPS con un token** (una contraseña temporal). Es válida, pero el token **caduca**; por eso recomendamos SSH. Verás las dos.

---

### 🛠️ Procedimiento Práctico

> [!example] Paso 0: Prepárate (todavía SIN grabar)
> 1. Abre la terminal (**Git Bash** en Windows / **Terminal** en Linux).
> 2. **Léete el procedimiento** (pasos 1 a 6): este procedimiento tiene **6 pasos** grabados.
> 3. **Ten OBS listo** y una pestaña con **tu perfil de GitHub** (para presentarte).
> **Y antes de grabar: crea la entrada de apuntes de esta fase** (`b0-0.2.2-clave-ssh.md`) con la estructura pegada y **vacía**. En el vídeo solo tienes que **enseñarla**, no rellenarla.

> [!example] Paso 1: Arranca la grabación y preséntate
> Inicia la grabación en **OBS**, preséntate y **enseña tu perfil de GitHub** 2-3 segundos para demostrar que eres tú. Di qué vas a hacer.

> [!example] Paso 2: Genera tu clave SSH
> Con **tu** correo de GitHub:
> ```
> ssh-keygen -t ed25519 -C "juan.garcia@alu.edu.gva.es"
> ```
> Pulsa **Enter en las tres preguntas** (ubicación por defecto, sin passphrase). Verás un "randomart": es normal.
> Comprueba que existen las dos claves:
> ```
> ls ~/.ssh
> ```
> Debes ver **`id_ed25519`** (privada) y **`id_ed25519.pub`** (pública).

> [!example] Paso 3: Añade tu clave PÚBLICA a GitHub
> 1. Muestra la clave **pública**:
>    ```
>    cat ~/.ssh/id_ed25519.pub
>    ```
> 2. Copia la línea **entera** (empieza por `ssh-ed25519`, termina en tu correo).
> 3. En GitHub: **foto de perfil → Settings → SSH and GPG keys → New SSH key**.
> 4. **Title:** `Equipo Centro` (en casa, `Equipo Casa`). **Key:** pega la línea. **Add SSH key**.

> [!example] Paso 4: Verifica que os reconocéis
> ```
> ssh -T git@github.com
> ```
> La primera vez escribe **`yes`**. Debe responder: `Hi TU-USUARIO! You've successfully authenticated…` (lo de "does not provide shell access" es normal).

> [!example] Paso 5: (Alternativa) HTTPS + token
> Para conocer la otra vía: GitHub → **Settings → Developer settings → Personal access tokens → Tokens (classic) → Generate**, con permiso **`repo`**. **Copia el token** (solo se ve una vez) y guárdalo. Cuando clones/empujes por `https://`, pon tu usuario y **pega el token como contraseña**. *(El token **caduca**; por eso preferimos SSH.)*

> [!example] Paso 6: Cierra el vídeo, nómbralo y súbelo
> Detén la grabación, nómbralo `B0.2.2 · Autenticación SSH`, súbelo a la playlist `B0_Prerrequisitos` (No listado) y añade **timestamps**:
> ```
> 00:00 Paso 1 - Presentacion
> 00:20 Paso 2 — Generar la clave SSH
> 01:30 Paso 3 — Añadir la clave pública a GitHub
> 02:40 Paso 4 — Verificar la conexión
> 03:30 Paso 5 — Alternativa HTTPS + token
> 04:20 Paso 6 — Repaso final
> ```

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | No consigo copiar la clave: `Ctrl+C` no hace nada. | En la terminal `Ctrl+C` **interrumpe**, no copia. | **Selecciona la línea con el ratón** (en Git Bash eso ya la copia) o usa `Ctrl+Insert`. Ver la Fase 0.2.1. |
> | `Permission denied (publickey)`. | La clave pública no se añadió bien o se pegó cortada. | Repite el Paso 3: copia la línea **entera** de `id_ed25519.pub`. |
> | `Overwrite?` al generar la clave. | Ya había una clave en este equipo. | Escribe `n` y reutiliza la existente (salta al Paso 3 con `cat`). |
> | "key is invalid" al pegar. | Copiaste líneas de más o falta `ssh-ed25519`. | Copia solo la línea que empieza por `ssh-ed25519` y acaba en tu correo. |

> [!help] Preguntas Críticas
> 1. ¿Cuál de las dos claves se pega en GitHub? ¿Cuál NO se comparte nunca?
> 2. ¿Por qué usamos SSH en vez de la contraseña?
> 3. Si el año que viene usas otro ordenador, ¿reutilizas la clave o creas una nueva? ¿Por qué?

---

### ✅ Checklist Final de la Fase 0.2.2

- [ ] Clave SSH generada (`id_ed25519` y `id_ed25519.pub` en `~/.ssh`).
- [ ] Clave **pública** añadida a GitHub.
- [ ] `ssh -T git@github.com` responde `Hi TU-USUARIO!`.
- [ ] *(Alternativa)* Token HTTPS creado y guardado.
- [ ] Vídeo `B0.2.2 · Autenticación SSH` subido a la playlist `B0_Prerrequisitos`, con timestamps.
- [ ] **Enlace del vídeo pegado en tu entrada de apuntes** de esta fase.
- [ ] Grabada **🏫 en el centro**.

> **Siguiente paso:** Fase 0.3 — Crear el repositorio de tus apuntes del **Trimestre 1** y escribir la **entrada de esa fase**.
