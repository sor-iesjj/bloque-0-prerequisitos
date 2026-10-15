## 🏫 Fase 0.8 · Práctica 01 · Cole: avisos del aula

### Tu primer proyecto HTML de esta práctica, desde una bóveda vacía hasta GitHub

> **[Módulo: SOR — Sistemas Operativos en Red · 2.º SMR]**  
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)  
> **📍 Dónde se hace:** en el centro, después de las fases 0.3 y 0.3.b.  
> **🧭 Índice:** [Práctica 01](../00_Indice_Practica_01_Web_HTML.md) · [Fase 0.8](../../../Fase_0.8_Practicas.md)  
> **📖 Si necesitas repasar:** [estructura de la bitácora](../../../Fase_0.1.b_El_Sistema_de_Apuntes.md) · [primera conexión GitHub](../../../Fase_0.3_Repo_Apuntes_y_Primera_Entrada.md).

---

> [!abstract] 🎯 Tu misión de hoy
> Crear **desde cero** una bóveda llamada `Boveda_HTML_Centro` para una página de avisos del aula. Dentro crearás **un repositorio Git local** y, en GitHub, un repositorio vacío al que conectarás por SSH. Guardarás una primera versión, cambiarás el estado del aula y añadirás un fichero CSS. Grabarás **un único vídeo de pantalla** que muestre todo el proceso.

> [!important] 📹 En el centro no tienes que narrar
> La grabación es **de pantalla, sin explicación oral**. Empieza a grabar **antes de crear la bóveda** y termina después de comprobar el resultado en GitHub. En pantalla deben verse tu identidad académica o tu perfil de GitHub, las carpetas, las páginas antes y después, los comandos y sus resultados. Mantén visible cada etapa lo suficiente para leerla. No muestres contraseñas ni claves privadas.
>
> **Título del vídeo:** `B0.P01 · Centro · Avisos del aula`. **Visibilidad:** No listado. **Playlist:** `B0.P01 · Dos bóvedas HTML con Git y GitHub`, igual que la tarea de Teams.

### 📍 Tu mapa de carpetas

```text
Boveda_HTML_Centro/                 ← la abres en Obsidian; aquí NO haces git init
├── .obsidian/                       ← configuración de Obsidian
├── 00_Grabaciones/                  ← guarda aquí el vídeo; queda fuera de Git
└── 01_Proyecto/                     ← SOLO aquí haces git init
    ├── .gitignore
    ├── README.md
    ├── 00_Bitacora/
    │   └── b0-p01-centro-avisos-aula.md
    └── web/
        ├── index.html
        └── estilos.css              ← lo crearás después del segundo commit
```

> [!tip] Antes de grabar
> Lee esta guía entera, abre OBS, Obsidian, Git Bash, GitHub y un editor de texto. Comprueba que Git y la conexión SSH funcionan como en las fases 0.2 y 0.3. **No crees la bóveda todavía:** eso debe verse en el vídeo. La bóveda se guarda en una ubicación local fuera de OneDrive.

---

## 1 · CREA LA BÓVEDA Y LA PRIMERA PÁGINA

> [!example] Paso C1 · Crea el lugar de trabajo
> Con OBS grabando, crea en Obsidian una bóveda **nueva** llamada `Boveda_HTML_Centro`. No utilices `Boveda_SOR` para este proyecto. Crea `00_Grabaciones/` y `01_Proyecto/`; dentro de `01_Proyecto/`, crea `00_Bitacora/` y `web/`. Muestra el árbol en la pantalla.

> [!example] Paso C2 · Prepara los ficheros iniciales
> En `00_Bitacora/` crea `b0-p01-centro-avisos-aula.md` con tu nombre y **los siete apartados de la Fase 0.1.b**. En `🔗 Enlaces`, deja `Vídeo: pendiente`; pegarás el enlace al terminar.
>
> En `01_Proyecto/README.md` escribe el título «Avisos del aula», tu nombre y una frase sobre la utilidad de la página. Con un editor de texto, crea `01_Proyecto/.gitignore` con:
>
> ```gitignore
> *.mp4
> *.mkv
> *.mov
> .DS_Store
> Thumbs.db
> ```
>
> El vídeo se guardará en `00_Grabaciones/`, **fuera** de Git. `.gitignore` ofrece una segunda barrera si un vídeo acaba por error dentro de `01_Proyecto/`. Para el HTML y el CSS usa un editor de texto y comprueba que el nombre **no termina en `.txt`**.

