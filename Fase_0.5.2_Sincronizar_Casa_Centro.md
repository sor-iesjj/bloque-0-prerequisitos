## 🔄 Fase 0.5.2: Sincronizar Casa ↔ Centro

### El ciclo `pull → trabajar → push` (y por qué NO OneDrive)

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0.5 — parte 2 de 2]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~1 hora · **Requisitos:** Fase 0.5.1 completa (entorno de casa montado).


> [!abstract] 📋 Qué se te evalúa en esta fase
> **RA.05**
>
> | Código | Criterio de evaluación |
> | :--- | :--- |
> | `CE.05.e` | Se han ejecutado operaciones para la automatización de tareas del sistema. |
>
> Los criterios están tomados literalmente del **RD 1691/2007** y de la programación del módulo.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin.
> 1. **Prepárate primero (sin grabar):** comprueba lo necesario, **léete el procedimiento entero** y **crea la entrada de apuntes de esta fase** en Obsidian: fichero `b0-0.5.2-sincronizar-casa-centro.md` con la estructura del **Bloque 0 · Fase 0.1.b**, **vacía**. Rellenarla es cosa tuya, después; hoy solo tiene que existir.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a explicar la Fase 0.5.2 — Sincronizar casa y centro."* Y **muestra tu perfil de GitHub**. Di qué vas a hacer.
> 3. **Graba TODO**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `B0.5.2 · Sincronizar casa y centro` y súbelo a tu playlist **`B0_Prerrequisitos`** (No listado).
> 6. **~5 min.** Se graba en **🏠 casa**.
> 7. **La entrega va por la TAREA de Teams.** Cuando toque, abriré una tarea que cubrirá **esta fase y otras**; te llegará notificación. Tú, hoy: graba, sube el vídeo a la playlist y **pega su enlace en tu entrada de apuntes**.
> 8. **El enlace del vídeo va DENTRO de tu entrada de apuntes**, en el apartado `🔗 Enlaces`. No lo guardes en un papel: va ahí.

---

### 🎯 Objetivos

- [ ] Dominar el **ciclo diario**: `pull` al empezar → trabajar → `commit` y `push` al terminar.
- [ ] Explicar que el ciclo se hace **en cada repositorio** que toques ese día, no una vez.
- [ ] Explicar por qué **OneDrive y Git no pueden gestionar la misma carpeta**.
- [ ] Confirmar que un cambio hecho en un equipo aparece en el otro.

---

### 📚 Fundamento Teórico

> [!danger] Por qué OneDrive y Git NO pueden convivir
> Son **dos sincronizadores** peleándose por los mismos ficheros:
> - **Git** guarda su historial en `.git`, una carpeta delicada. OneDrive la sincroniza a medias y la **corrompe**.
> - OneDrive crea **"copias en conflicto"** (`fichero-MiPC.md`) que ensucian todo.
> - Si OneDrive ya te trae los ficheros, el `git pull` **pierde sentido**.
>
> **Conclusión:** la bóveda va **local** (fuera de OneDrive) en los dos equipos. **GitHub es tu nube**; OneDrive, para otras cosas.

> [!important] El ciclo diario: PULL al empezar, PUSH al terminar
> ```
> 1. Llego a un ordenador  →  git pull   (bajo lo último del otro equipo)
> 2. Trabajo (Obsidian)    →  edito / creo entradas
> 3. Antes de irme         →  git add . → git commit → git push
> ```
> Si **siempre** haces `pull` al empezar y `push` al terminar, tus dos equipos nunca se desincronizan.
>
> > [!warning] ⚠️ Ojo: el ciclo es POR CARPETA, no por día
> > Aquí lo practicamos sobre `Trimestre_1`, pero **no es "el ciclo de los apuntes"**: es el ciclo **de cada repositorio**. Y tú tienes cuatro:
> > `00_Apuntes/Trimestre_1/` · `01_Practicas/B0_Prerrequisitos/` · `01_Practicas/B1_Entorno/` · `01_Practicas/B2_Ubuntu_Local/`
> >
> > Git **no sabe nada de tus otras carpetas**. Un `pull` en los apuntes no baja nada del Bloque 1. Si hoy vas a tocar dos, haces el ciclo **dos veces**, una en cada una.
> >
> > **Los cuatro son tuyos y en los cuatro puedes empujar.** Así que si un día anotas una duda en la carpeta de una práctica, esa carpeta también necesita su `push` antes de irte — o el sábado no estará.

