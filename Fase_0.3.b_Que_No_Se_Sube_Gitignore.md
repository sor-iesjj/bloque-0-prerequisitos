## 🚫 Fase 0.3.b: Qué NO se sube — el `.gitignore`

### Decidir qué queda fuera es tan importante como decidir qué entra

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~45 min · **Requisitos:** Fase 0.3 completa (tu repo `apuntes-sor-t1` funcionando).


> [!abstract] 📋 Qué se te evalúa en esta fase
> **RA.04**
>
> | Código | Criterio de evaluación |
> | :--- | :--- |
> | `CE.04.b` | Se han identificado los recursos del sistema que se van a compartir y en qué condiciones. |
>
> Los criterios están tomados literalmente del **RD 1691/2007** y de la programación del módulo.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin.
> 1. **Prepárate primero (sin grabar):** comprueba lo necesario, **léete el procedimiento entero** y **crea la entrada de apuntes de esta fase** en Obsidian: fichero `b0-0.3.b-gitignore.md` con la estructura del **Bloque 0 · Fase 0.1.b**, **vacía**. Rellenarla es cosa tuya, después.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a explicar la Fase 0.3.b — Qué no se sube: el `.gitignore`."* Y **muestra tu perfil de GitHub**. Di qué vas a hacer.
> 3. **Graba TODO**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Paso 1 — Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `B0.3.b · Qué no se sube, el gitignore` y súbelo a tu playlist **`B0_Prerrequisitos`** (No listado).
> 6. **~5 min.** Se graba en **🏫 el centro**.
> 7. **La entrega va por la TAREA de Teams.** Cuando toque, abriré una tarea que cubrirá **esta fase y otras**; te llegará notificación.
> 8. **El enlace del vídeo va DENTRO de tu entrada de apuntes**, en el apartado `🔗 Enlaces`.

---

### 🎯 Objetivos de la fase

- [ ] Explicar por qué **no todo** lo que hay en una carpeta debe subirse a GitHub.
- [ ] Crear un fichero **`.gitignore`** y entender su sintaxis básica.
- [ ] Comprobar con `git status` que Git **deja de ver** lo ignorado.
- [ ] Saber qué hacer cuando ya has subido algo que no debías — y por qué eso **no se arregla del todo**.

---

### 🎯 ¿Dónde Estamos?

> [!info] El Punto de Partida
> Tienes tu repo `apuntes-sor-t1` funcionando y ya has hecho varios `push`. Hasta ahora has usado `git add .`, que significa **"sube todo lo que haya"**. Y ha funcionado porque en esa carpeta solo hay ficheros `.md` pequeños.

> [!warning] El Problema
> Un martes grabas la práctica con OBS y, sin pensarlo, guardas el vídeo dentro de la carpeta de apuntes. Luego haces lo de siempre:
> ```bash
> git add .
> git commit -m "Apuntes de hoy"
> git push
> ```
> Y ese `git add .` acaba de meter **un fichero de 800 MB** en tu repositorio. Lo que pasa a partir de ahí depende del tamaño, y conviene que sepas distinguirlo:
>
> | El fichero pesa | Qué hace GitHub | Cómo te enteras |
> | :--- | :--- | :--- |
> | **Más de 100 MB** *(tu vídeo)* | **Rechaza el `push` entero.** Es un límite duro, no un aviso | `remote: error: File … is 800.00 MB; this exceeds GitHub's file size limit of 100.00 MB` |
> | **Menos de 100 MB** *(80 MB, por ejemplo)* | **Lo acepta sin decir nada** | No te enteras. Hasta que el repo pesa un giga |
>
> **Y en los dos casos el commit ya está hecho en tu ordenador.** Ahí está la trampa:
>
> - Si te lo **rechazó**: el fichero se queda en tu historial local y **te bloquea todos los `push` siguientes**. Puedes borrarlo y hacer commit del borrado — da igual, el `push` seguirá fallando, porque Git intenta subir *también* el commit en el que lo añadiste.
> - Si te lo **aceptó**: peor todavía. Está en el historial **para siempre**, y todo el que clone tu repositorio se lo descarga.
>
> En ambos casos, sacarlo de verdad exige **reescribir el historial**, que es una operación fea y peligrosa.
>
> Eso le pasa a todo el mundo una vez. Vamos a evitar que te pase a ti.

> [!success] Objetivo de esta Fase
> Enseñarle a Git qué ficheros debe **ignorar por completo**, para que `git add .` deje de ser peligroso.

---

### 📚 Fundamento Teórico

> [!important] 1. Qué es el `.gitignore`
> Es **un fichero de texto normal**, llamado exactamente `.gitignore` (con el punto delante), que se coloca en la raíz de tu repositorio. Dentro escribes, **una por línea**, las cosas que Git debe fingir que no existen.
>
> Git lo lee **antes** de cada `git add` y `git status`. Lo que coincida con esas líneas **no aparecerá jamás** como pendiente de subir, ni aunque uses `git add .`.
>
> No borra nada: los ficheros siguen en tu disco. Simplemente **Git deja de mirarlos**.

