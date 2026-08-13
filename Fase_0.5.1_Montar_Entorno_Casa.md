## 🏠 Fase 0.5.1: Montar el Entorno en Casa

### Instala, autentícate y reconstruye tu bóveda clonando tus repos ...

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0.5 — parte 1 de 2]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~1,5 horas (en casa) · **Requisitos:** Fases 0.1 a 0.4.b completas (con tu repositorio de apuntes ya en GitHub). En casa: un ordenador donde **sí** tengas permisos de administrador.


> [!abstract] 📋 Qué se te evalúa en esta fase
> **RA.01 · RA.05**
>
> | Código | Criterio de evaluación |
> | :--- | :--- |
> | `CE.01.g` | Se han aplicado preferencias en la configuración del entorno personal. |
> | `CE.05.d` | Se han realizado tareas de mantenimiento del software instalado en el sistema. |
>
> Los criterios están tomados literalmente del **RD 1691/2007** y de la programación del módulo.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin.
> 1. **Prepárate primero (sin grabar):** comprueba lo necesario, **léete el procedimiento entero** y **crea la entrada de apuntes de esta fase** en Obsidian: fichero `b0-0.5.1-entorno-en-casa.md` con la estructura del **Bloque 0 · Fase 0.1.b**, **vacía**. Rellenarla es cosa tuya, después; hoy solo tiene que existir.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a explicar la Fase 0.5.1 — Montar el entorno en casa."* Y **muestra tu perfil de GitHub** (o tu Teams/correo). Di qué vas a hacer.
> 3. **Graba TODO**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `B0.5.1 · Montar el entorno en casa` y súbelo a tu playlist **`B0_Prerrequisitos`** (No listado).
> 6. **~5 min.** Se graba en **🏠 casa** (en tu propio ordenador).
> 7. **La entrega va por la TAREA de Teams.** Cuando toque, abriré una tarea que cubrirá **esta fase y otras**; te llegará notificación. Tú, hoy: graba, sube el vídeo a la playlist y **pega su enlace en tu entrada de apuntes**.
> 8. **El enlace del vídeo va DENTRO de tu entrada de apuntes**, en el apartado `🔗 Enlaces`. No lo guardes en un papel: va ahí.

> [!danger] ⚠️ La bóveda de casa TAMPOCO va en OneDrive
> Igual que en el centro: la bóveda va **dentro de tu carpeta de usuario** (en `Documentos`, o directamente en tu carpeta personal), **fuera de OneDrive**. En casa haz la **misma comprobación** que hiciste en la Fase 0.1: si tu `Documentos` tiene el icono de **nube ☁️**, está sincronizado con OneDrive y no vale. Git y OneDrive se pelean. Tu "nube" es **GitHub**.

---

> [!info] 📌 Qué es realmente esta fase
> Es **la versión de casa de las Fases 0.1 a 0.4.b, todas juntas**: en el centro montaste el equipo del cole poco a poco; aquí dejas **tu ordenador de casa** en el mismo estado, de una sola vez (instalar → clave SSH → clonar tus repos). Lo que se hizo "una sola vez" (crear la cuenta de GitHub, crear los repos) **no** se repite: ya está hecho.

---

### 🎯 Objetivos

- [ ] Instalar en casa Obsidian, Git y OBS (en casa **sí** tienes permisos).
- [ ] Crear la **clave SSH del equipo de casa** y añadirla a GitHub.
- [ ] **Reconstruir la bóveda** en casa clonando tus repos desde GitHub.

---

### 📚 Fundamento Teórico

> [!info] Antes de empezar: no copies con pendrive, clona
> En el centro ya tienes todo subido a GitHub. En casa **no copias nada con pendrive**: **clonas desde GitHub**, que es donde está la versión buena. Así la copia de casa es idéntica a la del centro.

> [!warning] Una clave SSH por equipo
> La clave privada no se copia de un equipo a otro. En casa generas **una clave nueva** y la añades a GitHub (además de la del centro). Es normal tener varias.

---

### 🛠️ Procedimiento Práctico

> [!example] Paso 0: Prepárate (todavía SIN grabar)
> **Léete el procedimiento** (tiene **4 pasos** grabados). Ten **OBS** listo y tu **perfil de GitHub** en una pestaña.
> **Y antes de grabar: crea la entrada de apuntes de esta fase** (`b0-0.5.1-entorno-en-casa.md`) con la estructura pegada y **vacía**. En el vídeo solo tienes que **enseñarla**, no rellenarla.

> [!example] Paso 1: Arranca la grabación, preséntate e instala las herramientas
> Inicia la grabación, preséntate y **enseña tu perfil de GitHub**. Luego instala (en casa **sí** puedes):
> 1. **Obsidian** (`obsidian.md`), **Git** (`git-scm.com` / `sudo apt install git`), **OBS** (`obsproject.com`).
>    - 📎 **Los comandos exactos de instalación**, para Windows y para Linux, los tienes en la **nota de referencia de la Fase 0.2.1** ("cómo se instala Git por tu cuenta"). No los repito aquí: si cambian, cambian en un solo sitio.
>    - ⚠️ En Windows, al instalar Git **deja marcada la opción `Open Git Bash here`**: es la que te da el clic derecho sobre una carpeta que usas en todas las fases.
> 2. Comprueba: `git --version`.

