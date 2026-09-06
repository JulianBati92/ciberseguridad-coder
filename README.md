# Laboratorio de Ciberseguridad - Configuración de Entorno Aislado

## Introducción

Este laboratorio forma parte de las prácticas realizadas durante el curso de Ciberseguridad de Coderhouse.

El objetivo de esta actividad es crear un entorno de pruebas controlado utilizando VirtualBox y Kali Linux, aplicando conceptos de aislamiento de red y protección del estado inicial de una máquina virtual.

## Entorno utilizado

- **Host:** Windows 11
- **Virtualizador:** Oracle VirtualBox
- **Sistema invitado:** Kali Linux
- **Memoria RAM:** 2048 MB
- **Procesadores:** 2
- **Almacenamiento:** 40 GB
- **Adaptador de red:** Intel PRO/1000 MT Desktop
- **Modo de red:** Red Interna
- **Nombre de la red:** `intnet`

## Configuración de red

La máquina virtual fue configurada utilizando el modo **Red Interna (Internal Network)** de VirtualBox.

Se eligió esta modalidad porque el objetivo inicial del laboratorio es trabajar en un entorno controlado que no requiera acceso a Internet ni comunicación directa con la red doméstica. La Red Interna permite que las máquinas virtuales conectadas a la misma red virtual puedan comunicarse entre sí, manteniendo el laboratorio separado de la red física del equipo anfitrión.

Esta configuración resulta adecuada para futuras prácticas de ciberseguridad, ya que permite incorporar otras máquinas virtuales y realizar pruebas dentro de un entorno aislado, reduciendo el riesgo de afectar dispositivos o servicios de la red real.

### Evidencia de configuración

![Configuración de Red Interna](evidencias/red-interna.png)

## ¿Por qué no utilizar modo Puente (Bridged)?

No se utilizó el modo Puente porque este conecta la máquina virtual directamente con la red física a través del adaptador de red del equipo anfitrión. De esta manera, Kali Linux podría obtener conectividad dentro de la misma red doméstica que otros dispositivos físicos.

Para un laboratorio de ciberseguridad esto representa un nivel de exposición innecesario, especialmente cuando posteriormente pueden realizarse pruebas de análisis, escaneo o configuración de servicios. Utilizar una Red Interna permite mantener las pruebas dentro de un entorno virtual controlado.

## Snapshot del estado inicial

Una vez finalizada la instalación de Kali Linux, se creó una instantánea denominada:

**Instalación Base Limpia**

El objetivo del snapshot es conservar un punto de restauración correspondiente al estado inicial de la máquina virtual. De esta manera, si durante futuras prácticas se realizan cambios, configuraciones o pruebas que alteren el sistema, es posible regresar al estado base del laboratorio.

### Evidencia del snapshot

![Snapshot Instalación Base Limpia](evidencias/snapshot-base-limpia.png)

## Conclusión

La configuración realizada permite disponer de un laboratorio de pruebas aislado utilizando Kali Linux y VirtualBox.

La utilización de una Red Interna reduce la exposición de la máquina virtual frente a la red doméstica, mientras que el snapshot permite recuperar fácilmente el estado inicial del sistema.

Esta configuración constituye una base segura para continuar con futuras prácticas de análisis y seguridad informática.