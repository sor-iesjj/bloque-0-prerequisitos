## 🧰 Fase 0 — Puesta a Punto del Entorno de Trabajo (Índice)

> **[Módulo: SOR — Sistemas Operativos en Red · 2.º SMR]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> Bloque de **prerrequisitos** que se hace **antes** del proyecto Boochan. Monta el método de trabajo del curso: tomar apuntes en Obsidian, versionarlos con Git y enviarlos por GitHub para que el profesor los corrija. Se calcula que ocupa **2-3 semanas** de clase.

---

### ¿Por qué existe esta fase?

Un técnico no memoriza: **documenta**. Aquí se establece **cómo** trabajaremos todo el curso:

- **Apuntes** en Obsidian (una entrada por día), separados de las **prácticas** (Boochan).
- Todo **versionado con Git** y subido a **GitHub** (un repo de apuntes por trimestre).
- Todo **grabado con OBS** y **subido a YouTube** (playlist `B0_Prerrequisitos`), y **entregado en dos tareas de Teams** agrupadas, no fase a fase.

> [!important] Herramientas y cuentas necesarias
> - **Obsidian**, **Git** y **OBS Studio** — los instala **Consellería** en el centro (el alumno no tiene permisos); en **casa** los instala él (Fase 0.5.1).
> - **Cuenta de Gmail/YouTube** (para subir los vídeos) — la crea el alumno en el **Paso previo de la Fase 0.1**, con un nombre parecido a su correo `@alu.edu.gva.es`.

> [!important] 📹 Método de grabación (igual en TODAS las sub-fases)
> - Se **graba TODO el procedimiento con OBS, desde el principio** (no un repaso al final).
> - **Preparación primero (sin grabar):** comprobar lo necesario + leerse el procedimiento entero.
> - **Al empezar a grabar:** el alumno **se presenta**, **muestra en pantalla algo que demuestre que es él** (Teams/correo `@alu.edu.gva.es`; desde la 0.2.2, su perfil de GitHub) y dice qué va a hacer.
> - **Timestamps SIEMPRE** en la descripción: `00:00 Presentación` + uno por cada paso.
> - **Nombre del vídeo** = nombre de la fase. **Se sube a YouTube** (playlist `B0_Prerrequisitos`, como "No listado").
> - **Duración ~5 min.** Si una fase se pasa con creces, se **parte en dos** (como 0.2 y 0.5).
> - **Cada fase se graba una vez**, en su sitio: 🏫 **centro** (0.1, 0.2.1, 0.2.2, 0.3, 0.4, 0.6) · 🏠 **casa** (0.5.1, 0.5.2). En prerequisitos no se graba dos veces lo mismo: el "en casa" de las 0.1–0.4 **es** la Fase 0.5.1.
> - **Al subir cada vídeo, el alumno guarda su enlace.** Lo necesitará para la entrega.

> [!important] 📤 Cómo se ENTREGA (playlist ≠ entrega)
> Dos cosas distintas que el alumnado confunde el primer día:
>
> | | Qué es | Quién lo mueve |
> | :--- | :--- | :--- |
> | **Playlist `B0_Prerrequisitos`** | **Organización.** TODOS los vídeos del bloque van dentro, siempre. | El alumno, cada vez que graba |
> | **Tarea de Teams** | **La entrega evaluable.** Con notificación y **fecha límite de varios días**. | El profesor la abre; el alumno pega enlaces y pulsa `Entregar` |
>
> **No hay una entrega por fase.** Hay **dos entregas agrupadas**, cada una cerrada por un artefacto verificable:
>
> | Entrega | Fases | Qué se pega en la tarea |
> | :--- | :--- | :--- |
> | **Entrega 1 — Mi entorno de trabajo** | 0.1 · 0.2.1 · 0.2.2 · 0.3 | Los **4 enlaces de vídeo** + enlace del repo `apuntes-sor-t1` + enlace de la playlist (solo esta vez) |
> | **Entrega 2 — Práctica y sincronización** | 0.4 · 0.5.1 · 0.5.2 · 0.6 | Los **4 enlaces de vídeo** + enlace del repo `boochan-1` |
>
> **Se piden los vídeos uno a uno, no la playlist.** Una playlist puede estar vacía el día del plazo y llenarse el martes siguiente; el enlace de un vídeo concreto demuestra que existía. La playlist se pide igualmente **una vez**, para tenerla localizada.

