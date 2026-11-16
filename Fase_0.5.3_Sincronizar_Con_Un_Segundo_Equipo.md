## 🔄 Fase 0.5.3: Sincronizar con un Segundo Equipo (opcional)

### Un segundo ordenador en clase, sin una segunda cuenta

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0.5 — parte 3 de 3 · OPCIONAL y VOLUNTARIA]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~45 minutos · **Requisitos:** Fases 0.5.1 y 0.5.2 completas.

---

> [!abstract] 📋 Qué demuestras aquí
> **Esta práctica no añade criterio nuevo.** Refuerza el que ya declaras en la Fase 0.5.2:
>
> | Código | Criterio de evaluación |
> | :--- | :--- |
> | `CE.05.e` | Se han ejecutado operaciones para la automatización de tareas del sistema. |
>
> Es **voluntaria y opcional**. **No sustituye a ninguna entrega obligatoria.** Cómo cuenta para la nota lo digo yo en clase.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin.
> 1. **Prepárate primero (sin grabar):** lee el procedimiento entero y **crea la entrada de apuntes** `b0-0.5.3-sincronizar-con-un-segundo-equipo.md` con la estructura del **Bloque 0 · Fase 0.1.b**, **vacía**. Se rellena después.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a explicar la Fase 0.5.3 — Sincronizar con un segundo equipo."* Y **muestra tu perfil de GitHub**.
> 3. **Graba TODO**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `B0.5.3 · Sincronizar con un segundo equipo` y súbelo a tu playlist **`B0_Prerrequisitos`** (No listado).
> 6. **~8 min.** Se graba en **🏫 el centro** (o en casa, si lo haces allí).
> 7. **No hay tarea propia en Teams** para esta práctica: el vídeo se queda en la playlist y el enlace en tu entrada. Te digo en clase cómo lo recojo.
> 8. **El enlace del vídeo va DENTRO de tu entrada de apuntes**, en el apartado `🔗 Enlaces`.

---

### 🎯 Objetivos

- [ ] Comprobar si un equipo puede abrir **Windows Sandbox** (o si toca el **Plan B**).
- [ ] Montar un segundo equipo limpio en el centro, **sin una segunda cuenta** de Windows.
- [ ] Repetir el ciclo `pull → push` entre los dos equipos, **en los dos sentidos**.
- [ ] Explicar qué pasa con lo que no hayas empujado antes de cerrar el sandbox.

---

### 📚 Fundamento Teórico

> [!info] 🤔 El problema: dos equipos, una sola cuenta
> La **Fase 0.5.2** la grabaste en **casa**, con **un solo ordenador**: el ciclo `pull → push` se explica, pero no se demuestra. Para demostrarlo hacen falta **dos equipos**.
>
> En el centro hay un problema: **tu cuenta de Windows es la única que puedes usar**. No puedes crear otra, no puedes entrar con la de un compañero.
>
> | Opción | ¿Vale? | Por qué |
> | :--- | :--- | :--- |
> | Crear una cuenta nueva en el equipo | **No** | No tienes permisos de administrador. Y no los vas a tener. |
> | Traer tu ordenador de casa | Sí, pero... | No todo el mundo puede, y pesa. Vale como último recurso. |
> | Cambiarte a otro equipo del aula | Sí, pero... | Necesitas **dos** equipos libres por alumno. No hay. |
> | **Windows Sandbox** | **Sí** | Es un segundo Windows dentro del mismo equipo, con **tu misma cuenta**. |
>
> **Aquí usamos la cuarta.** Y de paso aprendes una herramienta que sirve para mucho más que esto.

> [!info] Qué es Windows Sandbox
> Un **Windows limpio, temporal y aislado** que arranca **dentro** de tu Windows. No es una máquina virtual que instalas y configuras: viene con el sistema.
> - Arranca en segundos.
> - No toca tu Windows: nada de lo que hagas dentro sale fuera.
> - **Al cerrar la ventana se borra entero.** Como si nunca hubiera existido.
>
> Es, literalmente, **un segundo ordenador dentro de tu ordenador** — y no necesita una segunda cuenta.

> [!danger] El fallo nº1: cerrar el sandbox sin subir el trabajo
> Todo lo que no hayas **empujado** a GitHub se pierde al cerrar la ventana. **No hay papelera.** Es el fallo que más veces se comete con una máquina desechable, y se comete una sola vez.
> **Regla:** `push` antes de cerrar. Siempre.

> [!warning] Windows Sandbox NO es la VM de VirtualBox
> | | VirtualBox | Windows Sandbox |
> | :--- | :--- | :--- |
> | Se instala | Sí | No, ya viene |
> | Se configura | Sí | No |
> | Guarda el estado | Sí, instantáneas | **No, nunca** |
> | Sirve para | Montar un servidor | Probar y **no ensuciar** |
>
> No intentes montar aquí tu servidor de prácticas: se borra.

> [!example] Vocabulario
> - **Sandbox:** caja de arena. Entorno aislado y desechable.
> - **Desechable:** se borra al cerrar. No hay que limpiarlo.
> - **Equipo Centro / Equipo Casa / Sandbox IES:** los **títulos** de tus claves SSH. Una clave por equipo, como en la Fase 0.5.1.

