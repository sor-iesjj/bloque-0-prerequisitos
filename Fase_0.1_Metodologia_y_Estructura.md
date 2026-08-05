## 🧭 Fase 0.1: Metodología de Trabajo y Estructura de la Bóveda

### Cómo vamos a trabajar todo el curso (y por qué...)

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> Esta fase **no** enseña redes ni servidores todavía: monta el **método** con el que trabajaremos el resto del curso. Sin esto, nada de lo que venga después se puede entregar ni corregir.
>
> **Profesor:** Pedro Navarro Miralles
> **Correo:** p.navarromiralles2@edu.gva.es
> **Centro:** IES Jorge Juan (ALICANTE)
>
> **⏱️ Tiempo estimado:** ~1,5 - 2 horas (explicación + montar el canal de vídeo + práctica grabada)
> **Requisitos:** Obsidian y OBS ya instalados en el equipo (los instala Consellería — tú no tienes permisos). Necesitarás una **cuenta de Gmail/YouTube** (la creas en el Paso previo). No hace falta Git en esta fase todavía.


> [!abstract] 📋 Qué se te evalúa en esta fase
> **RA.01**
>
> | Código | Criterio de evaluación |
> | :--- | :--- |
> | `CE.01.g` | Se han aplicado preferencias en la configuración del entorno personal. |
>
> Los criterios están tomados literalmente del **RD 1691/2007** y de la programación del módulo.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin. No es un repaso al final: quiero ver **cómo lo haces tú**.
> 1. **Prepárate primero (sin grabar):** comprueba que tienes lo necesario y **léete el procedimiento entero** para no atascarte a mitad del vídeo. *(En esta primera fase la entrada de apuntes la creas **dentro** de la práctica, en el Paso 5: todavía no sabes cómo se hace. **A partir de la 0.2.1, crearla será lo PRIMERO que hagas**, antes de grabar.)*
> 2. **Arranca OBS y, nada más empezar, PRESÉNTATE:** *"Hola y bienvenidos. Me llamo [Nombre], soy alumno de 2.º SMR, y en este vídeo voy a explicar la Fase 0.1 — Metodología y estructura de la bóveda."* Y **muestra en pantalla algo que demuestre que eres tú** (tu **Teams** o tu **correo `@alu.edu.gva.es`** con tu nombre; cuando tengas GitHub, tu perfil). Di **qué vas a hacer**.
> 3. **Graba TODO el procedimiento**, explicando cada paso en voz alta mientras lo haces.
> 4. **Timestamps SIEMPRE** en la descripción del vídeo: `00:00 Presentación` y **uno por cada paso** (formato `mm:ss`).
> 5. **Al terminar:** nombra el vídeo `B0.1 · Metodología y estructura`, **súbelo a tu playlist de YouTube `B0_Prerrequisitos`** (No listado) y **pega su enlace en tu entrada de apuntes**.
> 6. **~5 min.** Se graba en **🏫 el centro** (el equipo de casa se monta entero en la Fase 0.5.1, no aquí).
> 7. **La entrega va por la TAREA de Teams.** Cuando toque, abriré una tarea que cubrirá **esta fase y otras**; te llegará notificación. Tú, hoy: graba, sube el vídeo a la playlist y **pega su enlace en tu entrada de apuntes**.

---

### 🎯 Objetivos de la fase

Al terminar esta fase serás capaz de:

- [ ] Explicar con tus palabras qué es una **bóveda** de Obsidian y para qué la usamos.
- [ ] Explicar la diferencia entre **tus apuntes** y las **prácticas** (Boochan), y por qué viven en carpetas separadas.
- [ ] Tener tu **canal de YouTube** con la playlist `B0_Prerrequisitos` lista.
- [ ] Comprobar si tu carpeta `Documentos` está en OneDrive, y crear tu bóveda `Boveda_SOR` en la ruta correcta (sabiendo **por qué** no puede vivir en OneDrive).
- [ ] Crear la **estructura de carpetas** exacta que usaremos todo el curso, respetándola al detalle.
- [ ] Escribir tu **primera entrada de apuntes** con el nombre y la estructura obligatorios.
- [ ] **Grabar la práctica entera con OBS**, presentándote, y subirla a tu playlist.
- [ ] Distinguir **subir a la playlist** (organizar) de **entregar en la tarea de Teams** (evaluar).

---

### 🎯 ¿Dónde Estamos?

