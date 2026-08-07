# Fase 0 — Puesta a Punto del Entorno de Trabajo (SOR · 2.º SMR)

> **Autor y propietario:** © 2026 **Pedro Navarro Miralles** — IES Jorge Juan (Alicante)
> **Módulo:** Sistemas Operativos en Red (SOR) · 2.º Curso SMR
> **Licencia:** [CC BY-NC-SA 4.0](LICENSE) — atribución obligatoria al autor, uso no comercial.

Bloque de **prerrequisitos** que se hace **antes** del proyecto Boochan. Monta el **método de trabajo** del curso: tomar apuntes en **Obsidian**, versionarlos con **Git** y enviarlos por **GitHub** para que el profesor los corrija.

⏱️ Ocupa unas **2-3 semanas** de clase.

---

## 🧭 Cómo usar este material

Sigue las sub-fases **en orden**. Cada una es una práctica guiada, muy detallada, con teoría, pasos, verificaciones y preguntas de comprensión. Todas las prácticas se **graban con OBS** y se **suben a YouTube** (playlist `B0_Prerrequisitos`).

| Sub-fase | Qué consigue el alumno |
| :--- | :--- |
| [Índice de la Fase 0](Fase_0_Indice.md) | Visión general, estructura de la bóveda y regla de oro |
| [Fase 0.1 — Metodología y Estructura](Fase_0.1_Metodologia_y_Estructura.md) | Entiende el método; crea la bóveda y la estructura de carpetas |
| [Fase 0.2 — GitHub, Git y autenticación (índice)](Fase_0.2_GitHub_Git_y_SSH.md) | Conexión con GitHub, en 2 partes ↓ |
| &nbsp;&nbsp;↳ [Fase 0.2.1 — Cuenta de GitHub y Git](Fase_0.2.1_Cuenta_GitHub_y_Git.md) | Crea la cuenta de GitHub y configura Git |
| &nbsp;&nbsp;↳ [Fase 0.2.2 — Autenticación SSH](Fase_0.2.2_Autenticacion_SSH.md) | Clave SSH (y token HTTPS) + verificación |
| [Fase 0.3 — Repo de apuntes y primera entrada](Fase_0.3_Repo_Apuntes_y_Primera_Entrada.md) | Repo del Trimestre 1 + entrada de la fase |
| [Fase 0.3b — Qué no se sube: el `.gitignore`](Fase_0.3b_Que_No_Se_Sube_Gitignore.md) | Qué queda fuera del repositorio y por qué una clave subida no se borra |
| [Fase 0.4 — Bajar el material del curso](Fase_0.4_Clonar_Practica_Boochan.md) | Sus copias del Bloque 1 y de Boochan (`Use this template` + clonar); `status → commit → push` y **3 retos** de recuperación |
| [Fase 0.5 — Casa y centro (índice)](Fase_0.5_Casa_y_Centro_Sincronizacion.md) | Casa ↔ centro, en 2 partes ↓ |
| &nbsp;&nbsp;↳ [Fase 0.5.1 — Montar el entorno en casa](Fase_0.5.1_Montar_Entorno_Casa.md) | Instala en casa y clona sus repos |
| &nbsp;&nbsp;↳ [Fase 0.5.2 — Sincronizar casa ↔ centro](Fase_0.5.2_Sincronizar_Casa_Centro.md) | Ciclo `pull → push`; regla anti-OneDrive |
| [Fase 0.6 — Verificación y simulación](Fase_0.6_Verificacion_y_Simulacion_Final.md) | Simulación completa grabada + verificación global |
| [Fase 0.7 — Cuando todo se rompe (índice)](Fase_0.7_Cuando_Todo_Se_Rompe.md) | Dos catástrofes provocadas, en 2 partes ↓ |
| &nbsp;&nbsp;↳ [Fase 0.7.1 — He perdido lo que escribí](Fase_0.7.1_Catastrofe_Local_Recuperar_Con_Git.md) | Pierde el contenido y lo recupera **solo con Git**, sin Internet |
| &nbsp;&nbsp;↳ [Fase 0.7.2 — Se ha llevado el disco por delante](Fase_0.7.2_Catastrofe_Total_Recuperar_Desde_GitHub.md) | Borra la bóveda entera y la reconstruye **clonando** desde GitHub |

> 📹 Cada fase se **graba con OBS** (de principio a fin, con presentación e identidad) y se **sube a YouTube** (playlist `B0_Prerrequisitos`, No listado, con timestamps). Regla central: **donde hay vídeo, hay entrada** — cada fase tiene su nota de apuntes, con el **enlace de ese vídeo** y las **respuestas** a sus preguntas dentro. En la **tarea de Teams** se entregan solo los enlaces de **repositorio** y de la **playlist**; las entregas se **agrupan** por varias fases, no van una a una.

---

## 📌 Antes de la Fase 1 (Boochan)

- **[Prerrequisitos de 1.º SMR](Prerrequisitos_1SMR_para_Boochan.md)** — qué conocimientos previos hacen falta para el proyecto Boochan.
- **[Prueba diagnóstica inicial](Prueba_Diagnostica_Inicial_SOR.md)** — termómetro del primer día (no cuenta para nota).

---

## 🗺️ La estructura de trabajo del alumno (resumen)

```
Boveda_SOR/                 ← se abre en Obsidian. NUNCA se hace git init aquí.
├── 00_Apuntes/
│   ├── Trimestre_1/        ← repo propio → GitHub → enlace al profesor
│   ├── Trimestre_2/
│   └── Trimestre_3/
└── 01_Practicas/
    └── bloque-2-ubuntu-local/          ← tu copia de la plantilla = repo propio
```

Regla de oro: la bóveda **no** se versiona entera; cada trimestre de apuntes y cada práctica son **repositorios independientes**. El puente entre casa y centro es **Git + GitHub**, nunca OneDrive.

---

*Material docente. Cualquier uso debe reconocer la autoría de Pedro Navarro Miralles (IES Jorge Juan) según la licencia [CC BY-NC-SA 4.0](LICENSE).*
