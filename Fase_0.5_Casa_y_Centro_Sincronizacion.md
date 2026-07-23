## 🏠 Fase 0.5: Trabajar en Casa y en el Centro — Sincronización con Git

### El mismo entorno en los dos sitios, sin líos con OneDrive

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> Trabajarás en **dos ordenadores**: el del centro y el de tu casa. Esta fase te enseña a tener el **mismo entorno** en los dos y a **sincronizarlos con Git** (nunca con OneDrive), para que nunca pierdas trabajo ni se te dupliquen los ficheros.
>
> **Profesor:** Pedro Navarro Miralles
> **Correo:** p.navarromiralles2@edu.gva.es
> **Centro:** IES Jorge Juan (ALICANTE)
>
> **⏱️ Tiempo estimado:** ~2 horas (parte en casa) — instalar herramientas + clonar repos + practicar el ciclo pull/push
> **Requisitos:** Fases 0.1 a 0.4 completas (con tus repos ya en GitHub). En casa: un ordenador donde **sí** tengas permisos de administrador.

---

### 🎯 Objetivos de la fase

Al terminar esta fase serás capaz de:

- [ ] Instalar en casa las herramientas (Obsidian, Git, OBS) — en casa **sí** tienes permisos.
- [ ] Crear una **clave SSH del equipo de casa** y añadirla a GitHub.
- [ ] **Reconstruir la bóveda** en casa clonando tus repos desde GitHub.
- [ ] Dominar el **ciclo diario**: `pull` al empezar → trabajar → `commit` y `push` al terminar.
- [ ] Explicar por qué **OneDrive y Git no pueden gestionar la misma carpeta**.

---

### 🎯 ¿Dónde Estamos?

> [!info] El Punto de Partida
> En el centro ya tienes todo montado y subido a GitHub (Fases 0.1–0.4). Pero en casa tienes **otro ordenador**, que aún no sabe nada de tu trabajo. La gracia es que, como todo está en GitHub, puedes **reconstruirlo en casa en minutos** — sin copiar nada con un pendrive.

> [!warning] El Problema (¡el importante de esta fase!)
> Es tentador meter la bóveda en **OneDrive** para "tenerla en los dos sitios automáticamente". **NO lo hagas.** Si OneDrive y Git sincronizan la misma carpeta a la vez, se pelean: OneDrive corrompe el historial de Git y crea "copias en conflicto" (`fichero-PORTATIL.md`). Además, si OneDrive ya te trae los ficheros, el `git pull` deja de tener sentido y todo se desordena. **Un solo puente entre casa y centro: Git + GitHub. OneDrive fuera.**

> [!success] Objetivo de esta Fase
> Tener en casa una copia de tu bóveda **idéntica** a la del centro, sincronizada **solo** por Git, y saber el ciclo diario de memoria: **primero `pull`, al final `push`.**

> [!tip] Hoja de Ruta
> 1. En casa: instalar Obsidian, Git y OBS.
> 2. Crear la clave SSH del equipo de casa y añadirla a GitHub.
> 3. Recrear la estructura `Boveda_SOR` y clonar tus repos en su sitio.
> 4. Practicar el ciclo `pull → trabajar → push`.
> 5. Confirmar que un cambio hecho en casa aparece al día siguiente en el centro.
>
> **Resultado Final:** Dos ordenadores, un solo trabajo, sincronizado por Git.
> **Siguiente:** Fase 0.6 — Simulación final completa, grabada, que demuestra que TODO funciona.

---

### 📚 Fundamento Teórico

> [!danger] 1. Por qué OneDrive y Git NO pueden convivir en la misma carpeta
> Los dos son "sincronizadores", pero funcionan de formas incompatibles:
> - **Git** guarda su historial en una carpeta oculta llamada `.git`. Es delicada: si algo la copia a medias, el repositorio se **corrompe**.
> - **OneDrive** copia ficheros en segundo plano, cuando le parece, y **no entiende** qué es `.git`. Al sincronizarla a medias, la rompe.
> - Cuando **los dos** tocan los mismos ficheros, OneDrive crea **copias en conflicto** con nombres raros, y Git ya no sabe cuál es la buena.
>
> **Conclusión:** la bóveda va en una carpeta **local** (fuera de OneDrive) en los dos ordenadores. GitHub es tu "nube"; OneDrive, para otras cosas.

