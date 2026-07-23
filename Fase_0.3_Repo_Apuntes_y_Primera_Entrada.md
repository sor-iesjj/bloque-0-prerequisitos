## 📓 Fase 0.3: Repositorio de Apuntes del Trimestre y Primera Entrada

### Tus apuntes, versionados y en la nube — y cómo se escribe una entrada

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~1,5 - 2 horas · **Requisitos:** Fases 0.1, 0.2.1 y 0.2.2 completas (bóveda + cuenta GitHub + autenticación).

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin.
> 1. **Prepárate primero (sin grabar):** comprueba lo necesario y **léete el procedimiento entero**.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a explicar la Fase 0.3 — Repositorio de apuntes y primera entrada."* Y **muestra tu perfil de GitHub** (o tu Teams/correo). Di qué vas a hacer.
> 3. **Graba TODO**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `Fase 0.3 — Repo de apuntes y primera entrada` y súbelo a tu playlist **`00_Prerrequisitos`** (No listado).
> 6. **~5 min. Una sola entrega:** esta práctica se hace en **🏫 el centro**.

---

### 🎯 Objetivos de la fase

- [ ] Explicar por qué usamos **un repositorio por trimestre**.
- [ ] Crear un repositorio en GitHub y conectarlo con tu carpeta `Trimestre_1`.
- [ ] Escribir la **entrada del día** con el **nombre** y la **estructura** obligatorios.
- [ ] Hacer el ciclo `git add` → `commit` → `push` y **darme el enlace**.

---

### 🎯 ¿Dónde Estamos?

> [!info] El Punto de Partida
> Tienes `00_Apuntes/Trimestre_1/` en tu bóveda, pero es una carpeta normal: Git no la controla y GitHub no la conoce. Aquí le damos "vida": la convertimos en repositorio y la subimos.

> [!warning] El Problema
> No puedo esperar a final de trimestre para ver si tomas apuntes. Necesito poder decir *"enseñadme lo que lleváis"* **cualquier día**. Por eso tu repo del trimestre debe estar **siempre al día** y yo tener **tu enlace**.

---

### 📚 Fundamento Teórico

> [!info] ¿Por qué un repositorio por trimestre?
> Al cerrar cada trimestre, ese repo queda "congelado" y **te lo califico** limpio; es un enlace claro que me pasas una vez; y si algo se lía en uno, no afecta a los demás. Tendrás **tres**: `apuntes-sor-t1`, `apuntes-sor-t2`, `apuntes-sor-t3`. Montamos el primero.

> [!important] 1. La entrada del día: NOMBRE obligatorio
> Cada día de clase, **un fichero nuevo** en el bloque que toque, con este nombre exacto:
> ```
> AAAA-MM-DD_titulo-corto.md
> ```
> - `AAAA-MM-DD` con guiones (ej. `2026-09-15`) · `_` · `titulo-corto` en minúsculas con guiones, sin tildes ni espacios.
>
> **Correcto:** `2026-09-15_introduccion-al-modulo.md` · **Incorrecto:** `apuntes dia 1.md` ❌, `15-9.md` ❌.

