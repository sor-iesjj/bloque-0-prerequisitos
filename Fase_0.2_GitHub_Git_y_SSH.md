


## 🔑 Fase 0.2: Cuenta de GitHub, Configuración de Git y Clave SSH

### Preparar el canal por el que me enviarás tu trabajo

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> En la Fase 0.1 montaste tu bóveda. Ahora vas a preparar **cómo esos apuntes llegan hasta mí por Internet** para que pueda corregirlos: creando una cuenta de GitHub, configurando Git en el equipo y dejando una **clave SSH** que evita tener que escribir la contraseña cada vez.
>
> **Profesor:** Pedro Navarro Miralles
> **Correo:** p.navarromiralles2@edu.gva.es
> **Centro:** IES Jorge Juan (ALICANTE)
>
> **⏱️ Tiempo estimado:** ~1,5 - 2 horas (teoría + creación de cuenta + configuración + verificación grabada)
> **Requisitos:** Git ya instalado en el equipo (lo instala Consellería, en Windows y en Linux). Bóveda `Boveda_SOR` ya creada (Fase 0.1). Conexión a Internet.

---

### 🎯 Objetivos de la fase

Al terminar esta fase serás capaz de:

- [ ] Explicar con tus palabras qué es **Git** y qué es **GitHub**, y en qué se diferencian.
- [ ] Comprobar que Git está instalado y abrir la terminal correcta en tu sistema.
- [ ] Crear tu **cuenta de GitHub** y confirmar el correo.
- [ ] Configurar Git con tu **nombre y correo** (los mismos que en GitHub).
- [ ] Generar una **clave SSH** y añadirla a GitHub para no escribir la contraseña en cada envío.
- [ ] Verificar con un comando que tu equipo y GitHub **se reconocen**.

---

### 🎯 ¿Dónde Estamos?

> [!info] El Punto de Partida
> Ya tienes tu bóveda con la estructura de carpetas (Fase 0.1). Pero de momento tus apuntes **solo existen en este ordenador**. Si el equipo del aula se borra, o quieres seguir en casa, o quieres que yo los vea… necesitas una forma de **enviarlos por Internet**. Esa forma es **Git + GitHub**.

> [!warning] El Problema
> Escribir tu contraseña de GitHub cada vez que envías un cambio es incómodo y, además, GitHub ya **no** deja usar la contraseña normal para esto. La solución profesional es una **clave SSH**: un candado digital que dejas puesto una vez y ya no molesta más. Es un poco más de trabajo hoy, pero te ahorra problemas todo el curso.

> [!success] Objetivo de esta Fase
> Dejar tu equipo **conectado con GitHub** de forma segura: cuenta creada, Git configurado con tus datos, y una clave SSH funcionando. Al final, un comando te dirá *"Hi, TU-USUARIO"* — esa es la señal de que todo está listo.

> [!tip] Hoja de Ruta
> 1. Comprobar que Git está instalado y abrir la terminal.
> 2. Crear la cuenta de GitHub y confirmar el correo.
> 3. Configurar Git con tu nombre y correo.
> 4. Generar tu clave SSH.
> 5. Añadir la clave pública a GitHub.
> 6. Verificar la conexión.
>
> **Resultado Final:** Equipo y GitHub reconociéndose sin pedir contraseña.
> **Siguiente:** Fase 0.3 — Crear el repositorio de tus apuntes del Trimestre 1 y escribir tu primera entrada del día.

---

### 📚 Fundamento Teórico

> [!info] Git y GitHub NO son lo mismo
> Es la confusión número uno, así que quédate con esto:
>
> | | Qué es | Dónde vive | Analogía |
> | :--- | :--- | :--- | :--- |
> | **Git** | Un programa que guarda el **historial** de tus ficheros: cada cambio, cuándo y quién. | **En tu ordenador** (instalado). | El cuaderno de bitácora donde apuntas cada cambio. |
> | **GitHub** | Una **web** donde subes tus proyectos Git para guardarlos en la nube y compartirlos. | **En Internet** (github.com). | La estantería en la nube donde dejas una copia de tu cuaderno para que otros lo vean. |
>
> **Git** hace el trabajo en tu equipo; **GitHub** guarda la copia en Internet y me deja verla. Los dos juntos son los que me permiten corregir tus apuntes.

