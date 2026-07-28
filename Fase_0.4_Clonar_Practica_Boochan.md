## 📦 Fase 0.4: Tu Copia de la Práctica Boochan y el Ciclo de Trabajo con Git

### Descargar la práctica, hacerla tuya y subir cambios

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~1,5 horas · **Requisitos:** Fases 0.1, 0.2.1 y 0.2.2 completas.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin.
> 1. **Prepárate primero (sin grabar):** comprueba lo necesario y **léete el procedimiento entero**.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a explicar la Fase 0.4 — Clonar mi copia de la práctica Boochan."* Y **muestra tu perfil de GitHub** (o tu Teams/correo). Di qué vas a hacer.
> 3. **Graba TODO**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `Fase 0.4 — Clonar la práctica Boochan` y súbelo a tu playlist **`B0_Prerrequisitos`** (No listado).
> 6. **~5 min. Una sola entrega:** esta práctica se hace en **🏫 el centro**.

---

### 🎯 Objetivos de la fase

- [ ] Explicar qué es una **plantilla** de repositorio y qué hace "Use this template".
- [ ] Crear **tu propia copia** de `boochan-1` y **clonarla** dentro de `01_Practicas/`.
- [ ] Hacer un cambio y subirlo con `git status` → `add` → `commit` → `push`.

---

### 📚 Fundamento Teórico

> [!info] 1. Plantilla y "Use this template"
> Una **plantilla** es un repositorio pensado para sacar copias. Al pulsar **"Use this template"**, GitHub crea en **tu** cuenta un repositorio **nuevo e independiente** con el mismo contenido pero **historial propio**. No es un enlace a la plantilla del profesor: es **tuyo**.

> [!abstract] 2. Clonar vs. Push
> - **`git clone`** (GitHub → tu ordenador): **una sola vez**, para bajar el repo.
> - **`git push`** (tu ordenador → GitHub): **cada vez** que subes cambios.
> Regla: **clonas una vez**, luego trabajas con push/pull. Y al clonar, el remoto ya viene configurado (no hace falta `git init`).

---

### 🛠️ Procedimiento Práctico

> [!example] Paso 0: Prepárate (todavía SIN grabar)
> Comprueba tu bóveda y tu autenticación. **Léete el procedimiento** (tiene **5 pasos** grabados). Ten **OBS** listo y tu **perfil de GitHub** en una pestaña.

> [!example] Paso 1: Arranca la grabación y preséntate
> Inicia la grabación en **OBS**, preséntate, **enseña tu perfil de GitHub** 2-3 segundos y di qué vas a hacer.

> [!example] Paso 2: Crea tu copia de la plantilla en GitHub
> En `github.com/sor-iesjj/boochan-v1`, pulsa **`Use this template` → Create a new repository**: **Owner** tu usuario, **name** `boochan-1`, **Visibility** la que indique el profesor. **Create repository**. En **`Code`**, copia tu dirección (**SSH** `git@github.com:TU-USUARIO/boochan-1.git` o **HTTPS**).

> [!example] Paso 3: Clona tu copia dentro de `01_Practicas/`
> Igual que en la Fase 0.3: **clic derecho sobre la carpeta `01_Practicas` de tu bóveda** → `Abrir Git Bash aquí` (Windows) / `Abrir en un terminal` (Linux). Comprueba dónde estás **antes de clonar**:
> ```bash
> pwd          # tiene que terminar en .../Boveda_SOR/01_Practicas
> git clone git@github.com:TU-USUARIO/boochan-1.git
> cd boochan-1
> ls
> ```
> Debes ver los ficheros de la práctica (`Manual_BoochanV1.md`, `Fases/`…).
> > [!danger] ⚠️ Comprueba con `pwd` que clonas dentro de `.../Boveda_SOR/01_Practicas`.

> [!example] Paso 4: Ábrela en Obsidian y haz un cambio
> Como `01_Practicas/boochan-1/` está **dentro** de tu bóveda, Obsidian ya la ve (apuntes y práctica en una sola ventana). Crea ahí una nota `MIS_DATOS.md`:
> ```markdown
> # Mis datos
> - Alumno: Juan García
> - Grupo: 2º SMR
> ```
> Guarda y, en la terminal (dentro de `boochan-1`), mira el cambio:
> ```bash
> git status
> ```
> `MIS_DATOS.md` aparece como **untracked**.

> [!example] Paso 5: Sube el cambio (ciclo completo)
> ```bash
> git add .
> git commit -m "Anadir mis datos de alumno"
> git push
> ```
> Recarga tu repo `boochan-1` en GitHub: debe aparecer `MIS_DATOS.md`.

> [!example] Paso 6: Cierra el vídeo, nómbralo y súbelo
> Detén la grabación, nombra el vídeo `Fase 0.4 — Clonar la práctica Boochan`, súbelo a la playlist `B0_Prerrequisitos` (No listado) y añade **timestamps** (`00:00 Presentación` + uno por paso).

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | `git clone` da `Permission denied (publickey)`. | Usas SSH pero la clave no está lista. | Repasa la 0.2.2, **o** clona por HTTPS con tu token. |
> | La carpeta `boochan-1` no aparece en Obsidian. | La clonaste fuera de la bóveda. | Comprueba con `pwd`; clónala dentro de `01_Practicas/`. |
> | `git push` dice `nothing to commit`. | No hiciste `git add` o no guardaste. | Guarda en Obsidian, `git add .` y `git commit`. |
> | No veo "Use this template". | El repo no está como plantilla o no has iniciado sesión. | Inicia sesión; si sigue, avisa al profesor. |

> [!help] Preguntas Críticas
> 1. ¿Qué hace "Use this template"? ¿Trabajas sobre el repo del profesor o sobre tu copia?
> 2. ¿Cuántas veces se clona un repositorio? ¿Qué usas los demás días?
> 3. ¿Por qué al clonar no hace falta `git init`?

---

### ✅ Checklist Final de la Fase 0.4

- [ ] Copia de la plantilla creada (`boochan-1` en tu cuenta).
- [ ] Repo clonado dentro de `01_Practicas/boochan-1/` (se ve en Obsidian).
- [ ] `MIS_DATOS.md` creado y subido con `add` → `commit` → `push`; visible en GitHub.
- [ ] Vídeo `Fase 0.4 — Clonar la práctica Boochan` subido a la playlist, con timestamps.
- [ ] Una sola entrega, hecha **🏫 en el centro**.

> **Siguiente paso:** Fase 0.5 — Montar el mismo entorno **en casa** y sincronizar centro ↔ casa (va en 2 partes).
