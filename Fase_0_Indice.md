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
- Todo **grabado con OBS** y **subido a YouTube** (playlist `B0_Prerrequisitos`), con **una entrega por fase**, cada una en su sitio (centro o casa).

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
> - **Una sola entrega por fase**, en su sitio: 🏫 **centro** (0.1, 0.2.1, 0.2.2, 0.3, 0.4, 0.6) · 🏠 **casa** (0.5.1, 0.5.2). En prerequisitos no hay doble entrega: el "en casa" de las 0.1–0.4 **es** la Fase 0.5.1.

> [!tip] Otros convenios
> - **Entrada del día:** un fichero por día, nombre `AAAA-MM-DD_titulo-corto.md`, con estructura fija.
> - **Ciclo diario:** `git pull` al empezar → trabajar → `git add` / `commit` / `push` al terminar.

---

### Estructura de trabajo del alumno (la bóveda)

```
Boveda_SOR/                      ← se abre en Obsidian. NUNCA se hace git init aquí.
├── 00_Apuntes/
│   ├── Trimestre_1/             ← REPO propio (apuntes-sor-t1) → GitHub → enlace al profe
│   │   └── Bloque_1_Introduccion/
│   │       └── 2026-09-15_introduccion-al-modulo.md   ← una entrada por día
│   ├── Trimestre_2/             ← REPO propio (apuntes-sor-t2)
│   └── Trimestre_3/             ← REPO propio (apuntes-sor-t3)
└── Practicas/
    └── boochan-1/               ← tu copia de la plantilla = REPO propio
```

> [!note] La regla de oro del diseño
> La carpeta contenedor `Boveda_SOR` **no** se versiona (nada de `git init` en la raíz). Cada carpeta de dentro (cada trimestre, cada práctica) es **su propio repositorio independiente**. Así no hay "git dentro de git" y cada cosa sincroniza por su lado. El puente entre casa y centro es **Git + GitHub, nunca OneDrive**.

---

### Las sub-fases (en orden)

Cada sub-fase = **una práctica grabada** que se sube a YouTube. Las fases largas se **parten en dos** para que ningún vídeo se vaya de ~5 minutos.

| Sub-fase | Título | Qué consigue el alumno |
| :--- | :--- | :--- |
| **0.1** | [[Fase_0.1_Metodologia_y_Estructura]] | Método + bóveda + estructura + **canal de YouTube** con la playlist `B0_Prerrequisitos`. |
| **0.2** | [[Fase_0.2_GitHub_Git_y_SSH]] | *(índice)* Conexión con GitHub, en 2 partes ↓ |
| ↳ **0.2.1** | [[Fase_0.2.1_Cuenta_GitHub_y_Git]] | Crea la cuenta de GitHub y configura Git. |
| ↳ **0.2.2** | [[Fase_0.2.2_Autenticacion_SSH]] | Clave SSH (y token HTTPS) + verificación. |
| **0.3** | [[Fase_0.3_Repo_Apuntes_y_Primera_Entrada]] | Repo del Trimestre 1 + primera entrada del día (formato obligatorio). |
| **0.4** | [[Fase_0.4_Clonar_Practica_Boochan]] | Clona su copia de `boochan-1` y domina `status → commit → push`. |
| **0.5** | [[Fase_0.5_Casa_y_Centro_Sincronizacion]] | *(índice)* Casa ↔ centro, en 2 partes ↓ |
| ↳ **0.5.1** | [[Fase_0.5.1_Montar_Entorno_Casa]] | Monta el entorno en casa y clona sus repos. |
| ↳ **0.5.2** | [[Fase_0.5.2_Sincronizar_Casa_Centro]] | Ciclo `pull → push`; regla anti-OneDrive. |
| **0.6** | [[Fase_0.6_Verificacion_y_Simulacion_Final]] | Simulación completa grabada; verificación global. |

---