> [!important] 2. El ciclo diario: PULL al empezar, PUSH al terminar
> Esta es la rutina que evita el 99% de los problemas:
> ```
> 1. Llego a un ordenador  →  git pull     (bajo lo último que subí desde el otro)
> 2. Trabajo (Obsidian)    →  edito / creo entradas
> 3. Antes de irme         →  git add . → git commit → git push   (subo lo de hoy)
> ```
> Si **siempre** haces `pull` al empezar y `push` al terminar, tus dos ordenadores nunca se desincronizan.

> [!warning] 3. ¿Qué pasa si olvido el pull?
> Si editas en casa sin haber bajado antes lo que hiciste en el centro, puede aparecer un **conflicto** (Git no sabe qué versión vale). No es grave, pero es un lío para principiantes. Por eso: **primero `pull`, siempre.** Si alguna vez ves la palabra `CONFLICT`, para y pregúntame.

### 📖 Diccionario de Conceptos Clave

> [!quote] Terminología
> - **`git pull`:** baja de GitHub los cambios nuevos y los une a tu copia local.
> - **`git push`:** sube tus cambios locales a GitHub.
> - **Conflicto (merge conflict):** cuando el mismo fichero se cambió en dos sitios y Git no sabe cuál conservar.
> - **Copia en conflicto (OneDrive):** fichero duplicado con nombre raro que crea OneDrive cuando dos equipos lo tocan. Señal de que OneDrive está estorbando.
> - **Local:** que está en el disco de tu ordenador, no en la nube.

---

### 🛠️ Procedimiento Práctico (en casa)

> [!example] Paso 1: Instala las herramientas (en casa SÍ puedes)
> En tu ordenador de casa, con permisos de administrador:
> 1. **Obsidian:** descárgalo de `obsidian.md` e instálalo.
> 2. **Git:** descárgalo de `git-scm.com` (Windows) o instálalo con el gestor de paquetes (Linux: `sudo apt install git`).
> 3. **OBS Studio:** descárgalo de `obsproject.com` e instálalo (lo necesitas para grabar las entregas de casa).
>
> **Verificación:** abre la terminal (Git Bash en Windows / Terminal en Linux) y ejecuta `git --version`.

> [!example] Paso 2: Clave SSH del equipo de casa
> Repite lo de la Fase 0.2, **pero en este ordenador** (la clave es distinta en cada equipo):
> ```bash
> ssh-keygen -t ed25519 -C "tu-correo-de-github"
> cat ~/.ssh/id_ed25519.pub
> ```
> Copia la clave **pública** y añádela a GitHub (`Settings → SSH and GPG keys → New SSH key`), con el título **`Equipo Casa`**.
>
> **Verificación:**
> ```bash
> ssh -T git@github.com
> ```
> Debe responder `Hi TU-USUARIO!`.
>
> > [!tip] 💡 Configura también tu nombre y correo en Git aquí
> > ```bash
> > git config --global user.name "Tu Nombre"
> > git config --global user.email "tu-correo-de-github"
> > ```

> [!example] Paso 3: Reconstruye la bóveda clonando tus repos
> No copies nada con pendrive: **clona desde GitHub**, que es donde está lo bueno.
> 1. Crea la estructura contenedor (igual que en la Fase 0.1), en una ruta **local**:
>    ```bash
>    mkdir -p ~/SOR/Boveda_SOR/00_Apuntes
>    mkdir -p ~/SOR/Boveda_SOR/Practicas
>    ```
> 2. Clona tu repo de apuntes **dentro de `00_Apuntes/`**, con el nombre de carpeta `Trimestre_1`:
>    ```bash
>    cd ~/SOR/Boveda_SOR/00_Apuntes
>    git clone git@github.com:TU-USUARIO/apuntes-sor-t1.git Trimestre_1
>    ```
> 3. Clona tu práctica **dentro de `Practicas/`**:
>    ```bash
>    cd ~/SOR/Boveda_SOR/Practicas
>    git clone git@github.com:TU-USUARIO/boochan-1.git
>    ```
> 4. Abre Obsidian → **`Open folder as vault`** → elige `~/SOR/Boveda_SOR`.
>
> > [!tip] SSH o HTTPS, tú eliges
> > Los `git clone` de arriba usan SSH (`git@github.com:...`). Si en este equipo montaste la vía del **token**, clona por HTTPS cambiando la dirección a `https://github.com/TU-USUARIO/apuntes-sor-t1.git` (y añade `Trimestre_1` al final igual). Es el mismo repo.
>
> **Verificación:** en Obsidian, en casa, ves la misma estructura y los mismos ficheros que en el centro (tus apuntes y la práctica).
>
> > [!note] 📌 Fíjate en el truco del nombre
> > Al clonar los apuntes escribimos `... .git Trimestre_1` al final: eso le dice a Git que **la carpeta se llame `Trimestre_1`** (y no `apuntes-sor-t1`), para que la estructura sea idéntica a la del centro.

