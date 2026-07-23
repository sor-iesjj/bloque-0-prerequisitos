## 🏠 Fase 0.5.1: Montar el Entorno en Casa

### Instala, autentícate y reconstruye tu bóveda clonando tus repos ...

> **[Módulo: SOR — Sistemas Operativos en Red]**
> **[Bloque de Prerrequisitos · Fase 0.5 — parte 1 de 2]**
> **Profesor:** Pedro Navarro Miralles · IES Jorge Juan (Alicante)
>
> **⏱️ Tiempo estimado:** ~1,5 horas (en casa) · **Requisitos:** Fases 0.1 a 0.4 completas (con tus repos ya en GitHub). En casa: un ordenador donde **sí** tengas permisos de administrador.

---

> [!important] 📹 Obligaciones de grabación (LÉEME — es igual en TODAS las fases)
> Esta práctica se **graba entera con OBS**, de principio a fin.
> 1. **Prepárate primero (sin grabar):** comprueba lo necesario y **léete el procedimiento entero**.
> 2. **Arranca OBS y PRESÉNTATE:** *"Hola, me llamo [Nombre], 2.º SMR, en este vídeo voy a explicar la Fase 0.5.1 — Montar el entorno en casa."* Y **muestra tu perfil de GitHub** (o tu Teams/correo). Di qué vas a hacer.
> 3. **Graba TODO**, explicando cada paso en voz alta.
> 4. **Timestamps SIEMPRE:** `00:00 Presentación` + uno por paso.
> 5. **Al terminar:** nombra el vídeo `Fase 0.5.1 — Montar el entorno en casa` y súbelo a tu playlist **`00_Prerrequisitos`** (No listado).
> 6. **~5 min. Una sola entrega:** esta práctica se hace en **🏠 casa** (en tu propio ordenador).

> [!danger] ⚠️ La bóveda de casa TAMPOCO va en OneDrive
> Igual que en el centro: la bóveda va en una carpeta **local** (ej. `C:\SOR\` o `~/SOR/`), **fuera de OneDrive**. Git y OneDrive se pelean. Tu "nube" es **GitHub**.

---

> [!info] 📌 Qué es realmente esta fase
> Es **la versión de casa de las Fases 0.1 a 0.4, todas juntas**: en el centro montaste el equipo del cole poco a poco; aquí dejas **tu ordenador de casa** en el mismo estado, de una sola vez (instalar → clave SSH → clonar tus repos). Lo que se hizo "una sola vez" (crear la cuenta de GitHub, crear los repos) **no** se repite: ya está hecho.

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

> [!example] Paso 1: Arranca la grabación, preséntate e instala las herramientas
> Inicia la grabación, preséntate y **enseña tu perfil de GitHub**. Luego instala (en casa **sí** puedes):
> 1. **Obsidian** (`obsidian.md`), **Git** (`git-scm.com` / `sudo apt install git`), **OBS** (`obsproject.com`).
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
> 1. Crea la estructura contenedor (local, **fuera de OneDrive**):
>    ```bash
>    mkdir -p ~/SOR/Boveda_SOR/00_Apuntes
>    mkdir -p ~/SOR/Boveda_SOR/Practicas
>    ```
> 2. Clona tus apuntes **dentro de `00_Apuntes/`**, con nombre de carpeta `Trimestre_1`:
>    ```bash
>    cd ~/SOR/Boveda_SOR/00_Apuntes
>    git clone git@github.com:TU-USUARIO/apuntes-sor-t1.git Trimestre_1
>    ```
> 3. Clona la práctica **dentro de `Practicas/`**:
>    ```bash
>    cd ~/SOR/Boveda_SOR/Practicas
>    git clone git@github.com:TU-USUARIO/boochan-1.git
>    ```
> 4. Abre Obsidian → **`Open folder as vault`** → `~/SOR/Boveda_SOR`.
>
> > [!note] 📌 El truco del nombre: al escribir `... .git Trimestre_1` al final, la carpeta se llama `Trimestre_1` (no `apuntes-sor-t1`), idéntica a la del centro.

> [!example] Paso 4: Cierra el vídeo, nómbralo y súbelo
> En Obsidian, en casa, debes ver la **misma estructura** que en el centro. Detén la grabación, nombra el vídeo `Fase 0.5.1 — Montar el entorno en casa`, súbelo a la playlist `00_Prerrequisitos` con **timestamps**.

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
- [ ] Estructura `Boveda_SOR` recreada (local, fuera de OneDrive) con los repos clonados en su sitio.
- [ ] Vídeo `Fase 0.5.1 — Montar el entorno en casa` subido a la playlist, con timestamps.
- [ ] Una sola entrega, hecha **🏠 en casa**.

> **Siguiente paso:** Fase 0.5.2 — El ciclo `pull → push` para sincronizar casa ↔ centro.
