## Rúbrica · B0.P04 · Casa · Herramienta de diagnóstico

### Qué se evalúa y cómo se evalúa

> [!abstract] Primero, tu bitácora
> Si falta o no alcanza el 70 %, la nota es 0 y no se corrigen el repositorio ni el vídeo. El objetivo es llegar al 80 % o más; se acepta desde el 70 % a favor del alumno.

## 1 · QUÉ ENTREGAS

En la tarea de **B0.P04 · Casa · Herramienta de diagnóstico con Git y GitHub**, adjunta **dos enlaces** y pulsa **Entregar**:

1. Tu repositorio GitHub `sor-diagnostico-bash-casa`, que contiene la bitácora.
2. Tu playlist `B0.P04 · Casa · Herramienta de diagnóstico con Git y GitHub`, con **un único vídeo**, titulado `B0.P04 · Casa · Herramienta de diagnóstico`, en **No listado**.

Cole y Casa se entregan por separado. [Consulta la guía completa de esta práctica](Practica_04_Casa_Diagnostico_Bash.md).

## 2 · FILTROS ANTES DE PUNTUAR

| Orden | Evidencia exigida | Si falla |
| :--- | :--- | :--- |
| Entrega | Enlaces adjuntos y botón Entregar pulsado | 0 · No entregado. Pendiente de recuperación |
| F1 · Bitácora implementada | Repositorio accesible con commits y bitácora con contenido | 0 · Sin bitácora corregible; no se continúa |
| F2 · Bitácora completa | Porcentaje según la tabla siguiente: objetivo 80 %, aceptado desde 70 % | 0 · Bitácora incompleta; no se corrigen repositorio ni vídeo |

La plantilla tiene **7 apartados y un encabezado**. Las preguntas se puntúan por lo que explicas, no por copiar el enunciado. Cada peso se reconoce en proporción al contenido pertinente y correcto que documentas.

| Elemento de la bitácora | Peso para F2 | Máximo sobre 2,5 |
| :--- | ---: | ---: |
| Encabezado: nombre, apellidos, bloque, fase y fechas | 10 % | 0,25 |
| Qué se pedía, con tus palabras | 5 % | 0,125 |
| Comandos y pasos importantes, con explicación | 15 % | 0,375 |
| Qué he hecho: relato propio de la ejecución | 10 % | 0,25 |
| Qué me ha fallado: error y corrección; si no hubo, indícalo | 5 % | 0,125 |
| Respuestas a las 9 preguntas de la guía | 40 % | 1 |
| Enlaces reales al vídeo y playlist | 10 % | 0,25 |
| Dudas; si no tienes, indícalo | 5 % | 0,125 |
| **Total** | **100 %** | **2,5** |

Las 9 preguntas se reparten ese 40 % a partes iguales: **40/9 puntos porcentuales y 1/9 puntos de nota por pregunta**, antes de valorar su corrección. El porcentaje completo se multiplica por 2,5/100 para calcular la nota de bitácora.

| Pregunta | Qué debes responder en la bitácora |
| :---: | :--- |
| 1 | ¿Por qué ejecutas el script desde 01_Proyecto y mediante bash? |
| 2 | ¿Qué consulta cada comando del script inicial y por qué no modifica archivos? |
| 3 | ¿Qué diferencia observable tuvo la segunda versión y qué mostró diff antes de add? |
| 4 | ¿Por qué un informe creado con redirección puede guardarse en el disco sin entrar en Git? |
| 5 | ¿Qué regla excluye los informes y cómo comprobaste su contenido real y su exclusión? |
| 6 | ¿Qué cuatro archivos preparaste individualmente en la ampliación y cómo revisaste el índice? |
| 7 | ¿Qué comandos dejó de ejecutar el script al consultar el primer commit y cuáles recuperó al volver a main? |
| 8 | ¿Por qué la salida de git status dentro del script puede variar entre ejecuciones aunque el script no cambie? |
| 9 | ¿Qué demuestra una subida comprobada en GitHub y por qué un estado limpio no demuestra por sí solo el push? |

## 3 · NOTA Y DESCUENTOS

Solo tras superar los filtros: **bitácora 2,5 + repositorio 3,5 + vídeo 4 = 10**. Teams expresa la nota sobre 100: se multiplica por 10.