En `01_Proyecto/web/index.html`, escribe esta **primera versión**:

```html
<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <title>Avisos del aula</title>
</head>
<body>
  <h1>Avisos del aula</h1>
  <p>Estado: aula disponible.</p>
</body>
</html>
```

Abre `index.html` en el navegador y enseña **«Estado: aula disponible.»**. El fichero `estilos.css` **aún no existe**: aparecerá más adelante, en otro commit.

---

## 2 · INICIALIZA GIT Y CONÉCTALO A GITHUB

> [!example] Paso C3 · Abre la terminal en la carpeta correcta
> Abre Git Bash **dentro de `Boveda_HTML_Centro/01_Proyecto`**. Ejecuta:
>
> ```bash
> pwd
> git init
> git branch -M main
> git status
> git check-ignore -v grabacion.mp4
> ```
>
> **Punto de control:** `pwd` termina en `Boveda_HTML_Centro/01_Proyecto`; `git status` indica `main`, todavía sin commits, y muestra los ficheros iniciales *sin seguimiento*. `git check-ignore` muestra la regla que excluiría un vídeo; **no crea ese fichero**. Si `pwd` muestra la raíz de la bóveda, **detente**: Git quedaría en la carpeta equivocada.

> [!example] Paso C4 · Crea y conecta el repositorio remoto
> En tu cuenta de GitHub crea un repositorio llamado `sor-web-avisos-aula`. Déjalo **vacío**: no generes allí README, `.gitignore` ni licencia. Usa la visibilidad indicada en Teams; si es privado, concede acceso al profesor con la cuenta que se indique.
>
> En la pantalla del repositorio vacío, elige **SSH** y copia tu dirección. Tendrá esta forma: `git@github.com:TU-USUARIO/sor-web-avisos-aula.git`. Sustituye `TU-USUARIO` por tu usuario de GitHub real.
>
> En la terminal abierta en `01_Proyecto`:
>
> ```bash
> git remote add origin git@github.com:TU-USUARIO/sor-web-avisos-aula.git
> git remote -v
> ```
>
> **Punto de control:** `origin` termina en `sor-web-avisos-aula.git`. Si no, corrige el destino **antes de hacer push**. En este proyecto no volverás a ejecutar `git init` ni `git remote add origin` para cada cambio.

---

## 3 · GUARDA TRES VERSIONES DISTINTAS

> [!example] Paso C5 · Primera versión: el aviso inicial
> ```bash
> git status
> git add .gitignore README.md 00_Bitacora/b0-p01-centro-avisos-aula.md web/index.html
> git status
> git diff --cached --stat
> git commit -m "Crear pagina inicial de avisos del aula"
> git push -u origin main
> git status
> ```
>
> Antes de `add`, los ficheros están *sin seguimiento*. Después de `add`, están preparados para el commit. Al terminar, `git status` debe estar limpio. Actualiza GitHub y muestra allí el primer commit y `web/index.html`. La opción `-u origin main` configura la primera subida; después bastará `git push`.

> [!example] Paso C6 · Segunda versión: cambia el aviso
> En `web/index.html`, sustituye **solo** `Estado: aula disponible.` por `Estado: aula ocupada por mantenimiento.`. Guarda y actualiza el navegador. Antes de añadir el cambio, enseña la diferencia:
>
> ```bash
> git status
> git diff -- web/index.html
> git add web/index.html
> git diff --cached -- web/index.html
> git commit -m "Actualizar estado del aula por mantenimiento"
> git push
> ```
>
> En `git diff` debe verse la línea anterior y la nueva. Comprueba en GitHub que el estado del aula ha cambiado. Este commit guarda **el cambio del aviso**, todavía sin CSS.

> [!example] Paso C7 · Tercera versión: añade un fichero CSS
> Crea `web/estilos.css` con:
>
> ```css
> body { font-family: sans-serif; margin: 2rem; }
> h1 { color: #174ea6; }
> ```
>
> En `web/index.html`, **dentro de `<head>` y debajo de `<title>`**, añade:
>
> ```html
> <link rel="stylesheet" href="estilos.css">
> ```
>
> Actualiza la página en el navegador: **el título debe verse azul**. Comprueba en Git los dos estados: `estilos.css` es *nuevo, sin seguimiento*; `index.html` es un fichero *modificado*.
>
> ```bash
> git status
> git diff -- web/index.html
> git add web/estilos.css web/index.html
> git diff --cached --stat
> git commit -m "Anadir estilo azul a los avisos"
> git push
> git log --oneline
> git status
> ```
>
> GitHub debe mostrar los **tres commits en orden**, el HTML actualizado y el CSS. En el navegador debe verse el título azul. Si el CSS no se nota, comprueba que `href="estilos.css"` coincide con el fichero que está junto a `index.html`.

