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

### Arquitectura de potencia

El presupuesto de potencia se estructura a partir de las principales cargas del sistema:

```text
                    Input Power
                         │
                         ▼
                Power Management
                         │
          ┌──────────────┼──────────────┐
          │              │              │
          ▼              ▼              ▼
       STM32MP1       Memory          Peripherals
          │              │              │
          │              │        ┌─────┼─────┐
          │              │        │     │     │
          ▼              ▼        ▼     ▼     ▼
        VDDxxx          DDR      USB   HDMI   Ethernet
```

La arquitectura de alimentación deberá proporcionar las tensiones y corrientes requeridas por cada bloque, teniendo en cuenta las condiciones nominales y los escenarios de máximo consumo.

### Power Budget

El presupuesto de potencia se puede organizar de acuerdo con la siguiente estructura:

| Subsystem         | Supply Voltage | Typical Current | Maximum Current | Typical Power | Maximum Power |
| ----------------- | -------------: | --------------: | --------------: | ------------: | ------------: |
| STM32MP1          |            TBD |             TBD |             TBD |           TBD |           TBD |
| DDR Memory        |            TBD |             TBD |             TBD |           TBD |           TBD |
| eMMC / Storage    |            TBD |             TBD |             TBD |           TBD |           TBD |
| Ethernet          |            TBD |             TBD |             TBD |           TBD |           TBD |
| USB               |            TBD |             TBD |             TBD |           TBD |           TBD |
| Display Interface |            TBD |             TBD |             TBD |           TBD |           TBD |
| Audio             |            TBD |             TBD |             TBD |           TBD |           TBD |
| Other Peripherals |            TBD |             TBD |             TBD |           TBD |           TBD |
| **Total**         |              — |               — |               — |       **TBD** |       **TBD** |

Los valores deberán obtenerse a partir de las hojas de datos de los componentes, mediciones experimentales y condiciones de funcionamiento definidas para cada escenario.

### Operating Scenarios

El consumo del sistema se analizará bajo diferentes condiciones de funcionamiento:

| Scenario             | Description                        | Expected Power |
| -------------------- | ---------------------------------- | -------------: |
| Idle                 | Sistema encendido con carga mínima |            TBD |
| Normal Operation     | Uso habitual del sistema           |            TBD |
| CPU Intensive        | Alta utilización del procesador    |            TBD |
| Peripheral Intensive | Alta actividad de periféricos      |            TBD |
| Maximum Load         | Condición de carga máxima          |            TBD |
| Startup              | Secuencia de arranque              |            TBD |

### Design Margin

Para el dimensionamiento de la fuente y de los reguladores se incorporará un margen de diseño sobre el consumo máximo calculado.

```text
Required Power = Maximum System Power × Design Margin
```

Este margen permite considerar variaciones de consumo, tolerancias de los componentes, transitorios y posibles ampliaciones futuras del sistema.

### Validation

El presupuesto teórico será contrastado mediante mediciones sobre el prototipo final. Las medidas de tensión, corriente y potencia permitirán verificar las estimaciones realizadas y detectar posibles diferencias entre el modelo teórico y el comportamiento real del sistema.

---

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

### Power Architecture

The power budget is organized around the main system loads:

```text
                    Input Power
                         │
                         ▼
                Power Management
                         │
          ┌──────────────┼──────────────┐
          │              │              │
          ▼              ▼              ▼
       STM32MP1       Memory          Peripherals
          │              │              │
          │              │        ┌─────┼─────┐
          │              │        │     │     │
          ▼              ▼        ▼     ▼     ▼
        VDDxxx          DDR      USB   HDMI   Ethernet
```

The power architecture must provide the voltage and current requirements of each subsystem while accounting for both nominal operating conditions and maximum-load scenarios.

### Power Budget

The power budget can be organized as follows:

| Subsystem         | Supply Voltage | Typical Current | Maximum Current | Typical Power | Maximum Power |
| ----------------- | -------------: | --------------: | --------------: | ------------: | ------------: |
| STM32MP1          |            TBD |             TBD |             TBD |           TBD |           TBD |
| DDR Memory        |            TBD |             TBD |             TBD |           TBD |           TBD |
| eMMC / Storage    |            TBD |             TBD |             TBD |           TBD |           TBD |
| Ethernet          |            TBD |             TBD |             TBD |           TBD |           TBD |
| USB               |            TBD |             TBD |             TBD |           TBD |           TBD |
| Display Interface |            TBD |             TBD |             TBD |           TBD |           TBD |
| Audio             |            TBD |             TBD |             TBD |           TBD |           TBD |
| Other Peripherals |            TBD |             TBD |             TBD |           TBD |           TBD |
| **Total**         |              — |               — |               — |       **TBD** |       **TBD** |

Values should be obtained from component datasheets, experimental measurements, and the operating conditions defined for each scenario.

### Operating Scenarios

System power consumption will be evaluated under different operating conditions:

| Scenario             | Description                             | Expected Power |
| -------------------- | --------------------------------------- | -------------: |
| Idle                 | System powered on with minimal workload |            TBD |
| Normal Operation     | Typical system usage                    |            TBD |
| CPU Intensive        | High processor utilization              |            TBD |
| Peripheral Intensive | High peripheral activity                |            TBD |
| Maximum Load         | Maximum expected system load            |            TBD |
| Startup              | System boot sequence                    |            TBD |

### Design Margin

A design margin will be applied to the calculated maximum power consumption when sizing the power supply and voltage regulators.

```text
Required Power = Maximum System Power × Design Margin
```

This margin accounts for consumption variations, component tolerances, transient conditions, and potential future system expansions.

### Validation

The theoretical power budget will be validated through measurements on the final prototype. Voltage, current, and power measurements will be used to verify the initial estimates and identify potential differences between the theoretical model and the actual system behavior.