**Repositorio:** parte de **3,5 puntos**. Se contrastan los dos árboles, los cuatro commits y sus contenidos, el remoto de este proyecto y la exclusión de grabaciones e informes cuando corresponda. Se aplican estos descuentos, hasta agotar sus 3,5 puntos; nunca queda negativo:

| Gravedad | Error de proceso | Descuento por error |
| :--- | :--- | ---: |
| Crítico | Inicializar en la raíz de la bóveda; remoto de otro proyecto; subir contenido que debía ignorarse; falta un commit | −1 |
| Grave | Commits fusionados o desordenados; archivos repartidos en otra entrega | −0,5 |
| Leve | Mensaje de commit casi igual al pedido; carpeta de más o anidada | −0,25 |

**Nombres:** si cambias un nombre por otro distinto, se resta **el 25 % de la nota total, una sola vez**, aunque fallen varios nombres. Una coincidencia del **90 % o más** no descuenta: mayúsculas, puntuación, guiones o extensión repetida solo se recuerdan. Los nombres sancionados aquí **no se descuentan otra vez dentro del repositorio**. Se aplica a la suma de los tres bloques: `nota final = suma × 0,75` si procede; en otro caso, se conserva la suma.

| Elemento | Nombre exacto |
| :--- | :--- |
| Bóveda | `Boveda_Diagnostico_Casa` |
| Repositorio GitHub | `sor-diagnostico-bash-casa` |
| Bitácora, dentro de `01_Proyecto/00_Bitacora/` | `b0-p04-casa-diagnostico-bash.md` |
| Vídeo, No listado | `B0.P04 · Casa · Herramienta de diagnóstico` |
| Playlist, un vídeo | `B0.P04 · Casa · Herramienta de diagnóstico con Git y GitHub` |

## 4 · CARPETAS Y APARICIÓN DE ARCHIVOS

**H1: crea solo estas carpetas vacías.** Cada línea acabada en `/` es una carpeta; los archivos aparecen después.

```text
Boveda_Diagnostico_Casa/
├── 00_Grabaciones/
└── 01_Proyecto/
    ├── 00_Bitacora/
    └── diagnostico/
```

**Al terminar:** el árbol siguiente distingue lo versionado de lo que queda fuera. `.git/` lo genera Git al inicializar el repositorio; `.obsidian/` lo gestiona Obsidian fuera de `01_Proyecto` y no forma parte del producto entregado.

```text
Boveda_Diagnostico_Casa/
├── 00_Grabaciones/
└── 01_Proyecto/
    ├── .git/
    ├── 00_Bitacora/
    │   └── b0-p04-casa-diagnostico-bash.md
    ├── diagnostico/
    │   ├── imagenes/
    │   │   └── salida.png
    │   ├── informes/
    │   │   ├── prueba-01.txt
    │   │   └── prueba-02.txt
    │   ├── diagnostico.sh
    │   └── interpretacion.md
    ├── .gitignore
    └── README.md
```

| Hito | Qué aparece o cambia |
| :--- | :--- |
| H1 | Solo las carpetas del primer árbol |
| H2 | `.gitignore`, `00_Bitacora/b0-p04-casa-diagnostico-bash.md`, `README.md`, `diagnostico/diagnostico.sh` |
| H3 | `.git/`, generado por Git dentro de `01_Proyecto`; no se crea a mano ni se sube como carpeta |
| H6 | Se modifica `diagnostico/diagnostico.sh` |
| H7 | Carpetas nuevas: `diagnostico/imagenes/`, `diagnostico/informes/`; archivos nuevos: `diagnostico/interpretacion.md`, `diagnostico/imagenes/salida.png`. Se modifican `diagnostico/diagnostico.sh`, `README.md` |
| H7, fuera de Git | `diagnostico/informes/prueba-01.txt`, `diagnostico/informes/prueba-02.txt`; las grabaciones permanecen en `00_Grabaciones/`, fuera del repositorio |
| H8 · C–E | Solo se completa y vuelve a subir la bitácora con enlaces reales y respuestas definitivas |

## 5 · LOS CUATRO COMMITS

En este orden, con los mensajes y contenidos indicados. Consultar la primera versión no crea un commit adicional.

