---
titulo: "Prerrequisitos de 1º SMR para el itinerario Boochan (SOR)"
modulo: SOR — Sistemas Operativos en Red
curso: 2º SMR
centro: IES Jorge Juan (Alicante)
profesor: Pedro Navarro Miralles
fecha: 2026-07-21
tags: [SOR, Boochan, prerrequisitos, diagnostico, SMR]
---

# Prerrequisitos de 1º SMR para el itinerario Boochan

> [!info] Qué es este documento
> Estudio del **conocimiento previo** que un alumno debe traer de **1º SMR** para poder enfrentarse a las prácticas Boochan de 2º (SOR) sin naufragar. Aplica por igual a **todos los bloques del proyecto** —el servidor en local y el servidor en la nube—, porque todos enseñan los mismos conceptos y asumen el mismo sustrato.

---

## Método

Boochan enseña de forma **autocontenida** los conceptos *nuevos* de cada servicio (hipervisor, dominio, ACL, VPN…): cada fase trae su "Fundamento Teórico" y su "Diccionario de Conceptos Clave". Pero **da por sabido un sustrato** que nunca explica desde cero. Cuando en la Fase 1 aparece `10.10.10.10/24`, "gateway", "DNS", "DHCP desactivado", `ping` o "adaptador NAT", el material asume que el alumno ya sabe qué es cada cosa.

Ese sustrato es el **conocimiento previo**, y se ha derivado leyendo lo que las fases realmente exigen (rama Ubuntu y rama Windows), no del currículo genérico. Procede de **tres módulos de 1º** más uno transversal.

---

## Los módulos de 1º que alimentan Boochan

| Módulo de 1º (SMR) | Peso en Boochan | Qué aporta |
|---|---|---|
| **Redes Locales** | 🔴 Crítico | Prerrequisito nº1. Sin base de redes, la Fase 1 ya es un muro. |
| **Sistemas Operativos Monopuesto** | 🔴 Crítico | Instalar SO, virtualizar, línea de comandos, usuarios/permisos locales. |
| **Montaje y Mantenimiento de Equipos** | 🟡 Medio | Dimensionar hardware (RAM/CPU/disco), BIOS/UEFI, virtualización por HW. |
| **Aplicaciones Ofimáticas** | 🟢 Bajo / transversal | Navegar, descargar ISOs, documentar, copiar/pegar en terminal. |

---

## Prerrequisitos concretos, mapeados a fase y nivel exigido

**Nivel exigido:**
- **Dominar** = tiene que saber hacerlo solo.
- **Reconocer** = basta con que le suene y sepa seguir el paso guiado.

### De Redes Locales (el núcleo)

| Concepto previo | Dónde muerde en Boochan | Nivel |
|---|---|---|
| Direccionamiento IPv4, máscara, notación `/24` (CIDR) | Fase 1 (IP estática `10.10.10.10/24`), toda la matriz de redes | **Dominar** |
| Puerta de enlace (gateway) y cuándo se deja en blanco | Fase 1 (adaptador interno sin gateway) | Dominar |
| DNS: qué es y cómo resuelve nombres | Fase 1, y sobre todo Fase 4 (el DC *es* el DNS) | Dominar |
| DHCP: qué es, activarlo/desactivarlo | Fase 1 (desactivar DHCP en la host-only) | Dominar |
| NAT y red privada vs. pública | Fase 1 (adaptador NAT = salida a Internet) | Reconocer |
| `ping` / ICMP para diagnosticar conectividad | Verificación de casi todas las fases | **Dominar** |
| Modelo cliente-servidor | Concepto vertebrador de todo el proyecto | Dominar |
| Puertos TCP/UDP (qué es un puerto, protocolo ↔ puerto) | Fases cloud: Security Groups abren 3389 RDP, 53 DNS, 445 SMB, 88 Kerberos, 389 LDAP, 51820 WireGuard | Reconocer |
| Subredes distintas y por qué no se solapan | Bloques en la nube (la red del proveedor ≠ la del túnel VPN) | Reconocer |

### De Sistemas Operativos Monopuesto

