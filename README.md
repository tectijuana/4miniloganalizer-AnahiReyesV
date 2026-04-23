[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/EbtZGzoI)
[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=23684364)

# Práctica 1

## Implementación de un Mini Cloud Log Analyzer en ARM64
**Nombre:** Reyes Velasquez Anahi

**No. Control:** 23212056

**Horario:** 4:00 pm

**Modalidad:** Individual

**Entorno de trabajo:** AWS Ubuntu ARM64 + GitHub Classroom

**Lenguaje:** ARM64 Assembly (GNU Assembler) + Bash + GNU Make

---

## Introducción

Los sistemas modernos de cómputo en la nube generan continuamente registros (*logs*) que permiten monitorear el estado de servicios, detectar fallas y activar alertas ante eventos críticos.

Este programa implementa un analizador básico de logs en lenguaje ensamblador ARM64. Su función principal es leer códigos de estado HTTP desde la entrada estándar (stdin), procesarlos y clasificarlos en tres categorías: respuestas exitosas (2xx), errores del cliente (4xx) y errores del servidor (5xx).

A través de esta implementación se utilizan estructuras de control, manejo de registros y llamadas al sistema en Linux, permitiendo comprender cómo se procesan datos a bajo nivel y cómo se construye lógica de análisis directamente en ensamblador.

El programa procesará códigos de estado HTTP suministrados mediante entrada estándar (stdin):

```bash id="y1gcmc"
cat logs.txt | ./analyzer
```

---

## Objetivo general

Desarrollar un programa en lenguaje ensamblador ARM64 capaz de procesar códigos de estado HTTP desde la entrada estándar, clasificarlos según su categoría (2xx, 4xx y 5xx) y contabilizar su frecuencia, aplicando conceptos fundamentales de programación a bajo nivel en un entorno Linux.

---

## Objetivos específicos

El estudiante aplicará:

* programación en ARM64 bajo Linux
* manejo de registros
* direccionamiento y acceso a memoria
* instrucciones de comparación
* estructuras iterativas en ensamblador
* saltos condicionales
* uso de syscalls Linux
* compilación con GNU Make
* control de versiones con GitHub Classroom

Estos temas se alinean con contenidos clásicos de flujo de control, herramientas GNU, manejo de datos y convenciones de programación en ensamblador.   

---

## Material proporcionado

Se entregará un repositorio preconfigurado que contiene:

* plantilla base en ARM64
* archivo `Makefile`
* script Bash de ejecución
* archivo de datos (`logs.txt`)
* pruebas iniciales
* secciones marcadas con `TODO`

El estudiante deberá completar la lógica correspondiente.

---

## Variantes de la práctica

### Variante A

Contabilizar:

* respuestas exitosas (2xx)
* errores del cliente (4xx)
* errores del servidor (5xx)

---

### Variante B

Determinar el código de estado más frecuente.

---

### Variante C

Detectar el primer evento crítico (503).

---

### Variante D

Detectar tres errores consecutivos.

---

### Variante E

Calcular índice de salud:

```text id="2u4vvx"
Health Score = 100 - (errores × 10)
```

---

## Compilación

```bash id="bmubtb"
make
```

---

## Ejecución

```bash id="gcqlf2"
cat logs.txt | ./analyzer
```
<img width="1278" height="291" alt="Captura de pantalla 2026-04-22 165402" src="https://github.com/user-attachments/assets/e3dfff84-6176-4db4-9982-28f69ebc97dc" />

##

**Video en asciinema:**  https://asciinema.org/a/pOHEiuekcZlCaVt8

---

## Entregables

Cada estudiante deberá entregar en su repositorio:

* archivo fuente ARM64 funcional
* solución implementada
* README explicando diseño y lógica utilizada
* evidencia de ejecución
* commits realizados en GitHub Classroom

---

## Criterios de evaluación

| Criterio                    | Ponderación |
| --------------------------- | ----------- |
| Compilación correcta        | 20%         |
| Correctitud de la solución  | 35%         |
| Uso adecuado de ARM64       | 25%         |
| Documentación y comentarios | 10%         |
| Evidencia de pruebas        | 10%         |

---

## Restricciones

No está permitido:

* resolver la lógica en C
* resolver la lógica en Python
* modificar la variante asignada
* omitir el uso de ARM64 Assembly

---

## Competencia a desarrollar

Comprender cómo un problema de procesamiento de datos es implementado a nivel máquina mediante instrucciones ARM64.



---

## Nota

Aunque este problema puede resolverse fácilmente en lenguajes de alto nivel, el propósito de la práctica es implementar **cómo lo resolvería la arquitectura**, no únicamente obtener el resultado.

