# Audio Equalizer + High-Pass Filter (Proof of Concept)

## Overview

This directory contains the **Proof of Concept (PoC)** developed prior to the PCB design of a 5-band analog audio equalizer.

The objective of this stage was to validate the behavior of each filter section individually and verify that the proposed architecture met the intended frequency response requirements before committing to hardware fabrication.

The equalizer is composed of the following frequency bands:

| Band | Description |
|--------|-------------|
| Sub | Sub-bass frequencies |
| Bass | Low-frequency content |
| Mid | Mid-range frequencies |
| High | Upper mid/high frequencies |
| Treble | High-frequency content |

Additionally, a **variable high-pass filter** was implemented, allowing a continuous frequency sweep from approximately **50 Hz** to **above 20 kHz**.

---

## Objectives

The proof-of-concept stage was conducted to:

- Validate the theoretical filter designs.
- Verify cutoff frequencies of each filter stage.
- Confirm expected attenuation slopes.
- Evaluate gain behavior within the passband.
- Identify practical limitations before PCB implementation.
- Compare simulation results with real-world measurements.

---

## Methodology

### 1. Circuit Simulation

Each filter stage was initially designed and analyzed through circuit simulation.

The simulations were used to:

- Estimate cutoff frequencies.
- Observe passband behavior.
- Verify expected attenuation rates.
- Confirm unity-gain operation where applicable.
- Detect potential design issues prior to prototyping.

---

### 2. Breadboard Prototype

After simulation, the circuits were assembled on a solderless breadboard.

The prototype allowed validation of:

- Real component tolerances.
- Operational amplifier behavior.
- Interaction between stages.
- Practical implementation constraints.

---

### 3. Laboratory Validation

The assembled circuits were tested using:

- DC power supply
- AC signal source
- Digilent Analog Discovery

Measurements were performed to compare theoretical and practical responses.

---

## Frequency Response Analysis

The primary validation method consisted of generating and analyzing **Bode diagrams** for each filter section.

The Analog Discovery was used to perform frequency sweeps and obtain:

- Magnitude response
- Cutoff frequencies
- Passband gain
- Roll-off characteristics

The measurements were compared against simulation results to verify compliance with the design objectives.

---

## Validation Criteria

The proof of concept was considered successful when the following conditions were met:

- Cutoff frequencies matched design expectations.
- Passband gain remained approximately unity where required.
- Filter transitions occurred at the expected frequencies.
- Attenuation slopes followed theoretical predictions.
- No significant instability or unexpected resonances were observed.

---

## Results

The experimental measurements demonstrated that the proposed filter stages behaved consistently with the simulated designs.

The Bode plots confirmed:

- Correct cutoff frequencies.
- Expected attenuation behavior.
- Stable operation across the audio spectrum.
- Proper functionality of the variable high-pass filter across its tuning range.

These results provided sufficient confidence to proceed with the PCB design stage.

---

## Development Flow

Filter Design
      │
      ▼
Circuit Simulation
      │
      ▼
Breadboard Prototype
      │
      ▼
Bode Analysis (Analog Discovery)
      │
      ▼
Design Validation
      │
      ▼
PCB Development

---

# Ecualizador de Audio de 5 Bandas + Filtro Pasa Altas Variable (Prueba de Concepto)

## Descripción General

Esta carpeta contiene la **Prueba de Concepto (Proof of Concept, PoC)** desarrollada previamente al diseño de la PCB de un ecualizador analógico de audio de 5 bandas.

El objetivo de esta etapa fue validar experimentalmente el comportamiento de cada una de las etapas de filtrado y comprobar que la arquitectura propuesta cumpliera con los requisitos de respuesta en frecuencia antes de proceder al diseño y fabricación de la tarjeta de circuito impreso.

El ecualizador está compuesto por las siguientes bandas de frecuencia:

| Banda | Descripción |
|---------|-------------|
| Sub | Frecuencias subgraves |
| Bass | Frecuencias graves |
| Mid | Frecuencias medias |
| High | Frecuencias medio-altas |
| Treble | Frecuencias agudas |