| Concepto previo | Dónde muerde | Nivel |
|---|---|---|
| Instalar un SO desde una ISO (particionado, teclado, usuario) | Fase 1 (Ubuntu Server / Windows Server desde cero) | **Dominar** |
| Virtualización básica: crear una VM, host vs. guest | Fase 1 local (VirtualBox/Hyper-V) y Fase 8 (VM cliente Win11) | **Dominar** |
| Moverse por la línea de comandos (Ubuntu) / consola (Windows) | Todas las fases de la rama que toque | **Dominar** |
| Usuarios y grupos **locales**, contraseñas | Fase 5 lo lleva al dominio, pero parte del concepto local | Dominar |
| Permisos de ficheros: rwx (Linux) / NTFS básico (Windows) | Fase 7 (ACL/ABE) parte de aquí | Dominar |
| Sistema de archivos y estructura de directorios | Fases 6-7 (rutas `C:\ShareData\...`, `/etc/...`) | Dominar |
| Servicios/procesos: arrancar, parar, ver estado | Fases 2-4 (gestionar demonios / servicios de Windows) | Reconocer |

### De Montaje y Mantenimiento de Equipos

| Concepto previo | Dónde muerde | Nivel |
|---|---|---|
| Dimensionar RAM/CPU/disco con criterio | Fase 1 (2 GB → 4 GB para Samba; no ahogar el portátil) | Reconocer |
| BIOS/UEFI y virtualización por hardware (VT-x/AMD-V) | Fase 1 local (troubleshooting: "la VM no arranca") | Reconocer |

---

## Prerrequisitos críticos vs. deseables

> [!danger] 🔴 Sin esto naufragan en la Fase 1
> Direccionamiento IP + máscara · `ping` · instalar un SO desde ISO · crear una VM · moverse por la terminal.
> Si un alumno no trae esto, no es que le cueste: es que **no puede empezar**.

> [!success] 🟢 Deseables, que Boochan refuerza
> Puertos/protocolos · subredes · servicios. Boochan los reexplica lo justo; si vienen de 1º, el alumno va sobrado.

---

## Diferencia entre las dos ramas (Ubuntu vs. Windows)

Menor de lo que parece: **el prerrequisito es el mismo** (redes + SO + virtualización). Solo cambia el *dialecto* de la línea de comandos —bash/nano en las `.0`, PowerShell/Server Manager en las `.1`—. Un alumno con la base de 1º sólida sobrevive en ambas; la sintaxis concreta la enseña la propia fase.

---

## Competencias transversales que Boochan también asume

- Leer mensajes de error e interfaces **en inglés**.
- Seguir un procedimiento paso a paso siendo **metódico**.
- **Anotar credenciales** y gestionarlas (lo repite en varias fases).

No pertenecen a un módulo concreto, pero son mortales si faltan.

---

## Correspondencia con los Resultados de Aprendizaje de SOR

Cada RA del módulo presupone competencias de 1º:

| RA de SOR | Fase(s) | Prerrequisito de 1º que lo sostiene |
|---|---|---|
| RA.01 — Instala SO en red | 1-3 | Instalar SO desde ISO · virtualización · redes (IP/gateway/DNS) |
| RA.02 — Gestiona usuarios y grupos | 5 | Usuarios/grupos y contraseñas locales |
| RA.03 — Gestiona dominios | 4 | DNS · modelo cliente-servidor · servicios |
| RA.04 — Gestiona recursos compartidos | 6-7 | Permisos de ficheros (rwx / NTFS) · sistema de archivos |
| RA.06 — Integra SO libres y propietarios | 8 | Virtualización (VM cliente) · redes · cliente-servidor |

---

## Recomendación docente

1. **Prueba diagnóstica el primer día** (15-20 min): ver [[Prueba_Diagnostica_Inicial_SOR]]. Detecta al instante qué alumnos entran en riesgo y en qué fase caerán.
2. **Refuerzo exprés** de lo 🔴 antes de la Fase 1 para quien lo necesite: una sesión de redes básicas (IP/máscara/gateway/ping) y otra de instalar-una-VM cubren la mayor parte del riesgo.

---

*Este documento es transversal: lo que pide vale para cualquier bloque del proyecto, montes el servidor en tu ordenador o en la nube.*