> [!note] 2. Qué NO debe subirse nunca a un repositorio
> Esta es la parte que hay que entender, porque la regla vale para toda tu vida profesional:
>
> | Qué | Por qué no |
> | :--- | :--- |
> | **Vídeos, audio, imágenes pesadas** | Git guarda **cada versión entera** de cada fichero. Un vídeo de 800 MB modificado tres veces son 2,4 GB de historial |
> | **Contraseñas, claves, tokens** | **Lo más grave de todo.** Si subes una clave a un repo público, dala por robada: hay robots rastreando GitHub a todas horas buscándolas |
> | **Ficheros temporales del sistema** | `.DS_Store` (Mac), `Thumbs.db` (Windows). No aportan nada y ensucian |
> | **Configuración personal de programas** | La carpeta `.obsidian/`, ajustes de tu editor. Es *tuya*, no del proyecto |
> | **Lo que se puede regenerar** | Si un fichero se crea solo a partir de otros, no ocupes sitio con él |
>
> **La regla en una frase:** al repositorio va **lo que has escrito tú y no se puede recuperar de otro sitio**. Lo demás, fuera.

> [!danger] 3. El fallo nº1: llegar tarde
> `.gitignore` **solo funciona con lo que Git todavía no controla**. Si ya hiciste `commit` de un fichero, añadirlo al `.gitignore` **no lo saca**: Git ya lo tiene fichado y lo sigue vigilando.
>
> Y aunque lo borres y hagas commit del borrado, **el fichero sigue en el historial**: si llegó a subirse, quien clone tu repo se lo descargará igualmente, porque `git clone` trae **toda la historia**.
>
> Sacarlo de verdad exige reescribir el historial entero, que es una operación fea y peligrosa. **Por eso el `.gitignore` se escribe al principio, no cuando ya ha pasado.**

> [!example] Vocabulario de esta práctica
> - **`.gitignore`:** fichero con la lista de lo que Git debe ignorar.
> - **Untracked:** fichero que Git ve pero que aún no controla.
> - **Ignorado:** fichero que Git ni siquiera menciona.
> - **`*`:** comodín. `*.mp4` significa *"cualquier fichero acabado en `.mp4`"*.
> - **`/`:** al final de una línea indica **carpeta**. `videos/` ignora la carpeta entera.

---

### 🛠️ Procedimiento Práctico

> [!example] Paso 0: Prepárate (todavía SIN grabar)
> **Léete el procedimiento entero** (tiene **5 pasos** grabados). Crea tu entrada de apuntes. Ten **OBS** listo y la terminal abierta en `Trimestre_1`.

> [!example] Paso 1: Arranca la grabación y preséntate
> Inicia la grabación en **OBS**, preséntate, enseña tu perfil de GitHub y di qué vas a hacer.

> [!example] Paso 2: Provoca el problema (sin llegar a subirlo)
> Vamos a simular el desastre **sin cometerlo**. Dentro de `Trimestre_1`:
> 1. Crea un fichero que imite un vídeo. En la terminal:
>    ```bash
>    echo "esto simula un video enorme" > practica_grabada.mp4
>    echo "clave secreta = 12345" > claves.txt
>    ```
> 2. Mira qué opina Git:
>    ```bash
>    git status
>    ```
>
> > [!danger] ⚠️ Mira bien la salida
> > Ahí están los dos, marcados como **`Untracked files`**. Git los ve y **está esperando a que le digas que los suba**.
> > Si ahora hicieras `git add .`, entrarían los dos. **Incluido el fichero de claves.** Dilo en voz alta: *"si hago `git add .` ahora mismo, subo mi contraseña a Internet."*

> [!example] Paso 3: Crea tu `.gitignore`
> En Obsidian **no puedes** crear ficheros que empiecen por punto, así que este va por terminal. Dentro de `Trimestre_1`:
> ```bash
> nano .gitignore
> ```
> *(En Windows con Git Bash, `nano` funciona igual. Para guardar: `Ctrl+O`, `Enter`, y `Ctrl+X` para salir.)*
>
> > [!tip] 💡 Si tu terminal te dice `nano: command not found`
> > Pasa en algunas instalaciones de Git para Windows. Tienes dos salidas, las dos válidas:
> > ```bash
> > notepad .gitignore     # Windows: abre el Bloc de notas
> > touch .gitignore       # crea el fichero vacío y lo editas donde quieras
> > ```
> > **Lo que importa es el contenido del fichero, no con qué lo escribas.**
>
> Escribe esto dentro:
> ```gitignore
> # Vídeos y audio — nunca al repositorio
> *.mp4
> *.mkv
> *.mov
> *.mp3
> *.wav
>
> # Nada que contenga claves o contraseñas
> *clave*
> *password*
> *.key
> *.pem
> id_*
> .env
>
> # Basura del sistema operativo
> .DS_Store
> Thumbs.db
>
> # Configuración personal de Obsidian
> .obsidian/
> ```
> Fíjate en las tres cosas que hay ahí: **comentarios** con `#`, **comodines** con `*`, y **carpetas** con `/` al final.

