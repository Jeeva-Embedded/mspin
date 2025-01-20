Timer Interrupt: Configured to trigger every 20 ms.
Data Collection: Samples data at regular intervals (every 20 ms) and stores it in an array.
Cycle Counting: Tracks the number of completed cycles (3 cycles in this case).
LED Toggle: Indicates the completion of data collection by toggling an LED.

**Components**
STM32 Microcontroller: The project is designed for the STM32F401RE microcontroller using STM32CubeIDE.
Timer (TIM2): Configured to generate interrupts every 20 ms.
LED (LD2): Toggles upon completion of the task.
USART2: Configured for serial communication 
System Clock: The system is clocked at 150 MHz.
Timer Prescaler: Set to 149 to achieve a 1 µs timer tick.
Timer Period: Set to 19999 for a 20 ms interrupt period.
Timer Interrupt Configuration
TIM2 with the following parameters:

**Calculation**
Timer clock = SystemCoreClock = 150MHz
Desired interrupt period = 20ms = 0.02s
To get 20ms:
prescaler of 150
Timer tick = 1/(150MHz/150) = 1μs
Counter period = 20ms/1μs = 20,000 counts
Therefore:
Prescaler = 150 - 1 = 149 register value
Counter period = 20000 - 1 = 19999 register value

Prescaler: 149
Period: 19999
Interrupt Period: 20 ms
