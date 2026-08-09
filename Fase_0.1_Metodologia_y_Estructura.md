## 🧭 Fase 0.1: Metodología de Trabajo y Estructura de la Bóveda

### Cómo vamos a trabajar todo el curso (y por qué así) — **ÍNDICE · 3 partes**

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0 — Puesta a punto del entorno de trabajo]**
> Esta fase **no** enseña redes ni servidores todavía: monta el **método** con el que trabajaremos el resto del curso. Sin esto, nada de lo que venga después se puede entregar ni corregir.
>
> **Profesor:** Pedro Navarro Miralles
> **Correo:** p.navarromiralles2@edu.gva.es
> **Centro:** IES Jorge Juan (ALICANTE)
>
> **⏱️ Tiempo estimado:** ~1,5 - 2 horas (lectura + montar el canal de vídeo + práctica grabada)
> **Requisitos:** Obsidian y OBS ya instalados en el equipo (los instala Consellería — tú no tienes permisos). Necesitarás una **cuenta de Gmail/YouTube** (la creas en el Paso previo). No hace falta Git en esta fase todavía.

---

## 🗺️ **LAS TRES PARTES DE ESTA FASE**

> [!important] Léelas en orden. La `c` es la única que se graba
> | | Parte | Qué hay dentro | Cuándo |
> | :--- | :--- | :--- | :--- |
> | 📗 | **[[Fase_0.1.a_Obsidian_y_la_Boveda\|a · Obsidian y la bóveda]]** | Qué es una bóveda · apuntes vs. prácticas · por qué las carpetas se llaman como los bloques · **diccionario** | Antes de tocar el ordenador |
> | 📘 | **[[Fase_0.1.b_El_Sistema_de_Apuntes\|b · El sistema de apuntes]]** | La regla de oro · **el nombre del fichero** · **la plantilla** · por qué se graba todo | Hoy, y **todo el curso** |
> | 📙 | **[[Fase_0.1.c_Procedimiento\|c · Procedimiento]]** | **Paso previo** (montar el canal) + los **6 pasos grabados** · problemas frecuentes | Con OBS delante |

> [!danger] 🔖 La parte `b` no es de un día: es tu manual de referencia
> Cuando en **cualquier** práctica del curso leas *"crea tu entrada de apuntes con la estructura del **Bloque 0 · Fase 0.1.b**"*, se refiere a **[[Fase_0.1.b_El_Sistema_de_Apuntes|la parte b]]**.
>
> **Márcala en Obsidian** (clic derecho sobre la nota → `Add to bookmarks`). La vas a abrir cien veces.

---

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
> 1. **Prepárate primero (sin grabar):** comprueba que tienes lo necesario y **léete el procedimiento entero**. *(En esta primera fase la entrada de apuntes la creas **dentro** de la práctica, en el Paso 5: todavía no sabes cómo se hace. **A partir de la 0.2.1, crearla será lo PRIMERO que hagas**, antes de grabar.)*
> 2. **Arranca OBS y, nada más empezar, PRESÉNTATE:** *"Hola y bienvenidos. Me llamo [Nombre], soy alumno de 2.º SMR, y en este vídeo voy a explicar la Fase 0.1 — Metodología y estructura de la bóveda."* Y **muestra en pantalla algo que demuestre que eres tú** (tu **Teams** o tu **correo `@alu.edu.gva.es`** con tu nombre; cuando tengas GitHub, tu perfil). Di **qué vas a hacer**.
> 3. **Graba TODO el procedimiento**, explicando cada paso en voz alta mientras lo haces.
> 4. **Timestamps SIEMPRE** en la descripción del vídeo: `00:00 Presentación` y **uno por cada paso** (formato `mm:ss`).
> 5. **Al terminar:** nombra el vídeo `B0.1 · Metodología y estructura`, **súbelo a tu playlist de YouTube `B0_Prerrequisitos`** (No listado) y **pega su enlace en tu entrada de apuntes**.
> 6. **~5 min.** Se graba en **🏫 el centro** (el equipo de casa se monta entero en la Fase 0.5.1, no aquí).
> 7. **La entrega va por la TAREA de Teams.** Cuando toque, abriré una tarea que cubrirá **esta fase y otras**; te llegará notificación. Tú, hoy: graba, sube el vídeo a la playlist y **pega su enlace en tu entrada de apuntes**.

---

## 🎯 **OBJETIVOS DE LA FASE**

Al terminar serás capaz de:

