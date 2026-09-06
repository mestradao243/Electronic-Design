# STM32MP1 Mini PC — Power Budget

## Español

### Descripción

Este documento define y analiza el **presupuesto de potencia (Power Budget)** del mini PC desarrollado alrededor de la familia **STM32MP1**. El objetivo es identificar el consumo energético de los principales bloques del sistema y dimensionar adecuadamente la arquitectura de alimentación.

El análisis considera tanto el consumo del procesador como el de los diferentes periféricos y subsistemas conectados a la placa, permitiendo establecer los requisitos de corriente y potencia para las diferentes líneas de alimentación.

### Objetivos

* Estimar el consumo de potencia de cada subsistema.
* Definir los requisitos de corriente de las diferentes líneas de alimentación.
* Dimensionar los reguladores y convertidores DC/DC.
* Determinar el consumo máximo esperado del sistema.
* Estimar el consumo durante diferentes estados de funcionamiento.
* Incorporar un margen de diseño adecuado para garantizar la estabilidad del sistema.
* Utilizar los resultados para seleccionar una fuente de alimentación apropiada.


## English

### Description

This document defines and analyzes the **Power Budget** of the mini PC developed around the **STM32MP1** family. The main objective is to identify the power consumption of the major system blocks and properly size the power delivery architecture.

The analysis considers the processor, peripherals, memory, storage, and other connected subsystems in order to establish the required voltage and current levels for the different power rails.

### Objectives

* Estimate the power consumption of each subsystem.
* Define the current requirements for the different power rails.
* Size the required regulators and DC/DC converters.
* Determine the expected maximum system power consumption.
* Estimate power consumption under different operating conditions.
* Include an appropriate design margin to ensure system stability.
* Use the resulting power budget to select an appropriate power supply.


This margin accounts for consumption variations, component tolerances, transient conditions, and potential future system expansions.

### Validation

The theoretical power budget will be validated through measurements on the final prototype. Voltage, current, and power measurements will be used to verify the initial estimates and identify potential differences between the theoretical model and the actual system behavior.
