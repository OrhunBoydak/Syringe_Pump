# Syringe Pump Control with STM32

This project is designed to control a syringe pump using an STM32 microcontroller. The code operates a stepper motor to move the syringe pump forward and backward, allowing a specified amount of fluid to be injected or withdrawn.

## Features

- Controls a stepper motor to operate a syringe pump
- Adjustable step delay to control the speed of the stepper motor
- Calculates the number of steps required for the desired fluid volume
- Provides functions for compressing and decompressing the syringe

## Components

- STM32 Microcontroller
- Stepper Motor (e.g., NEMA 17)
- Motor Driver
- Syringe Pump
- Power Supply

## Code Overview

### main.c

The `main.c` file contains the main program logic, including initialization of peripherals and the main control loop.

#### Key Functions

- `microDelay(uint16_t delay)`: Provides a microsecond delay using a hardware timer.
- `de_compress(void)`: Moves the syringe pump to inject fluid.
- `compress(void)`: Moves the syringe pump to withdraw fluid.
- `transaction_percentage(void)`: Calculates the percentage of the transaction completed.
- `syringe_laps_calculator(int ul)`: Calculates the number of laps required for the desired volume.
- `instant_ul_calculator(void)`: Calculates the instantaneous volume of fluid based on the current position.

### GPIO and Timer Initialization

The GPIO and timer peripherals are initialized to control the stepper motor. The direction and step pins are configured as output, and the timer is used to generate precise delays.

### System Clock Configuration

The system clock is configured to provide the necessary clock signals for the microcontroller and peripherals.

## Getting Started

### Prerequisites

- STM32 development board
- STM32CubeIDE or any compatible IDE
- USB cable for programming the microcontroller

### Installation

1. Clone this repository:
   ```sh
   git clone https://github.com/yourusername/syringe-pump.git
