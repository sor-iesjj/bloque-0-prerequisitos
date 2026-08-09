## 📙 Fase 0.1.c: Procedimiento

### Montar la bóveda, grabando de principio a fin

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0.1 — parte c de c]**
>
> 🧭 **Índice de la fase:** [[Fase_0.1_Metodologia_y_Estructura]]
>
> **📍 Cuándo se lee:** **entera y antes de grabar.** Son **6 pasos** grabados.
> **⏱️ El vídeo:** ~5 minutos.

---

> [!danger] 🛑 Antes de abrir esto, léete las partes a y b
> - **[[Fase_0.1.a_Obsidian_y_la_Boveda|Parte a]]** — qué es una bóveda y por qué las carpetas se llaman así.
> - **[[Fase_0.1.b_El_Sistema_de_Apuntes|Parte b]]** — el nombre y la plantilla de la entrada. **La vas a necesitar en el Paso 5.**
>
> Si vienes directo aquí, en el Paso 5 te vas a quedar parado buscando la plantilla con OBS grabando.

---

> [!danger] ⚠️ LÉEME ANTES DE EMPEZAR: la bóveda NO va en OneDrive
> Es muy tentador guardar la carpeta dentro de OneDrive *"para tenerla en la nube"*. **No lo hagas.**
>
> Más adelante usaremos **Git** para enviar tus apuntes por Internet, y Git y OneDrive **se pelean** por los mismos ficheros: se corrompen las carpetas ocultas del control de versiones y aparecen "copias en conflicto" que lo estropean todo.
>
> - **La bóveda va en una carpeta LOCAL del equipo**, no dentro de OneDrive.
> - Tu "copia en la nube" será **GitHub** (lo montamos en la **Fase 0.2**), no OneDrive.
> - Si no sabes dónde está tu carpeta de OneDrive, **pregúntame antes de crear la bóveda**.

---

## **🎬 PASO PREVIO — monta tu canal de vídeo**

> [!example] UNA sola vez en todo el curso. Esto NO se graba
> Necesitas un sitio donde subir todos los vídeos del curso. Se hace **una vez** y sirve para todas las fases:
>
> 1. Crea una **cuenta de Gmail** parecida a tu correo del instituto. Ejemplo: si tu correo es `luis.garcia@alu.edu.gva.es`, crea algo como `luis.garcia.smr@gmail.com` (que se te reconozca).
> 2. Con esa cuenta, entra en **YouTube** y crea tu **canal**.
> 3. Crea una **playlist** llamada exactamente **`B0_Prerrequisitos`**. Ahí subirás los vídeos de las fases 0.1 a 0.7.
> 4. Sube los vídeos como **"No listado"** (unlisted): así solo quien tenga el enlace (yo) los ve, y no salen en búsquedas.
>
> > [!tip] 💡 Esta cuenta te vale para todo el curso
> > Más adelante crearás **más playlists** en este mismo canal —una por bloque y una por curso: `B0_Curso_Git`, `B0_Curso_Shell`, `B1_Entorno`, `B2_Ubuntu_Local`…— siempre con el nombre del bloque. **Guárdate bien el usuario y la contraseña.**

---

## **🛠️ EL PROCEDIMIENTO — 6 pasos grabados**

> [!example] Paso 0: Prepárate (todavía SIN grabar)
> Antes de darle a grabar, deja todo listo para que el vídeo salga del tirón. *(Este paso previo se explica en detalle aquí; en el resto de procedimientos del curso se dará por sabido.)*
>
> 1. **Comprueba lo instalado:** busca **Obsidian** y **OBS Studio** en el menú de aplicaciones. Si **falta alguno**, avísame: **no intentes instalarlo tú** ni bajar versiones "portables" no autorizadas.
> 2. **Léete los 6 pasos de abajo enteros**: así, cuando grabes, sabrás lo que viene y no te quedarás en blanco.
> 3. **Ten a mano la [[Fase_0.1.b_El_Sistema_de_Apuntes|parte b]]**, que es de donde vas a copiar la plantilla en el Paso 5.
> 4. **Ten OBS a mano** y una pestaña del navegador abierta con tu **Teams** o tu **correo `@alu.edu.gva.es`** (la usarás para presentarte).