> [!info] El Punto de Partida
> Este es el primer día de verdad. No vamos a tocar servidores todavía: primero vamos a montar **tu forma de trabajar conmigo durante todo el curso**. En este módulo vas a hacer **prácticas** que imitan situaciones reales de un técnico (las prácticas *Boochan* en recuerdo de Iker y Héctor), y a la vez vas a **tomar apuntes** de todo lo que expliquemos. Las dos cosas se entregan, y las dos cosas cuentan para nota.

> [!warning] El Problema
> Un técnico no memoriza: **documenta**. Si no tienes un sitio ordenado donde anotar lo que haces, dentro de dos semanas no te acordarás de nada, no podrás repetir una práctica en casa, y yo no podré corregir tu trabajo. Por eso lo primero no es "instalar cosas", es **decidir dónde y cómo se guarda la información** — y que todos lo hagamos exactamente igual.

> [!success] Objetivo de esta Fase
> Dejar montada, en tu equipo, una **bóveda de Obsidian** llamada `Boveda_SOR` con una estructura de carpetas fija: una zona para **tus apuntes** (por trimestres) y otra para las **prácticas** (Boochan). Y entregar el **vídeo grabado** de todo el proceso en tu playlist de YouTube.

---

### 📚 Fundamento Teórico

> [!info] ¿Qué es Obsidian?
> Obsidian es un programa para **tomar notas** en formato de texto. No es como Word: cada nota es un fichero de texto simple (con extensión `.md`, llamado *Markdown*) que pesa muy poco, se lee en cualquier ordenador y se puede versionar y enviar por Internet fácilmente. Es la herramienta que usaremos para **todos tus apuntes** del módulo. Está disponible en **Windows, Linux, Mac, Android e iOS**, y como tus notas son solo ficheros de texto, **la misma bóveda funciona igual en el equipo del centro y en tu casa**.

> [!abstract] 1. Qué es una "bóveda" (vault)
> Una **bóveda** es, simplemente, **una carpeta de tu disco duro** que Obsidian abre y gestiona. Todo lo que metas dentro de esa carpeta (notas, subcarpetas, imágenes) forma parte de la bóveda. No es nada mágico ni un formato raro: es una carpeta normal. Cuando "abres una bóveda" en Obsidian, le estás diciendo: *"trabaja con todo lo que hay dentro de esta carpeta"*.
>
> Nuestra bóveda se llamará **`Boveda_SOR`** y será el **punto de referencia** de todo el curso: dentro estarán tus apuntes y las prácticas.

> [!important] 2. Apuntes vs. Prácticas: dos cosas distintas que NO se mezclan
> Dentro de la bóveda tendremos **dos zonas separadas a propósito**:
>
> | Zona | Qué es | Ejemplo |
> | :--- | :--- | :--- |
> | **`00_Apuntes/`** | **Lo que TÚ escribes**: tus notas de lo que yo explico cada día. Es tu cuaderno digital. | "Hoy hemos visto qué es una IP y para qué sirve el ping…" |
> | **`01_Practicas/`** | **El material que YO te doy**: las prácticas Boochan que descargarás de Internet. Tú las sigues y trabajas sobre ellas. | La práctica `boochan-1` con sus fases. |
>
> **¿Por qué separadas?** Porque tus apuntes son **tuyos** y me los entregas para que los corrija; las prácticas son material del curso. Mezclarlos sería como escribir tus apuntes encima del libro de otra persona: un lío para ti y para mí.

> [!note] 3. La metodología: una entrada por FASE
> Tus apuntes se organizan así, de lo más grande a lo más pequeño:
>
> **Trimestre → Bloque → Entrada de fase**
>
> - **Trimestre:** primero, segundo o tercero. Cada uno en su carpeta.
> - **Bloque:** cada parte grande del curso. Son **los míos, los que yo numero**: el **Bloque 0 son los Prerrequisitos** (esto que estamos haciendo ahora), el **Bloque 1 es el Entorno**, y así. Tus carpetas se llaman **igual que mis bloques**, a propósito.
> - **Entrada de fase:** **un fichero por cada fase**, no uno por día. Si una fase nos lleva tres clases, **sigues escribiendo en el mismo fichero** durante esos tres días. Así toda la información de esa fase está junta en un sitio, y no repartida en tres trozos que no se entienden por separado.
>
> Hoy dejas preparadas las carpetas **y escribes tu primera entrada**.