---

## 4 · TERMINA LA GRABACIÓN Y DOCUMENTA

> [!example] Paso C8 · Cierra el vídeo
> Enseña el repositorio en GitHub, `git log --oneline`, `git remote -v` y `git status` limpio. Detén OBS y guarda el vídeo en `00_Grabaciones/`. Súbelo como **No listado** con el título y la playlist indicados al principio.
>
> En la **descripción del vídeo**, pon el minuto **real** de cada etapa. Cambia cada marcador por un tiempo `mm:ss`:
>
> ```text
> 00:00 Inicio e identidad en pantalla
> TU_TIEMPO Bóveda y carpetas
> TU_TIEMPO HTML inicial en navegador
> TU_TIEMPO git init y git status
> TU_TIEMPO Repositorio GitHub y origin
> TU_TIEMPO Primera versión y primer push
> TU_TIEMPO Cambio del aviso
> TU_TIEMPO Nuevo fichero CSS
> TU_TIEMPO Historial y comprobación final
> ```
>
> Comprueba que las marcas llevan a la etapa correcta. Completa la bitácora con los siete apartados de la Fase 0.1.b; en `🔗 Enlaces` pega el enlace **de este vídeo** y el de la playlist. Responde las preguntas del apartado 5 y anota los fallos que realmente resolviste.
>
> El enlace de YouTube **no existía** al hacer el primer commit. Súbelo ahora desde `Boveda_HTML_Centro/01_Proyecto`:
>
> ```bash
> pwd
> git remote -v
> git status
> git add 00_Bitacora/b0-p01-centro-avisos-aula.md
> git commit -m "Completar bitacora y enlace del video del centro"
> git push
> git status
> ```

> [!note] 📤 Todavía no entregas la tarea completa
> Guarda el enlace del repositorio del centro y el de su vídeo. La tarea de Teams `B0.P01 · Dos bóvedas HTML con Git y GitHub` se entrega cuando también esté hecho el trabajo de casa. Entonces incluirá **los dos repositorios y la playlist**. **Este vídeo no lleva narración**; las marcas de tiempo ayudan a corregirlo.

---

## 5 · COMPRUEBA QUE ENTIENDES LO QUE HAS HECHO

> [!help] Preguntas críticas para la bitácora
> 1. ¿Por qué `git init` se hizo en `01_Proyecto` y no en `Boveda_HTML_Centro`?
> 2. ¿Qué diferencia viste en `git status` antes y después de `git add`?
> 3. ¿Qué dirección guarda `origin` y cuándo volverías a ejecutar `git remote add origin`?
> 4. ¿Por qué `estilos.css` aparecía como fichero nuevo y `index.html` como modificado?
> 5. ¿Qué te aporta separar los tres cambios en commits distintos?

> [!bug] Si algo no sale
> | Síntoma | Comprueba primero |
> | :--- | :--- |
> | `nothing to commit` | ¿Guardaste el fichero? Mira `pwd`, `git status` y `git log --oneline`. |
> | `remote origin already exists` | Ya añadiste `origin`. Mira `git remote -v`; no repitas el alta. |
> | El título no se ve azul | ¿`estilos.css` está junto a `index.html`? ¿Coincide el `href`? |
> | GitHub muestra la versión anterior | Revisa `git status` y si ejecutaste `git push` en **este** repo. |
> | `pwd` termina en la raíz de la bóveda | **Detente.** Abre Git Bash dentro de `01_Proyecto` antes de crear el repositorio. |

> [!success] ✅ Al acabar en el centro
> - [ ] Bóveda `Boveda_HTML_Centro` creada en la grabación y fuera de OneDrive.
> - [ ] `.git` está dentro de `01_Proyecto`, y `origin` apunta a `sor-web-avisos-aula`.
> - [ ] Primera versión, cambio de estado y CSS aparecen como decisiones separadas en GitHub.
> - [ ] El HTML muestra el aviso nuevo y el título azul.
> - [ ] El vídeo de pantalla tiene timestamps reales.
> - [ ] La bitácora incluye su vídeo y está subida al repositorio del centro.