> [!example] Paso 2: Clave SSH del equipo de casa
> ```bash
> ssh-keygen -t ed25519 -C "tu-correo-de-github"
> cat ~/.ssh/id_ed25519.pub
> ```
> Añade la clave **pública** a GitHub (`Settings → SSH and GPG keys → New SSH key`), título **`Equipo Casa`**. Configura también Git:
> ```bash
> git config --global user.name "Tu Nombre"
> git config --global user.email "tu-correo-de-github"
> ```
> Verifica: `ssh -T git@github.com` → `Hi TU-USUARIO!`.

> [!example] Paso 3: Reconstruye la bóveda clonando tus repos
> 1. Crea la estructura contenedor (local, **fuera de OneDrive**). Sustituye `RUTA_SOR` por tu carpeta (la que apuntaste en la Fase 0.1: `~/Documents/SOR`, `~/Documentos/SOR` o `~/SOR`):
>    ```bash
>    mkdir -p RUTA_SOR/Boveda_SOR/00_Apuntes
>    mkdir -p RUTA_SOR/Boveda_SOR/01_Practicas
>    ```
>    Ejemplo si en casa usas Linux en español: `mkdir -p ~/Documentos/SOR/Boveda_SOR/00_Apuntes`
> 2. Clona tus apuntes **dentro de `00_Apuntes/`**, con nombre de carpeta `Trimestre_1`:
>    ```bash
>    cd RUTA_SOR/Boveda_SOR/00_Apuntes
>    pwd          # comprueba que estás donde crees
>    git clone git@github.com:TU-USUARIO/apuntes-sor-t1.git Trimestre_1
>    ```
> 3. Clona el material **dentro de `01_Practicas/`**. Son **tres**, los mismos que bajaste en el centro en la **Bloque 0 · Fase 0.4.a**:
>    ```bash
>    cd RUTA_SOR/Boveda_SOR/01_Practicas
>    git clone git@github.com:TU-USUARIO/bloque-2-ubuntu-local.git B2_Ubuntu_Local
>    git clone git@github.com:sor-iesjj/bloque-0-prerequisitos.git B0_Prerrequisitos
>    git clone git@github.com:sor-iesjj/bloque-1-entorno.git B1_Entorno
>    ```
>    > [!warning] ⚠️ Mira bien de quién es cada dirección: **no son todas iguales**
>    > | Repositorio | El dueño es | Por qué |
>    > | :--- | :--- | :--- |
>    > | `bloque-2-ubuntu-local` | **`TU-USUARIO`** | Es **tu copia**: el `Use this template` lo hiciste en el centro, y ahí dentro está tu trabajo |
>    > | `bloque-0-prerequisitos` · `bloque-1-entorno` | **`sor-iesjj`** | Material **mío**, que solo lees. No hay copia tuya que clonar |
>    >
>    > Si te equivocas y pones tu usuario en los dos últimos, Git te dirá `Repository not found`. Y si pones `sor-iesjj` en el primero, te bajarás **mi** Boochan sin tu trabajo dentro.
>
>    Aquí van los tres por SSH, que es la vía por defecto. Los dos míos también los puedes clonar por HTTPS, como en la 0.4.a: son públicos.
> 4. Abre Obsidian → **`Open folder as vault`** → tu `Boveda_SOR`.
>
> > [!note] 📌 El truco del nombre: al escribir `... .git Trimestre_1` al final, la carpeta se llama `Trimestre_1` (no `apuntes-sor-t1`), idéntica a la del centro.

> [!example] Paso 4: Cierra el vídeo, nómbralo y súbelo
> En Obsidian, en casa, debes ver la **misma estructura** que en el centro. Detén la grabación, nombra el vídeo `B0.5.1 · Montar el entorno en casa`, súbelo a la playlist `B0_Prerrequisitos` con **timestamps**.

---

### 🚩 Resolución de Problemas y Evaluación

> [!bug] Troubleshooting
> | Problema | Causa | Solución |
> | :--- | :--- | :--- |
> | En casa no me deja instalar. | Usuario sin permisos. | Usa una cuenta con administrador; si no, coméntamelo. |
> | La carpeta de apuntes se llama `apuntes-sor-t1`. | Olvidaste el nombre al final del clone. | Renómbrala a `Trimestre_1` o clona de nuevo con `... .git Trimestre_1`. |
> | Aparecen ficheros `... -MiPC.md` duplicados. | La bóveda está en OneDrive. | Sácala a una carpeta local. |

> [!help] Preguntas Críticas
> 1. ¿Por qué clonas desde GitHub en vez de copiar con pendrive?
> 2. ¿Por qué generas una clave SSH nueva en casa?
> 3. ¿Dónde NO debe estar la bóveda?

---

### ✅ Checklist Final de la Fase 0.5.1

- [ ] Obsidian, Git y OBS instalados en casa.
- [ ] Clave SSH de casa creada y añadida a GitHub (`Equipo Casa`).
- [ ] Estructura `Boveda_SOR` recreada (local, fuera de OneDrive) con los **cuatro** repositorios clonados en su sitio: `Trimestre_1`, `B0_Prerrequisitos`, `B1_Entorno` y `B2_Ubuntu_Local`.
- [ ] Vídeo `B0.5.1 · Montar el entorno en casa` subido a la playlist, con timestamps.
- [ ] **Enlace del vídeo pegado en tu entrada de apuntes** de esta fase.
- [ ] Grabada **🏠 en casa**.

> **Siguiente paso:** Fase 0.5.2 — El ciclo `pull → push` para sincronizar casa ↔ centro.
