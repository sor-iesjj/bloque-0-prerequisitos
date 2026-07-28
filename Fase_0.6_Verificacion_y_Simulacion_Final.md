## 🎬 Fase 0.6: Verificación Final y Simulación Completa

### Demostrar, de principio a fin y grabado, que todo tu entorno funciona

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~1 - 1,5 horas · **Requisitos:** Fases 0.1 a 0.5.2 completas.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta fase **es** un vídeo: una simulación completa grabada de principio a fin.
> 1. **Prepárate primero (sin grabar):** repasa mentalmente todo el flujo (apuntes y práctica) y **crea la entrada de apuntes de esta fase** en Obsidian (nombre `MMDDAA_fase-0.6-titulo.md`, estructura de la Fase 0.1). La vas rellenando **mientras** haces la práctica, no al final.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a hacer la simulación final de la Fase 0."* **Muestra tu perfil de GitHub**. Di qué vas a demostrar.
> 3. **Graba TODO el circuito**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `Fase 0.6 — Simulación final` y súbelo a tu playlist **`B0_Prerrequisitos`** (No listado).
> 6. **~5-7 min.** Se graba en **🏫 el centro** (o donde indique el profesor).
> 7. **La entrega va por la TAREA de Teams.** Cuando toque, abriré una tarea que cubrirá **esta fase y otras**; te llegará notificación.

---

### 🎯 Objetivos de la fase

- [ ] Recorrer el **flujo completo** sin ayuda: apuntes y práctica, de la bóveda a GitHub.
- [ ] Grabar la **simulación de principio a fin**, explicándola.
- [ ] Comprobar con la lista global que **no falta nada**.

---

### 📚 Fundamento

> [!info] Por qué se hace esta simulación
> Una cosa es que cada pieza funcione por separado y otra que sepas **encadenarlas tú solo**, el día que empiece una práctica de verdad. Esta fase se asegura de eso. Si algo falla, lo arreglamos **antes** de empezar Boochan.

> [!important] El circuito completo, de un vistazo
> ```
>   Obsidian (escribo)  →  git add  →  git commit  →  git push  →  GitHub (guardado)
>        ↑                                                              │
>        └──────────────────────  git pull  ←───────────────────────────┘
> ```

---

### 🛠️ Procedimiento Práctico (la simulación)

> [!example] Paso 0: Prepárate (sin grabar) y arranca OBS
> Repasa el flujo y **léete el procedimiento entero** (tiene **5 pasos** grabados). **Crea la entrada de apuntes de esta fase** antes de empezar. Abre **OBS**, comprueba pantalla y **micrófono** (vas a hablar) y empieza a grabar.

> [!example] Paso 1: Preséntate
> *"Soy [Nombre], 2.º SMR, simulación final de la Fase 0."* Enseña tu **perfil de GitHub** 2-3 segundos.

> [!example] Paso 2: Simulación A — ciclo de apuntes
> Narrándolo:
> ```bash
> pwd          # .../Boveda_SOR/00_Apuntes/Trimestre_1  (abre la terminal ahí con clic derecho)
> git pull
> ```
> Crea la **entrada de esta fase** (nombre `MMDDAA_titulo-corto.md` y estructura de la 0.1) y súbela:
> ```bash
> git add .
> git commit -m "Entrada de la simulacion final"
> git push
> ```

> [!example] Paso 3: Simulación B — ciclo de práctica
> ```bash
> pwd          # .../Boveda_SOR/01_Practicas/boochan-1  (abre la terminal ahí con clic derecho)
> ```
> Edita `MIS_DATOS.md`, míralo con `git status` y súbelo:
> ```bash
> git add .
> git commit -m "Cambio en la practica (simulacion final)"
> git push
> ```

> [!example] Paso 4: Comprobación final en GitHub
> Abre en el navegador tus **dos** repos (`apuntes-sor-t1` y `boochan-1`) y muestra que los **últimos commits** son los que acabas de hacer.

