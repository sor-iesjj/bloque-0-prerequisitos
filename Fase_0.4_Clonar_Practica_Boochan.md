## 📦 Fase 0.4: Tu Copia de la Práctica Boochan y el Ciclo de Trabajo con Git

### Descargar la práctica, hacerla tuya y aprender a subir cambios

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> Hasta ahora has trabajado con **tus apuntes**. Ahora toca el otro lado: las **prácticas**. Vas a crear **tu propia copia** de la práctica `boochan-1` a partir de la plantilla del profesor, clonarla dentro de `Practicas/`, y practicar el ciclo `status → add → commit → push` sobre ella.
>
> **Profesor:** Pedro Navarro Miralles
> **Correo:** p.navarromiralles2@edu.gva.es
> **Centro:** IES Jorge Juan (ALICANTE)
>
> **⏱️ Tiempo estimado:** ~1,5 - 2 horas (teoría + copia de plantilla + clonado + ciclo de cambios + verificación grabada)
> **Requisitos:** Fases 0.1, 0.2 y 0.3 completas. Clave SSH funcionando.

---

### 🎯 Objetivos de la fase

Al terminar esta fase serás capaz de:

- [ ] Explicar qué es una **plantilla** de repositorio y qué hace "Use this template".
- [ ] Crear **tu propia copia** de `boochan-1` en tu cuenta de GitHub.
- [ ] **Clonar** esa copia dentro de la carpeta `Practicas/` de tu bóveda.
- [ ] Hacer un cambio, verlo con `git status`, y subirlo con `add` → `commit` → `push`.
- [ ] Entender la diferencia entre **clonar** (bajar por primera vez) y **hacer push** (subir cambios).

---

### 🎯 ¿Dónde Estamos?

> [!info] El Punto de Partida
> El profesor tiene publicadas las prácticas Boochan como **plantillas públicas** en la organización `sor-iesjj` de GitHub. Tú no vas a trabajar sobre la plantilla del profesor (no puedes, ni debes): vas a crear **tu copia**, que será **tuya**, y trabajar sobre ella.

> [!warning] El Problema
> Si 20 alumnos trabajaran sobre el mismo repositorio, sería un caos y os pisaríais los cambios. Por eso cada uno saca **su propia copia** de la plantilla. Así cada alumno tiene su repo, con su historial, que puede modificar y entregar sin molestar a nadie.

> [!success] Objetivo de esta Fase
> Tener, dentro de `Practicas/boochan-1/`, tu copia de la práctica, conectada a **tu** GitHub, y haber demostrado que sabes subir un cambio con el ciclo completo de Git.

> [!tip] Hoja de Ruta
> 1. Crear tu copia de la plantilla con "Use this template".
> 2. Clonar tu copia dentro de `Practicas/`.
> 3. Abrirla en Obsidian (dentro de la misma bóveda).
> 4. Hacer un cambio (poner tu nombre), ver `git status`.
> 5. Subirlo con `add` → `commit` → `push` y verificarlo.
>
> **Resultado Final:** Tu práctica `boochan-1` clonada y con un primer cambio subido.
> **Siguiente:** Fase 0.5 — Montar el mismo entorno en casa y aprender a sincronizar centro ↔ casa con `git pull`.

---

### 📚 Fundamento Teórico

> [!info] 1. Plantilla y "Use this template"
> Una **plantilla** (template) es un repositorio pensado para que otros saquen copias de él. Al pulsar **"Use this template"**, GitHub crea en **tu** cuenta un repositorio **nuevo e independiente** con el mismo contenido, pero **con historial propio**. No es un enlace a la plantilla del profesor: es **tu** repo, y puedes cambiarlo a tu gusto.