> [!warning] Si olvidas el `pull`
> Puede aparecer un **conflicto** (Git no sabe qué versión vale). Por eso: **primero `pull`, siempre.** Si ves la palabra `CONFLICT`, para y pregúntame.

---

### 🛠️ Procedimiento Práctico

> [!example] Paso 0: Prepárate (todavía SIN grabar)
> **Léete el procedimiento** (tiene **3 pasos** grabados). Ten **OBS** listo y tu **perfil de GitHub** en una pestaña.
> **Y antes de grabar: crea la entrada de apuntes de esta fase** (`b0-0.5.2-sincronizar-casa-centro.md`) con la estructura pegada y **vacía**. En el vídeo solo tienes que **enseñarla**, no rellenarla.

> [!example] Paso 1: Arranca la grabación y practica el ciclo (en casa)
> Inicia la grabación, preséntate y muestra tu identidad. Luego:
> 1. **Al empezar**, baja lo último (clic derecho sobre `Trimestre_1` → abrir terminal ahí, como en la Fase 0.3):
>    ```bash
>    pwd          # .../Boveda_SOR/00_Apuntes/Trimestre_1
>    git pull
>    ```
> 2. En Obsidian, abre **la entrada de esta fase** —`b0-0.5.2-sincronizar-casa-centro.md`, la que creaste en el Paso 0— y escribe algo de verdad en ella.
>
>    > [!tip] 💡 No crees una entrada "de prueba"
>    > Se quedaría en tu repositorio para siempre, y **rompe la regla del bloque**: una fase, una entrada. Usa la que ya te toca escribir hoy — así el ejercicio y la entrega son lo mismo.
>
> 3. **Al terminar**, sube:
>    ```bash
>    git add .
>    git commit -m "Fase 0.5.2: apuntes escritos desde casa"
>    git push
>    ```
> 4. Compruébalo en GitHub.

> [!example] Paso 2: Confirma la sincronización centro ↔ casa
> Explica que, al día siguiente **en el centro**, lo primero es:
> ```bash
> pwd          # .../Boveda_SOR/00_Apuntes/Trimestre_1
> git pull
> ```
> y que eso **baja** la entrada que hiciste en casa. (Si puedes, demuéstralo con el otro equipo; si no, explícalo con el flujo.)

> [!example] Paso 3: Cierra el vídeo, nómbralo y súbelo
> Detén la grabación, nombra el vídeo `B0.5.2 · Sincronizar casa y centro`, súbelo a la playlist `B0_Prerrequisitos` con **timestamps**.

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | Aparecen `... -MiPC.md` duplicados. | La bóveda está en OneDrive. | Sácala a local; borra las copias en conflicto. |
> | `git pull` dice `CONFLICT`. | Editaste el mismo fichero en dos sitios sin `pull` antes. | Para y pregunta. Para evitarlo: **`pull` siempre al empezar**. |
> | `git pull` dice `Your branch is behind`. | Hay cambios en GitHub. Es lo normal y bueno. | Deja que baje los cambios. |

> [!help] Preguntas Críticas
> 1. ¿Por qué NO se mete la bóveda en OneDrive si usamos Git?
> 2. Escribe el ciclo diario de tres pasos.
> 3. ¿Qué problema puede aparecer si olvidas el `pull` al empezar?

---

### ✅ Checklist Final de la Fase 0.5.2

- [ ] Ciclo `pull → editar → push` practicado y grabado.
- [ ] Sincronización confirmada (o explicada) entre casa y centro.
- [ ] Sabes explicar por qué la bóveda no va en OneDrive.
- [ ] Vídeo `B0.5.2 · Sincronizar casa y centro` subido a la playlist, con timestamps.
- [ ] **Enlace del vídeo pegado en tu entrada de apuntes** de esta fase.
- [ ] Grabada **🏠 en casa**.

> **Siguiente paso:** Fase 0.6 — Verificación final y simulación completa.
