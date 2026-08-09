## 🎬 Fase 0.6: Verificación Final y Simulación Completa

### Demostrar, de principio a fin y grabado, que todo tu entorno funciona

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~1 - 1,5 horas · **Requisitos:** Fases 0.1 a 0.5.2 completas.


> [!abstract] 📋 Qué se te evalúa en esta fase
> **RA.05**
>
> | Código | Criterio de evaluación |
> | :--- | :--- |
> | `CE.05.f` | Se ha interpretado la información de configuración del sistema operativo en red. |
>
> Los criterios están tomados literalmente del **RD 1691/2007** y de la programación del módulo.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta fase **es** un vídeo: una simulación completa grabada de principio a fin.
> 1. **Prepárate primero (sin grabar):** repasa mentalmente todo el flujo (apuntes y práctica) y **crea la entrada de apuntes de esta fase** en Obsidian: fichero `b0-0.6-simulacion-final.md` con la estructura del **Bloque 0 · Fase 0.1.b**, **vacía**.
>
>    > [!warning] ⚠️ Esta fase es la única donde SÍ te grabas escribiendo
>    > En las demás la entrada se rellena después, sin grabar. Aquí no: **el ejercicio de hoy es demostrar el ciclo entero** —`pull` → escribir → `add` → `commit` → `push`— y eso incluye escribir algo de verdad. La rellenas en la Simulación A, delante de la cámara.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a hacer la simulación final de la Fase 0."* **Muestra tu perfil de GitHub**. Di qué vas a demostrar.
> 3. **Graba TODO el circuito**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `B0.6 · Simulación final` y súbelo a tu playlist **`B0_Prerrequisitos`** (No listado).
> 6. **~5-7 min.** Se graba en **🏫 el centro** (o donde indique el profesor).
> 7. **El enlace del vídeo va DENTRO de tu entrada de apuntes**, en el apartado `🔗 Enlaces`. No lo guardes en un papel: va ahí.
> 8. **La entrega va por la TAREA de Teams.** Cuando toque, abriré una tarea que cubrirá **esta fase y otras**; te llegará notificación.

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
> Y una cosa que se olvida siempre: **este circuito es de UN repositorio**. Tú tienes tres, así que tienes **tres circuitos independientes** funcionando en paralelo. Cada uno con su `pull` y su `push`.

---

### 🛠️ Procedimiento Práctico (la simulación)

> [!example] Paso 0: Prepárate (sin grabar) y arranca OBS
> Repasa el flujo y **léete el procedimiento entero** (tiene **5 pasos** grabados). **Crea la entrada de apuntes de esta fase** (`b0-0.6-simulacion-final.md`), con su estructura y vacía. Abre **OBS**, comprueba pantalla y **micrófono** (vas a hablar) y empieza a grabar.

> [!example] Paso 1: Preséntate
> *"Soy [Nombre], 2.º SMR, simulación final de la Fase 0."* Enseña tu **perfil de GitHub** 2-3 segundos.

> [!example] Paso 2: Simulación A — ciclo de apuntes
> Narrándolo:
> ```bash
> pwd          # .../Boveda_SOR/00_Apuntes/Trimestre_1  (abre la terminal ahí con clic derecho)
> git pull
> ```
> Rellena la **entrada de esta fase** (la que creaste en el Paso 0) y súbela:
> ```bash
> git add .
> git commit -m "Entrada de la simulacion final"
> git push
> ```

> [!example] Paso 3: Simulación B — el MISMO ciclo, en otro repositorio
> Fíjate en que es **exactamente lo mismo** que acabas de hacer, cambiando de carpeta. Empieza igual, por el `pull`:
> ```bash
> pwd          # .../Boveda_SOR/01_Practicas/B2_Ubuntu_Local  (abre la terminal ahí con clic derecho)
> git pull
> ```
> Edita `MIS_DATOS.md`, míralo con `git status` y súbelo:
> ```bash
> git add .
> git commit -m "Cambio en la practica (simulacion final)"
> git push
> ```
>
> > [!important] ⚠️ El ciclo va POR REPOSITORIO, no una vez al día
> > Esto es lo que hay que llevarse de la fase, y es lo que más se falla en la práctica.
> >
> > **`git pull` y `git push` NO son "lo que se hace al llegar y al irme".** Son **lo que se hace en cada carpeta en la que vas a trabajar**. Git no sabe nada de tus otras carpetas: cada repositorio va por su cuenta y **no se entera de lo que pasa en los demás**.
> >
> > Ahora mismo tienes **tres**:
> > ```
> > 00_Apuntes/Trimestre_1/        ← tus apuntes
> > 01_Practicas/B1_Entorno/ ← tu copia del Bloque 1
> > 01_Practicas/B2_Ubuntu_Local/        ← tu copia de Boochan
> > ```
> > Si hoy tocas los apuntes y el Bloque 1, hoy haces **dos `pull` y dos `push`**, uno en cada carpeta. Si solo tocas uno, uno.
> >
> > **Hoy simulamos dos** porque con dos ya se ve el patrón y el vídeo tiene que durar cinco minutos. Pero el tercero funciona **exactamente igual**: mismo comando, otra carpeta.