> [!abstract] 2. Clonar vs. Push (no los confundas)
> | Acción | Dirección | Cuándo |
> | :--- | :--- | :--- |
> | **`git clone`** | GitHub → tu ordenador | **Una sola vez**, la primera, para bajar el repo. |
> | **`git push`** | tu ordenador → GitHub | **Cada vez** que quieras subir tus cambios. |
> | **`git pull`** | GitHub → tu ordenador | Para **bajar** cambios nuevos (lo verás en la Fase 0.5). |
>
> Regla: **clonas una vez, y luego trabajas con push/pull.** No se clona cada día.

> [!important] 3. Cuando clonas, ya viene "conectado"
> A diferencia de tus apuntes (donde tuviste que hacer `git init` y `git remote add`), al **clonar** una copia de GitHub el repositorio ya viene con su remoto configurado. Puedes hacer `push` directamente, sin preparar nada más.

### 📖 Diccionario de Conceptos Clave

> [!quote] Terminología
> - **Plantilla (template):** repositorio del que se sacan copias con "Use this template".
> - **`git clone`:** descarga por primera vez un repositorio de GitHub a tu ordenador.
> - **`git status`:** muestra qué ficheros han cambiado y cuáles están listos para el commit.
> - **Fork vs. copia de plantilla:** un *fork* mantiene un vínculo con el original; una **copia de plantilla** es independiente. Nosotros usamos **plantilla**.

---

### 🛠️ Procedimiento Práctico

> [!example] Paso 1: Crea tu copia de la plantilla en GitHub
> 1. Entra en la plantilla del profesor: `github.com/sor-iesjj/boochan-v1`
> 2. Pulsa el botón verde **`Use this template`** → **`Create a new repository`**.
> 3. Rellena:
>    - **Owner:** tu usuario.
>    - **Repository name:** `boochan-1`
>    - **Visibility:** como te indique el profesor (normalmente **Private**).
> 4. Pulsa **`Create repository`**.
> 5. En tu nuevo repo, botón **`Code`**, copia la dirección de tu vía: **SSH** `git@github.com:TU-USUARIO/boochan-1.git` **o** **HTTPS** `https://github.com/TU-USUARIO/boochan-1.git`.
>
> > [!tip] 💡 ¿No ves "Use this template"?
> > Significa que el repo del profesor todavía no está marcado como plantilla, o no has iniciado sesión. Avisa al profesor.

> [!example] Paso 2: Clona tu copia dentro de `Practicas/`
> Abre la terminal y **entra en la carpeta `Practicas`** de tu bóveda:
> ```bash
> cd ~/SOR/Boveda_SOR/Practicas
> ```
> Clona **tu** copia (usa tu dirección SSH):
> ```bash
> git clone git@github.com:TU-USUARIO/boochan-1.git
> ```
> Esto crea la carpeta `Practicas/boochan-1/` con todo el contenido.
>
> **Verificación:**
> ```bash
> cd boochan-1
> ls
> ```
> Debes ver los ficheros de la práctica (`Manual_BoochanV1.md`, carpeta `Fases/`, etc.).
>
> > [!danger] ⚠️ Clona dentro de `Practicas/`, no en cualquier sitio
> > Comprueba con `pwd` **antes** de clonar que estás en `.../Boveda_SOR/Practicas`. Si clonas en el sitio equivocado, borra la carpeta y clónala en su lugar correcto.

> [!example] Paso 3: Ábrela en Obsidian (sin cambiar de bóveda)
> Como `Practicas/boochan-1/` está **dentro** de tu bóveda `Boveda_SOR`, Obsidian ya la ve. Abre Obsidian y, en el panel izquierdo, despliega `Practicas/boochan-1/`. Podrás leer el manual y las fases **sin salir de tu bóveda de apuntes**. Ese es justo el objetivo del diseño: apuntes y prácticas, en una sola ventana.

