# Fase 0 — Puesta a Punto del Entorno de Trabajo (SOR · 2.º SMR)

> **Autor y propietario:** © 2026 **Pedro Navarro Miralles** — IES Jorge Juan (Alicante)
> **Módulo:** Sistemas Operativos en Red (SOR) · 2.º Curso SMR
> **Licencia:** [CC BY-NC-SA 4.0](LICENSE) — atribución obligatoria al autor, uso no comercial.

Bloque de **prerrequisitos** que se hace **antes** del proyecto Boochan. Monta el **método de trabajo** del curso: tomar apuntes en **Obsidian**, versionarlos con **Git** y enviarlos por **GitHub** para que el profesor los corrija.

⏱️ Ocupa unas **2-3 semanas** de clase.

---

## 🧭 Cómo usar este material

Sigue las sub-fases **en orden**. Cada una es una práctica guiada, muy detallada, con teoría, pasos, verificaciones y preguntas de comprensión. Todas las prácticas se **graban con OBS** y se entregan **dos veces** (en el centro y en casa).

| Sub-fase | Qué consigue el alumno |
| :--- | :--- |
| [Índice de la Fase 0](Fase_0_Indice.md) | Visión general, estructura de la bóveda y regla de oro |
| [Fase 0.1 — Metodología y Estructura](Fase_0.1_Metodologia_y_Estructura.md) | Entiende el método; crea la bóveda y la estructura de carpetas |
| [Fase 0.2 — GitHub, Git y SSH](Fase_0.2_GitHub_Git_y_SSH.md) | Cuenta de GitHub, Git configurado, autenticación (SSH o token) |
| [Fase 0.3 — Repo de apuntes y primera entrada](Fase_0.3_Repo_Apuntes_y_Primera_Entrada.md) | Repo del Trimestre 1 + primera entrada del día |
| [Fase 0.4 — Clonar la práctica Boochan](Fase_0.4_Clonar_Practica_Boochan.md) | Clona su copia de una práctica y domina `status → commit → push` |
| [Fase 0.5 — Casa y centro](Fase_0.5_Casa_y_Centro_Sincronizacion.md) | Replica el entorno en casa; ciclo `pull → push`; regla anti-OneDrive |
| [Fase 0.6 — Verificación y simulación](Fase_0.6_Verificacion_y_Simulacion_Final.md) | Simulación completa grabada + verificación global |

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
└── Practicas/
    └── boochan-1/          ← tu copia de la plantilla = repo propio
```

Regla de oro: la bóveda **no** se versiona entera; cada trimestre de apuntes y cada práctica son **repositorios independientes**. El puente entre casa y centro es **Git + GitHub**, nunca OneDrive.

---

*Material docente. Cualquier uso debe reconocer la autoría de Pedro Navarro Miralles (IES Jorge Juan) según la licencia [CC BY-NC-SA 4.0](LICENSE).*