> [!example] Paso 4: Practica el ciclo diario
> Simula un día de trabajo en casa:
> 1. **Al empezar**, baja lo último:
>    ```bash
>    cd ~/SOR/Boveda_SOR/00_Apuntes/Trimestre_1
>    git pull
>    ```
> 2. En Obsidian, crea una entrada de prueba (con el formato de la Fase 0.3).
> 3. **Al terminar**, sube:
>    ```bash
>    git add .
>    git commit -m "Apuntes desde casa (prueba)"
>    git push
>    ```
> 4. Compruébalo en GitHub.

> [!example] Paso 5: Confirma la sincronización centro ↔ casa
> Al día siguiente, **en el centro**, antes de nada:
> ```bash
> cd ~/SOR/Boveda_SOR/00_Apuntes/Trimestre_1
> git pull
> ```
> Debe **bajar** la entrada que creaste en casa. Si aparece, la sincronización funciona: has trabajado en dos ordenadores distintos con un solo trabajo, sin pendrives y sin OneDrive.
>
> > [!success] ✅ Si el `pull` en el centro trae lo que hiciste en casa, la Fase 0.5 está completa
> > Entorno replicado + ciclo pull/push dominado + cero OneDrive. Ya trabajas como un técnico de verdad.

> [!example] Paso 6: Grábalo con OBS
> Graba en casa (Paso 4) el ciclo `pull → editar → push`, explicándolo. Recuerda: **cada práctica tiene doble entrega, una en el centro y otra en casa.** Esta fase es un buen ejemplo de la entrega "de casa".

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Tabla de Troubleshooting (¿Algo no funciona?)
> | Problema | Causa Probable | Solución Sugerida |
> | :--- | :--- | :--- |
> | Aparecen ficheros `... -MiPortatil.md` duplicados. | La bóveda está dentro de OneDrive: son "copias en conflicto". | Saca la bóveda de OneDrive a una carpeta local, borra las copias en conflicto y trabaja solo con Git. |
> | `git pull` dice `CONFLICT (content)`. | Editaste el mismo fichero en casa y en el centro sin hacer `pull` antes. | Para y pregunta al profesor. Para evitarlo: **siempre `pull` al empezar**. |
> | `git pull` dice `Your branch is behind... fast-forward`. | Hay cambios en GitHub que no tenías. Es lo normal y bueno. | Deja que haga el `pull`; baja los cambios sin problema. |
> | Cloné los apuntes pero la carpeta se llama `apuntes-sor-t1`, no `Trimestre_1`. | Olvidaste poner el nombre al final del `git clone`. | Renómbrala a `Trimestre_1`, o bórrala y clona de nuevo con `... .git Trimestre_1`. |
> | En casa no me deja instalar Git/Obsidian. | Usuario sin permisos en el equipo de casa. | Usa una cuenta con permisos de administrador; si no la tienes, coméntamelo. |

> [!help] Preguntas Críticas (Autoevaluación del alumno)
> 1. ¿Por qué NO se puede meter la bóveda dentro de OneDrive si usamos Git?
> 2. Escribe el ciclo diario de tres pasos (qué haces al llegar, mientras trabajas y antes de irte).
> 3. ¿Qué comando usas para **bajar** cambios y cuál para **subirlos**?
> 4. Si olvidas hacer `pull` al empezar y editas, ¿qué problema puede aparecer?
> 5. 🔬 **Reto:** haz un cambio pequeño en casa y súbelo; al día siguiente, en el centro, haz `pull` y comprueba que aparece. Describe en tus apuntes qué comandos usaste en cada sitio.

---

### ✅ Checklist Final de la Fase 0.5

- [ ] Obsidian, Git y OBS instalados en el equipo de casa.
- [ ] Clave SSH del equipo de casa creada y añadida a GitHub (`Equipo Casa`).
- [ ] Estructura `Boveda_SOR` recreada en casa (local, fuera de OneDrive).
- [ ] Repos clonados en su sitio: apuntes en `00_Apuntes/Trimestre_1`, práctica en `Practicas/boochan-1`.
- [ ] Ciclo `pull → editar → push` practicado en casa.
- [ ] Cambio de casa confirmado con `pull` en el centro (o viceversa).
- [ ] Vídeo de OBS de la entrega de casa.

> **Siguiente paso:** Fase 0.6 — Simulación final: un recorrido completo de principio a fin, grabado, que demuestra que todo tu entorno funciona.