> [!abstract] 1. Repositorio, commit, push, pull (vocabulario mínimo)
> - **Repositorio ("repo"):** una carpeta cuyo historial controla Git. Tu repo de apuntes del Trimestre 1 será uno de ellos.
> - **Commit:** una "foto" guardada de tus cambios en un momento, con un mensaje que la describe. *("Apuntes del 15 de septiembre")*.
> - **Push:** **subir** tus commits a GitHub (de tu ordenador → a la nube).
> - **Pull:** **bajar** los cambios desde GitHub (de la nube → a tu ordenador). Lo usarás sobre todo en casa.
>
> No te agobies: estos comandos los practicaremos de verdad en la Fase 0.3 y 0.4. Aquí solo te suenan.

> [!important] 2. Qué es una clave SSH (y por qué usamos esto en vez de la contraseña)
> Una clave SSH es una **pareja de ficheros** que se generan juntos:
> - **Clave privada:** se queda **siempre** en tu ordenador. **NUNCA se comparte, nunca se sube a ningún sitio.** Es tu llave secreta.
> - **Clave pública:** se puede compartir sin problema. **Esta es la que pegas en GitHub.**
>
> Funciona como un candado y su llave: la clave **pública** es el candado (lo pones en GitHub, a la vista); la clave **privada** es la única llave que lo abre (la guardas tú). Cuando envías cambios, GitHub comprueba que tu llave privada encaja con el candado público que dejaste — y te deja pasar **sin pedir contraseña**.

> [!warning] 3. Una clave por equipo
> La clave privada no se copia de un sitio a otro. Por eso **generarás una clave en el equipo del centro y otra distinta en casa**, y añadirás **las dos** a tu cuenta de GitHub. Es normal tener varias claves (una por dispositivo) en la misma cuenta.

### 📖 Diccionario de Conceptos Clave

> [!quote] Terminología profesional
> - **Git:** programa de control de versiones instalado en tu ordenador.
> - **GitHub:** web donde se alojan repositorios Git en la nube (`github.com`).
> - **Repositorio (repo):** carpeta con historial controlado por Git.
> - **Commit:** foto guardada de un conjunto de cambios, con su mensaje.
> - **Push / Pull:** subir / bajar cambios entre tu ordenador y GitHub.
> - **Clave SSH:** pareja pública/privada que autentica tu equipo ante GitHub sin contraseña.
> - **Clave privada:** secreta, se queda en tu equipo. NUNCA se comparte.
> - **Clave pública:** se pega en GitHub. Sin peligro compartirla.
> - **Terminal:** la ventana donde escribes comandos. En Windows usaremos **Git Bash**; en Linux, **Terminal**.

---

### 🛠️ Procedimiento Práctico

> [!danger] ⚠️ LÉEME: la clave privada no se comparte JAMÁS
> Durante esta fase vas a copiar y pegar una clave. Asegúrate de copiar **solo la clave PÚBLICA** (el fichero que termina en **`.pub`**). Si alguien te pide la privada, o la subes a algún sitio, o la pegas en un chat: **NO**. La privada se queda en tu equipo y punto.

> [!example] Paso 0: Comprueba Git y abre la terminal correcta
> **Abrir la terminal:**
> - **Windows:** busca **`Git Bash`** en el menú de inicio y ábrelo. (Git Bash viene con Git e incluye todo lo que necesitamos: `git`, `ssh-keygen`, `ssh`.) **Usa siempre Git Bash**, no el "Símbolo del sistema".
> - **Linux:** abre la aplicación **`Terminal`**.
>
> **Comprueba que Git está instalado**, escribiendo:
> ```bash
> git --version
> ```
> Deberías ver algo como `git version 2.40.0`. Si sale un error de "comando no encontrado", **avisa al profesor** (no lo instales tú).

> [!example] Paso 1: Crea tu cuenta de GitHub
> 1. Entra en **`github.com`** y pulsa **`Sign up`**.
> 2. Rellena:
>    - **Email:** usa un correo al que tengas acceso (tu correo educativo o personal). **Recuérdalo**, lo usarás en el Paso 3.
>    - **Password:** una contraseña segura. **Anótala** en un sitio fiable.
>    - **Username (nombre de usuario):** algo serio y reconocible, tipo `nombre-apellido` (ej. `juan-garcia-smr`). **Este nombre lo veré yo**, así que nada de motes raros.
> 3. Completa la verificación y **confirma el correo** (te llega un email con un enlace o un código).
>
> **Verificación:** entra en `github.com` con tu usuario; deberías ver tu panel (dashboard) vacío.