> [!example] Paso 4: Comprobación final en GitHub
> Abre en el navegador tus **tres** repositorios y enséñalos:
> - `apuntes-sor-t1` → el último commit debe ser el de hace un minuto (Simulación A).
> - `bloque-2-ubuntu-local` → el último commit debe ser el de hace unos segundos (Simulación B).
> - `bloque-1-entorno` → **este no lo has tocado hoy**, así que su último commit es el de cuando lo copiaste. Y está bien que sea así: enséñalo y explica por qué.
>
> Ese contraste es la prueba de que lo has entendido: **los tres repos van por su cuenta**, y cada uno refleja lo que tú has hecho en él.

> [!example] Paso 5: Cierra el vídeo, nómbralo y súbelo
> Detén la grabación, nombra el vídeo `B0.6 · Simulación final`, súbelo a la playlist `B0_Prerrequisitos` con **timestamps** (`00:00 Presentación`, Paso 2 apuntes, Paso 3 práctica, Paso 4 comprobación).

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | No se me oye en el vídeo. | Micrófono no seleccionado en OBS. | Añade "Captura de entrada de audio" y prueba el nivel. |
> | Un `push` falla en la simulación. | Olvidaste el `pull`, o hay cambios del otro equipo. | `git pull`, resuelve (o pregunta) y repite el `push`. |
> | Me lío con las rutas apuntes/práctica. | Son repos distintos. | `pwd`: apuntes en `00_Apuntes/Trimestre_1`, práctica en `01_Practicas/B2_Ubuntu_Local`. |

> [!help] Preguntas Críticas
> 1. Describe el "circuito completo" (Obsidian → add → commit → push → GitHub → pull).
> 2. ¿Qué comando haces **siempre** al llegar a un ordenador?
> 3. Ahora tienes **tres repositorios**: dilos, y di en qué carpeta está cada uno.
> 4. Si un día trabajas en los apuntes y en el Bloque 1, ¿cuántos `pull` haces? ¿Y cuántos `push`? **¿Por qué?**

---

### ✅ Checklist Global del Bloque de Prerrequisitos (Fase 0 completa)

- [ ] **0.1:** bóveda `Boveda_SOR` con estructura + canal de YouTube con playlist `B0_Prerrequisitos`.
- [ ] **0.2.1 / 0.2.2:** cuenta de GitHub + Git configurado + autenticación (SSH/token).
- [ ] **0.3:** repo `apuntes-sor-t1` con entradas con formato correcto; enlace enviado.
- [ ] **0.3.b:** `.gitignore` escrito, commiteado y **comprobado** con un fichero que no debe subir.
- [ ] **0.4:** **tus copias** del Bloque 1 y de `bloque-2-ubuntu-local` creadas y clonadas, con un cambio subido. Los **3 retos** de borrado y recuperación resueltos.
- [ ] **0.5.1 / 0.5.2:** entorno replicado en casa + ciclo `pull → push` demostrado.
- [ ] **0.6:** simulación final grabada.
- [ ] **0.7.1 / 0.7.2:** las dos catástrofes provocadas y recuperadas (local con `git restore`, total clonando).
- [ ] **Vídeos: los ONCE** (0.1 · 0.2.1 · 0.2.2 · 0.3 · 0.3.b · 0.4 · 0.5.1 · 0.5.2 · 0.6 · 0.7.1 · 0.7.2) subidos a la playlist `B0_Prerrequisitos`, con presentación y timestamps. Grabados en su sitio: 🏫 **centro** (todos menos dos) · 🏠 **casa** (0.5.1 y 0.5.2).
- [ ] **Una entrada por fase — once**, cada una con **su enlace de vídeo** y **sus respuestas**. Donde hay vídeo, hay entrada.
- [ ] **Todas las tareas de Teams** del bloque entregadas, con `Entregar` pulsado.

> [!example] Último paso: repasa, sube y entrega
> 1. **Repasa que no te falta ninguna entrada.** Abre `B0_Prerrequisitos/` y cuenta: debe haber **una entrada por cada fase que has grabado**, y cada una con **su enlace de vídeo** y **sus respuestas**. Si falta alguna, escríbela ahora — todavía estás a tiempo.
> 2. **Sube todo:** `git add .` → `git commit -m "Cierre de los prerrequisitos"` → `git push`.
> 3. **Ve a Teams → `Tareas`** y abre la que cubre estas fases. Pega **los tres enlaces**:
>
> | Qué se entrega | Ejemplo |
> | :--- | :--- |
> | Enlace de tu **repositorio de apuntes** | `https://github.com/TU-USUARIO/apuntes-sor-t1` |
> | Enlace de tu **repositorio de la práctica** | `https://github.com/TU-USUARIO/bloque-2-ubuntu-local` |
> | Enlace de tu **playlist** | `https://youtube.com/playlist?list=…` |
>
> 4. Pulsa **`Entregar`**.
>
> > [!important] 📌 Los vídeos ya me los has dado
> > No hace falta que pegues ningún enlace de vídeo en la tarea: **cada uno está dentro de su entrada**, en tu repositorio. Por eso la regla es *una entrada por fase* — si me falta una entrada, sé exactamente qué fase falta.

---

> **Siguiente paso:** Fase 0.7 — **Cuando todo se rompe**: vamos a destruir tu trabajo a propósito, dos veces, y a recuperarlo. Es lo último de los prerrequisitos.