> [!tip] 💡 Tus carpetas se llaman igual que mis bloques. No es casualidad
> Cuando yo diga en clase *"esto es del Bloque 1"*, tú ya sabes **exactamente** en qué carpeta va: `B1_Entorno`. No hay que traducir nada. Por eso **no te inventes tus propios nombres ni tu propia numeración**: si cada uno organiza sus apuntes a su manera, ni tú encuentras nada en junio ni yo puedo corregir a veinte personas.
>
> Los bloques del curso son estos, y los iremos abriendo según lleguemos:
> `B0_Prerrequisitos` · `B1_Entorno` · `B2_Ubuntu_Local` · `B3_Windows_Local` · `B4_Ubuntu_Nube` · `B5_Windows_Nube` · `B6_Contenedores`
>
> **Hoy solo creas el primero.** Los demás los irás creando cuando toquen — no adelantes carpetas vacías.
>
> Y fíjate en un detalle que **te va a ahorrar líos**: tu carpeta de apuntes del Bloque 0 se llama `B0_Prerrequisitos`… y tu **playlist de YouTube** de este bloque se llama **exactamente igual**. Es a propósito: **un bloque = un nombre**, valga para la carpeta o para la lista de vídeos. Cuando lleguemos al Bloque 1 tendrás la carpeta `B1_Entorno` y la playlist `B1_Entorno`, y así siempre.

> [!important] 4. La regla de oro de los apuntes: DONDE HAY VÍDEO, HAY ENTRADA
> Esta es la norma que más te conviene entender, porque de ella sale tu nota de apuntes:
>
> - **Una fase = una entrada.** Ni más ni menos.
> - **Si una fase dura varios días**, NO creas una entrada nueva cada día: **abres la de siempre y sigues escribiendo**. Toda la fase, en un solo sitio.
> - **Si un día hacemos dos fases**, escribes **dos** entradas, no una. La 0.2.1 y la 0.2.2 la misma tarde son dos ficheros con la misma fecha y distinto título.
> - **Si damos teoría que no pertenece a ninguna fase**, esa clase también tiene su entrada, con el tema como título.
> - **La entrada se CREA al empezar la fase**, antes incluso de arrancar OBS: con su nombre y su estructura pegada, aunque esté vacía. En el vídeo solo tienes que **enseñarla**. **Rellenarla es cosa tuya, a tu ritmo**, mientras dure la fase — no hay que grabarse escribiendo.
>
> ¿Por qué así? Por dos razones, y las dos te convienen:
> 1. **La entrada es donde vive el enlace de tu vídeo** (apartado 6). Una entrada por fase = tu repositorio me cuenta solo la historia: qué hiciste, qué entendiste y dónde está el vídeo que lo demuestra. Si me falta una entrada, sé exactamente qué fase falta.
> 2. **Para ti, en junio.** Buscar "lo de las claves SSH" en un fichero llamado `Fase 0.2.2` es inmediato. Buscarlo repartido en tres entradas de tres martes distintos es perder la tarde.

> [!important] 5. La entrada: NOMBRE obligatorio
> **Un fichero por fase** dentro de la carpeta del bloque que toque. **La entrada se llama como la fase**:
> ```
> fase-CODIGO-titulo-corto.md
> ```
> Todo en minúsculas, con guiones, **sin tildes ni espacios**.
>
> **¿Y la fecha? No va en el nombre.** No hace falta: **el código de la fase ya ordena**. `fase-0.1`, `fase-0.2.1`, `fase-0.2.2`, `fase-0.3`… se colocan solas y en el orden en que las hemos dado. Meter además la fecha sería repetir información y encima descolocaría el orden si una fase se retrasa. La fecha va **dentro** de la entrada, en su campo.
>
> **Correcto:** `fase-0.1-metodologia-y-estructura.md` · `fase-0.2.2-clave-ssh.md`
> **Incorrecto:** `apuntes dia 1.md` ❌ · `Fase 0.1.md` ❌ (espacios y mayúsculas) · `0.1.md` ❌ (sin decir de qué va)
>
> La **carpeta ya te dice el bloque**, así que en el título no lo repitas: `fase-0.2.2-clave-ssh` y no `fase-0.2.2-bloque-0-clave-ssh`.
>
> > [!note] 📌 ¿Y los días de teoría, que no son ninguna fase?
> > Esos sí llevan fecha, porque no tienen código que los ordene. Se nombran `teoria-MMDDAA-tema.md`:
> > `teoria-091726-que-es-un-dominio.md`
> > Así, dentro de la carpeta del bloque, **las fases van juntas y en orden, y la teoría va junta y por fecha**.