Adicionalmente, se implementó un **filtro pasa altas de frecuencia variable**, capaz de realizar un barrido continuo desde aproximadamente **50 Hz hasta más de 20 kHz**, permitiendo evaluar el comportamiento del sistema en distintas regiones del espectro audible.

---

## Objetivos

La etapa de prueba de concepto se realizó con los siguientes propósitos:

- Validar los diseños teóricos de los filtros.
- Verificar experimentalmente las frecuencias de corte calculadas.
- Comprobar las pendientes de atenuación esperadas.
- Evaluar la respuesta en banda pasante.
- Comparar resultados de simulación con mediciones reales.
- Detectar posibles limitaciones prácticas antes del diseño de la PCB.
- Confirmar la viabilidad de la arquitectura propuesta.

---

## Metodología

### 1. Simulación de Circuitos

Cada etapa de filtrado fue diseñada y analizada inicialmente mediante simulación.

Las simulaciones permitieron:

- Estimar las frecuencias de corte.
- Analizar la respuesta en frecuencia.
- Verificar la ganancia en banda pasante.
- Evaluar las pendientes de atenuación.
- Identificar posibles problemas de diseño antes de la implementación física.

---

### 2. Implementación en Protoboard

Una vez validados los diseños en simulación, los circuitos fueron ensamblados en protoboard para realizar pruebas experimentales.

Esta etapa permitió verificar:

- El comportamiento real de los componentes.
- El efecto de las tolerancias de fabricación.
- El funcionamiento de los amplificadores operacionales utilizados.
- La interacción entre las distintas etapas del sistema.
- La viabilidad práctica del diseño.

---

### 3. Validación Experimental

Las pruebas de laboratorio se realizaron utilizando:

- Fuente de alimentación DC.
- Generador de señales AC.
- Digilent Analog Discovery.

Los resultados obtenidos fueron comparados con las simulaciones para evaluar la precisión del diseño y validar su comportamiento.

---

## Análisis de Respuesta en Frecuencia

La principal herramienta de validación fue el análisis mediante **diagramas de Bode**.

Para cada etapa se realizaron barridos de frecuencia utilizando el Analog Discovery con el fin de obtener:

- Magnitud de la respuesta en frecuencia.
- Frecuencias de corte.
- Ganancia en banda pasante.
- Pendientes de atenuación.

Posteriormente, los resultados experimentales fueron contrastados con los obtenidos en simulación.

---

## Criterios de Validación

La prueba de concepto se consideró satisfactoria cuando se verificó que:

- Las frecuencias de corte coincidían con los valores de diseño.
- La ganancia en banda pasante era la esperada.
- Las pendientes de atenuación correspondían a la teoría de cada filtro.
- No existían resonancias o inestabilidades significativas.
- El filtro pasa altas variable cubría correctamente el rango de ajuste previsto.
- El comportamiento experimental coincidía razonablemente con las simulaciones.

---

## Resultados

Las mediciones realizadas demostraron que las distintas etapas del sistema presentaron un comportamiento consistente con los resultados obtenidos durante la simulación.

Los diagramas de Bode permitieron verificar:

- Frecuencias de corte correctas.
- Ganancias adecuadas en banda pasante.
- Atenuaciones acordes con la teoría.
- Operación estable en todo el rango analizado.
- Funcionamiento correcto del filtro pasa altas de frecuencia variable.

Los resultados obtenidos proporcionaron evidencia suficiente para avanzar hacia la etapa de diseño de la PCB.

---

## Flujo de Desarrollo

```text
Diseño Teórico
      │
      ▼
Simulación
      │
      ▼
Montaje en Protoboard
      │
      ▼
Análisis de Bode
(Analog Discovery)
      │
      ▼
Validación Experimental
      │
      ▼
Diseño de PCB
```

---

## Herramientas Utilizadas

- Software de simulación electrónica.
- Protoboard.
- Amplificadores operacionales.
- Fuente de alimentación DC.
- Generador de señales AC.
- Digilent Analog Discovery.

---

## Propósito de Esta Carpeta

Esta carpeta documenta la etapa de validación previa al desarrollo de la PCB final. Aquí se encuentran las simulaciones, pruebas experimentales y resultados utilizados para verificar el correcto funcionamiento de la arquitectura propuesta para el ecualizador de audio.