---

### 🛠️ Procedimiento Práctico

> [!example] Paso 0: Comprueba tu equipo (todavía SIN grabar)
> 1. Abre una terminal y escribe `winver`. Tiene que ser **Windows 11 Pro, Enterprise o Education**. En **Home** no existe.
> 2. Busca **Windows Sandbox** en el menú Inicio.
>    - **Aparece** → adelante.
>    - **No aparece** → no está activada. Eso solo lo puede hacer un administrador: **avísame**. No lo intentes tú.
> 3. Comprueba que el equipo tenga **4 GB de RAM** y **dos núcleos**. Es el mínimo.

> [!warning] Plan B · Si el sandbox no arranca o no existe
> Entonces lo hacemos como estaba pensado al principio: **dos equipos del aula**.
> - Te sientas en el equipo A y en el equipo B, uno detrás de otro.
> - Los dos con **tu misma cuenta de GitHub**. En cada equipo generas su clave SSH y la titulas `Equipo Centro 1` y `Equipo Centro 2`.
> - El procedimiento es **el mismo de abajo**, saltando el Paso 3 (instalar Git: en el aula ya está) y cambiando "sandbox" por "el otro equipo".
>
> Si te toca Plan B, dilo al empezar el vídeo: *"En este equipo no arranca Windows Sandbox, así que uso dos equipos."*

> [!example] Paso 1: Arranca la grabación y empuja desde el centro
> Inicia OBS, preséntate y muestra tu perfil de GitHub.
> 1. En Obsidian, crea **la entrada vacía** de esta fase (`b0-0.5.3-sincronizar-con-un-segundo-equipo.md`), con la plantilla de la Fase 0.1.b.
> 2. Súbela. Clic derecho sobre `Trimestre_1` → abrir terminal ahí:
>    ```bash
>    pwd          # .../Boveda_SOR/00_Apuntes/Trimestre_1
>    git add .
>    git commit -m "Fase 0.5.3: entrada creada en el centro"
>    git push
>    ```
> 3. Compruébalo en GitHub. **Ese es el estado de partida del "otro equipo".**

> [!example] Paso 2: Abre el sandbox y mira qué hay dentro
> Menú Inicio → **Windows Sandbox**. Espera a que cargue.
> Dentro **no están** tus cosas: ni tu usuario, ni Obsidian, ni Git, ni tus apuntes. Di en voz alta: **"este es mi segundo equipo"**.
> Arranca con 4 GB, con red y con el portapapeles compartido con tu equipo del centro.

> [!example] Paso 3: Instala Git DENTRO del sandbox
> 1. Abre **Edge** dentro del sandbox → `git-scm.com/download/win` → descarga el instalador de 64 bits.
> 2. Ejecútalo y dale a **Siguiente** hasta el final, sin cambiar nada. **Dentro del sandbox eres administrador**, así que aquí sí puedes instalar.
> 3. Menú Inicio **del sandbox** → **Git Bash**. Comprueba:
>    ```bash
>    git --version
>    ```
>    > [!tip] 💡 Si la descarga está bloqueada
>    > Trae el instalador en un pendrive y cópialo a tu carpeta antes de abrir el sandbox. El sandbox **no ve** tus carpetas: solo lo que le pases a mano o copies por el portapapeles (los ficheros también se copian y se pegan).

> [!example] Paso 4: La clave SSH del sandbox
> En el **Git Bash del sandbox**:
> ```bash
> git config --global user.name "Tu Nombre"
> git config --global user.email "tu-correo-de-github"
> ssh-keygen -t ed25519 -C "sandbox IES"
> cat ~/.ssh/id_ed25519.pub
> ```
> 1. Selecciona **toda** la línea que empieza por `ssh-ed25519` y cópiala. El portapapeles está compartido: puedes pegarla en el navegador del equipo del centro.
> 2. En GitHub → `Settings` → `SSH and GPG keys` → **New SSH key**. Título: **`Sandbox IES`**. Pega y guarda.
>
> Es lo mismo que hiciste en casa en la Fase 0.5.1: **una clave por equipo**. La privada no sale del sandbox.

> [!example] Paso 5: Clona y empuja desde el sandbox (el "casa" simulado)
> En el **Git Bash del sandbox**:
> ```bash
> mkdir -p ~/Boveda_SOR/00_Apuntes
> cd ~/Boveda_SOR/00_Apuntes
> git clone git@github.com:TU-USUARIO/TU-REPO-APUNTES.git Trimestre_1
> cd Trimestre_1
> ls b0-0.5.3-*.md
> ```
> `TU-USUARIO/TU-REPO-APUNTES` es **el tuyo**: el de la Fase 0.3. Ahora escribe en la entrada desde aquí, sin editor:
> ```bash
> echo "" >> b0-0.5.3-sincronizar-con-un-segundo-equipo.md
> echo "Escrito desde el sandbox del IES." >> b0-0.5.3-sincronizar-con-un-segundo-equipo.md
> git add .
> git commit -m "Fase 0.5.3: linea escrita desde el sandbox"
> git push
> ```
> Explícalo: **esto es lo que haces en casa un domingo por la noche**.

