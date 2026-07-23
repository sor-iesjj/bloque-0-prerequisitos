## 🎬 Fase 0.6: Verificación Final y Simulación Completa

### Demostrar, de principio a fin y grabado, que todo tu entorno funciona

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> Esta es la fase que **cierra** la puesta a punto. No se aprende nada nuevo: se **demuestra** que todo lo montado en las Fases 0.1 a 0.5 funciona junto, de una tacada y grabado. Es tu "examen práctico" del método de trabajo.
>
> **Profesor:** Pedro Navarro Miralles
> **Correo:** p.navarromiralles2@edu.gva.es
> **Centro:** IES Jorge Juan (ALICANTE)
>
> **⏱️ Tiempo estimado:** ~1 - 1,5 horas (la simulación completa, grabada)
> **Requisitos:** Fases 0.1 a 0.5 completas.

---

### 🎯 Objetivos de la fase

Al terminar esta fase serás capaz de:

- [ ] Recorrer el **flujo completo** de trabajo sin ayuda: apuntes y práctica, de la bóveda a GitHub.
- [ ] Grabar con OBS una **simulación de principio a fin** explicándola en voz alta.
- [ ] Comprobar, con una lista final, que **no falta nada** del entorno.
- [ ] Entregar los **enlaces** de tus repositorios.

---

### 🎯 ¿Dónde Estamos?

> [!info] El Punto de Partida
> Ya tienes: bóveda (0.1), GitHub + SSH (0.2), repo de apuntes con entradas (0.3), tu práctica clonada (0.4) y el entorno replicado en casa con sincronización (0.5). Todas las piezas están. Ahora toca verlas funcionar **juntas**.

> [!warning] El Problema
> Una cosa es que cada pieza funcione por separado y otra que sepas **encadenarlas tú solo**, sin la guía delante, el día que empiece una práctica de verdad. Esta fase se asegura de eso. Si aquí algo falla, lo arreglamos **antes** de empezar Boochan — no en mitad de la Fase 1.

> [!success] Objetivo de esta Fase
> Un **vídeo de simulación completa** en el que, de principio a fin, tomas una entrada de apuntes, la subes, haces un cambio en la práctica, lo subes, y demuestras que todo llega a GitHub. Más la **lista de verificación final** de todo el bloque de prerrequisitos.

> [!tip] Hoja de Ruta
> 1. Preparar la grabación (OBS + micrófono).
> 2. Simulación A: ciclo de apuntes (pull → entrada → push).
> 3. Simulación B: ciclo de práctica (cambio → status → push).
> 4. Comprobación final en GitHub.
> 5. Lista de verificación global y entrega de enlaces.
>
> **Resultado Final:** Prerrequisitos superados. Entorno listo para empezar el proyecto Boochan.
> **Siguiente:** ¡La práctica **Boochan** de verdad! (Y, antes, la prueba diagnóstica de redes que hará el profesor para ver de qué base partimos.)

---

### 📚 Fundamento Teórico

> [!info] Por qué se graba TODO
> Regla del curso, otra vez, porque es la más importante: **una práctica que no se graba, no cuenta.** El vídeo demuestra que lo hiciste tú, sirve para que te corrija, y —sobre todo— cuando lo grabas **explicando en voz alta**, te obligas a entender lo que haces. Explicar es la mejor forma de aprender.

> [!important] El flujo completo, de un vistazo
> Todo lo que has montado se resume en este circuito, que repetirás toda tu vida de técnico:
> ```
>   Obsidian (escribo)  →  git add  →  git commit  →  git push  →  GitHub (queda guardado)
>        ↑                                                              │
>        └──────────────────────  git pull  ←───────────────────────────┘
>                        (cuando cambio de ordenador)
> ```

---

### 🛠️ Procedimiento Práctico (la simulación)

> [!example] Paso 1: Prepara la grabación
> 1. Abre **OBS Studio**.
> 2. Comprueba que capturas la **pantalla** y que el **micrófono** se oye (harás la simulación **hablando**).
> 3. Empieza a grabar. Di tu nombre y grupo al principio: *"Soy Juan García, 2º SMR, simulación final de la Fase 0."*

> [!example] Paso 2: Simulación A — ciclo de apuntes
> Narrándolo en voz alta:
> 1. Abre la terminal, entra en tu repo de apuntes y baja lo último:
>    ```bash
>    cd ~/SOR/Boveda_SOR/00_Apuntes/Trimestre_1
>    git pull
>    ```
> 2. En Obsidian, crea una **entrada del día** nueva, con el **nombre correcto** (`AAAA-MM-DD_titulo.md`) y la **estructura** de la Fase 0.3.
> 3. Escribe unas líneas reales (por ejemplo, resumiendo esta Fase 0).
> 4. Sube:
>    ```bash
>    git add .
>    git commit -m "Entrada de la simulacion final"
>    git push
>    ```

