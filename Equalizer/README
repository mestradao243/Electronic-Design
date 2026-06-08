# Project Description

This project consists of a **5-band analog audio equalizer** with **real-time digital monitoring and visualization**, designed around a hybrid analog–digital architecture. The system processes audio signals through dedicated analog filtering stages while using a microcontroller exclusively for measurement, user monitoring, and display control.

The audio signal is received through a 3.5 mm audio jack and conditioned by an input buffer stage. It is then distributed into five second-order Butterworth Sallen-Key band-pass filters, each responsible for a specific region of the audible spectrum (sub-bass, bass, midrange, high, and treble frequencies). Each band includes an independent level control, allowing the user to adjust the relative contribution of each frequency range before recombination through an analog summing stage.

In addition to the equalization network, the system incorporates a **variable High-Pass Filter (HPF)** with an adjustable cutoff frequency ranging approximately from **50 Hz to 6 kHz**, enabling frequency sweep analysis and spectral exploration of the audio signal.

A **STM32F030C8T6** microcontroller continuously acquires analog measurements through its internal ADC channels. The MCU reads both the filtered audio signals and the positions of the user controls, performs digital processing, and generates a graphical representation of the system status. The audio path remains entirely analog, ensuring zero processing latency and preserving signal integrity.

A **16×2 LCD display with I²C interface** provides real-time feedback, including:

- Individual band level visualization
- User-configured attenuation levels
- HPF cutoff frequency indication
- Real-time signal activity monitoring

The entire system is powered from a **USB Type-C 5 V input**, regulated to a single **3.3 V rail** that supplies both the analog and digital subsystems. The design is optimized for PCB implementation and demonstrates the integration of analog audio processing, embedded systems, power management, and user-interface design within a complete electronic product.

---

# Descripción del Proyecto

Este proyecto consiste en un **ecualizador analógico de audio de 5 bandas** con **monitoreo y visualización digital en tiempo real**, diseñado bajo una arquitectura híbrida analógico-digital. El sistema procesa la señal de audio mediante etapas de filtrado analógicas dedicadas, mientras que el microcontrolador se utiliza exclusivamente para tareas de adquisición, monitoreo y visualización.

La señal de audio es recibida a través de una entrada jack de 3.5 mm y acondicionada mediante una etapa buffer de entrada. Posteriormente, se distribuye hacia cinco filtros pasa banda Butterworth Sallen-Key de segundo orden, cada uno encargado de procesar una región específica del espectro audible (subgraves, graves, medios, altos y agudos). Cada banda dispone de un control independiente que permite ajustar su nivel relativo antes de ser recombinada mediante una etapa sumadora analógica.

Además de la red de ecualización, el sistema incorpora un **filtro pasa altos (HPF) variable** con frecuencia de corte ajustable aproximadamente entre **50 Hz y 6 kHz**, permitiendo realizar barridos de frecuencia y exploración espectral de la señal de audio.

Un microcontrolador **STM32F030C8T6** adquiere continuamente mediciones analógicas utilizando sus convertidores ADC internos. El microcontrolador lee tanto las señales provenientes de los filtros como la posición de los controles del usuario, realiza el procesamiento digital correspondiente y genera una representación gráfica del estado del sistema. La ruta principal de audio permanece completamente en el dominio analógico, evitando introducir latencia o degradación en la señal.

La interfaz de usuario está compuesta por un **display LCD 16×2 con interfaz I²C**, encargado de mostrar información en tiempo real como:

- Visualización del nivel de cada banda.
- Niveles de atenuación configurados por el usuario.
- Frecuencia de corte del filtro HPF.
- Actividad de la señal en tiempo real.

Todo el sistema es alimentado mediante una entrada **USB Tipo-C de 5 V**, regulada a un único riel de **3.3 V** que suministra energía tanto a los subsistemas analógicos como digitales. El diseño está optimizado para implementación en PCB y representa la integración de procesamiento analógico de audio, sistemas embebidos, gestión de potencia e interfaces de usuario dentro de un producto electrónico completo.
