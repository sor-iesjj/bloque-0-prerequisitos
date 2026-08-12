---
titulo: "Prueba diagnóstica inicial — SOR (2º SMR)"
modulo: SOR — Sistemas Operativos en Red
curso: 2º SMR
centro: IES Jorge Juan (Alicante)
profesor: Pedro Navarro Miralles
fecha: 2026-07-21
duracion: 15-20 min
tags: [SOR, Boochan, diagnostico, prerrequisitos]
---
# Prueba diagnóstica inicial — SOR

> [!info] Para qué sirve
> **No cuenta para nota.** Es un termómetro del primer día: mide si traes de 1º la base mínima para empezar el proyecto Boochan. El profesor la usa para saber a quién reforzar y en qué, antes de la Fase 1. Contesta con sinceridad: si no sabes algo, escribe "no lo sé" — es información útil, no un suspenso.

**Nombre:** ______________________  **Fecha:** __________  **Rama que haré:** ☐ Ubuntu (.0)  ☐ Windows (.1)

---

## Bloque A — Redes (Módulo: Redes Locales) 🔴

**A1.** En la dirección `10.10.10.10/24`, ¿qué significa el `/24`? ¿Cuántos bits usa la máscara de red?

**A2.** Escribe la máscara de subred de un `/24` en formato decimal (los cuatro números).

**A3.** ¿Para qué sirve la **puerta de enlace (gateway)** de un equipo? Si una tarjeta de red **no** necesita salir a Internet, ¿qué pondrías en su gateway?

**A4.** ¿Qué hace un servidor **DNS**? Pon un ejemplo de qué "traduce".

**A5.** ¿Qué hace un servidor **DHCP**? ¿Por qué a veces interesa **desactivarlo** y poner la IP a mano?

**A6.** Estás en tu ordenador y quieres comprobar si "ves" a otra máquina de la red con IP `10.10.10.10`. ¿Qué **comando** usarías?

**A7.** Explica en una frase la diferencia entre un **cliente** y un **servidor**.

**A8.** *(Reconocer)* Une cada servicio con su puerto: `RDP` · `DNS` · `SMB (compartir archivos)`  →  `445` · `3389` · `53`.

---

## Bloque B — Sistemas Operativos y Virtualización (Módulo: Sistemas Operativos Monopuesto) 🔴

**B1.** ¿Qué es un archivo **`.ISO`** y para qué se usa al instalar un sistema operativo?

**B2.** ¿Qué es una **máquina virtual (VM)**? En virtualización, explica con tus palabras qué es el **anfitrión (host)** y qué es el **invitado (guest)**.

**B3.** Nombra un programa que sirva para crear máquinas virtuales.

**B4.** *(Según tu rama)*
- **Ubuntu:** ¿qué comando usas para **listar** el contenido de una carpeta? ¿Y para **cambiar** de carpeta?
- **Windows:** ¿sabes qué es **PowerShell** y para qué se usa una consola de comandos en un servidor?

**B5.** ¿Qué es un **usuario** y qué es un **grupo** en un sistema operativo? ¿Por qué se usan grupos en vez de dar permisos uno a uno?

**B6.** En un archivo o carpeta, ¿qué significan los permisos de **lectura**, **escritura** y **ejecución**? Pon un ejemplo de cuándo darías solo lectura.

---

## Bloque C — Hardware (Módulo: Montaje y Mantenimiento) 🟡

**C1.** Si un portátil tiene **8 GB de RAM en total**, ¿te parece buena idea asignarle 7 GB a una máquina virtual? Razona por qué sí o por qué no.

**C2.** *(Reconocer)* Al intentar arrancar una máquina virtual, a veces hay que activar la **"virtualización por hardware" (VT-x / AMD-V)**. ¿Sabes dónde se activa eso? (pista: no es en Windows).

---

## Bloque D — Actitud técnica (transversal)

**D1.** Durante la instalación de un servidor creas un usuario y una contraseña. ¿Qué haces con esa contraseña para no perderla? ¿La reutilizas de otra cuenta tuya?

**D2.** Te aparece un mensaje de error en pantalla **en inglés** que no entiendes. ¿Qué haces? (marca todas las que apliques)
☐ Cierro y vuelvo a empezar sin leerlo  ☐ Lo leo con calma / lo traduzco  ☐ Lo busco en Internet  ☐ Aviso al profesor con el texto exacto del error

---

---

# 🔑 SOLUCIONARIO Y BAREMO (uso del profesor)

> [!caution] No repartir esta parte a los alumnos.

## Respuestas esperadas

**A1.** `/24` = los primeros **24 bits** son de red. Máscara de 24 bits. · **A2.** `255.255.255.0`. · **A3.** Es la "salida" hacia otras redes/Internet; el router al que se manda lo que no es de la red local. Si no necesita Internet → **en blanco / vacío**. · **A4.** Traduce **nombres a IPs** (`google.com` → `142.250.x.x`). · **A5.** Reparte IPs automáticamente. Se desactiva cuando quieres **IP fija/estática** que no cambie (un servidor). · **A6.** `ping 10.10.10.10`. · **A7.** El cliente **pide** un servicio; el servidor lo **ofrece/responde**. · **A8.** RDP→3389, DNS→53, SMB→445.

**B1.** Imagen exacta de un disco de instalación en un solo archivo; se "monta" como si fuera el DVD del instalador. · **B2.** Un ordenador simulado por software. Host = la máquina física real; guest = el SO que corre dentro. · **B3.** VirtualBox / Hyper-V / VMware. · **B4.** Ubuntu: `ls` y `cd`. Windows: consola/PowerShell para administrar por comandos. · **B5.** Usuario = una identidad; grupo = conjunto de usuarios. Grupos → dar permisos a muchos de golpe, más mantenible. · **B6.** Lectura=ver/abrir, escritura=modificar/borrar, ejecución=ejecutar. Solo lectura: un documento que todos consultan pero nadie debe cambiar.

**C1.** No: dejaría al host (Windows/macOS + navegador + la propia VM) sin RAM → todo se congela. Hay que dejar margen al anfitrión. · **C2.** En la **BIOS/UEFI** del equipo.

**D1.** Se **anota** en lugar seguro; **no** se reutiliza una contraseña personal. · **D2.** Correctas: leer/traducir, buscar, avisar con el texto exacto. La primera (cerrar sin leer) es la mala.

## Baremo orientativo

| Bloque | Puntos | Umbral de alerta |
|---|---|---|
| A — Redes | 8 (1 c/u) | **< 5 → riesgo alto**: caerá en la Fase 1 |
| B — SO/Virtualización | 6 (1 c/u) | **< 4 → riesgo alto**: caerá al instalar/crear la VM |
| C — Hardware | 2 | Informativo (no bloqueante) |
| D — Actitud | 2 | Informativo (pero importante) |

> [!tip] Lectura rápida del resultado
> - **A ≥ 5 y B ≥ 4** → listo para empezar Boochan.
> - **A < 5** → sesión de refuerzo de redes (IP/máscara/gateway/DNS/DHCP/ping) **antes** de la Fase 1.
> - **B < 4** → taller "instala una VM desde una ISO" antes de la Fase 1.
> - **Muchos alumnos flojos en lo mismo** → refuerzo colectivo; si es puntual → apoyo individual/tutoría entre iguales.

---

*Diagnóstico basado en [[Prerrequisitos_1SMR_para_Boochan]]. Cubre lo marcado 🔴 (crítico) y muestrea 🟡. Transversal a las 6 versiones Boochan.*