> [!example] Paso 4: Haz un cambio y míralo con `git status`
> Vamos a hacer un cambio pequeño para practicar el ciclo:
> 1. En Obsidian, dentro de `Practicas/boochan-1/`, crea una nota nueva llamada `MIS_DATOS.md`.
> 2. Escribe dentro tu nombre y tu grupo, por ejemplo:
>    ```markdown
>    # Mis datos
>    - Alumno: Juan García
>    - Grupo: 2º SMR
>    ```
> 3. Guarda.
> 4. En la terminal, dentro de `Practicas/boochan-1/`:
>    ```bash
>    git status
>    ```
>    Git te mostrará `MIS_DATOS.md` como fichero **nuevo / sin seguimiento**.

> [!example] Paso 5: Sube el cambio (ciclo completo) y verifica
> Dentro de `Practicas/boochan-1/`:
> ```bash
> git add .
> git commit -m "Anadir mis datos de alumno"
> git push
> ```
> No pide contraseña (clave SSH de la Fase 0.2).
>
> **Verificación:** recarga tu repo `boochan-1` en GitHub. Debe aparecer `MIS_DATOS.md`.
>
> > [!success] ✅ Si `MIS_DATOS.md` aparece en GitHub, la Fase 0.4 está completa
> > Has creado tu copia, la has clonado en su sitio, y has subido un cambio con el ciclo completo de Git. Ya sabes trabajar con una práctica.

> [!example] Paso 6: Grábalo con OBS
> Graba con OBS el Paso 4 y 5 (el `git status` con el cambio, y el ciclo `add`/`commit`/`push` con la verificación en GitHub), explicando en voz alta cada comando.

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Tabla de Troubleshooting (¿Algo no funciona?)
> | Problema | Causa Probable | Solución Sugerida |
> | :--- | :--- | :--- |
> | `git clone` da `Permission denied (publickey)`. | Estás usando la URL SSH pero la clave no está configurada. | Repasa la Fase 0.2 (`ssh -T git@github.com`), **o** clona por HTTPS (`https://github.com/...`) y usa tu token. |
> | Cloné pero la carpeta `boochan-1` no aparece en Obsidian. | La clonaste fuera de la bóveda. | Comprueba con `pwd` dónde estás; mueve `boochan-1` dentro de `Practicas/` o clónala de nuevo en el sitio correcto. |
> | `git push` dice `nothing to commit`. | No hiciste `git add` o no guardaste el fichero en Obsidian. | Guarda en Obsidian, repite `git add .` y `git commit`. |
> | No encuentro el botón "Use this template". | El repo no está marcado como plantilla o no has iniciado sesión. | Inicia sesión en GitHub; si sigue sin salir, avisa al profesor. |
> | Clone lento o se corta. | Conexión del aula inestable. | Reintenta `git clone`; si la carpeta quedó a medias, bórrala antes de reintentar. |

> [!help] Preguntas Críticas (Autoevaluación del alumno)
> 1. ¿Qué hace "Use this template"? ¿Trabajas sobre el repo del profesor o sobre una copia tuya?
> 2. ¿Cuántas veces se clona un repositorio: una vez o cada día? ¿Qué usas los demás días?
> 3. ¿Por qué al clonar no hace falta `git init` ni `git remote add`?
> 4. Explica la diferencia entre `git clone`, `git push` y `git pull`.
> 5. 🔬 **Reto:** edita `MIS_DATOS.md` añadiendo tu correo, y vuelve a hacer `status → add → commit → push`. Observa que esta vez Git dice "modified" en lugar de "untracked". ¿Por qué?

---

### ✅ Checklist Final de la Fase 0.4

- [ ] Copia de la plantilla creada con "Use this template" (`boochan-1` en tu cuenta).
- [ ] Repo clonado dentro de `Practicas/boochan-1/`.
- [ ] La práctica se ve en Obsidian sin cambiar de bóveda.
- [ ] `MIS_DATOS.md` creado y detectado por `git status`.
- [ ] Cambio subido con `add` → `commit` → `push`; visible en GitHub.
- [ ] Vídeo de OBS del ciclo completo.

> **Siguiente paso:** Fase 0.5 — Montar el mismo entorno **en casa** y aprender el ciclo diario `pull` → trabajar → `push`, evitando el conflicto con OneDrive.