> [!example] Paso 1: Arranca la grabación y preséntate
> 1. Abre **OBS Studio** y pulsa **"Iniciar grabación"**. A partir de aquí, **todo queda grabado**.
> 2. **Preséntate en voz alta:** *"Hola y bienvenidos. Me llamo [tu nombre], soy alumno de 2.º SMR, y en este vídeo voy a explicar la Fase 0.1 — Metodología y estructura de la bóveda."*
> 3. **Demuestra que eres tú:** cambia a la pestaña de tu **Teams** o tu **correo `@alu.edu.gva.es`** y enséñalo 2-3 segundos, para que se vea tu nombre.
> 4. Di **qué vas a hacer:** *"Voy a crear mi bóveda de Obsidian y su estructura de carpetas, siguiendo el procedimiento de esta fase."*

> [!example] Paso 2: Comprueba tu carpeta `Documentos` (grabando)
> La bóveda va **dentro de tu carpeta de usuario**: ahí tienes permisos siempre, tanto en el Windows del centro como en tu Linux. Pero antes de crear nada hay que comprobar **una cosa**, y es importante:
>
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
> > Porque en muchos equipos del centro OneDrive "se lleva" la carpeta `Documentos` a la nube sin avisar. Y Git (que montamos en la Fase 0.2) y OneDrive **se pelean** por los mismos ficheros: aparecen "copias en conflicto" y se corrompe el control de versiones.
> >
> > **Diez segundos de comprobación ahora te ahorran una tarde de líos en noviembre.**

> [!example] Paso 3: Crea la bóveda y **apunta tu ruta** (grabando y explicando)
> Explicando en voz alta lo que haces:
>
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
> > **Anótala en un papel o en una nota.** No pasa nada por que la tuya no sea igual que la de tu compañero: a partir de la Fase 0.3 **no vas a teclear la ruta nunca** — abrirás la terminal directamente sobre la carpeta. Pero saber dónde vive tu bóveda es lo mínimo que se le pide a un técnico.

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
> La carpeta `B0_Prerrequisitos` está vacía, y una carpeta vacía no son apuntes. Vamos a estrenarla:
>
> 1. En Obsidian, **clic derecho sobre `B0_Prerrequisitos`** → **`New note`**.
> 2. **Nómbrala como la fase**, con el formato de la [[Fase_0.1.b_El_Sistema_de_Apuntes|parte b]]: `b0-0.1-metodologia-y-estructura`.
> 3. **Pega la plantilla** (también de la parte b) y rellena **solo la cabecera**: alumno, bloque, fase y fecha de inicio.
> 4. **Recorre los apartados vacíos con el ratón** y di en voz alta qué vas a poner en cada uno. Eso es lo que quiero ver: que sabes para qué sirve cada sección.
> 5. **Guarda** y comprueba que el fichero aparece dentro de `B0_Prerrequisitos`.
>
> > [!important] ⏱️ NO te grabes escribiendo los apuntes
> > En el vídeo la entrada tiene que **existir y verse**, con su nombre y su estructura. **Nada más.** Escribir el contenido lo haces **después**, sin grabar y a tu ritmo, mientras dure la fase.
> >
> > Si te grabas redactando, el vídeo se te va a cuarenta minutos y nadie lo va a ver — ni yo. **Cinco minutos.**
>
> > [!note] 📌 Esto todavía NO está en GitHub
> > Tu entrada existe solo en este ordenador. Para que yo pueda verla hace falta Git, y eso es la **Fase 0.2**. No te preocupes ahora: escríbela bien y déjala ahí. En la **Fase 0.3** la subiremos junto con las de las fases que hayas hecho para entonces.

