## 🔬 Fase 0.4.b: Tres Retos — Rómpelo y Recupéralo

### Borra lo que acabas de bajar. Dos veces vuelve; la tercera, no

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~1 hora · **Requisitos:** Bloque 0 · Fase 0.4.a completa, con los tres repositorios clonados y `MIS_DATOS.md` subido.


> [!abstract] 📋 Qué se te evalúa en esta fase
> **RA.05**
>
> | Código | Criterio de evaluación |
> | :--- | :--- |
> | `CE.05.d` | Se han realizado tareas de mantenimiento del software instalado en el sistema. |
>
> Los criterios están tomados literalmente del **RD 1691/2007** y de la programación del módulo.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin.
> 1. **Prepárate primero (sin grabar):** comprueba lo necesario, **léete el procedimiento entero** y **crea la entrada de apuntes de esta fase** en Obsidian: fichero `b0-0.4.b-tres-retos-de-recuperacion.md` con la estructura del **Bloque 0 · Fase 0.1.b**, **vacía**.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a explicar la Fase 0.4.b — Tres retos de recuperación."* Y **muestra tu perfil de GitHub**. Di qué vas a hacer.
> 3. **Graba TODO**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Presentación` + **uno por reto** — son los tres que voy a mirar primero.
> 5. **Al terminar:** nombra el vídeo `B0.4.b · Tres retos de recuperación` y súbelo a tu playlist **`B0_Prerrequisitos`** (No listado).
> 6. **~5 min.** Se graba en **🏫 el centro**.
> 7. **La entrega va por la TAREA de Teams**, agrupada con otras fases. Tú, hoy: graba, sube y **pega el enlace en tu entrada de apuntes**.

---

### 🎯 Objetivos de la fase

- [ ] **Recuperar ficheros borrados** con `git restore`, sin Internet.
- [ ] **Reconstruir un repositorio entero** clonando, cuando ya no queda ni el historial.
- [ ] Explicar **por qué** el segundo caso no se arregla como el primero.
- [ ] Demostrar que **lo que no se empuja no se recupera**.
- [ ] Deducir **dónde NO se escriben tus notas** y por qué.

---

### 🎯 ¿Dónde Estamos?

> [!info] El Punto de Partida
> Acabas de bajar tres repositorios y de subir tu primer cambio a Boochan. Todo funciona. **Hoy lo rompes.**

> [!warning] El Problema
> Un técnico no se entera de si sus copias de seguridad valen **el día que las hace**: se entera el día que las necesita. Y ese día suele ser tarde.
> Así que hoy provocamos el desastre nosotros, con el material del curso —que no me importa que rompas—, para que cuando pase de verdad con tu trabajo sepas exactamente qué hacer.

---

### 📚 Fundamento Teórico

> [!important] La única idea de esta fase: dónde está guardado cada cosa
> Cuando clonaste, te trajiste **dos cosas**, no una:
>
> | Qué | Dónde vive | Qué te permite |
> | :--- | :--- | :--- |
> | Los **ficheros** | A la vista, en la carpeta | Trabajar |
> | El **historial** | En **`.git`**, oculta **dentro de esa misma carpeta** | Volver atrás |
>
> Fíjate en la trampa: **`.git` está DENTRO de la carpeta del repositorio.** Es tu máquina del tiempo, sí — pero vive en el mismo sitio que lo que protege.
>
> Y de ahí salen los tres retos de hoy:
>
> | Reto | Qué borras | ¿Sigue habiendo `.git`? |
> | :---: | :--- | :--- |
> | **1** | Unos ficheros de dentro | ✅ Sí → se arregla en local |
> | **2** | La carpeta entera | ❌ No → hay que ir a GitHub |
> | **3** | La carpeta entera, con algo tuyo **sin subir** dentro | ❌ No, **y en GitHub tampoco estaba** |

> [!quote] Terminología
> - **`git restore .`:** devuelve los ficheros a como estaban en el último commit. El **punto** significa *"todo desde aquí hacia abajo"*.
> - **`working tree clean`:** no hay ninguna diferencia entre tu carpeta y el último commit.
> - **`D` en `git status`:** *deleted*. Git sabe que ese fichero falta.

---

### 🛠️ Procedimiento Práctico

> [!example] Paso 0: Prepárate (todavía SIN grabar)
> Comprueba que tienes las tres carpetas de la 0.4.a y que `MIS_DATOS.md` está **subido** a tu repositorio de Boochan. **Léete los tres retos enteros antes de empezar** — hoy más que nunca, porque vas a borrar cosas.
> **Y crea la entrada de apuntes** (`b0-0.4.b-tres-retos-de-recuperacion.md`), vacía.

> [!example] Paso 1: Arranca la grabación y preséntate
> Inicia **OBS**, preséntate, **enseña tu perfil de GitHub** 2-3 segundos y di qué vas a hacer: *"voy a romper el material del curso tres veces y a ver qué se puede recuperar."*

> [!example] 🔬 Paso 2 — RETO 1: bórralo y recupéralo (sin Internet)
> 1. En el Explorador, entra en `01_Practicas/B2_Ubuntu_Local/Fases/` y **borra TODOS los ficheros de fase**. Todos. Mira la carpeta vacía.
> 2. En la terminal, **dentro de `B2_Ubuntu_Local`**, pregúntale a Git:
>    ```bash
>    pwd          # .../01_Practicas/B2_Ubuntu_Local
>    git status
>    ```
>    Verás tus fases marcadas con **`D`** (de *deleted*). Git sabe perfectamente lo que falta.
> 3. **Piénsalo dos segundos antes de leer la solución.** ¿Necesitas Internet para recuperarlas? ¿Necesitas volver a GitHub?
>
> > [!success] ✅ Solución del Reto 1
> > **No hace falta Internet.** Un comando:
> > ```bash
> > git restore .
> > ```
> > ⚠️ **El punto no es decorativo.** Si escribes `git restore` a secas, Git responde `fatal: you must specify path(s) to restore`: no adivina qué quieres recuperar. El `.` significa *"todo lo que hay desde donde estoy hacia abajo"*.
> > Comprueba con `git status`: vuelve a decir `working tree clean`. Y las fases están otra vez ahí.
> >
> > **¿Por qué ha funcionado?** Porque al clonar te trajiste **también el historial**, que vive en la carpeta oculta `.git` dentro de `B2_Ubuntu_Local`. Esos ficheros estaban guardados ahí, **en tu propio ordenador**. `git restore` los ha copiado de vuelta.
> > Dilo en voz alta en el vídeo: *"he recuperado el material sin conectarme a nada, porque el historial está en mi equipo."*
>
> > [!tip] 💡 Y acuérdate del ZIP de ayer
> > Si te hubieras quedado con la carpeta descomprimida del ZIP, **este reto no tendría solución**. Sin `.git` no hay `git restore`. Ahí es donde se nota la diferencia que en el Explorador no se veía.

> [!example] 🔬 Paso 3 — RETO 2: ahora bórralo TODO (y aquí sí cambia la cosa)
> El reto anterior fue fácil. Este no se arregla igual.
>
> 1. Cierra Obsidian.
> 2. Borra **la carpeta `B2_Ubuntu_Local` ENTERA**, con todo dentro. Sí, la carpeta completa.
> 3. Abre la terminal en `01_Practicas/` y prueba el truco de antes:
>    ```bash
>    git status
>    ```
>    Responde:
>    ```
>    fatal: not a git repository (or any of the parent directories): .git
>    ```
> 4. **Explica en voz alta por qué el Reto 1 ya no sirve.** Si no lo ves, la pista está en la respuesta de Git — y en la tabla del Fundamento.
>
> > [!success] ✅ Solución del Reto 2
> > **Aquí Git en tu ordenador no puede hacer nada**, y la razón es esta: la carpeta oculta `.git` —tu historial, tu máquina del tiempo— **estaba DENTRO de `B2_Ubuntu_Local`**. Al borrar la carpeta, la has borrado con ella. `git restore` no existe si no hay repositorio.
> >
> > Lo único que queda está **fuera de tu ordenador**: en GitHub. Así que se vuelve a clonar. Desde `01_Practicas/`:
> > ```bash
> > pwd          # .../Boveda_SOR/01_Practicas
> > git clone git@github.com:TU-USUARIO/bloque-2-ubuntu-local.git B2_Ubuntu_Local
> > ```
> > En segundos lo tienes todo otra vez: el manual, las fases **y tu historial completo** (`git log --oneline` lo demuestra).
> >
> > > [!important] 🔍 Fíjate en un detalle que lo explica todo
> > > **`MIS_DATOS.md` también ha vuelto.** ¿Por qué? Porque en la 0.4.a hiciste `push`. Estaba en GitHub.
> > > Si lo hubieras creado y **no** lo hubieras empujado, ahora no estaría. Se habría perdido para siempre, junto con la carpeta.
> > > **Esa es toda la lección:** lo que está en GitHub sobrevive; lo que solo está en tu ordenador, no. Por eso `push` al terminar cada sesión.

> [!example] 🔬 Paso 4 — RETO 3: ¿y si lo que borro son MIS anotaciones?
> Los dos retos anteriores han ido bien porque recuperaste **material que yo había escrito**. Ahora vamos a por lo que has escrito **tú**, que es lo que de verdad no se puede rehacer.
>
> 1. Entra en `01_Practicas/B1_Entorno/` y **escribe algo tuyo**: crea ahí `MIS_NOTAS_B1.md` con dos o tres líneas de verdad, algo que te costaría rehacer.
> 2. **Intenta ponerlo a salvo**, como te he enseñado:
>    ```bash
>    pwd          # .../01_Practicas/B1_Entorno
>    git add .
>    git commit -m "Mis notas del Bloque 1"
>    git push
>    ```
> 3. **El `push` te lo rechaza** con un `403` o un `Permission denied`. Y ya sabes por qué: **ese repositorio es mío**, lo clonaste directamente de `sor-iesjj` en la 0.4.a. Tú ahí no escribes.
> 4. Da igual, sigue: borra **la carpeta `B1_Entorno` entera** y vuelve a clonarla:
>    ```bash
>    cd ..
>    pwd          # .../Boveda_SOR/01_Practicas
>    git clone https://github.com/sor-iesjj/bloque-1-entorno.git B1_Entorno
>    ```
> 5. **Busca tu `MIS_NOTAS_B1.md`.**
>
> > [!success] ✅ Solución del Reto 3 — y la conclusión de la fase
> > **No hay solución.** El material del Bloque 1 ha vuelto entero, porque estaba en mi GitHub. **Tus notas no vuelven**, y no hay ningún comando que las traiga.
> >
> > Y fíjate en lo que ha pasado exactamente, que es peor de lo que parece: **hiciste `commit`**. Tenías tu punto de restauración… **dentro de la carpeta que has borrado**. El commit vivía en el `.git` de `B1_Entorno`. Y `push`, que lo habría sacado de tu ordenador, **no podías hacerlo**.
> >
> > | Qué borraste | ¿Vuelve? | Por qué |
> > | :--- | :---: | :--- |
> > | El material del Bloque 1 | ✅ | Estaba en el repositorio del profesor |
> > | `MIS_DATOS.md` del Reto 2 | ✅ | **Le hiciste `push`**, a un repositorio **tuyo** |
> > | `MIS_NOTAS_B1.md` de ahora | ❌ | **Nunca salió de tu ordenador**, y no podía salir |
> >
> > > [!danger] 🛑 De aquí sale una regla que vale para todo el curso
> > > **Tus notas NUNCA se escriben dentro de una carpeta de `01_Practicas/` que sea material mío.** Ahí no hay `push` posible, así que nada de lo que escribas está protegido.
> > > Tus apuntes van donde han ido siempre: **`00_Apuntes/Trimestre_1/`**, que es tu repositorio `apuntes-sor-t1` y **sí puedes empujar**. Esa es la razón de fondo por la que la bóveda está partida en dos desde la **Bloque 0 · Fase 0.1.a**. Hoy la has tocado con las manos.
> >
> > **Y la norma que vas a oírme todo el curso:** `commit` y `push` **al terminar cada sesión de trabajo**. No cuando te acuerdes, no el viernes. Al terminar.
> > Escríbelo en tu entrada de hoy con tus palabras. Es la respuesta que más peso tiene de esta fase.
>
> > [!note] 📌 Esto lo volveremos a ver, y con calma
> > Los retos de hoy son un aperitivo, hechos deprisa sobre material que acabas de clonar. En la **Bloque 0 · Fase 0.7** los repetiremos **sobre todo tu trabajo del curso** —apuntes incluidos—, con la teoría detrás y las comprobaciones de seguridad que hoy nos hemos saltado porque aquí no arriesgabas nada.

> [!example] Paso 5: Cierra el vídeo, nómbralo y súbelo
> Detén la grabación, nombra el vídeo `B0.4.b · Tres retos de recuperación` y súbelo a la playlist `B0_Prerrequisitos` (No listado). **Cada reto lleva su timestamp**, que es lo que voy a mirar primero:
> ```
> 00:00 Presentacion
> 00:30 RETO 1 - Borrar las fases y recuperarlas con git restore
> 01:50 RETO 2 - Borrar B2_Ubuntu_Local entera y clonar
> 03:20 RETO 3 - Mis propias notas sin push (NO vuelven)
> 04:40 Repaso final
> ```
> Y en tu **entrada de apuntes**, además de las respuestas, contesta a esto con tus palabras: **¿por qué el Reto 2 no se arregla igual que el Reto 1, y por qué en el Reto 3 no vuelve todo?** Es la pregunta que resume la fase.

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | `fatal: you must specify path(s) to restore`. | Escribiste `git restore` **sin el punto**. | `git restore .` — el punto significa *"todo desde aquí hacia abajo"*. |
> | `git restore .` no recupera nada. | No estás dentro de la carpeta del repositorio. | `pwd`: tienes que estar en `B2_Ubuntu_Local`, no en `01_Practicas`. |
> | Tras el Reto 2, `git clone` dice `destination path already exists`. | La carpeta no se borró del todo. | Bórrala por completo y repite. |
> | Tras el Reto 2 falta `MIS_DATOS.md`. | No le hiciste `push` en la 0.4.a. | No hay solución: no estaba en GitHub. Es justo la lección del reto. |
> | En el Reto 3 el `push` no falla. | Estás en la carpeta equivocada, o clonaste el Bloque 1 de tu cuenta. | `git remote -v`: en `B1_Entorno` debe poner **`sor-iesjj`**. |
> | `Permission denied (publickey)` al reclonar. | Tu clave SSH no responde en ese equipo. | Repasa la **Bloque 0 · Fase 0.2.2**, o clona ese repositorio por **HTTPS** si es público. |
> | La pantalla se queda atascada tras `git log`. | Estás en el **paginador**. | Pulsa **`q`**. |

> [!help] Preguntas Críticas
> 1. ¿Por qué el Reto 1 se arregla **sin Internet** y el Reto 2 no? Contéstalo diciendo **dónde estaba guardado** lo que recuperaste en cada caso.
> 2. En el Reto 3 llegaste a hacer `commit` y aun así perdiste las notas. **¿De qué sirvió ese commit?**
> 3. Un compañero guarda sus apuntes dentro de `01_Practicas/B1_Entorno/`. **Dile en dos frases por qué es mala idea** y dónde debería ponerlos.

---

### ✅ Checklist Final de la Fase 0.4.b

- [ ] **Reto 1 resuelto:** fases borradas y recuperadas con `git restore .`, explicando por qué no hizo falta Internet.
- [ ] **Reto 2 resuelto:** carpeta borrada entera y recuperada clonando, explicando por qué `git restore` ya no valía.
- [ ] **Reto 3 resuelto:** notas propias perdidas, con el `push` rechazado enseñado en el vídeo.
- [ ] Explicado **dónde van tus notas** y por qué no dentro de mi material.
- [ ] Las tres carpetas de la 0.4.a siguen en su sitio y con su nombre.
- [ ] Vídeo `B0.4.b · Tres retos de recuperación` subido a la playlist, **con un timestamp por reto**.
- [ ] **Enlace del vídeo pegado en tu entrada de apuntes** de esta fase.
- [ ] Grabada **🏫 en el centro**.

> **Siguiente paso:** Fase 0.5 — Montar el mismo entorno **en casa** y sincronizar centro ↔ casa (va en 2 partes).
