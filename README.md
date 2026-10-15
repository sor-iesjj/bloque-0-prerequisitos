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
| [Fase 0.3.b — Qué no se sube: el `.gitignore`](Fase_0.3.b_Que_No_Se_Sube_Gitignore.md) | Qué queda fuera del repositorio y por qué una clave subida no se borra |
| [Fase 0.4.a — Bajar el material del curso](Fase_0.4.a_Bajar_El_Material_Del_Curso.md) | Sus **tres copias** (`Use this template`) clonadas por **tres vías** (SSH · HTTPS · ZIP); `status → commit → push` |
| [Fase 0.4.b — Tres retos de recuperación](Fase_0.4.b_Tres_Retos_De_Recuperacion.md) | Romper lo recién bajado y recuperarlo: `git restore`, reclonar, y lo único que **no vuelve** |
| [Fase 0.5 — Casa y centro (índice)](Fase_0.5_Casa_y_Centro_Sincronizacion.md) | Casa ↔ centro, en 2 partes ↓ |
| &nbsp;&nbsp;↳ [Fase 0.5.1 — Montar el entorno en casa](Fase_0.5.1_Montar_Entorno_Casa.md) | Instala en casa y clona sus repos |
| &nbsp;&nbsp;↳ [Fase 0.5.2 — Sincronizar casa ↔ centro](Fase_0.5.2_Sincronizar_Casa_Centro.md) | Ciclo `pull → push`; regla anti-OneDrive |
| [Fase 0.6 — Verificación y simulación](Fase_0.6_Verificacion_y_Simulacion_Final.md) | Simulación completa grabada + verificación global |
| [Fase 0.7 — Cuando todo se rompe (índice)](Fase_0.7_Cuando_Todo_Se_Rompe.md) | Dos catástrofes provocadas, en 2 partes ↓ |
| &nbsp;&nbsp;↳ [Fase 0.7.1 — He perdido lo que escribí](Fase_0.7.1_Catastrofe_Local_Recuperar_Con_Git.md) | Pierde el contenido y lo recupera **solo con Git**, sin Internet |
| &nbsp;&nbsp;↳ [Fase 0.7.2 — Se ha llevado el disco por delante](Fase_0.7.2_Catastrofe_Total_Recuperar_Desde_GitHub.md) | Borra la bóveda entera y la reconstruye **clonando** desde GitHub |
| [Fase 0.8 — Prácticas (índice)](Fase_0.8_Practicas.md) | Aplicar Obsidian, Git y GitHub a proyectos nuevos con guías separadas para centro y casa |
| &nbsp;&nbsp;↳ [Práctica 01 — Página web HTML](Fase_0.8_Practicas/Practica_01_Web_HTML/00_Indice_Practica_01_Web_HTML.md) | Dos bóvedas y dos repositorios independientes; abre **solo** la guía del lugar donde trabajas |

> 📹 Las fases **0.1–0.7** se graban con OBS y van a la playlist `B0_Prerrequisitos` (No listado, con timestamps). La **Fase 0.8** indica sus grabaciones y su playlist propia dentro de cada práctica. En ambos casos rige la regla: **donde hay vídeo, hay bitácora con el enlace de ese vídeo**. En Teams se entregan los enlaces de repositorios y playlist que indique la tarea.

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
    ├── B0_Prerrequisitos/        ← tu copia de los prerrequisitos = repo propio
    ├── B1_Entorno/               ← tu copia del Bloque 1 = repo propio
    └── B2_Ubuntu_Local/          ← tu copia del Bloque 2 = repo propio
```

Regla de oro: la bóveda **no** se versiona entera; cada trimestre de apuntes y cada práctica son **repositorios independientes**. El puente entre casa y centro es **Git + GitHub**, nunca OneDrive.

> [!note] Fase 0.8: proyectos de práctica aparte
> Las bóvedas nuevas de la Práctica 01 se crean **fuera de `Boveda_SOR`**. Cada guía de `Cole/` y `Casa/` muestra su árbol propio y la carpeta exacta donde se inicializa Git.

---

*Material docente. Cualquier uso debe reconocer la autoría de Pedro Navarro Miralles (IES Jorge Juan) según la licencia [CC BY-NC-SA 4.0](LICENSE).*