> [!example] Paso 3: Simulación B — ciclo de práctica
> Sin cortar la grabación:
> 1. Entra en tu práctica:
>    ```bash
>    cd ~/SOR/Boveda_SOR/Practicas/boochan-1
>    ```
> 2. En Obsidian, edita `MIS_DATOS.md` (añade una línea, lo que sea).
> 3. Míralo con:
>    ```bash
>    git status
>    ```
> 4. Súbelo:
>    ```bash
>    git add .
>    git commit -m "Cambio en la practica (simulacion final)"
>    git push
>    ```

> [!example] Paso 4: Comprobación final en GitHub
> Todavía grabando:
> 1. Abre el navegador y entra en tus **dos** repositorios de GitHub (`apuntes-sor-t1` y `boochan-1`).
> 2. Muestra que **los últimos commits** son los que acabas de hacer (la entrada nueva y el cambio en la práctica).
> 3. Detén la grabación y **guarda el vídeo** con un nombre claro, por ejemplo `Fase0_Simulacion_Final_JuanGarcia.mp4`.
>
> > [!success] ✅ Si los dos repos muestran tus últimos cambios, la Fase 0 está SUPERADA
> > Sabes tomar apuntes con método, versionarlos, subirlos, clonar y trabajar una práctica, y sincronizar entre casa y centro. Estás listo para Boochan.

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Tabla de Troubleshooting (¿Algo no funciona?)
> | Problema | Causa Probable | Solución Sugerida |
> | :--- | :--- | :--- |
> | El micrófono no se oye en el vídeo. | No está seleccionado como fuente de audio en OBS. | En OBS, "Fuentes" → añade "Captura de entrada de audio" (micrófono) y prueba el nivel. |
> | Un `push` falla justo en la simulación. | Olvidaste el `pull` al empezar, o hay un cambio pendiente del otro equipo. | Haz `git pull`, resuelve si te lo pide (o pregunta), y repite el `push`. |
> | En GitHub no veo el último commit. | El `push` no llegó a ejecutarse o dio error que no viste. | Repite `git push` y mira el mensaje; recarga la página de GitHub. |
> | Me lío con las rutas al cambiar entre apuntes y práctica. | Son carpetas distintas (repos distintos). | Usa `pwd` para saber dónde estás; recuerda: apuntes en `00_Apuntes/Trimestre_1`, práctica en `Practicas/boochan-1`. |

> [!help] Preguntas Críticas (Autoevaluación del alumno)
> 1. Dibuja o describe el "circuito completo" (Obsidian → add → commit → push → GitHub → pull).
> 2. ¿Por qué grabamos las prácticas explicándolas en voz alta?
> 3. Los apuntes y la práctica son **dos repositorios distintos**. ¿En qué carpeta está cada uno?
> 4. ¿Qué comando haces **siempre** al llegar a un ordenador antes de trabajar?
> 5. 🔬 **Reto final:** haz la simulación entera **una segunda vez en casa**, sin mirar esta guía. Si te sale sola, has superado de verdad la Fase 0.

---

### ✅ Checklist Global del Bloque de Prerrequisitos (Fase 0 completa)

**Entorno (Fases 0.1–0.2):**
- [ ] Bóveda `Boveda_SOR` en ruta local (fuera de OneDrive), con su estructura de carpetas.
- [ ] Cuenta de GitHub creada; Git configurado; clave SSH funcionando (`Hi TU-USUARIO`).

**Apuntes y práctica (Fases 0.3–0.4):**
- [ ] Repo `apuntes-sor-t1` en GitHub, con entradas con el formato correcto.
- [ ] Práctica `boochan-1` clonada en `Practicas/` y con un cambio subido.

**Sincronización y cierre (Fases 0.5–0.6):**
- [ ] Entorno replicado en casa y ciclo `pull → push` demostrado.
- [ ] Vídeo de la simulación final grabado y guardado.

**Entrega al profesor:**
- [ ] Enlace de `apuntes-sor-t1` enviado (con acceso concedido si es privado).
- [ ] Enlace de `boochan-1` enviado.
- [ ] Vídeos de las prácticas de la Fase 0 (centro y casa) disponibles según indique el profesor.

> **Siguiente paso:** empieza el proyecto **Boochan** (Fase 1). Antes, el profesor pasará una **prueba diagnóstica de redes** (ver `Prueba_Diagnostica_Inicial_SOR`) para ver qué base traéis de 1º y reforzar lo necesario.
