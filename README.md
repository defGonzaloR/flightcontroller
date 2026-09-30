# flightcontroller

During a time of growing interest in embedded systems, and currently within flight systems, I designed this simple flight controller. 
Its design consists of a 5V input from a battery that will be used to power the rest of the board. From here it's outputted to 4 actuators, connected through JST connectors. The 5V is stepped down to 3.3V through an LDO and to the digital half of the board. 
The brain of the board is an STM32103C8T6, a selection I took from a STM32 blue pill design, which was commonly referred to for techniques withing this board. The main peripherals on this board are the barometer and IMU, which will give information about the orientation and direction of the flight system. The STM32 also controls the PWM driver responsible for actuator control. A design technique I tried to implement here was trace length matching for an alignment of the signals between the four actuators. The STM32 is also connected to a NEO 9M gps module with an external antenna, something I've never worked with before but am really excited to learn to setup. There's two programming/debugging inputs, being the SWD and USB-C ports. I also added a USART header for later convenience should I want to add anything external to both the STM32 and GPS module. I also provided boot mode and power connection switches. 
This is my most complex PCB yet, and once it arrives I hope to learn even more through debugging and assembly, as well as testing with a model plane.
# Schematic

<img width="1156" height="650" alt="image" src="https://github.com/user-attachments/assets/2824eaa7-70b2-4b6c-883a-489654d5a4bf" />

# Layout

<img width="1059" height="693" alt="image" src="https://github.com/user-attachments/assets/91c138ee-f194-4bf7-b813-a79703a3b94f" />

# 3D View

<img width="734" height="368" alt="image" src="https://github.com/user-attachments/assets/b9c14ee7-6500-4406-950a-b692789cbb4a" />