> [!example] Paso 2: Configura Git con tu nombre y correo
> En la terminal (Git Bash / Terminal), escribe estos dos comandos, **cambiando los datos por los tuyos** (usa el **mismo correo** que pusiste en GitHub):
> ```bash
> git config --global user.name "Juan Garcia"
> git config --global user.email "juan.garcia@alu.edu.gva.es"
> ```
> **Verificación:** comprueba que se guardaron bien:
> ```bash
> git config --global user.name
> git config --global user.email
> ```
> Deben devolverte tu nombre y tu correo.
>
> > [!tip] 💡 ¿Por qué el mismo correo que en GitHub?
> > Porque cada commit lleva "firmado" ese correo. Si coincide con el de tu cuenta, GitHub sabe que ese trabajo es tuyo y lo asocia a tu perfil.

> [!example] Paso 3: Genera tu clave SSH
> En la terminal, escribe (con **tu** correo de GitHub):
> ```bash
> ssh-keygen -t ed25519 -C "juan.garcia@alu.edu.gva.es"
> ```
> Te hará tres preguntas — **pulsa Enter en las tres** para aceptar lo que propone:
> 1. *Dónde guardar la clave* → Enter (ubicación por defecto).
> 2. *Passphrase (contraseña de la clave)* → Enter (la dejamos vacía).
> 3. *Repetir passphrase* → Enter.
>
> Al terminar verás un dibujo raro de letras y símbolos ("randomart"): es normal, significa que la clave se creó bien.
>
> **Verificación:** comprueba que existen los dos ficheros de la clave:
> ```bash
> ls ~/.ssh
> ```
> Debes ver **`id_ed25519`** (la privada, secreta) y **`id_ed25519.pub`** (la pública, la que compartes).

> [!example] Paso 4: Copia tu clave PÚBLICA y añádela a GitHub
> 1. Muestra la clave **pública** en pantalla:
>    ```bash
>    cat ~/.ssh/id_ed25519.pub
>    ```
>    Verás una línea larga que empieza por `ssh-ed25519 AAAA...` y termina con tu correo.
> 2. **Selecciona esa línea entera** y cópiala (en Git Bash: seleccionar con el ratón ya copia; o clic derecho → Copy).
> 3. En GitHub (navegador): pulsa tu **foto de perfil** (arriba a la derecha) → **`Settings`** → en el menú de la izquierda, **`SSH and GPG keys`** → botón **`New SSH key`**.
> 4. Rellena:
>    - **Title:** un nombre para identificar el equipo, ej. `Equipo Centro` (en casa pondrás `Equipo Casa`).
>    - **Key:** pega la línea que copiaste.
> 5. Pulsa **`Add SSH key`**.
>
> > [!warning] ⚠️ Copia la clave entera, sin cortarla
> > Debe empezar por `ssh-ed25519` e ir hasta el final (tu correo). Si te dejas un trozo, la conexión fallará en el Paso 5.

> [!example] Paso 5: Verifica que tu equipo y GitHub se reconocen
> En la terminal, escribe:
> ```bash
> ssh -T git@github.com
> ```
> - La primera vez te preguntará *"Are you sure you want to continue connecting?"* → escribe **`yes`** y Enter.
> - Deberías ver un mensaje tipo:
>   ```
>   Hi juan-garcia-smr! You've successfully authenticated, but GitHub does not provide shell access.
>   ```
>
> > [!success] ✅ Si ves "Hi TU-USUARIO! You've successfully authenticated", la Fase 0.2 está completa
> > No te asustes por la parte de *"does not provide shell access"*: es normal, no es un error. Significa que la clave funciona.

