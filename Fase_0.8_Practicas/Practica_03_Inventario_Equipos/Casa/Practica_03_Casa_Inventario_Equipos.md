## B0.P03 · Casa · Inventario de equipos

### Una bóveda y un repositorio nuevos: el ciclo completo desde cero

> **Módulo:** SOR — Sistemas Operativos en Red · 2.º SMR  
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)  
> **Dónde:** casa · [Índice de la práctica](../00_Indice_Practica_03_Inventario_Equipos.md) · [Bloque 0 · Fase 0.8](../../../Fase_0.8_Practicas.md)  
> **Repaso:** [Bitácora · Bloque 0 · Fase 0.1.b](../../../Fase_0.1.b_El_Sistema_de_Apuntes.md)

> [!abstract] Tu misión
> Crear inventario de equipos desde cero, guardarlo en tres versiones y consultar la primera antes de regresar a main. Cerrarás después la bitácora en un cuarto commit documental. Usarás la bóveda `Boveda_Inventario_Casa` y el repositorio `sor-inventario-equipos-casa`. No clones ni continúes el trabajo del otro contexto.

> [!important] Lee la rúbrica antes de empezar
> Consulta [la rúbrica de Casa](Rubrica_B0_P03_Casa.md) y su [referencia pública en GitHub](https://github.com/sor-iesjj/bloque-0-prerequisitos/blob/main/Fase_0.8_Practicas/Practica_03_Inventario_Equipos/Casa/Rubrica_B0_P03_Casa.md). Indica los filtros de la bitácora, los puntos y las marcas de vídeo. La bitácora vale 2,5; el repositorio 3,5; el vídeo 4. Sin bitácora corregible o con menos del 70 % no se corrige lo demás. La rúbrica concreta cómo se mide. Conserva la referencia para revisar tu entrega.

> [!danger] Aislamiento antes de crear nada
> Elige una ubicación local independiente fuera de OneDrive y fuera de TODO árbol `SOR` o `Boveda_SOR`. Comprueba la ruta completa y todas sus carpetas superiores: `Boveda_Inventario_Casa` no puede estar bajo ninguna de ellas. Cole y Casa conservan bóveda, repositorio, tarea, playlist y bitácora propios. SOLO `01_Proyecto` llevará Git; la configuración de Obsidian y la grabación quedan fuera. Si el nombre elegido ya existe, detente: no reutilices ni borres trabajos anteriores.

## 0 · EL ENCARGO Y LOS DOS MAPAS

> [!info] Caso real
> Una empresa registra equipos en una hoja de texto compartida por entregas. Un equipo cambia de aula, otro entra en mantenimiento y finalmente se incorpora uno nuevo. Te encargan conservar cada entrega, justificar los cambios y añadir una ficha de mantenimiento. Todos los datos son ficticios: no uses números de serie, usuarios ni identificadores reales.

> [!abstract] Por qué necesitas Git
> Un historial es como conservar entregas fechadas de un expediente: permite comparar qué recibió el equipo en cada momento. Git guarda versiones localmente; GitHub conserva el remoto. Un commit no sube nada y un push no elige los archivos por ti. Primero revisas, luego preparas archivos concretos, guardas y subes. Aquí no se practica colaboración simultánea ni integración de ramas.

| Concepto | Uso en esta práctica |
| :--- | :--- |
| Bóveda | Carpeta que abres en Obsidian; contiene grabación y proyecto. |
| Repositorio | Solo 01_Proyecto, con historial en .git. |
| Índice | Selección de contenido preparado con git add para el próximo commit. |
| Commit | Versión local con un código real y un mensaje. |
| Origin | Nombre del remoto SSH de este proyecto en GitHub. |

> [!warning] El fallo número uno
> Confundir guardar, preparar y subir. Guardar en el editor cambia el disco; add prepara una selección; commit guarda una versión local; push la envía al remoto. .gitignore excluye archivos sin seguimiento: no retira archivos que ya se habían versionado. Git no conserva carpetas vacías.

### 0A · Solo las carpetas del inicio

Crea únicamente estas carpetas en H1. No crees todavía ningún fichero ni las carpetas tardías. `.obsidian/` la puede crear Obsidian automáticamente: no la crees a mano.

```text
Boveda_Inventario_Casa/
    00_Grabaciones/
    01_Proyecto/
    01_Proyecto/00_Bitacora/
    01_Proyecto/inventario/
```
### 0B · Cómo quedará al terminar

Este segundo mapa es para consultar la evolución; **no es una lista para crear ahora**. Las rutas se muestran relativas a la bóveda.

```text
Boveda_Inventario_Casa/
    .obsidian/                         (automática, H1; fuera de Git)
    00_Grabaciones/                    (H1; vídeo guardado en H8, fuera de Git)
    01_Proyecto/
        .git/                         (automática al inicializar, H3)
        .gitignore    (H2)
        00_Bitacora/b0-p03-casa-inventario-equipos.md    (H2)
        README.md    (H2; modificado en H6/H7)
        inventario/equipos.csv    (H2; modificado en H6/H7)
        inventario/mantenimiento/EQ02.md    (H7)
        inventario/criterios-estados.md    (H7)
        inventario/imagenes/equipo.png    (H7)
        inventario/videos/revision-01.mp4    (H7; local, ignorado)
        inventario/videos/revision-02.mp4    (H7; local, ignorado)
```
Los archivos iniciales que se modifican en H6/H7 conservan su ruta: no crees copias «final» ni «versión 2». Las carpetas nuevas de H7 se detallan en ese paso.

## 1 · GRABA Y PREPARA EL PROYECTO

> [!important] Grabación completa antes de H0
> 1. Prepara Obsidian, Git Bash, editor de texto, GitHub y OBS; lee la guía completa antes de empezar.
> 2. Empieza a grabar antes de H0, preséntate y muestra tu perfil de GitHub. En Casa explica con tu voz qué haces, por qué y qué compruebas; no basta con leer comandos.
> 3. Graba el proceso completo, incluidos fallos y correcciones, hasta la comprobación final en GitHub. No muestres claves privadas ni contraseñas; utiliza el correo de alumno o el noreply de GitHub configurado para Git.
> 4. Guarda la grabación fuera de Git en `00_Grabaciones`; no copies el fichero mientras OBS lo esté escribiendo.
> 5. Súbela como No listado con título `B0.P03 · Casa · Inventario de equipos`, a la playlist `B0.P03 · Casa · Inventario de equipos con Git y GitHub`, con las nueve marcas reales de H8. Cada playlist contiene un único vídeo de entrega de su contexto.

Prepara dos clips MP4 propios y reales para H7. Son recursos de prueba locales, no entregas. No uses el vídeo que OBS está grabando. La captura PNG se crea en H7.

> [!example] H0 · Comprueba Git, identidad y SSH antes del proyecto
> **Objetivo:** consultar el equipo y la cuenta que usarás, sin mostrar el contenido de las claves. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> git --version
> git config --global user.name
> git config --global user.email
> ls -l ~/.ssh/id_ed25519 ~/.ssh/id_ed25519.pub
> ssh -T git@github.com
> ```
>
> **Línea por línea:**
>
> - **1.** Muestra la versión instalada de Git.
> - **2.** Consulta el nombre global del autor: tiene que ser el tuyo.
> - **3.** Consulta el correo del autor; usa el correo de alumno o noreply autorizado.
> - **4.** Comprueba la existencia de la clave privada y pública, sin leerlas.
> - **5.** Prueba la autenticación SSH. Comprueba que el saludo identifica a TU usuario.
>
> **Resultado y condición para seguir:** Git disponible, identidad propia y SSH autenticado. GitHub puede terminar con código 1 porque no ofrece shell: mira el saludo. Ante cualquier fallo, detente y repasa [Git e identidad](../../../Fase_0.2.1_Cuenta_GitHub_y_Git.md) y [SSH](../../../Fase_0.2.2_Autenticacion_SSH.md) a través del índice del Bloque 0; no continúes ni generes claves nuevas por cada proyecto.

> [!example] H1 · Crea la bóveda y únicamente sus carpetas
> En Obsidian crea una bóveda nueva `Boveda_Inventario_Casa` en la ubicación local independiente ya comprobada. Verifica en el gestor de archivos la ruta completa y sus padres: fuera de OneDrive, SOR y Boveda_SOR. Crea solo el árbol 0A y muestra en pantalla que sus carpetas de trabajo están vacías. No inicialices Git en la bóveda. Configura OBS para guardar fuera de `01_Proyecto`; no muevas una grabación en curso.

> [!example] H2 · Crea la bitácora y los archivos iniciales
> Dentro de `01_Proyecto`, crea `00_Bitacora/b0-p03-casa-inventario-equipos.md`. Usa la plantilla única de [Bloque 0 · Fase 0.1.b](../../../Fase_0.1.b_El_Sistema_de_Apuntes.md): encabezado con nombre y apellidos, bloque, fase y fecha; y los siete apartados: Qué se pedía, Comandos y pasos importantes, Qué he hecho, Qué me ha fallado y cómo lo he resuelto, Respuestas a las preguntas, Enlaces y Dudas / a repasar.
>
> Escribe con tus palabras el objetivo. En Enlaces marca `Vídeo: pendiente` y `Playlist: pendiente` hasta que existan, e incorpora el repositorio cuando lo crees. No inventes incidencias: si no hubo errores o dudas, indícalo y explica qué comprobaste. Puedes tomar notas provisionales fuera del repositorio hasta cerrar H8 para mantener limpios los cambios de producto.
>
> En la raíz de `01_Proyecto`, crea `.gitignore` con este contenido:
>
> ```gitignore
> *.mp4
> *.mkv
> *.mov
> .DS_Store
> Thumbs.db
> ```
>
> Los patrones excluyen vídeos locales y archivos auxiliares del sistema. Los clips de H7 quedarán excluidos por *.mp4. El propio .gitignore sí se versiona.
>
> Todos los nombres se guardan sin .txt añadido. Usa el editor de texto para CSV y Bash; Obsidian para leer Markdown.
>
> **Crea `README.md` con el editor de texto y guarda:**
>
> ```markdown
> # Inventario de equipos
>
> Datos ficticios para el ejercicio.
>
> [Inventario](inventario/equipos.csv)
>
> Campos: id identifica el equipo; ubicacion indica dónde está; estado indica su disponibilidad.
> El CSV usa comas como separador y una fila por equipo.
> ```
>
> **Crea `inventario/equipos.csv` con el editor de texto y guarda:**
>
> ```csv
> id,ubicacion,estado
> EQ01,Aula-1,disponible
> EQ02,Aula-2,disponible
> ```
>
> Abre el CSV en el editor de texto y comprueba la cabecera de tres campos y las filas EQ01 y EQ02. Sigue el enlace de README en Obsidian; si Obsidian no previsualiza CSV, utiliza el editor de texto. Conserva UTF-8, separadores por comas y extensión `.csv`, sin `.txt` añadido. No lo guardes con separadores cambiados desde una hoja de cálculo.

## 2 · INICIALIZA GIT Y CONECTA TU REMOTO

> [!example] H3 · Comprueba la ruta antes de inicializar
> **Objetivo:** ver tu ubicación sin cambiar nada. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> pwd
> ```
>
> **Línea por línea:**
>
> - **1.** Muestra la ruta completa de la carpeta de trabajo.
>
> **Resultado y condición para seguir:** Debe terminar en `Boveda_Inventario_Casa/01_Proyecto`. Compara también TODOS sus padres: no puede estar bajo SOR, Boveda_SOR ni OneDrive. Si no coincide, detente; abre Git Bash en la carpeta correcta y repite esta comprobación. **No ejecutes el siguiente bloque hasta cumplirlo.**

> [!example] H3 · Inicializa solo la carpeta comprobada
> **Objetivo:** crear el historial local y fijar main como rama. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> git init
> git branch -M main
> git status
> ```
>
> **Línea por línea:**
>
> - **1.** Crea .git en 01_Proyecto, no en la raíz de la bóveda.
> - **2.** Nombra main la rama actual; -M fuerza ese nombre en este repositorio nuevo.
> - **3.** Consulta la rama y los archivos iniciales sin seguimiento.
>
> **Resultado y condición para seguir:** Rama main sin commits. Los archivos iniciales están sin seguimiento. No repitas init en las versiones siguientes.

> [!example] H4 · Crea tu repositorio GitHub vacío
> Crea en TU cuenta `sor-inventario-equipos-casa`. Debe estar vacío: sin README, licencia ni .gitignore generados por GitHub. Elige la visibilidad indicada por el profesor; si es privado, dale acceso con la cuenta facilitada en Teams. No clones otro contexto.
>
> Copia la dirección SSH del repositorio recién creado. **Antes del bloque sustituye TU-USUARIO por tu usuario real.**
>
> **Objetivo:** registrar y consultar el remoto; aún no se sube nada. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> git remote add origin git@github.com:TU-USUARIO/sor-inventario-equipos-casa.git
> git remote -v
> ```
>
> **Línea por línea:**
>
> - **1.** Registra la URL SSH como origin en este repositorio.
> - **2.** Muestra las URLs de consulta y envío del remoto.
>
> **Resultado y condición para seguir:** Origin debe ser TU cuenta y `sor-inventario-equipos-casa.git`. Si es otro, detente antes de cualquier push. No repitas remote add en las siguientes entregas.

## 3 · CONSERVA TRES VERSIONES

> [!info] Cómo leer las diferencias
> git status muestra nuevos, modificados y preparados. git diff compara disco e índice: antes de add, sin otros cambios preparados, ves lo que cambia respecto al último commit. Los archivos nuevos sin seguimiento no aparecen todavía en ese diff. git diff --cached compara el índice con el commit; muestra lo preparado. `--` separa opciones de rutas; `--stat` resume por archivos. Si aparece un visor, sal con la tecla q.

> [!example] H5 · Primera versión y primer push
> **Objetivo:** seleccionar cada archivo inicial, revisar, guardar y subir. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> git status
> git add .gitignore
> git add 00_Bitacora/b0-p03-casa-inventario-equipos.md
> git add README.md
> git add inventario/equipos.csv
> git status
> git diff --cached --stat
> git diff --cached
> ```
>
> **Línea por línea:**
>
> - **1.** Consulta los archivos sin seguimiento.
> - **2.** Prepara exclusivamente .gitignore; no crea un commit ni sube nada.
> - **3.** Prepara exclusivamente 00_Bitacora/b0-p03-casa-inventario-equipos.md; no crea un commit ni sube nada.
> - **4.** Prepara exclusivamente README.md; no crea un commit ni sube nada.
> - **5.** Prepara exclusivamente inventario/equipos.csv; no crea un commit ni sube nada.
> - **6.** Comprueba que la selección contiene solo los archivos iniciales.
> - **7.** Resume los archivos preparados para esta primera versión.
> - **8.** Lee el contenido preparado antes de guardarlo; sal con q si aparece visor.
>
> **PARA Y COMPRUEBA ANTES DE GUARDAR:** La selección debe contener únicamente `.gitignore`, `00_Bitacora/b0-p03-casa-inventario-equipos.md`, `README.md`, `inventario/equipos.csv`. En diff --cached revisa el contenido y en status los preparados: no puede haber archivos ajenos ni recursos ignorados. Si no coincide, no ejecutes el bloque siguiente. La consulta no guarda ni sube nada.
>
> **Objetivo del siguiente bloque:** guardar la selección ya comprobada y enviarla al remoto.
>
> ```bash
> git commit -m "Crear inventario inicial de equipos"
> git push -u origin main
> git status
> ```
>
> **Línea por línea:**
>
> - **1.** Crea la primera versión local con el mensaje exacto.
> - **2.** Sube main y fija origin/main como seguimiento; -u permite luego usar push sin repetir destino.
> - **3.** Consulta que estás en main y sin cambios pendientes.
>
> **Resultado y condición para seguir:** La primera versión está guardada y la subida termina sin errores. En GitHub abre README, `inventario/equipos.csv` y `00_Bitacora/b0-p03-casa-inventario-equipos.md`: deben tener el contenido inicial; la bitácora aún puede indicar el vídeo pendiente. Si algo falla, detente antes de editar la segunda versión.

> [!example] H6 · Modifica un archivo ya conocido
> En `inventario/equipos.csv`, cambia la ubicación de EQ01 de `Aula-1` a `Aula-3` y el estado de EQ02 de `disponible` a `mantenimiento`. No cambies el identificador, la cabecera ni la ubicación de EQ02. Guarda y comprueba las dos filas en el editor de texto.
>
> **Objetivo:** revisar la modificación conocida, preparar, guardar y subir. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> git status
> git diff -- inventario/equipos.csv
> git add inventario/equipos.csv
> git diff --cached
> git status
> ```
>
> **Línea por línea:**
>
> - **1.** Debe identificar el archivo modificado, sin otros cambios pendientes.
> - **2.** Compara disco con índice: - retira líneas y + incorpora las nuevas.
> - **3.** Prepara solo este cambio.
> - **4.** Revisa las líneas realmente preparadas; sal con q si aparece visor.
> - **5.** Comprueba que solo está preparado el archivo indicado.
>
> **PARA Y COMPRUEBA ANTES DE GUARDAR:** La selección debe contener únicamente `inventario/equipos.csv`. En diff --cached revisa el contenido y en status los preparados: no puede haber archivos ajenos ni recursos ignorados. Si no coincide, no ejecutes el bloque siguiente. La consulta no guarda ni sube nada.
>
> **Objetivo del siguiente bloque:** guardar la selección ya comprobada y enviarla al remoto.
>
> ```bash
> git commit -m "Actualizar ubicacion y estado de equipos"
> git push
> git status
> ```
>
> **Línea por línea:**
>
> - **1.** Guarda la segunda versión local con el mensaje exacto.
> - **2.** Envía los commits nuevos al seguimiento ya configurado.
> - **3.** Comprueba que no quedan cambios pendientes.
>
> **Resultado y condición para seguir:** EQ01 pasa a Aula-3 y EQ02 a mantenimiento; el diff debe identificar ambas filas modificadas. En GitHub abre el archivo modificado y comprueba esa segunda versión; no basta con ver estado limpio.

> [!example] H7 · A · Construye y comprueba la ampliación
> La empresa pide ampliar el producto. Crea ahora estas carpetas que no existían al inicio: `inventario/mantenimiento/`, `inventario/imagenes/`, `inventario/videos/`. Todas están dentro de `01_Proyecto`.
>
> **Crea `inventario/mantenimiento/EQ02.md` con el editor de texto y guarda:**
>
> ```markdown
> # Mantenimiento de EQ02
>
> Datos ficticios.
>
> Estado: mantenimiento.
> Motivo: revisión preventiva de ventilación.
> Actuación pendiente: inspección por el equipo técnico antes de devolverlo al uso.
>
> [Ver inventario](../equipos.csv)
> [Volver al índice](../../README.md)
> ```
>
> **Crea `inventario/criterios-estados.md` con el editor de texto y guarda:**
>
> ```markdown
> # Criterios de estado
>
> - disponible: el equipo está autorizado para su uso.
> - mantenimiento: está retirado del uso mientras soporte lo revisa.
>
> No marques disponible un equipo pendiente de revisión.
>
> [Volver al índice](../README.md)
> ```
>
> **Añade al final de `inventario/equipos.csv`, conservando lo anterior y guardando:**
>
> ```csv
> EQ03,Aula-1,disponible
> ```
>
> **Añade al final de `README.md`, conservando lo anterior y guardando:**
>
> ```markdown
> - [Ficha de EQ02](inventario/mantenimiento/EQ02.md)
> - [Criterios de estado](inventario/criterios-estados.md)
>
> ![Equipo de ejemplo](inventario/imagenes/equipo.png)
> ```
>
> Dibuja un equipo genérico y guarda una captura PNG propia sin datos personales como `inventario/imagenes/equipo.png`. Comprueba que es un PNG real; cambiar la extensión no convierte una imagen.
>
> Comprueba que el CSV tiene EQ01 en Aula-3, EQ02 en mantenimiento y EQ03 en Aula-1 disponible. En Obsidian comprueba la imagen y los enlaces de README y los enlaces de vuelta. La ficha de EQ02 y los criterios no deben contradecir el CSV.

> [!example] H7 · B · Incorpora clips reales de prueba
> Copia tus dos MP4 propios reales en `inventario/videos/`, con nombres `revision-01.mp4` y `revision-02.mp4`. Reprodúcelos para comprobar que son vídeos válidos. No basta cambiar una extensión ni crear archivos de texto con nombre MP4. No copies la grabación de OBS mientras está en curso. Estos clips locales no son entregas y no van a la playlist.

> [!example] H7 · C · Revisa antes de preparar
> **Objetivo:** distinguir nuevos y modificados, y confirmar las reglas de exclusión. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> git status --short --untracked-files=all
> git diff -- inventario/equipos.csv README.md
> git check-ignore -v inventario/videos/revision-01.mp4 inventario/videos/revision-02.mp4
> ```
>
> **Línea por línea:**
>
> - **1.** --short muestra dos columnas de estado y --untracked-files=all enumera cada fichero nuevo.
> - **2.** Compara las modificaciones del disco con el índice para esos archivos; los nuevos aún sin seguimiento no están en ese diff.
> - **3.** -v identifica la regla y su línea para cada archivo excluido; no activa la exclusión ni borra los archivos.
>
> **Resultado y condición para seguir:** Deben aparecer los archivos nuevos y modificados de la ampliación; los recursos locales ignorados no aparecen en status. Check-ignore debe justificar ambos recursos. Comprueba además en el gestor de archivos que siguen en el disco. Si un recurso aparece para subir o falta alguno, detente antes de preparar.

> [!info] Dos columnas que debes observar
> `??` identifica un archivo nuevo sin seguimiento. En las dos columnas de status, `A[ ]` significa nuevo preparado, `[ ]M` modificado sin preparar y `M[ ]` modificación preparada; `[ ]` representa un espacio, no texto literal. La columna izquierda corresponde al índice y la derecha al disco.

> [!example] H7 · D1 · Prepara exclusivamente inventario/mantenimiento/EQ02.md
> **Objetivo:** seleccionar un archivo y observar el cambio de estado. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> git add inventario/mantenimiento/EQ02.md
> git status --short --untracked-files=all
> ```
>
> **Línea por línea:**
>
> - **1.** Prepara solo el contenido actual de inventario/mantenimiento/EQ02.md.
> - **2.** Muestra lo preparado y lo que continúa esperando.
>
> **Resultado y condición para seguir:** `inventario/mantenimiento/EQ02.md` debe figurar como A[ ]: nuevo preparado. No crees un commit por cada add: forman una ampliación relacionada.

> [!example] H7 · D2 · Prepara exclusivamente inventario/criterios-estados.md
> **Objetivo:** seleccionar un archivo y observar el cambio de estado. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> git add inventario/criterios-estados.md
> git status --short --untracked-files=all
> ```
>
> **Línea por línea:**
>
> - **1.** Prepara solo el contenido actual de inventario/criterios-estados.md.
> - **2.** Muestra lo preparado y lo que continúa esperando.
>
> **Resultado y condición para seguir:** `inventario/criterios-estados.md` debe figurar como A[ ]: nuevo preparado. No crees un commit por cada add: forman una ampliación relacionada.

> [!example] H7 · D3 · Prepara exclusivamente inventario/imagenes/equipo.png
> **Objetivo:** seleccionar un archivo y observar el cambio de estado. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> git add inventario/imagenes/equipo.png
> git status --short --untracked-files=all
> ```
>
> **Línea por línea:**
>
> - **1.** Prepara solo el contenido actual de inventario/imagenes/equipo.png.
> - **2.** Muestra lo preparado y lo que continúa esperando.
>
> **Resultado y condición para seguir:** `inventario/imagenes/equipo.png` debe figurar como A[ ]: nuevo preparado. No crees un commit por cada add: forman una ampliación relacionada.

> [!example] H7 · D4 · Prepara exclusivamente inventario/equipos.csv
> **Objetivo:** seleccionar un archivo y observar el cambio de estado. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> git add inventario/equipos.csv
> git status --short --untracked-files=all
> ```
>
> **Línea por línea:**
>
> - **1.** Prepara solo el contenido actual de inventario/equipos.csv.
> - **2.** Muestra lo preparado y lo que continúa esperando.
>
> **Resultado y condición para seguir:** `inventario/equipos.csv` debe figurar como M[ ]: modificación preparada. No crees un commit por cada add: forman una ampliación relacionada.

> [!example] H7 · D5 · Prepara exclusivamente README.md
> **Objetivo:** seleccionar un archivo y observar el cambio de estado. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> git add README.md
> git status --short --untracked-files=all
> ```
>
> **Línea por línea:**
>
> - **1.** Prepara solo el contenido actual de README.md.
> - **2.** Muestra lo preparado y lo que continúa esperando.
>
> **Resultado y condición para seguir:** `README.md` debe figurar como M[ ]: modificación preparada. No crees un commit por cada add: forman una ampliación relacionada.

> [!danger] H7 · E · Condición antes del commit
> Revisa primero los tres comandos de consulta del bloque siguiente. El índice debe contener exactamente 5 archivos: `inventario/mantenimiento/EQ02.md`, `inventario/criterios-estados.md`, `inventario/imagenes/equipo.png`, `inventario/equipos.csv`, `README.md`. No debe haber recursos ignorados ni archivos ajenos. Si no coincide, detente antes de commit y push; no ejecutes el bloque entero de corrido.

> [!example] H7 · E · Revisa la selección, guarda y sube
> **Objetivo:** validar exactamente la ampliación antes de publicarla. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> git diff --cached --stat
> git diff --cached
> git status
> ```
>
> **Línea por línea:**
>
> - **1.** Resume los archivos del índice, incluidos los nuevos.
> - **2.** Muestra el contenido preparado; los cambios binarios pueden aparecer como resumen, no como líneas de texto.
> - **3.** Revisa que no haya archivos ajenos ni cambios sin preparar.
>
> **PARA Y COMPRUEBA ANTES DE GUARDAR:** Contrasta la selección con la lista exacta de archivos del aviso anterior. En diff --cached revisa el contenido y en status los preparados: no puede haber archivos ajenos ni recursos ignorados. Si no coincide, no ejecutes el bloque siguiente. La consulta no guarda ni sube nada.
>
> **Objetivo del siguiente bloque:** guardar la selección ya comprobada y enviarla al remoto.
>
> ```bash
> git commit -m "Ampliar inventario y documentar mantenimiento"
> git push
> git log --oneline
> git status
> ```
>
> **Línea por línea:**
>
> - **1.** Guarda juntos los archivos de esta ampliación.
> - **2.** Sube el tercer commit al mismo origin.
> - **3.** Muestra los tres commits, del más reciente al más antiguo; sal con q si aparece visor.
> - **4.** Comprueba main y árbol de trabajo limpio.
>
> **Resultado y condición para seguir:** La tercera entrega debe estar guardada y subida con sus 5 archivos: `inventario/mantenimiento/EQ02.md`, `inventario/criterios-estados.md`, `inventario/imagenes/equipo.png`, `inventario/equipos.csv`, `README.md`. Comprueba los tres commits y el estado limpio. En GitHub abre estos archivos, comprueba enlaces e imagen y confirma que los recursos ignorados NO aparecen. Si la subida falla, detente y resuélvela antes de consultar la versión antigua. Git no conserva una carpeta si solo contiene archivos ignorados.

## 4 · CONSULTA LA PRIMERA ENTREGA Y REGRESA

> [!danger] No edites durante la consulta histórica
> Primero debes estar en main con el trabajo limpio. Durante la consulta no edites en Obsidian ni en el editor: cierra las pestañas con autoguardado si hace falta. No hagas commit, push ni acciones para borrar historial. Apunta las observaciones fuera del repositorio y completa la bitácora después de volver a main.

> [!example] H7b · A · Comprueba y localiza el código real
> **Objetivo:** comprobar que no dejas cambios pendientes y leer el historial. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> git status
> git log --oneline
> ```
>
> **Línea por línea:**
>
> - **1.** Debe indicar main y ningún cambio pendiente. Si no, detente antes de continuar.
> - **2.** Busca el mensaje del primer commit y copia SU código real; sal con q si aparece visor.
>
> **Resultado y condición para seguir:** Identifica «Crear inventario inicial de equipos». Antes del bloque siguiente sustituye CODIGO_PRIMER_COMMIT por ese código; no uses un código inventado.

> [!example] H7b · B · Observa la versión antigua
> **Objetivo:** consultar un commit sin alterar ni borrar el historial. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> git switch --detach CODIGO_PRIMER_COMMIT
> git status
> ```
>
> **Línea por línea:**
>
> - **1.** --detach cambia temporalmente los archivos seguidos a ese commit sin situarte en una rama.
> - **2.** Es normal ver HEAD separado o detached; no hay cambios pendientes.
>
> **Resultado y condición para seguir:** Abre el CSV en el editor: EQ01 vuelve a Aula-1 y EQ02 a disponible; EQ03 no existe. La ficha, los criterios y la imagen tampoco pertenecen a esta versión. Los recursos ignorados pueden permanecer porque no pertenecen al historial. No los interpretes como archivos recuperados por Git.

> [!example] H7b · C · Regresa a main y comprueba
> **Objetivo:** volver a la rama actual con todos sus commits. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> git switch main
> git status
> git log --oneline
> ```
>
> **Línea por línea:**
>
> - **1.** Recupera los archivos seguidos de la rama main.
> - **2.** Confirma main y árbol de trabajo limpio.
> - **3.** Confirma que los tres commits siguen en el historial; sal con q si aparece visor.
>
> **Resultado y condición para seguir:** Reabre el CSV: EQ01 debe estar en Aula-3, EQ02 en mantenimiento y EQ03 debe reaparecer. Comprueba de nuevo ficha, criterios y portada. La consulta no genera otro commit ni requiere push.

## 5 · CIERRA LA GRABACIÓN Y LA BITÁCORA

> [!example] H8 · A · Evidencia final antes de detener OBS
> **Objetivo:** mostrar historial, remoto y estado y cotejar GitHub. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> git log --oneline
> git remote -v
> git status
> ```
>
> **Línea por línea:**
>
> - **1.** Muestra los tres commits del producto; sal con q si aparece visor.
> - **2.** Confirma la cuenta y el repositorio propios de este contexto.
> - **3.** Debe mostrar main y trabajo limpio.
>
> **Resultado y condición para seguir:** Muestra también en GitHub el contenido de la tercera entrega y la ausencia de recursos ignorados. Un estado limpio no demuestra que el push haya llegado. Si no coincide, corrige antes de terminar.

> [!example] H8 · B · Sube el vídeo y añade marcas reales
> Detén OBS. Guarda el vídeo en `Boveda_Inventario_Casa/00_Grabaciones`, fuera de Git. Súbelo como **No listado**, título `B0.P03 · Casa · Inventario de equipos`, a la playlist `B0.P03 · Casa · Inventario de equipos con Git y GitHub`. La playlist tendrá este único vídeo de entrega.
>
> En la descripción pega las nueve etapas siguientes y **sustituye cada TU_TIEMPO por el minuto real mm:ss de TU grabación**. La presentación empieza en 00:00. Comprueba que cada marca abre lo que anuncia; no inventes tiempos. Las críticas se puntúan a 0,6 y las menores a 0,25, según la rúbrica.
>
> ```text
> 00:00 Presentación e identidad
> TU_TIEMPO Comprobaciones Git identidad y SSH
> TU_TIEMPO Bóveda carpetas y producto inicial
> TU_TIEMPO Git init repositorio GitHub y remoto SSH
> TU_TIEMPO Primera versión y primer push
> TU_TIEMPO Modificación segunda versión y push
> TU_TIEMPO Ampliación gitignore preparación individual y tercer push
> TU_TIEMPO Consulta primer commit y regreso a main
> TU_TIEMPO Historial estado y comprobación GitHub final
> ```
>
> Comprueba que vídeo y playlist pueden abrirse con los permisos adecuados. Los clips y los informes locales de H7 nunca son vídeos de entrega.

> [!example] H8 · C · Completa tus siete apartados
> Ahora que existe el enlace real del vídeo, completa `00_Bitacora/b0-p03-casa-inventario-equipos.md` con tus pasos, comandos y resultados, las respuestas propias del apartado 6, los errores/correcciones reales y las dudas. Añade las marcas reales y enlaces al repositorio, a esta bitácora en GitHub, al vídeo y a la playlist; no dejes marcadores pendientes. No copies el enunciado como si fuera tu trabajo.
>
> El vídeo ya está cerrado: este cierre documental posterior no puede aparecer en esa misma grabación. Se demuestra en el repositorio final. No es una cuarta versión del producto.

> [!example] H8 · D · Comprueba el destino antes del cierre
> **Objetivo:** comprobar ubicación y remoto antes del último commit. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> pwd
> git remote -v
> git status
> ```
>
> **Línea por línea:**
>
> - **1.** Muestra la ruta completa actual.
> - **2.** Consulta la cuenta y repositorio de origin.
> - **3.** Debe mostrar únicamente la bitácora modificada.
>
> **Resultado y condición para seguir:** Debe terminar en `Boveda_Inventario_Casa/01_Proyecto`, estar en main y apuntar a `sor-inventario-equipos-casa`. Si no coincide, detente antes de preparar o subir.

> [!example] H8 · E · Guarda y sube la bitácora completa
> **Objetivo:** guardar únicamente el cierre documental y comprobarlo arriba. Ejecuta una línea, lee el resultado y solo entonces pasa a la siguiente; si una orden falla, detente.
>
> ```bash
> git diff -- 00_Bitacora/b0-p03-casa-inventario-equipos.md
> git add 00_Bitacora/b0-p03-casa-inventario-equipos.md
> git diff --cached --stat
> ```
>
> **Línea por línea:**
>
> - **1.** Revisa que la nota contenga enlaces reales y tus respuestas; sal con q si aparece visor.
> - **2.** Prepara solo esta bitácora.
> - **3.** Comprueba que la selección solo incluye la nota.
>
> **PARA Y COMPRUEBA ANTES DE GUARDAR:** La selección debe contener únicamente `00_Bitacora/b0-p03-casa-inventario-equipos.md`. En diff --cached revisa el contenido y en status los preparados: no puede haber archivos ajenos ni recursos ignorados. Si no coincide, no ejecutes el bloque siguiente. La consulta no guarda ni sube nada.
>
> **Objetivo del siguiente bloque:** guardar la selección ya comprobada y enviarla al remoto.
>
> ```bash
> git commit -m "Completar bitacora y enlace del video de casa"
> git push
> git status
> git log --oneline
> ```
>
> **Línea por línea:**
>
> - **1.** Crea el cuarto commit, documental, posterior al vídeo.
> - **2.** Envía la bitácora final al repositorio propio.
> - **3.** Confirma main y ningún cambio pendiente.
> - **4.** Muestra tres commits de producto y el cierre documental; sal con q si aparece visor.
>
> **Resultado y condición para seguir:** En GitHub abre la bitácora: deben verse respuestas y URL real del vídeo y playlist. Haz clic en ambos enlaces y comprueba sus destinos. El cuarto commit no aparece en el vídeo cerrado, sí en el historial final.

### Entrega independiente en Teams

Busca la tarea de **Casa** con el nombre `B0.P03 · Casa · Inventario de equipos con Git y GitHub` indicado por el profesor. La playlist se llama exactamente igual. Entrega **dos enlaces**: el repositorio `sor-inventario-equipos-casa` y la playlist de Casa, con su único vídeo de entrega. Comprueba permisos y pulsa **Entregar**. No adjuntes los enlaces del otro contexto ni esperes a terminarlo: las calificaciones son independientes.

## 6 · RESPONDE CON TUS RESULTADOS

> [!question] Preguntas para tu bitácora
> 1. ¿Por qué el repositorio está en 01_Proyecto y no en la raíz de la bóveda?
> 2. ¿Qué dos celdas de datos cambiaste en la segunda versión y cómo se ven en diff?
> 3. ¿Qué diferencia hay entre editar una fila y preparar ese cambio con add?
> 4. ¿Por qué la ficha nueva aparece en status y no en el diff de equipos.csv?
> 5. ¿Qué archivos preparaste individualmente en la ampliación y qué mostró diff --cached?
> 6. ¿Cómo demostraste que los clips existen y están ignorados sin subirlos?
> 7. ¿Qué ubicación y estado recuperaste al visitar el primer commit y qué ocurrió con EQ03?
> 8. ¿Por qué este CSV necesita historial y qué limitaciones tiene frente a un inventario multiusuario real?
> 9. ¿Cómo comprobaste la subida de la bitácora y por qué su cierre ocurre después del vídeo?

## 7 · ERRORES, COMPROBACIONES Y CIERRE

| Error | Qué pasa | Cómo evitarlo |
| :--- | :--- | :--- |
| Ruta de la bóveda equivocada | Puedes mezclar apuntes reales y laboratorio. | Detente en H1/H3 y comprueba ruta completa y padres antes de operar. |
| Identity o SSH de otra cuenta | El autor o remoto no serán los propios. | Detente en H0 y recupera la configuración de los prerrequisitos. |
| Archivo con .txt añadido | El enlace o script no encuentra su ruta. | Comprueba nombres y extensiones reales al guardar en H2/H7. |
| Diff vacío | El cambio no está guardado o ya está preparado. | Consulta status; usa diff para lo no preparado y diff --cached para el índice. |
| Origin ya existe | Repetir su alta falla. | No repitas H4; consulta remote -v antes de subir. |
| Recurso local listo para subir | El patrón no coincide o el archivo ya estaba seguido. | Detente en H7-C; no confíes en .gitignore para retirar archivos ya versionados. |
| Cambio histórico con archivos editados | Podrías llevar cambios entre versiones. | Exige estado limpio antes de H7b y no edites en detached. |
| GitHub no refleja lo local | Un commit local no implica subida. | Comprueba el resultado del push y abre los archivos en GitHub. |
| El push es rechazado | El remoto puede no estar vacío o existe otro cambio. | Detente, conserva tu trabajo y consulta al profesor; no fuerces la subida ni borres el remoto. |

> [!success] Checklist de este contexto
> - [ ] He creado `Boveda_Inventario_Casa` desde cero fuera de OneDrive, SOR y Boveda_SOR.
> - [ ] Solo `01_Proyecto` tiene el repositorio de esta práctica.
> - [ ] Origin pertenece a mi cuenta y a `sor-inventario-equipos-casa`.
> - [ ] He probado cada versión del producto antes de guardarla.
> - [ ] He preparado individualmente los archivos de la ampliación.
> - [ ] Los dos recursos locales de H7 existen, están ignorados y no aparecen en GitHub.
> - [ ] He consultado el primer commit, observado sus diferencias y regresado a main limpio.
> - [ ] El vídeo de Casa tiene título, playlist y nueve marcas reales correctos.
> - [ ] La bitácora completa está subida con sus enlaces reales en el cuarto commit.
> - [ ] He revisado la rúbrica y entregado solo mi repositorio y playlist de Casa.

> [!summary] Qué has aprendido
> Este inventario sirve para aprender cambios entre entregas de texto. Git no sustituye a una aplicación de inventario con permisos, validación de datos y edición simultánea; un historial no garantiza que la información registrada sea verdadera. Has aplicado Git a un producto que cambia: comprobar, preparar, guardar, subir y consultar otra versión sin perder la actual.

**Siguiente:** [índice de esta práctica](../00_Indice_Practica_03_Inventario_Equipos.md) · [Bloque 0 · Fase 0.8](../../../Fase_0.8_Practicas.md).