> [!example] Paso 6: Baja el cambio en el equipo del centro
> En el **Git Bash del equipo del centro**, en `Trimestre_1`:
> ```bash
> pwd
> git pull
> git log --oneline -3
> ```
> Abre la entrada en Obsidian: **la línea está ahí**. El trabajo hecho "en el otro equipo" ha llegado solo, sin pendrive y sin correo.

> [!example] Paso 7: El viaje de vuelta
> 1. **En el centro:** escribe algo de verdad en la entrada con Obsidian y súbelo.
>    ```bash
>    git add .
>    git commit -m "Fase 0.5.3: escrito en el centro"
>    git push
>    ```
> 2. **En el sandbox:** baja lo que acabas de subir.
>    ```bash
>    cd ~/Boveda_SOR/00_Apuntes/Trimestre_1
>    git pull
>    tail -5 b0-0.5.3-sincronizar-con-un-segundo-equipo.md
>    ```
> Las dos direcciones funcionan. **Ese es el ciclo completo** de la Fase 0.5.2, demostrado de verdad.

> [!example] Paso 8: Cierra el sandbox y compruébalo
> 1. Cierra la ventana del sandbox y confirma. **Todo se borra.**
> 2. Vuelve a abrir un sandbox y enseña que **no hay repo, ni clave, ni Git**. Eso es "desechable".
> 3. Di lo que habría pasado si no hubieras hecho el `push` del Paso 5.

> [!example] Paso 9: Limpia la clave `Sandbox IES`
> En GitHub → `Settings` → `SSH and GPG keys` → borra **solo** la clave `Sandbox IES`.
>
> La máquina ya no existe: esa clave es una puerta abierta que no usa nadie.
> 🛑 **No borres `Equipo Centro` ni `Equipo Casa`.** Si las borras, esos equipos dejan de poder subir tu trabajo.

> [!example] Paso 10: Cierra el vídeo, nómbralo y súbelo
> Detén la grabación, nombra el vídeo `B0.5.3 · Sincronizar con un segundo equipo`, súbelo a la playlist `B0_Prerrequisitos` (No listado) con **timestamps**. Pega el enlace en tu entrada, en `🔗 Enlaces`.

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | Windows Sandbox no aparece en el menú Inicio. | No está activado, o el equipo es Windows Home. | Avísame. Si no se puede activar, **Plan B**. |
> | `No hypervisor was found`. | El equipo no tiene la virtualización disponible. | No se arregla desde tu cuenta: **Plan B**. |
> | `git: command not found` dentro del sandbox. | No instalaste Git **dentro** del sandbox. | Repite el Paso 3. El Git de fuera no entra. |
> | `Permission denied (publickey)`. | La clave del sandbox no está en GitHub, o pegaste la privada. | Añade `id_ed25519.pub` (la que acaba en `.pub`). |
> | Pide usuario y contraseña al clonar. | Clonaste por HTTPS, no por SSH. | Usa `git@github.com:...` |
> | `CONFLICT` en el `pull`. | Editaste el mismo trozo en los dos equipos. | Para y pregúntame. |
> | La línea no aparece tras el `pull`. | No hiciste `push`, o estás en otra carpeta. | `pwd` y `git log --oneline -3` en los dos. |
> | Cierro el sandbox y he perdido el trabajo. | No empujaste antes de cerrar. |  `push` antes de cerrar. Siempre. |

> [!help] Preguntas Críticas
> 1. ¿Por qué el sandbox no necesita una segunda cuenta de Windows y el equipo del aula sí?
> 2. ¿Qué pasa con la clave SSH del sandbox al cerrar la ventana? ¿Y por qué hay que borrarla también de GitHub?
> 3. Explica con tus palabras por qué este ejercicio demuestra lo mismo que la Fase 0.5.2, que grabaste en casa.
> 4. Si mañana tienes que probar un programa que no te fías, ¿qué ganas haciéndolo en un sandbox y qué pierdes frente a una máquina virtual?

---

### ✅ Checklist Final de la Fase 0.5.3

- [ ] Comprobé que el equipo puede abrir Windows Sandbox (o usé el **Plan B**).
- [ ] Entrada `b0-0.5.3-sincronizar-con-un-segundo-equipo.md` creada y subida.
- [ ] Sandbox abierto, Git instalado **dentro** y clave `Sandbox IES` añadida a GitHub.
- [ ] Repo clonado dentro del sandbox y **push** hecho desde ahí.
- [ ] `pull` en el equipo del centro: el cambio aparece.
- [ ] Viaje de vuelta: `pull` dentro del sandbox.
- [ ] Comprobado que el sandbox se borra al cerrar.
- [ ] Clave `Sandbox IES` borrada de GitHub. `Equipo Centro` y `Equipo Casa` intactas.
- [ ] Vídeo `B0.5.3 · Sincronizar con un segundo equipo` en la playlist, con timestamps.
- [ ] **Enlace del vídeo pegado en tu entrada de apuntes.**

> **Siguiente paso:** Fase 0.6 — Verificación final y simulación completa.
