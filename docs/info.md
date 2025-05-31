<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

# ALU con Sumador Prefix

Este proyecto implementa una Unidad Aritmética Lógica (ALU) que incluye un sumador de tipo **Prefix** para realizar operaciones aritméticas de alta velocidad, como suma, resta y otras funciones lógicas básicas.

## How it works

La ALU es capaz de realizar operaciones aritméticas y lógicas sobre dos operandos de N bits. La principal característica del diseño es el uso de un **sumador prefix**, que reduce el tiempo de cómputo de la operación de suma mediante un enfoque paralelo y jerárquico.

Entre las operaciones que soporta la ALU se encuentran:

- **Suma** (`A + B`) usando el sumador prefix (como Kogge-Stone, Brent-Kung, etc.)
- **Resta** (`A - B`)
- **AND** lógico (`A & B`)
- **OR** lógico (`A | B`)
- **XOR** lógico (`A ^ B`)
- **NOT** lógico (`~A` o `~B`)
- Comparaciones (`A == B`, `A > B`, etc., si aplica)

El sumador prefix mejora el rendimiento frente a los sumadores tradicionales (como el ripple-carry) gracias a su estructura paralela, logrando menor tiempo de propagación de acarreo.

## How to test

Puedes probar esta ALU en un entorno de simulación (como **ModelSim**, **Vivado**, **GHDL**, etc.) o en hardware real (como una **FPGA**).

### Simulación

1. Abre el entorno de simulación.
2. Compila los archivos del proyecto (por ejemplo, `.v`, `.vhd`, etc.).
3. Corre el **testbench** incluido, que prueba las diferentes operaciones con múltiples vectores de prueba.
4. Verifica la salida para asegurarte de que los resultados son correctos.

### Hardware (si aplica)

1. Sintetiza el proyecto en la herramienta correspondiente.
2. Carga el diseño en la FPGA.
3. Usa switches, botones o una interfaz UART para ingresar los operandos y seleccionar la operación.
4. Observa la salida por LEDs, displays o monitor UART.

## External hardware

Este proyecto puede requerir los siguientes componentes externos si se implementa en FPGA:

- **Switches o botones**: para ingresar los operandos y seleccionar operaciones.
- **LEDs**: para mostrar la salida.
- **Display de 7 segmentos** (opcional): para mostrar resultados en decimal/hexadecimal.
- **UART** (opcional): para comunicación con una PC.
- **Placa FPGA**: por ejemplo, Digilent Nexys A7, Basys 3, etc.

---