> [!tip] Otros convenios
> - **Entrada del día:** un fichero por día, nombre `MMDDAA_titulo-corto.md` (mes, día, año), con estructura fija. Se define en la **Fase 0.1**.
> - **Ciclo diario:** `git pull` al empezar → trabajar → `git add` / `commit` / `push` al terminar.

---

### Estructura de trabajo del alumno (la bóveda)

```
Boveda_SOR/                      ← se abre en Obsidian. NUNCA se hace git init aquí.
├── 00_Apuntes/
│   ├── Trimestre_1/             ← REPO propio (apuntes-sor-t1) → GitHub → enlace al profe
│   │   └── B0_Prerrequisitos/
│   │       └── 091526_metodologia-y-estructura.md   ← una entrada por día (MMDDAA)
│   ├── Trimestre_2/             ← REPO propio (apuntes-sor-t2)
│   └── Trimestre_3/             ← REPO propio (apuntes-sor-t3)
└── 01_Practicas/
    └── boochan-1/               ← tu copia de la plantilla = REPO propio
```
> `Boveda_SOR/` vive **dentro de la carpeta de usuario** del alumno: `~/Documents/SOR/`, `~/Documentos/SOR/` o `~/SOR/` según el equipo (se decide en la Fase 0.1). **Nunca en OneDrive.**

> [!note] La regla de oro del diseño
> La carpeta contenedor `Boveda_SOR` **no** se versiona (nada de `git init` en la raíz). Cada carpeta de dentro (cada trimestre, cada práctica) es **su propio repositorio independiente**. Así no hay "git dentro de git" y cada cosa sincroniza por su lado. El puente entre casa y centro es **Git + GitHub, nunca OneDrive**.

---

### Las sub-fases (en orden)

Cada sub-fase = **una práctica grabada** que se sube a YouTube. Las fases largas se **parten en dos** para que ningún vídeo se vaya de ~5 minutos.

| Sub-fase | Título | Qué consigue el alumno |
| :--- | :--- | :--- |
| **0.1** | [[Fase_0.1_Metodologia_y_Estructura]] | Método + bóveda + estructura + **canal de YouTube** con la playlist + **su primera entrada de apuntes** escrita. |
| **0.2** | [[Fase_0.2_GitHub_Git_y_SSH]] | *(índice)* Conexión con GitHub, en 2 partes ↓ |
| ↳ **0.2.1** | [[Fase_0.2.1_Cuenta_GitHub_y_Git]] | Crea la cuenta de GitHub y configura Git. |
| ↳ **0.2.2** | [[Fase_0.2.2_Autenticacion_SSH]] | Clave SSH (y token HTTPS) + verificación. |
| **0.3** | [[Fase_0.3_Repo_Apuntes_y_Primera_Entrada]] | Repo del Trimestre 1 + entrada del día + **ENTREGA 1** en Teams. |
| **0.4** | [[Fase_0.4_Clonar_Practica_Boochan]] | Clona su copia de `boochan-1` y domina `status → commit → push`. |
| **0.5** | [[Fase_0.5_Casa_y_Centro_Sincronizacion]] | *(índice)* Casa ↔ centro, en 2 partes ↓ |
| ↳ **0.5.1** | [[Fase_0.5.1_Montar_Entorno_Casa]] | Monta el entorno en casa y clona sus repos. |
| ↳ **0.5.2** | [[Fase_0.5.2_Sincronizar_Casa_Centro]] | Ciclo `pull → push`; regla anti-OneDrive. |
| **0.6** | [[Fase_0.6_Verificacion_y_Simulacion_Final]] | Simulación completa grabada; verificación global + **ENTREGA 2** en Teams. |

---

