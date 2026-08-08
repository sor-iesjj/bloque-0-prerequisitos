## 📘 Fase 0.1.b: El sistema de apuntes

### Cómo se llama y qué lleva dentro cada entrada — **de aquí no te vas a mover en todo el curso**

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0.1 — parte b de c]**
>
> 🧭 **Índice de la fase:** [[Fase_0.1_Metodologia_y_Estructura]]
>
> **📍 Cuándo se lee:** hoy entera. Y **cada vez que empieces una entrada nueva**, durante todo el curso.

---

> [!danger] 🔖 ESTA ES LA PÁGINA QUE MÁS VAS A ABRIR. MÁRCALA
> No es teoría de un día: es **el manual de referencia de tus apuntes**. Aquí está el nombre que le pones a cada fichero y la plantilla que va dentro.
>
> Cuando en cualquier práctica del curso —prerrequisitos, curso de Git, curso de Shell, Boochan— leas *"crea tu entrada de apuntes con la estructura del **Bloque 0 · Fase 0.1.b**"*, **se refiere a esta página**.
>
> En Obsidian: clic derecho sobre esta nota → **`Add to bookmarks`**. Treinta segundos que te ahorran buscarla cincuenta veces.

---

## **1 · LA REGLA DE ORO: DONDE HAY VÍDEO, HAY ENTRADA**

> [!important] De esta norma sale tu nota de apuntes
> - **Una fase = una entrada.** Ni más ni menos.
> - **Si una fase dura varios días**, NO creas una entrada nueva cada día: **abres la de siempre y sigues escribiendo**. Toda la fase, en un solo sitio.
> - **Si un día hacemos dos fases**, escribes **dos** entradas, no una. La 0.2.1 y la 0.2.2 la misma tarde son dos ficheros con la misma fecha y distinto título.
> - **Si damos teoría que no pertenece a ninguna fase**, esa clase también tiene su entrada, con el tema como título.
> - **La entrada se CREA al empezar la fase**, antes incluso de arrancar OBS: con su nombre y su estructura pegada, aunque esté vacía. En el vídeo solo tienes que **enseñarla**. **Rellenarla es cosa tuya, a tu ritmo**, mientras dure la fase — no hay que grabarse escribiendo.

> [!info] 🎓 Por qué así, y por qué te conviene
> 1. **La entrada es donde vive el enlace de tu vídeo.** Una entrada por fase = tu repositorio me cuenta sola la historia: qué hiciste, qué entendiste y dónde está el vídeo que lo demuestra. Si me falta una entrada, sé exactamente qué fase falta.
> 2. **Para ti, en junio.** Buscar *"lo de las claves SSH"* en un fichero llamado `b0-0.2.2-clave-ssh` es inmediato. Buscarlo repartido en tres entradas de tres martes distintos es perder la tarde.

---

## **2 · 🔴 EL NOMBRE DEL FICHERO**

**Un fichero por fase**, dentro de la carpeta del bloque que toque. Y el nombre se construye **siempre igual, en todo el curso**:

```
material - código - titulo-corto . md
```

Todo en minúsculas, con guiones, **sin tildes ni espacios**.

| Trozo | Qué hace | Ejemplos |
| :--- | :--- | :--- |
| **material** | Dice **de dónde sale** | `b0` `b1` `b2` `b6` · `git` `shell` |
| **código** | **Ordena.** Los niveles se separan con **punto** | `0.2.2` · `1.4` · `1.2.1` |
| **título corto** | Dice **de qué va**. Los espacios, con guion | `clave-ssh` |

**✅ Correcto:**
`b0-0.2.2-clave-ssh.md` · `b2-1.4-verificacion-y-acceso-remoto.md` · `git-1.2.1-amplia-el-manual.md`

**❌ Incorrecto:**
`apuntes dia 1.md` *(no dice nada)* · `Fase 0.1.md` *(espacios y mayúsculas)* · `0.1.md` *(no dice de qué va ni de dónde sale)*

> [!info] 🎓 Por qué el punto separa el código y el guion separa las palabras
> Para que **se vea dónde acaba el código y empieza el título**. En `b2-1.4-verificacion` no hay duda: el código es `1.4`.
>
> Si todo fueran guiones —`b2-1-4-verificacion`— tendrías que adivinar si el `4` es parte del código o la primera palabra del título. **Un carácter, un trabajo.**

> [!info] 📅 ¿Y la fecha? No va en el nombre
> No hace falta: **el código ya ordena**. `b0-0.1`, `b0-0.2.1`, `b0-0.2.2`, `b0-0.3`… se colocan solas y en el orden en que las hemos dado.
>
> Meter la fecha sería repetir información, y encima **descolocaría el orden** si una fase se retrasa. La fecha va **dentro** de la entrada, en su campo.

> [!tip] 💡 El prefijo ya dice el bloque
> Así que no lo repitas en palabras: `b0-0.2.2-clave-ssh` y **no** `b0-0.2.2-bloque-0-clave-ssh`.