> [!example] Paso 5: Cierra el vídeo, nómbralo y súbelo
> Detén la grabación, nombra el vídeo `Fase 0.6 — Simulación final`, súbelo a la playlist `B0_Prerrequisitos` con **timestamps** (`00:00 Presentación`, Paso 2 apuntes, Paso 3 práctica, Paso 4 comprobación).

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | No se me oye en el vídeo. | Micrófono no seleccionado en OBS. | Añade "Captura de entrada de audio" y prueba el nivel. |
> | Un `push` falla en la simulación. | Olvidaste el `pull`, o hay cambios del otro equipo. | `git pull`, resuelve (o pregunta) y repite el `push`. |
> | Me lío con las rutas apuntes/práctica. | Son repos distintos. | `pwd`: apuntes en `00_Apuntes/Trimestre_1`, práctica en `01_Practicas/boochan-1`. |

> [!help] Preguntas Críticas
> 1. Describe el "circuito completo" (Obsidian → add → commit → push → GitHub → pull).
> 2. ¿Qué comando haces **siempre** al llegar a un ordenador?
> 3. Apuntes y práctica son **dos repos distintos**: ¿en qué carpeta está cada uno?

---

### ✅ Checklist Global del Bloque de Prerrequisitos (Fase 0 completa)

- [ ] **0.1:** bóveda `Boveda_SOR` con estructura + canal de YouTube con playlist `B0_Prerrequisitos`.
- [ ] **0.2.1 / 0.2.2:** cuenta de GitHub + Git configurado + autenticación (SSH/token).
- [ ] **0.3:** repo `apuntes-sor-t1` con entradas con formato correcto; enlace enviado.
- [ ] **0.4:** práctica `boochan-1` clonada y con un cambio subido.
- [ ] **0.5.1 / 0.5.2:** entorno replicado en casa + ciclo `pull → push` demostrado.
- [ ] **0.6:** simulación final grabada.
- [ ] **0.7.1 / 0.7.2:** las dos catástrofes provocadas y recuperadas (local con `git restore`, total clonando).
- [ ] **Vídeos:** TODAS las fases (0.1 a 0.6) subidas a la playlist `B0_Prerrequisitos`, con presentación y timestamps. Grabadas en su sitio: 🏫 centro (0.1–0.4, 0.6) · 🏠 casa (0.5.1, 0.5.2).
- [ ] **Una entrada por fase** (0.1, 0.2.1, 0.2.2, 0.3, 0.4, 0.5.1, 0.5.2, 0.6), cada una con **su enlace de vídeo** y **sus respuestas**.
- [ ] **Todas las tareas de Teams** del bloque entregadas, con `Entregar` pulsado.

> [!example] Último paso: repasa, sube y entrega
> 1. **Repasa que no te falta ninguna entrada.** Abre `B0_Prerrequisitos/` y cuenta: debe haber **una entrada por cada fase que has grabado**, y cada una con **su enlace de vídeo** y **sus respuestas**. Si falta alguna, escríbela ahora — todavía estás a tiempo.
> 2. **Sube todo:** `git add .` → `git commit -m "Cierre de los prerrequisitos"` → `git push`.
> 3. **Ve a Teams → `Tareas`** y abre la que cubre estas fases. Pega **los dos enlaces**:
>
> | Qué se entrega | Ejemplo |
> | :--- | :--- |
> | Enlace de tu **repositorio de apuntes** | `https://github.com/TU-USUARIO/apuntes-sor-t1` |
> | Enlace de tu **repositorio de la práctica** | `https://github.com/TU-USUARIO/boochan-1` |
>
> 4. Pulsa **`Entregar`**.
>
> > [!important] 📌 Los vídeos ya me los has dado
> > No hace falta que pegues ningún enlace de vídeo en la tarea: **cada uno está dentro de su entrada**, en tu repositorio. Por eso la regla es *una entrada por fase* — si me falta una entrada, sé exactamente qué fase falta.

---

> **Siguiente paso:** Fase 0.7 — **Cuando todo se rompe**: vamos a destruir tu trabajo a propósito, dos veces, y a recuperarlo. Es lo último de los prerrequisitos.