> [!important] 6. La entrada: ESTRUCTURA obligatoria
> Todas tus entradas se escriben igual. Cópiala tal cual y rellénala:
> ```markdown
> # Fase 0.1 — Metodología y estructura
>
> **Fecha:** 15/09/2026            (si la fase dura varios días: 15/09/2026 - 17/09/2026)
> **Bloque:** B0 — Prerrequisitos
> **Fase / práctica:** Fase 0.1 — Metodología y estructura
>
> ## Qué hemos visto hoy
> - (con tus palabras)
>
> ## Conceptos clave
> - **Término:** definición corta.
>
> ## Comandos / pasos importantes
> - `comando` — para qué sirve.
>
> ## Respuesta a las preguntas
> 1. (respuesta a la pregunta 1 de la fase)
> 2. (respuesta a la pregunta 2)
> 3. …
>
> ## Enlace al vídeo explicativo
> - https://youtu.be/XXXXXXXXXXX
>
> ## Dudas / a repasar en casa
> - (lo que no te ha quedado claro)
> ```
>
> Dos apartados son **nuevos y obligatorios**, y son los que más peso tienen:
>
> | Apartado | Qué va ahí |
> | :--- | :--- |
> | **Respuesta a las preguntas** | Las **Preguntas Críticas** que hay al final de cada fase, contestadas **con tus palabras**. Las respuestas están en la teoría de esa misma fase: si no sabes contestar, es que hay que releerla. El **🔬 Reto** es voluntario. |
> | **Enlace al vídeo explicativo** | La dirección del vídeo **de esa fase concreta**, no la de la playlist. Sin este enlace, la entrada está incompleta. |
>
> > [!warning] ⚠️ El enlace del VÍDEO, no el de la playlist
> > Son cosas distintas y aquí va **el del vídeo**. En YouTube: abre **ese vídeo**, `Compartir` → `Copiar enlace`. Te saldrá algo como `https://youtu.be/aB3dE5f...`.
> > Si pegas el de la playlist (lleva `list=` dentro), me estás mandando a una lista de ocho vídeos para que adivine cuál es el de esta fase. Eso no lo voy a hacer.
>
> > [!tip] 💡 Escribe con tus palabras, no copies lo que yo diga
> > El apartado **"Dudas"** no es para rellenar: es lo que me dice en qué tengo que insistir. Si lo dejas vacío siempre, o no te estás enterando de nada o no te estás enterando de que no te enteras.

> [!warning] 7. Por qué se graba TODO (y desde el principio)
> Regla de oro del curso: **una práctica que no se graba, no cuenta.** Y se graba **de principio a fin**, no un repaso al final:
> - Grabar todo el proceso demuestra que **lo has hecho tú** y me deja ver **cómo** lo haces (dónde dudas, dónde te atascas).
> - Por eso **primero te preparas** (te lees el procedimiento) y **luego grabas** del tirón: así el vídeo sale limpio y no lleno de "espera, que no me acuerdo".
> - Cada fase se graba **una sola vez**, en el sitio que le toca: las 0.1–0.4 se hacen **en el centro** (montas el equipo del cole), y montar el equipo de **casa** es la **Fase 0.5.1**. Así no repites lo mismo dos veces.

### 📖 Diccionario de Conceptos Clave

> [!quote] Terminología que usaremos todo el curso
> - **Obsidian:** programa para tomar notas en ficheros de texto (Markdown).
> - **Bóveda (vault):** la carpeta del disco que Obsidian gestiona. La nuestra: `Boveda_SOR`.
> - **Markdown (`.md`):** formato de texto simple para escribir notas con títulos, listas, etc.
> - **Apuntes:** lo que escribes tú (carpeta `00_Apuntes/`). Se corrige.
> - **Práctica:** el material Boochan que te doy y sobre el que trabajas (carpeta `01_Practicas/`).
> - **Bloque:** cada parte grande del curso, numerada por mí (Bloque 0 — Prerrequisitos, Bloque 1 — Entorno…). Tus carpetas de apuntes se llaman igual.
> - **Entrada:** el fichero de notas de **un día concreto** de clase.
> - **OBS:** programa para **grabar la pantalla** mientras haces la práctica.
> - **Playlist:** una lista de reproducción de YouTube donde agrupas tus vídeos. La de este bloque: `B0_Prerrequisitos`.
> - **Timestamp:** una marca de tiempo (`mm:ss`) en la descripción del vídeo que salta a un momento concreto (cada paso).
> - **Tarea (de Teams):** el sitio donde se **entrega**. La doy de alta yo, te llega notificación y tiene fecha límite. La playlist organiza tus vídeos; **la tarea es la entrega**. No es lo mismo.
> - **OneDrive:** el disco en la nube de Microsoft. **Ojo:** aquí NO guardamos la bóveda (se explica abajo).