> [!note] 📌 ¿Y los días de teoría, que no son ninguna fase?
> Esos **sí llevan fecha**, porque no tienen código que los ordene. Se nombran `teoria-MMDDAA-tema.md`:
>
> `teoria-091726-que-es-un-dominio.md`
>
> Así, dentro de la carpeta del bloque, **las fases van juntas y en orden, y la teoría va junta y por fecha**.

---

## **3 · 🔴 LA PLANTILLA — qué lleva dentro**

> [!important] La misma en TODO el curso
> Prerrequisitos, curso de Git, curso de Shell, Boochan y lo que venga después. **Se aprende una vez y se repite doscientas.**

Cópiala tal cual y rellénala:

```markdown
# b0-0.1 · Metodología y estructura

- **Alumno:** Nombre Apellido
- **Bloque:** B0 — Prerrequisitos
- **Fase / ejercicio:** Fase 0.1
- **Fecha de inicio:** 15/09/2026
- **Fecha de entrega:** 17/09/2026

---

## 🎯 Qué se pedía

(Dos o tres líneas con tus palabras: qué había que conseguir.)

## ⌨️ Comandos y pasos importantes

- `comando` — para qué sirve.

## 🛠️ Qué he hecho

(Los pasos que has seguido. No copies el enunciado: cuenta lo que hiciste tú.)

## 🚩 Qué me ha fallado y cómo lo he resuelto

(El mensaje de error LITERAL y qué hiciste. Si no falló nada, escribe "nada"
— pero piénsalo dos veces antes.)

## 🤔 Respuestas a las preguntas

1.
2.
3.

## 🔗 Enlaces

- **Vídeo de esta fase:** https://youtu.be/XXXXXXXXXXX
- **Playlist:** B0_Prerrequisitos

## 💭 Dudas / a repasar

- (lo que no te ha quedado claro)
```

---

## **4 · LOS TRES APARTADOS QUE MÁS PESAN**

> [!warning] ⚠️ 🚩 Los fallos — el que más se deja vacío, y el que más dice de ti
> **Una fase donde todo salió a la primera es casi siempre una fase que no se ha entendido**, o una donde se copió y pegó sin mirar.
>
> Anota el mensaje de error **literal**, no *"me dio un error"*. Te va a servir a ti dentro de tres semanas y a un compañero la semana que viene.

> [!warning] ⚠️ 🤔 Las respuestas — con tus palabras, no copiando
> Son las **Preguntas Críticas** que hay al final de cada fase. Las respuestas están en la teoría de esa misma fase: **si no sabes contestar, es que hay que releerla**. El **🔬 Reto**, cuando lo haya, es voluntario.

> [!danger] 🛑 🔗 El enlace — el del VÍDEO, no el de la playlist
> Son cosas distintas y aquí va **el del vídeo**. En YouTube: abre **ese vídeo**, `Compartir` → `Copiar enlace`. Te saldrá algo como `https://youtu.be/aB3dE5f...`.
>
> Si pegas el de la playlist (lleva `list=` dentro), me estás mandando a una lista de ocho vídeos para que adivine cuál es el de esta fase. **Eso no lo voy a hacer.**

> [!tip] 💭 Y las dudas no son de relleno
> El apartado **"Dudas"** es lo que me dice **en qué tengo que insistir**. Si lo dejas vacío siempre, o no te estás enterando de nada, o no te estás enterando de que no te enteras.

---

## **5 · POR QUÉ DOS FECHAS Y NO UNA**

> [!info] 📅 Porque una fase puede durarte varios días, y eso es normal
> **Lo que no se hace es abrir una entrada nueva cada día.** Abres la de la fase el primer día y sigues escribiendo en ella hasta terminarla.
>
> **Una entrada = una fase**, dure lo que dure.

---

## **6 · POR QUÉ SE GRABA TODO, Y DESDE EL PRINCIPIO**

> [!warning] Una práctica que no se graba, no cuenta
> Y se graba **de principio a fin**, no un repaso al final:
>
> - Grabar todo el proceso demuestra que **lo has hecho tú**, y me deja ver **cómo** lo haces: dónde dudas, dónde te atascas.
> - Por eso **primero te preparas** (te lees el procedimiento) y **luego grabas** del tirón: así el vídeo sale limpio y no lleno de *"espera, que no me acuerdo"*.
> - Cada fase se graba **una sola vez**, en el sitio que le toca: las **0.1 a 0.4** se hacen **en el centro**, y montar el equipo de **casa** es la **Fase 0.5.1**. Así no repites lo mismo dos veces.

---

> [!summary] 🎓 Qué te llevas de esta parte
> **Dos cosas, y las dos las vas a usar cien veces:** cómo se llama un fichero de apuntes (`material-código-titulo.md`) y qué lleva dentro (la plantilla de siete apartados).
>
> Si solo te marcas una página de todo el curso, **que sea esta**.
>
> **Siguiente:** [[Fase_0.1.c_Procedimiento]] — ahora sí, a montar la bóveda con OBS grabando.