- [ ] Explicar con tus palabras qué es una **bóveda** de Obsidian y para qué la usamos. → *parte a*
- [ ] Explicar la diferencia entre **tus apuntes** y las **prácticas**, y por qué viven en carpetas separadas. → *parte a*
- [ ] Nombrar una entrada de apuntes **con el formato obligatorio** y saber qué lleva dentro. → *parte b*
- [ ] Tener tu **canal de YouTube** con la playlist `B0_Prerrequisitos` lista. → *parte c*
- [ ] Comprobar si tu carpeta `Documentos` está en OneDrive, y crear tu bóveda `Boveda_SOR` en la ruta correcta (sabiendo **por qué** no puede vivir en OneDrive). → *parte c*
- [ ] Crear la **estructura de carpetas** exacta que usaremos todo el curso. → *parte c*
- [ ] Escribir tu **primera entrada de apuntes**. → *parte c*
- [ ] **Grabar la práctica entera con OBS**, presentándote, y subirla a tu playlist. → *parte c*
- [ ] Distinguir **subir a la playlist** (organizar) de **entregar en la tarea de Teams** (evaluar).

---

## 🎯 **¿DÓNDE ESTAMOS?**

> [!info] El punto de partida
> Este es el primer día de verdad. No vamos a tocar servidores todavía: primero vamos a montar **tu forma de trabajar conmigo durante todo el curso**.
>
> En este módulo vas a hacer **prácticas** que imitan situaciones reales de un técnico (las prácticas *Boochan*, en recuerdo de Iker y Héctor), y a la vez vas a **tomar apuntes** de todo lo que expliquemos. Las dos cosas se entregan, y las dos cuentan para nota.

> [!warning] El problema
> Un técnico no memoriza: **documenta**. Si no tienes un sitio ordenado donde anotar lo que haces, dentro de dos semanas no te acordarás de nada, no podrás repetir una práctica en casa, y yo no podré corregir tu trabajo.
>
> Por eso lo primero no es "instalar cosas", es **decidir dónde y cómo se guarda la información** — y que todos lo hagamos exactamente igual.

> [!success] Objetivo de esta fase
> Dejar montada, en tu equipo, una **bóveda de Obsidian** llamada `Boveda_SOR` con una estructura de carpetas fija: una zona para **tus apuntes** (por trimestres) y otra para las **prácticas**. Y entregar el **vídeo grabado** de todo el proceso en tu playlist de YouTube.

---

## ❓ **PREGUNTAS CRÍTICAS** *(van en tu entrada de apuntes)*

> [!help] Autoevaluación
> 1. ¿Qué es una bóveda de Obsidian? ¿Es un formato especial o una carpeta normal?
> 2. ¿Qué diferencia hay entre la carpeta `00_Apuntes/` y la carpeta `01_Practicas/`?
> 3. ¿Por qué **no** guardamos la bóveda dentro de OneDrive?
> 4. ¿En qué momento del vídeo te presentas y demuestras que eres tú: al principio o al final?
> 5. 🔬 **Reto:** sin mirar la guía, dibuja en un papel el árbol de carpetas de la bóveda. Luego compáralo con Obsidian: ¿te faltaba alguna?

---

## ✅ **CHECKLIST FINAL DE LA FASE 0.1**

- [ ] Leídas las partes **[[Fase_0.1.a_Obsidian_y_la_Boveda|a]]** y **[[Fase_0.1.b_El_Sistema_de_Apuntes|b]]** antes de grabar.
- [ ] Canal de YouTube creado con la playlist `B0_Prerrequisitos`.
- [ ] Obsidian y OBS comprobados en el equipo (instalados por Consellería).
- [ ] Carpeta `Documentos` comprobada (¿nube o local?) y bóveda `Boveda_SOR` creada en una ruta **local** (no en OneDrive).
- [ ] **Tu ruta apuntada** en un papel o una nota.
- [ ] Estructura de carpetas exacta: `00_Apuntes/` (con `Trimestre_1/2/3` y `B0_Prerrequisitos` en T1) + `01_Practicas/`.
- [ ] Vídeo grabado **de principio a fin**, con presentación e identidad al inicio.
- [ ] Vídeo nombrado `B0.1 · Metodología y estructura` y subido a la playlist `B0_Prerrequisitos`.
- [ ] Timestamps en la descripción (uno por paso).
- [ ] **Primera entrada escrita** en `B0_Prerrequisitos/`, con nombre `b0-0.1-metodologia-y-estructura.md` y la estructura obligatoria.
- [ ] **Enlace del vídeo pegado en tu entrada**, en el apartado `🔗 Enlaces`.
- [ ] **Preguntas Críticas contestadas** en tu entrada (el 🔬 Reto es voluntario).
- [ ] Grabada **🏫 en el centro**.

---

> **Siguiente paso:** **Fase 0.2** — crear tu cuenta de **GitHub** y configurar **Git** en el equipo, para poder enviarme tus apuntes por Internet y que yo pueda corregirlos.