> [!example] Paso 5B (alternativa): conectar por HTTPS + token
> SSH es la vía **recomendada**, pero GitHub admite otra: **HTTPS con un token**. En vez de una clave, creas un *Personal Access Token* que usarás como contraseña. Puedes montar esta vía **además** de SSH, para conocer las dos (así, cuando yo te pase un repo, podrás clonarlo del modo que prefieras).
> 1. En GitHub: **foto de perfil → Settings → Developer settings → Personal access tokens → Tokens (classic) → Generate new token (classic)**.
> 2. Marca el permiso **`repo`**, pon una caducidad y pulsa **Generate token**.
> 3. **Copia el token ahora** (solo se muestra una vez) y guárdalo en un sitio seguro.
> 4. La primera vez que hagas `git push` o `git clone` **por HTTPS**, GitHub pedirá usuario y contraseña: pon tu usuario y **pega el token como contraseña** (nunca tu contraseña normal).
>
> > [!warning] La diferencia clave con SSH
> > El token **caduca** y hay que renovarlo cada cierto tiempo; la clave SSH no. Por eso, para el día a día, recomendamos SSH. Pero un técnico sabe usar las dos: es lo mismo repo por dos puertas (`git@github.com:...` con SSH, `https://github.com/...` con token).

> [!example] Paso 6: Grábalo con OBS
> Como en toda práctica: abre **OBS**, graba una toma corta mostrando el resultado del Paso 5 (el mensaje *"Hi TU-USUARIO"*) y explicando en voz alta que has creado la cuenta, configurado Git y añadido tu clave SSH. Guarda el vídeo como evidencia.

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Tabla de Troubleshooting (¿Algo no funciona?)
> | Problema | Causa Probable | Solución Sugerida |
> | :--- | :--- | :--- |
> | `git: command not found`. | Git no está instalado, o en Windows abriste el "Símbolo del sistema" en vez de Git Bash. | En Windows, abre **Git Bash**. Si aun así falla, avisa al profesor: Git lo instala Consellería. |
> | `ssh -T git@github.com` responde `Permission denied (publickey)`. | La clave pública no se añadió bien a GitHub, o se pegó cortada. | Repite el Paso 4: vuelve a copiar la línea **entera** de `id_ed25519.pub` y pégala en una nueva SSH key. |
> | Al generar la clave me pide un fichero que ya existe (`Overwrite?`). | Ya habías creado una clave antes en este equipo. | Escribe `n` (no sobrescribir) y usa la clave existente; salta al Paso 4 con `cat ~/.ssh/id_ed25519.pub`. |
> | No me llega el correo de confirmación de GitHub. | Está en spam, o escribiste mal el correo. | Revisa la carpeta de spam. Si no aparece, en GitHub puedes reenviar la confirmación desde `Settings → Emails`. |
> | Pegué la clave pero GitHub da error "key is invalid". | Copiaste también líneas de más, o falta el principio `ssh-ed25519`. | Copia solo la línea que empieza por `ssh-ed25519` y termina en tu correo, sin saltos de línea. |

> [!help] Preguntas Críticas (Autoevaluación del alumno)
> 1. Explica con tus palabras la diferencia entre **Git** y **GitHub**.
> 2. ¿Cuál de las dos claves (pública o privada) se pega en GitHub? ¿Cuál no se comparte NUNCA?
> 3. ¿Por qué usamos una clave SSH en vez de escribir la contraseña en cada envío?
> 4. Si el año que viene trabajas desde un ordenador nuevo, ¿tendrás que crear una clave nueva o puedes copiar la de este equipo? ¿Por qué?
> 5. 🔬 **Reto:** ejecuta `cat ~/.ssh/id_ed25519` (la **privada**) solo para *ver* qué aspecto tiene… y luego explica por qué ese contenido no debe salir jamás de tu ordenador. (No lo copies a ningún sitio.)

---

### ✅ Checklist Final de la Fase 0.2

- [ ] `git --version` funciona en la terminal (Git Bash en Windows / Terminal en Linux).
- [ ] Cuenta de GitHub creada y correo confirmado.
- [ ] Git configurado con `user.name` y `user.email` (mismo correo que GitHub).
- [ ] Clave SSH generada (`id_ed25519` y `id_ed25519.pub` existen en `~/.ssh`).
- [ ] Clave **pública** añadida a GitHub (`Settings → SSH and GPG keys`).
- [ ] `ssh -T git@github.com` responde `Hi TU-USUARIO! You've successfully authenticated`.
- [ ] *(Alternativa)* Token HTTPS creado y guardado, para poder clonar también por `https://`.
- [ ] Vídeo de OBS grabado con la verificación.

> **Siguiente paso:** Fase 0.3 — Crear el repositorio de tus apuntes del **Trimestre 1**, conectarlo con GitHub y escribir tu **primera entrada del día** con el formato obligatorio.
