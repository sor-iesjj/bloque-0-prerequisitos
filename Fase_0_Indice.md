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
- Todo **grabado con OBS**, con **doble entrega**: una en el centro y otra en casa.

> [!important] Herramientas necesarias (las instala Consellería en el centro)
> **Obsidian**, **Git** y **OBS Studio**, en Windows y en Linux. El alumno **no tiene permisos** para instalarlas en el centro; en **casa** sí las instala él (Fase 0.5).

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

| Sub-fase | Título | Qué consigue el alumno |
| :--- | :--- | :--- |
| **0.1** | [[Fase_0.1_Metodologia_y_Estructura]] | Entiende el método; crea la bóveda y la estructura de carpetas. |
| **0.2** | [[Fase_0.2_GitHub_Git_y_SSH]] | Cuenta de GitHub, Git configurado, clave SSH (sin contraseñas). |
| **0.3** | [[Fase_0.3_Repo_Apuntes_y_Primera_Entrada]] | Repo del Trimestre 1 + primera entrada del día (formato obligatorio). |
| **0.4** | [[Fase_0.4_Clonar_Practica_Boochan]] | Clona su copia de `boochan-1` y domina `status → commit → push`. |
| **0.5** | [[Fase_0.5_Casa_y_Centro_Sincronizacion]] | Replica el entorno en casa; ciclo `pull → push`; regla anti-OneDrive. |
| **0.6** | [[Fase_0.6_Verificacion_y_Simulacion_Final]] | Simulación completa grabada; verificación global; entrega de enlaces. |

---

### Qué va después de la Fase 0

1. **Prueba diagnóstica de redes** ([[Prueba_Diagnostica_Inicial_SOR]]): el profesor mide qué base de 1º trae cada alumno (IP, máscara, ping, instalar una VM…) para reforzar lo necesario. Ver también [[Prerrequisitos_1SMR_para_Boochan]].
2. **Proyecto Boochan** (Fase 1 en adelante): la práctica real, que el alumno clona en `Practicas/` y documenta en sus apuntes.

> [!tip] Convenios que se repiten en todas las sub-fases
> - **Entrada del día:** un fichero por día, nombre `AAAA-MM-DD_titulo-corto.md`, con estructura fija.
> - **Ciclo diario:** `git pull` al empezar → trabajar → `git add` / `commit` / `push` al terminar.
> - **Todo se graba** con OBS y se entrega **dos veces** (centro + casa).