---

### 🛠️ Procedimiento Práctico

> [!danger] ⚠️ LÉEME ANTES DE EMPEZAR: la bóveda NO va en OneDrive
> Es muy tentador guardar la carpeta dentro de OneDrive "para tenerla en la nube". **No lo hagas.** Más adelante usaremos **Git** para enviar tus apuntes por Internet, y Git y OneDrive **se pelean** por los mismos ficheros: se corrompen las carpetas ocultas del control de versiones y aparecen "copias en conflicto" que lo estropean todo.
> - **La bóveda va en una carpeta LOCAL del equipo**, no dentro de OneDrive.
> - Tu "copia en la nube" será **GitHub** (lo montamos en la Fase 0.2), no OneDrive.
> - Si no sabes dónde está tu carpeta de OneDrive, pregúntame antes de crear la bóveda.

> [!example] 🎬 Paso previo (UNA sola vez, no se graba): monta tu canal de vídeo
> Necesitas un sitio donde subir todos los vídeos del curso. Esto se hace **una vez** y sirve para todas las fases:
> 1. Crea una **cuenta de Gmail** parecida a tu correo del instituto. Ejemplo: si tu correo es `luis.garcia@alu.edu.gva.es`, crea algo como `luis.garcia.smr@gmail.com` (que se te reconozca).
> 2. Con esa cuenta, entra en **YouTube** y crea tu **canal**.
> 3. Crea una **playlist** llamada exactamente **`B0_Prerrequisitos`**. Ahí subirás los vídeos de las fases 0.1 a 0.6.
> 4. Sube los vídeos como **"No listado"** (unlisted): así solo quien tenga el enlace (yo) los ve, no salen en búsquedas.
>
> > [!tip] 💡 Esta cuenta te vale para todo el curso
> > Cuando más adelante hagamos el proyecto Boochan y el curso de Git, crearás **más playlists** (una por bloque) en este mismo canal. Guárdate bien el usuario y la contraseña.

> [!example] Paso 0: Prepárate (todavía SIN grabar)
> Antes de darle a grabar, deja todo listo para que el vídeo salga del tirón: (este procedimiento se explica CLARAMENTE AHORA, en el resto de procedimiento se dará por entendido)
> 1. **Comprueba lo instalado:** busca **Obsidian** y **OBS Studio** en el menú de aplicaciones. Si **falta alguno**, avísame: **no intentes instalarlo tú** ni bajar versiones "portables" no autorizadas.
> 2. **Léete el procedimiento entero** (los pasos 1 a 6 de abajo): así, cuando grabes, sabrás lo que viene y no te quedarás en blanco. Este procedimiento tiene **6 pasos** que se graban.
> 3. **Ten OBS a mano** y una pestaña del navegador abierta con tu **Teams** o tu **correo `@alu.edu.gva.es`** (la usarás para presentarte).

> [!example] Paso 1: Arranca la grabación y preséntate
> 1. Abre **OBS Studio** y pulsa **"Iniciar grabación"**. A partir de aquí, **todo queda grabado**.
> 2. **Preséntate en voz alta:** *"Hola y bienvenidos. Me llamo [tu nombre], soy alumno de 2.º SMR, y en este vídeo voy a explicar la Fase 0.1 — Metodología y estructura de la bóveda."*
> 3. **Demuestra que eres tú:** cambia a la pestaña de tu **Teams** o tu **correo `@alu.edu.gva.es`** y enséñalo 2-3 segundos, para que se vea tu nombre.
> 4. Di **qué vas a hacer:** *"Voy a crear mi bóveda de Obsidian y su estructura de carpetas, siguiendo el procedimiento de esta fase."*

