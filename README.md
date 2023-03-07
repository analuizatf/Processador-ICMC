# ICMC-Processor
[![en](https://img.shields.io/badge/lang-en-red.svg)](https://github.com/simoesusp/Processador-ICMC/blob/master/README.md)
[![pt-br](https://img.shields.io/badge/lang-pt--br-green.svg)](https://github.com/simoesusp/Processador-ICMC/blob/master/README.pt-br.md)


Development of a complete environment to teach and learn computer architecture, VHDL processor design and Assembly language

This project consists of the development of a complete environment to teach and learn computer architecture, VHDL processor design and Assembly language.

The proposed ICMC-Processor was designed to be simple, efficient, and easy to teach and understand. It was proposed as the main project for Computer Organization classes at the ICMC-University of Sao Paulo, in Sao Carlos, Sao Paulo state, Brazil.

This project consists of five parts:

1.	FPGA processor design (Altera VHDL project for Cyclone II DE2-70 board)

2.	Assembler software (to generate binary code for the ICMC-Processor implemented on FPGA)

3.	Simulator software (to simulate the execution of code on the ICMC-Processor)

4.	Compiler software (to compile a reduced set of  C language commands)

5.	Documentation (Processor architecture and Assembly language description)



# Configuration of DE0 Board:

1. Configure the Clock to 1MHz: SW[2] = 1; SW[1]=1; SW[0]=0

2. Select the AUTHOMATIC clock => sw[8] = 0

3. Now, just program the Quartus board

4. For MANUAL clock => SW[8]=1 and change the SW[9] to give the clock signal on the circuit

# Configuration of DE115 Board:

1. Configure the Clock para 1MHz: SW[6] = 1 and ALL others to 0 (For other Clocks, try to raise one by one (and only one!) of the SW[0]=1Hz, SW[1]=10Hz  until SW[6]=1MHz)

2. Select the AUTHOMATIC clock => sw[16] = 1

3. Now just program the Quartus board

4- To MANUAL clock => SW[16]=1  and  change SW[17] to give the clock signal on the circuit

# How to generate the PROGRAM:

1. Write the program AS USUAL on Sublime (name.ASM)

2. Press F7 to mount the binary file (name.MIF) e Simulate (to check whether it works BEFORE having to wait 20min on Quartus!!)

3. Change the NAME of the file name.MIF to CPURAM.MIF

4. Copy CPURAM.MIF to the Project folder on Quartus

5. Compile the project on Quartus

6. Program the Board and PRAY!!!!

7. Change the input from Monitor to VGA input (you will suffer on Philipis' menus!!!)

# Online Simulator

There is an online version of the simulator simplify the development of applications compatible with the processor. This is the most stable version between the ones available in the repository, and it doesn't require any additional instalation steps on the local machine. 

- It can be accessed through the link: [https://thiagoambiel.github.io/SimuladorICMC/](https://thiagoambiel.github.io/SimuladorICMC/)