> [!example] Paso 6: Cierra el vídeo, nómbralo y súbelo a YouTube
> 1. **Detén la grabación** en OBS y localiza el archivo del vídeo.
> 2. **Renombra el archivo** (el `.mkv` o `.mp4` que ha dejado OBS) a `B0.1 - Metodologia y estructura`. Con **guion normal y sin tildes**: es un nombre de fichero, no un título.
> 3. **Súbelo a YouTube**, a tu playlist **`B0_Prerrequisitos`**, como **"No listado"**. Ahí sí, el **título del vídeo** en YouTube va tal cual: `B0.1 · Metodología y estructura`.
>
>    > [!warning] ⚠️ YouTube te pone de título el nombre del fichero. **Cámbialo tú**
>    > Al subirlo verás `B0.1 - Metodologia y estructura` en la casilla del título — lo ha copiado del `.mkv`. **Bórralo y escribe el bueno**, con el punto medio (`·`) y las tildes.
>    >
>    > De aquí salen la mayoría de los vídeos mal nombrados: nadie los nombra mal, simplemente **nadie toca lo que YouTube rellenó solo**.
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
> 6. **Copia el enlace del vídeo** (`Compartir` → `Copiar enlace`) y **pégalo en la entrada que escribiste en el Paso 5**, en el apartado `🔗 Enlaces`. Ahí es donde vive, no en un papel.
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

---

## **🚩 SI ALGO NO FUNCIONA**

> [!bug] Tabla de problemas frecuentes
> | Problema | Causa probable | Solución |
> | :--- | :--- | :--- |
> | No encuentro Obsidian / OBS en el equipo. | No están instalados o tienen otro nombre en el menú. | Avisa al profesor. **No los instales tú**: dependemos de Consellería. |
> | OBS no graba / se ve la pantalla en negro. | Falta seleccionar la fuente de captura de pantalla. | En OBS, en "Fuentes", añade una **"Captura de pantalla / Display Capture"**. Si sigue en negro, avísame. |
> | No se me oye en el vídeo. | El micrófono no está como fuente de audio en OBS. | En OBS añade "Captura de entrada de audio" (micrófono) y comprueba el nivel. |
> | El vídeo se va de 5 minutos. | Te has enrollado o repites cosas. | Prepárate mejor antes de grabar (Paso 0). Los timestamps son obligatorios igualmente. |
> | El profesor me dice que no ve mi vídeo. | Lo subiste como "No listado" y no le pasaste el enlace. | Playlist → `Compartir` → `Copiar enlace` → mándamelo por Teams. Si lo subiste como **"Privado"** por error, cámbialo a **"No listado"**: en privado no lo veo ni con el enlace. |
> | No me deja crear la carpeta con ese nombre. | Has dejado un espacio al final, o un carácter raro. | Bórrala y créala de nuevo copiando el nombre exacto, sin espacios. |
> | Creé la bóveda dentro de OneDrive sin querer. | Tu `Documentos` estaba redirigido a OneDrive y no lo viste (Paso 2). | Cierra Obsidian, mueve la carpeta `SOR` entera a tu carpeta de usuario (`C:\Users\TU-USUARIO\`) y reábrela con `Open folder as vault`. Ante la duda, pregúntame. |
> | No sé si mi `Documentos` está en OneDrive o no. | El icono de nube no siempre se ve bien. | Entra en `Documentos` y mira la **barra de direcciones** del Explorador: si aparece `OneDrive` en la ruta, está en la nube. Si dudas, tira por la carpeta de usuario: **esa nunca falla**. |

---

> [!success] ✅ La Fase 0.1 está completa cuando…
> Tienes la bóveda `Boveda_SOR` con su estructura exacta, **tu primera entrada escrita** dentro de `B0_Prerrequisitos/`, y el vídeo subido a tu playlist `B0_Prerrequisitos` (con presentación al principio y timestamps en la descripción), **y su enlace pegado dentro de esa entrada**, junto con las respuestas a las Preguntas Críticas.
>
> **Vuelve al [[Fase_0.1_Metodologia_y_Estructura|índice de la fase]]** y repasa el checklist final antes de darla por cerrada.