> [!example] Paso 2: Comprueba tu carpeta `Documentos` (grabando)
> La bóveda va **dentro de tu carpeta de usuario**: ahí tienes permisos siempre, tanto en el Windows del centro como en tu Linux. Pero antes de crear nada hay que comprobar **una cosa**, y es importante:
> 1. Abre el **Explorador de archivos** (Windows) o el **gestor de archivos** (Linux) y ve a tu carpeta **`Documentos`**.
> 2. **Mira el icono que tiene al lado, y dilo en voz alta:**
>
> | Lo que ves | Qué significa | Qué haces |
> | :--- | :--- | :--- |
> | Una **nube ☁️** (o pone "OneDrive" en la barra de direcciones) | Tu `Documentos` **está dentro de OneDrive**. No vale. | Sal de ahí y usa **directamente tu carpeta de usuario**: `C:\Users\TU-USUARIO\` (Windows) o `/home/tu-usuario/` (Linux) |
> | Una **carpeta normal**, sin nube | Es local. Perfecta. | Trabajas dentro de `Documentos` |
>
> 3. **Crea ahí una carpeta llamada `SOR`** (en `Documentos` o en tu carpeta de usuario, según lo que te haya salido). Dentro de ella irá la bóveda.
>
> > [!tip] 💡 ¿Por qué te hago mirar esto?
> > Porque en muchos equipos del centro OneDrive "se lleva" la carpeta `Documentos` a la nube sin avisar. Y Git (que montamos en la Fase 0.2) y OneDrive **se pelean** por los mismos ficheros: aparecen "copias en conflicto" y se corrompe el control de versiones. Diez segundos de comprobación ahora te ahorran una tarde de líos en noviembre.

> [!example] Paso 3: Crea la bóveda y **apunta tu ruta** (grabando y explicando)
> Explicando en voz alta lo que haces:
> 1. Abre **Obsidian** y pulsa **`Create new vault`** (Crear nueva bóveda).
> 2. En **`Vault name`** escribe exactamente: **`Boveda_SOR`**
> 3. En **`Location`** pulsa **`Browse`** y elige la carpeta **`SOR`** que acabas de crear en el paso anterior.
> 4. Pulsa **`Create`**. Obsidian se abre con la bóveda vacía `Boveda_SOR`.
>
> > [!important] 📌 APÚNTATE TU RUTA — la vas a necesitar en todas las fases
> > Según lo que te haya salido en el Paso 2, tu bóveda está en **una** de estas:
> >
> > | | Ruta |
> > | :--- | :--- |
> > | Windows, `Documentos` local | `C:\Users\TU-USUARIO\Documents\SOR\Boveda_SOR` |
> > | Windows, `Documentos` en OneDrive | `C:\Users\TU-USUARIO\SOR\Boveda_SOR` |
> > | Linux, `Documentos` | `/home/tu-usuario/Documentos/SOR/Boveda_SOR` |
> > | Linux, sin `Documentos` | `/home/tu-usuario/SOR/Boveda_SOR` |
> >
> > **Anótala en un papel o en una nota.** No pasa nada por que la tuya no sea igual que la de tu compañero: a partir de la Fase 0.3 **no vas a teclear la ruta nunca** — abrirás la terminal directamente sobre la carpeta (te lo explico allí). Pero saber dónde vive tu bóveda es lo mínimo que se le pide a un técnico.

> [!example] Paso 4: Crea la estructura de carpetas y compruébala (grabando)
> Crea esta estructura **exacta** (nombres **sin tildes ni espacios**), explicando cada carpeta:
> ```
> Boveda_SOR/
> ├── 00_Apuntes/
> │   ├── Trimestre_1/
> │   │   └── B0_Prerrequisitos/
> │   ├── Trimestre_2/
> │   └── Trimestre_3/
> └── 01_Practicas/
> ```
> **Cómo:** clic derecho en el panel izquierdo → **`New folder`** → escribe el nombre **tal cual**. Para crear una carpeta **dentro** de otra, clic derecho **sobre la carpeta padre**. Créalas en este orden: `00_Apuntes` → dentro `Trimestre_1/2/3` → dentro de `Trimestre_1` la `B0_Prerrequisitos` → y `01_Practicas` en la raíz.
>
> Al terminar, **recorre la estructura con el ratón** y compruébala en voz alta: *"Aquí están mis apuntes por trimestres, aquí el bloque 0 de prerrequisitos, y aquí la carpeta de prácticas."*
>
> > [!warning] ⚠️ El nombre importa
> > No pongas `Apuntes` en vez de `00_Apuntes`, ni `Trimestre 1` con espacio, ni `Bloque1`. Si cada uno lo escribe a su manera, es imposible corregir a 20 personas. **Cópialo carácter a carácter.**

> [!example] Paso 5: Crea tu PRIMERA entrada de apuntes (grabando)
> La carpeta `B0_Prerrequisitos` está vacía, y una carpeta vacía no son apuntes. Vamos a dejarla estrenada:
> 1. En Obsidian, **clic derecho sobre `B0_Prerrequisitos`** → **`New note`**.
> 2. **Nómbrala como la fase**, con el formato del apartado 5: `fase-0.1-metodologia-y-estructura`.
> 3. **Pega la plantilla** (apartado 6 del fundamento) y rellena **solo la cabecera**: `Fecha`, `Bloque` y `Fase / práctica`.
> 4. **Recorre los apartados vacíos con el ratón** y di en voz alta qué vas a poner en cada uno. Eso es lo que quiero ver: que sabes para qué sirve cada sección.
> 5. **Guarda** y comprueba que el fichero aparece dentro de `B0_Prerrequisitos`.
>
> > [!important] ⏱️ NO te grabes escribiendo los apuntes
> > En el vídeo la entrada tiene que **existir y verse**, con su nombre y su estructura. **Nada más.** Escribir el contenido lo haces **después**, sin grabar y a tu ritmo, mientras dure la fase.
> > Si te grabas redactando, el vídeo se te va a cuarenta minutos y nadie lo va a ver — ni yo. **Cinco minutos.**
>
> > [!note] 📌 Esto todavía NO está en GitHub
> > Tu entrada existe solo en este ordenador. Para que yo pueda verla hace falta Git, y eso es la **Fase 0.2**. No te preocupes ahora: escríbela bien y déjala ahí. En la **Fase 0.3** la subiremos junto con las de las fases que hayas hecho para entonces.

> [!example] Paso 6: Cierra el vídeo, nómbralo y súbelo a YouTube
> 1. **Detén la grabación** en OBS y localiza el archivo del vídeo.
> 2. **Renombra el archivo** (el `.mkv` o `.mp4` que ha dejado OBS) a `B0.1 - Metodologia y estructura`. Con **guion normal y sin tildes**: es un nombre de fichero, no un título.
> 3. **Súbelo a YouTube**, a tu playlist **`B0_Prerrequisitos`**, como **"No listado"**. Ahí sí, el **título del vídeo** en YouTube va tal cual: `B0.1 · Metodología y estructura`.
> 4. En la **descripción**, añade los **timestamps** (uno por paso). Ejemplo:
>    ```
>    00:00 Presentacion
>    00:20 Paso 2 - Comprobar la carpeta Documentos
>    00:50 Paso 3 - Crear la boveda Boveda_SOR
>    01:30 Paso 4 - Crear la estructura de carpetas
>    02:40 Paso 5 - Primera entrada de apuntes
>    04:10 Paso 6 - Repaso final
>    ```
>    *(Pon los minutos:segundos reales de tu vídeo.)*
> 5. **Comprueba la duración:** debe rondar los **5 minutos**. Si se te va mucho, ve más al grano; los timestamps son obligatorios de todos modos.
> 6. **Copia el enlace del vídeo** (`Compartir` → `Copiar enlace`) y **pégalo en la entrada que escribiste en el Paso 5**, en el apartado `Enlace al vídeo explicativo`. Ahí es donde vive, no en un papel.
>
> > [!important] 📤 Ojo: subir el vídeo NO es entregar
> > Esto es lo que más confunde el primer día, así que léelo dos veces. Hay **tres** sitios distintos y cada uno tiene su trabajo:
> >
> > | | Qué es | Para qué |
> > | :--- | :--- | :--- |
> > | **La playlist `B0_Prerrequisitos`** | Organización tuya. TODOS los vídeos del bloque van dentro, siempre. | Que no se te pierdan |
> > | **Tu entrada de apuntes** | Donde pegas **el enlace de ESE vídeo** y contestas las preguntas. | Que yo sepa qué has hecho y qué has entendido |
> > | **La tarea de Teams** | **La entrega.** La doy de alta yo, con notificación y fecha límite. | Poner nota |
> >
> > **Hoy no se entrega nada todavía**, porque tus apuntes aún no están en Internet: eso lo montamos en la Fase 0.3. Cuando llegue el momento abriré la tarea en Teams y te avisará sola.
> >
> > Tú, hoy: **graba, sube el vídeo a la playlist y pega su enlace en tu entrada.** Nada más.
>
> > [!success] ✅ La Fase 0.1 está completa cuando…
> > Tienes la bóveda `Boveda_SOR` con su estructura exacta, **tu primera entrada escrita** dentro de `B0_Prerrequisitos/`, y el vídeo subido a tu playlist `B0_Prerrequisitos` (con presentación al principio y timestamps en la descripción), **y su enlace pegado dentro de esa entrada**, junto con las respuestas a las Preguntas Críticas.

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Tabla de Troubleshooting (¿Algo no funciona?)
> | Problema | Causa Probable | Solución Sugerida |
> | :--- | :--- | :--- |
> | No encuentro Obsidian / OBS en el equipo. | No están instalados o tienen otro nombre en el menú. | Avisa al profesor. No los instales tú: dependemos de Consellería. |
> | OBS no graba / se ve la pantalla en negro. | Falta seleccionar la fuente de captura de pantalla. | En OBS, en "Fuentes" añade una **"Captura de pantalla / Display Capture"**. Si sigue en negro, avísame. |
> | No se me oye en el vídeo. | El micrófono no está como fuente de audio en OBS. | En OBS añade "Captura de entrada de audio" (micrófono) y comprueba el nivel. |
> | El vídeo se va de 5 minutos. | Te has enrollado o repites cosas. | Prepárate mejor antes de grabar (Paso 0). Los timestamps son obligatorios igualmente. |
> | El profesor me dice que no ve mi vídeo. | Lo subiste como "No listado" y no le pasaste el enlace de la playlist. | Playlist → `Compartir` → `Copiar enlace` → mándamelo por Teams. Si lo subiste como **"Privado"** por error, cámbialo a **"No listado"**: en privado no lo veo ni con el enlace. |
> | No me deja crear la carpeta con ese nombre. | Has dejado un espacio al final, o un carácter raro. | Bórrala y créala de nuevo copiando el nombre exacto, sin espacios. |
> | Creé la bóveda dentro de OneDrive sin querer. | Tu `Documentos` estaba redirigido a OneDrive y no lo viste (Paso 2). | Cierra Obsidian, mueve la carpeta `SOR` entera a tu carpeta de usuario (`C:\Users\TU-USUARIO\`) y reábrela con `Open folder as vault`. Ante la duda, pregúntame. |
> | No sé si mi `Documentos` está en OneDrive o no. | El icono de nube no siempre se ve bien. | Entra en `Documentos` y mira la **barra de direcciones** del Explorador: si aparece `OneDrive` en la ruta, está en la nube. Si dudas, tira por la carpeta de usuario: esa nunca falla. |

> [!help] Preguntas Críticas (Autoevaluación del alumno)
> 1. ¿Qué es una bóveda de Obsidian? ¿Es un formato especial o una carpeta normal?
> 2. ¿Qué diferencia hay entre la carpeta `00_Apuntes/` y la carpeta `01_Practicas/`?
> 3. ¿Por qué **no** guardamos la bóveda dentro de OneDrive?
> 4. ¿En qué momento del vídeo te presentas y demuestras que eres tú: al principio o al final?
> 5. 🔬 **Reto:** sin mirar la guía, dibuja en un papel el árbol de carpetas de la bóveda. Luego compáralo con Obsidian: ¿te faltaba alguna?

---

### ✅ Checklist Final de la Fase 0.1

- [ ] Canal de YouTube creado con la playlist `B0_Prerrequisitos`.
- [ ] Obsidian y OBS comprobados en el equipo (instalados por Consellería).
- [ ] Carpeta `Documentos` comprobada (¿nube o local?) y bóveda `Boveda_SOR` creada en una ruta **local** (no en OneDrive).
- [ ] **Tu ruta apuntada** en un papel o una nota.
- [ ] Estructura de carpetas exacta: `00_Apuntes/` (con `Trimestre_1/2/3` y `B0_Prerrequisitos` en T1) + `01_Practicas/`.
- [ ] Vídeo grabado **de principio a fin**, con presentación e identidad al inicio.
- [ ] Vídeo nombrado `B0.1 · Metodología y estructura` y subido a la playlist `B0_Prerrequisitos`.
- [ ] Timestamps en la descripción (uno por paso).
- [ ] **Primera entrada escrita** en `B0_Prerrequisitos/`, con nombre `fase-0.1-metodologia-y-estructura.md` y la estructura obligatoria.
- [ ] **Enlace del vídeo pegado en tu entrada**, en el apartado `Enlace al vídeo explicativo`.
- [ ] **Preguntas Críticas contestadas** en tu entrada (el 🔬 Reto es voluntario).
- [ ] Grabada **🏫 en el centro**.

> **Siguiente paso:** Fase 0.2 — Crear tu cuenta de **GitHub** y configurar **Git** en el equipo, para poder enviarme tus apuntes por Internet y que yo pueda corregirlos.