> [!example] Paso 4: Comprueba que funciona
> ```bash
> git status
> ```
>
> > [!success] ✅ Ahora los dos ficheros HAN DESAPARECIDO de la lista
> > `practica_grabada.mp4` y `claves.txt` **siguen estando en tu carpeta** —míralo en el Explorador— pero **Git ya no los ve**. Han dejado de existir para él.
> >
> > El único fichero nuevo que aparece es **`.gitignore`**, y ese **sí** hay que subirlo: es parte del proyecto y tiene que llegarle a cualquiera que clone tu repo.
>
> Súbelo:
> ```bash
> git add .gitignore
> git commit -m "Anadir gitignore: videos, claves y basura del sistema"
> git push
> ```
> Recarga GitHub: aparece el `.gitignore` **y no aparecen** ni el `.mp4` ni el `claves.txt`. Enséñalo en el vídeo.
>
> Cuando termines, borra los dos ficheros de prueba: `rm practica_grabada.mp4 claves.txt`

> [!example] Paso 5: Cierra el vídeo, nómbralo y súbelo
> Detén la grabación, nombra el vídeo `B0.3.b · Qué no se sube, el gitignore`, súbelo a la playlist `B0_Prerrequisitos` con **timestamps**:
> ```
> 00:00 Presentacion
> 00:25 Paso 2 - Creo los ficheros peligrosos y los ve git
> 01:30 Paso 3 - Escribo el gitignore
> 02:45 Paso 4 - Git ya no los ve, y subo el gitignore
> 04:00 Paso 5 - Repaso final
> ```

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | El fichero **sigue apareciendo** en `git status`. | Ya le habías hecho `commit` antes de ignorarlo. | `git rm --cached NOMBRE` (lo saca de Git **sin borrarlo de tu disco**) y luego `commit`. |
> | Obsidian no me deja crear `.gitignore`. | Es lo normal: Obsidian no crea ficheros que empiezan por punto. | Créalo desde la terminal con `nano`, como en el Paso 3. |
> | Guardé el `.gitignore` y no hace nada. | Lo has puesto en la carpeta equivocada. | Tiene que estar en **la raíz del repositorio** (`Trimestre_1`), junto al `.git`. Compruébalo con `ls -a`. |
> | No veo el `.gitignore` en el Explorador. | Los ficheros que empiezan por punto están **ocultos**. | En la terminal, `ls -a`. En el Explorador, activa "mostrar archivos ocultos". |
> | Ignoré una carpeta pero se sigue subiendo su contenido. | Te falta la barra final. | `videos/` con barra, no `videos`. |

> [!help] Preguntas Críticas (Autoevaluación del alumno)
> 1. Con tus palabras: ¿qué hace exactamente el `.gitignore`? ¿Borra ficheros?
> 2. ¿Por qué **el `.gitignore` sí se sube** al repositorio, si es un fichero de configuración?
> 3. Subes por error un fichero con una contraseña, te das cuenta al día siguiente y lo borras. **¿Está resuelto el problema? Explica por qué.**
> 4. Da **tres** ejemplos de ficheros que nunca subirías, cada uno por un motivo distinto.
> 5. ¿Qué diferencia hay entre un fichero **untracked** y uno **ignorado**?
> 6. 🔬 **Reto:** en tu repo `bloque-2-ubuntu-local` de la Fase 0.4, ¿qué pondrías en su `.gitignore`? Piensa qué generarás ahí durante el proyecto.

---

### ✅ Checklist Final de la Fase 0.3.b

- [ ] Sabes explicar qué hace el `.gitignore` y qué **no** hace.
- [ ] Ficheros de prueba creados y vistos como `Untracked` por Git.
- [ ] `.gitignore` creado en la **raíz del repositorio**, con comentarios, comodines y una carpeta.
- [ ] `git status` demostrado **antes y después**: los ficheros desaparecen de la lista.
- [ ] `.gitignore` subido a GitHub y comprobado que el `.mp4` y el `claves.txt` **no** están.
- [ ] Sabes por qué subir una clave por error **no se arregla borrándola**.
- [ ] Vídeo `B0.3.b · Qué no se sube, el gitignore` subido a la playlist, con timestamps.
- [ ] **Enlace del vídeo pegado en tu entrada de apuntes** de esta fase, con las respuestas.
- [ ] Grabada **🏫 en el centro**.

> [!summary] 🎓 Lo que te llevas de aquí
> Que **un repositorio no es una copia de seguridad de tu carpeta**. Es el sitio donde vive lo que has escrito tú y merece conservarse, y eso implica **decidir qué queda fuera**.
> La regla de las claves vale para siempre y no admite matices: **lo que sube a un repositorio, sube para quedarse.** Por eso se piensa antes, no después.

> **Siguiente paso:** Fase 0.4 — Bajar el material del curso: tus copias del Bloque 1 y de Boochan, y tres retos de recuperación.