| Orden | Mensaje exacto | Qué guarda |
| :---: | :--- | :--- |
| 1 | `Crear herramienta inicial de diagnostico` | `.gitignore`, `00_Bitacora/b0-p04-casa-diagnostico-bash.md`, `README.md`, `diagnostico/diagnostico.sh` |
| 2 | `Consultar rama y estado en el diagnostico` | `diagnostico/diagnostico.sh` |
| 3 | `Ampliar diagnostico con remoto historial y guia` | `diagnostico/interpretacion.md`, `diagnostico/imagenes/salida.png`, `diagnostico/diagnostico.sh`, `README.md` |
| 4 | `Completar bitacora y enlace del video de casa` | `00_Bitacora/b0-p04-casa-diagnostico-bash.md` |

Los tres primeros guardan versiones del producto. El cuarto cierra la documentación después de disponer del enlace real del vídeo. Hay que hacer su push y comprobar en GitHub que la bitácora definitiva está publicada.

## 6 · LAS NUEVE MARCAS DEL VÍDEO

En Casa grabas **explicando en voz alta** cada etapa.

Escribe **las 9 marcas siguientes en la descripción con tus tiempos reales**, empezando por `00:00`. Las etiquetas describen qué debe verse; no inventes tiempos. Las 5 críticas suman **5 × 0,6 = 3 puntos**; las 4 menores, **4 × 0,25 = 1 punto**. Total: **4 puntos**.

| Marca obligatoria | Tipo y máximo | Qué tiene que verse |
| :--- | :--- | :--- |
| Presentación e identidad | menor · 0,25 | Inicio a `00:00`: nombre y apellidos, contexto y objetivo; terminal y texto legibles. |
| Comprobaciones Git identidad y SSH | crítica · 0,6 | `git --version`, identidad configurada y saludo SSH de tu cuenta de GitHub; sin enseñar claves privadas. |
| Bóveda carpetas y producto inicial | menor · 0,25 | Creación de `Boveda_Diagnostico_Casa`, carpetas vacías y archivos iniciales de H2; producto inicial visible. |
| Git init repositorio GitHub y remoto SSH | crítica · 0,6 | `pwd` y comprobación de ruta antes de inicializar `01_Proyecto`, rama `main`, repositorio GitHub vacío y remoto SSH propio. |
| Primera versión y primer push | crítica · 0,6 | Preparación, primer commit `Crear herramienta inicial de diagnostico`, push y versión publicada en GitHub. |
| Modificación segunda versión y push | menor · 0,25 | Edición de `diagnostico/diagnostico.sh`, diferencias, segundo commit, push y cambio visible. |
| Ampliación gitignore preparación individual y tercer push | crítica · 0,6 | Archivos de ampliación añadidos uno a uno, `status` entre ellos, índice revisado con `diff --cached`, exclusión comprobada de pruebas locales, tercer commit y push. |
| Consulta primer commit y regreso a main | crítica · 0,6 | `git log --oneline`, código real del primer commit, `git switch --detach`, producto antiguo comprobado y regreso con `git switch main`; producto actual recuperado. |
| Historial estado y comprobación GitHub final | menor · 0,25 | Historial de las tres versiones, remoto correcto, estado limpio y producto/bitácora provisional visibles en GitHub en H8 · A, antes de subir el vídeo y cerrar la documentación. |

- Evidencia completa: puntuación íntegra. Etapa visible pero incompleta: la mitad (**0,3** si es crítica; **0,125** si es menor). Otra cosa o ninguna evidencia: **0**.
- Sin marcas, el vídeo no se revisa y vale 0. Con **3 o más de las 5 críticas** que no se corresponden con lo anunciado, todo el bloque de vídeo vale 0. Una etapa parcialmente demostrada conserva la mitad; no equivale automáticamente a una marca que muestra otra cosa.
- El cierre documental H8 · C–E ocurre tras subir el vídeo en H8 · B: se comprueba en GitHub y en el último commit, **no exige una décima marca ni otro vídeo**.

> [!warning] Evidencias seguras
> No muestres claves privadas, contraseñas ni datos personales innecesarios. Si hay una clave privada publicada, se avisa además de la nota: debe retirarse y sustituirse. Utiliza los datos ficticios indicados por la guía.

## 7 · EL COMENTARIO EN TEAMS

Si no entregas: «No entregado. Pendiente de recuperación.» Si falla F1 o F2, se indica el filtro, el motivo y el resultado; no se comenta una parte que no se ha corregido.

Si superas los filtros, el comentario distingue F1, porcentaje de F2, **bitácora /2,5**, **repositorio /3,5**, **vídeo /4**, nombres y resultado final. Cada descuento lleva su motivo. Puedes así localizar qué evidencia necesitas corregir.
