## 🧰 Fase 0 — Puesta a Punto del Entorno de Trabajo (Índice)

> **[Módulo: SOR — Sistemas Operativos en Red · 2.º SMR]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> Bloque de **prerrequisitos** que se hace **antes** del proyecto Boochan. Monta el método de trabajo del curso: tomar apuntes en Obsidian, versionarlos con Git y enviarlos por GitHub para que el profesor los corrija. Se calcula que ocupa **2-3 semanas** de clase.


> [!abstract] 📋 Qué se evalúa en el Bloque 0
> Este bloque es **instrumental**: monta el entorno con el que entregarás todo lo demás (Git, GitHub, SSH, Obsidian). No es el contenido central del módulo, pero **sí demuestra criterios de evaluación reales**, sobre todo de configuración del entorno, seguridad de acceso y mantenimiento.
>
> | CE | Criterio | Dónde |
> | :--- | :--- | :--- |
> | `CE.01.g` | Preferencias en la configuración del entorno personal | 0.1 · 0.2.1 · 0.3 · 0.5.1 |
> > | `CE.04.b` | Qué recursos se comparten y en qué condiciones | 0.3b |
> | `CE.04.f` | Niveles de seguridad para controlar el acceso | 0.2.2 |
> | `CE.05.d` | Mantenimiento del software instalado | 0.4 · 0.5.1 · 0.7.1 · 0.7.2 |
> | `CE.05.e` | Automatización de tareas del sistema | 0.5.2 |
> | `CE.05.f` | Interpretar la información de configuración | 0.6 |
>
> Cada fase indica en su cabecera los suyos, con el texto literal del **RD 1691/2007**.


---

### ¿Por qué existe esta fase?

Un técnico no memoriza: **documenta**. Aquí se establece **cómo** trabajaremos todo el curso:

- **Apuntes** en Obsidian (**una entrada por fase**), separados de las **prácticas** (Boochan).
- Todo **versionado con Git** y subido a **GitHub** (un repo de apuntes por trimestre).
- Todo **grabado con OBS** y **subido a YouTube** (playlist `B0_Prerrequisitos`), con el **enlace de cada vídeo dentro de su entrada de apuntes**, y entregado en **tareas de Teams agrupadas**, no fase a fase.

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
> - **Cada fase se graba una vez**, en su sitio: 🏫 **centro** (0.1, 0.2.1, 0.2.2, 0.3, 0.4, 0.6, 0.7.1, 0.7.2) · 🏠 **casa** (0.5.1, 0.5.2). En prerequisitos no se graba dos veces lo mismo: el "en casa" de las 0.1–0.4 **es** la Fase 0.5.1.
> - **Al subir cada vídeo, el alumno guarda su enlace.** Lo necesitará para la entrega.

> [!important] 📤 Cómo se ENTREGA (tres sitios, tres trabajos distintos)
> Lo que más se confunde el primer día. Cada cosa tiene su función y **no se sustituyen entre sí**:
>
> | | Qué es | Para qué sirve |
> | :--- | :--- | :--- |
> | **Playlist `B0_Prerrequisitos`** | Organización del alumno. TODOS los vídeos del bloque van dentro. | Que no se pierdan |
> | **La entrada de apuntes** | Una **por fase**. Dentro va el **enlace de ESE vídeo** y las **respuestas** a las Preguntas Críticas. | Que el profesor vea qué hizo y qué entendió |
> | **La tarea de Teams** | La entrega evaluable. La abre el profesor, con notificación y **fecha límite de varios días**. | Poner nota |
>
> **La regla que lo sostiene todo: DONDE HAY VÍDEO, HAY ENTRADA.** Una entrada por fase grabada, con su enlace y sus respuestas dentro. Así el repositorio cuenta la historia completa y no hace falta cotejar nada contra ninguna lista.
>
> **En la tarea de Teams se pegan SOLO enlaces de repositorio** (el de apuntes y, al final, el de la práctica) **y el de la playlist**. **Nunca enlaces de vídeo sueltos**: esos ya están dentro de las entradas.
>
> > **Las entregas se agrupan**, no van fase a fase. El profesor decide qué fases cubre cada tarea y lo dice al abrirla en Teams: un bloque puede tener dos, tres o cuatro entregas según lo denso que sea. El alumno **no tiene que adivinarlo** — le llega la notificación.

> [!tip] Otros convenios
> - **Entrada:** una **por fase**, no una por día. Si una fase dura varias clases, se sigue escribiendo en el mismo fichero. Nombre `fase-CODIGO-titulo-corto.md` — **se llama como la fase, sin fecha** (el código ya ordena). Los días de teoría suelta: `teoria-MMDDAA-tema.md`. Estructura fija con dos apartados obligatorios: **Respuesta a las preguntas** y **Enlace al vídeo explicativo**. Se define en la **Fase 0.1**.
> - **Ciclo diario:** `git pull` al empezar → trabajar → `git add` / `commit` / `push` al terminar.

---

### Estructura de trabajo del alumno (la bóveda)

```
Boveda_SOR/                      ← se abre en Obsidian. NUNCA se hace git init aquí.
├── 00_Apuntes/
│   ├── Trimestre_1/             ← REPO propio (apuntes-sor-t1) → GitHub → enlace al profe
│   │   └── B0_Prerrequisitos/
│   │       └── fase-0.1-metodologia-y-estructura.md  ← una entrada por FASE
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
| **0.3** | [[Fase_0.3_Repo_Apuntes_y_Primera_Entrada]] | Repo del Trimestre 1 + entrada de la fase + **primera entrega** en Teams. |
| **0.3b** | [[Fase_0.3b_Que_No_Se_Sube_Gitignore]] | El **`.gitignore`**: qué no se sube nunca y por qué subir una clave no se arregla borrándola. |
| **0.4** | [[Fase_0.4_Clonar_Practica_Boochan]] | Crea **sus copias** del Bloque 1 y de `boochan-1` (`Use this template`) y las clona. Domina `status → commit → push` + **3 retos** de borrado y recuperación. |
| **0.5** | [[Fase_0.5_Casa_y_Centro_Sincronizacion]] | *(índice)* Casa ↔ centro, en 2 partes ↓ |
| ↳ **0.5.1** | [[Fase_0.5.1_Montar_Entorno_Casa]] | Monta el entorno en casa y clona sus repos. |
| ↳ **0.5.2** | [[Fase_0.5.2_Sincronizar_Casa_Centro]] | Ciclo `pull → push`; regla anti-OneDrive. |
| **0.6** | [[Fase_0.6_Verificacion_y_Simulacion_Final]] | Simulación completa grabada; verificación global. |
| **0.7** | [[Fase_0.7_Cuando_Todo_Se_Rompe]] | *(índice)* Romper el trabajo a propósito y recuperarlo, en 2 partes ↓ |
| ↳ **0.7.1** | [[Fase_0.7.1_Catastrofe_Local_Recuperar_Con_Git]] | Pierde el contenido de sus apuntes y lo recupera **solo con Git**, sin Internet. |
| ↳ **0.7.2** | [[Fase_0.7.2_Catastrofe_Total_Recuperar_Desde_GitHub]] | Borra la bóveda entera (apuntes **y** práctica) y la reconstruye **clonando**. |

---