> [!important] 2. La entrada del día: ESTRUCTURA obligatoria
> ```markdown
> # 2026-09-15 — Introducción al módulo
>
> **Fecha:** 2026-09-15
> **Bloque:** Bloque 1 — Introducción
>
> ## Qué hemos visto hoy
> - (con tus palabras)
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
> > [!tip] 💡 Escribe con tus palabras. El apartado "Dudas" me dice en qué reforzar.

### 📖 Diccionario de Conceptos Clave

> [!quote] Terminología
> - **`git init`:** convierte una carpeta en repositorio. · **Remoto (`origin`):** la dirección en GitHub.
> - **`git add` / `commit` / `push`:** preparar / guardar / subir. · **Entrada:** el fichero de apuntes de un día.

---

### 🛠️ Procedimiento Práctico

> [!example] Paso 0: Prepárate (todavía SIN grabar)
> Comprueba que tienes la bóveda y la autenticación de la 0.2. **Léete el procedimiento** (tiene **6 pasos** grabados). Ten **OBS** listo y tu **perfil de GitHub** en una pestaña.

> [!example] Paso 1: Arranca la grabación y preséntate
> Inicia la grabación en **OBS**, preséntate, **enseña tu perfil de GitHub** 2-3 segundos y di qué vas a hacer.

> [!example] Paso 2: Escribe tu primera entrada en Obsidian
> En `00_Apuntes/Trimestre_1/Bloque_1_Introduccion/`, clic derecho → **New note**, nómbrala `2026-09-15_introduccion-al-modulo` y pega la **plantilla** (apartado 2), rellenándola con lo de hoy. Guarda.

> [!example] Paso 3: Convierte `Trimestre_1` en repositorio
> ```bash
> cd ~/SOR/Boveda_SOR/00_Apuntes/Trimestre_1
> git init
> git branch -M main
> git status
> ```
> > [!danger] ⚠️ `git init` **solo** dentro de `Trimestre_1`. Comprueba con `pwd` antes. Nunca en `Boveda_SOR`.

> [!example] Paso 4: Crea el repositorio en GitHub
> En `github.com` → **`+` → New repository**: **name** `apuntes-sor-t1`, **Private**, **SIN** README/gitignore/license. En el botón **`Code`** copia tu dirección (**SSH** `git@github.com:...` o **HTTPS** `https://github.com/...`).

> [!example] Paso 5: Conecta y sube
> Dentro de `Trimestre_1`:
> ```bash
> git remote add origin git@github.com:TU-USUARIO/apuntes-sor-t1.git
> git add .
> git commit -m "Primera entrada: introduccion al modulo"
> git push -u origin main
> ```
> Recarga GitHub: debe verse `Bloque_1_Introduccion/` con tu entrada.

> [!example] Paso 6: Cierra el vídeo, nómbralo, súbelo y pásame el enlace
> 1. **Detén la grabación**, nombra el vídeo `Fase 0.3 — Repo de apuntes y primera entrada` y súbelo a la playlist `00_Prerrequisitos` con **timestamps** (`00:00 Presentación`, y uno por paso).
> 2. **Pásame por Teams el enlace** de tu repo (`https://github.com/TU-USUARIO/apuntes-sor-t1`). Al ser privado, te diré mi usuario para que me añadas en `Settings → Collaborators`.

> [!note] 📌 A partir de ahora, cada día de clase
> Creas la **entrada del día** (nombre + estructura) y, dentro de `Trimestre_1`: `git add .` → `git commit -m "Apuntes del ..."` → `git push`. Así el repo está siempre al día.

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | `fatal: not a git repository`. | No estás en `Trimestre_1` o no hiciste `git init`. | `pwd` para comprobar; haz `git init` ahí. |
> | `remote origin already exists`. | Ejecutaste `git remote add` dos veces. | `git remote set-url origin git@github.com:...`. |
> | `Updates were rejected`. | Creaste el repo con README (no vacío). | Recréalo vacío, o `git pull origin main --rebase` y `push`. |
> | Hice `git init` en `Boveda_SOR`. | Carpeta equivocada. | Borra ese `.git` (`rm -rf .git` en `Boveda_SOR`) y hazlo en `Trimestre_1`. |

> [!help] Preguntas Críticas
> 1. ¿Por qué un repositorio por trimestre?
> 2. Escribe el nombre de una entrada del 3 de octubre de 2026 titulada "servidor DNS".
> 3. ¿En qué carpeta EXACTA se hace `git init`?

---

### ✅ Checklist Final de la Fase 0.3

- [ ] Primera entrada en `Bloque_1_Introduccion/` con nombre y estructura correctos.
- [ ] `Trimestre_1` convertido en repositorio; repo `apuntes-sor-t1` en GitHub.
- [ ] `commit` + `push` hechos; la entrada se ve en GitHub.
- [ ] Enlace enviado (y acceso concedido si es privado).
- [ ] Vídeo `Fase 0.3 — Repo de apuntes y primera entrada` subido a la playlist, con timestamps.
- [ ] Una sola entrega, hecha **🏫 en el centro**.

> **Siguiente paso:** Fase 0.4 — Clonar tu copia de la práctica **`boochan-1`** y dominar el ciclo `status → commit → push`.
