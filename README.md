# ICMC-Processor
[![en](https://img.shields.io/badge/lang-en-red.svg)](https://github.com/simoesusp/Processador-ICMC/blob/master/README.md)
[![pt-br](https://img.shields.io/badge/lang-pt--br-green.svg)](https://github.com/simoesusp/Processador-ICMC/blob/master/README.pt-br.md)


Development of a complete environment to teach and learn computer architecture, VHDL processor design and Assembly language

This project consists of the development of a complete environment to teach and learn computer architecture, VHDL processor design and Assembly language.

The proposed ICMC-Processor was designed to be simple, efficient, and easy to teach and understand. It was proposed as the main project for Computer Organization classes at the ICMC-University of São Paulo, in São Carlos, São Paulo state, Brazil.

This project consists of five parts:

1.	FPGA processor design (Altera VHDL project for Cyclone II DE2-70 board)

2.	Assembler software (to generate binary code for the ICMC-Processor implemented on FPGA)

3.	Simulator software (to simulate the execution of code on the ICMC-Processor)

4.	Compiler software (to compile a reduced set of  C language commands)

5.	Documentation (Processor architecture and Assembly language description)

# Installation and Usage
## Processor
### Configuration of DE0 Board:
1. Configure the Clock to 1MHz: SW[2] = 1; SW[1]=1; SW[0]=0

2. Select the AUTHOMATIC clock => sw[8] = 0

3. Now, just program the Quartus board

4. For MANUAL clock => SW[8]=1 and change the SW[9] to give the clock signal on the circuit
### Configuration of DE70 Board:

### Configuration of DE115 Board:
1. Configure the Clock para 1MHz: SW[6] = 1 and ALL others to 0 (For other Clocks, try to raise one by one (and only one!) of the SW[0]=1Hz, SW[1]=10Hz  until SW[6]=1MHz)

2. Select the AUTHOMATIC clock => sw[16] = 1

3. Now just program the Quartus board

4. To MANUAL clock => SW[16]=1  and  change SW[17] to give the clock signal on the circuit

## Assembler
### Version 0.0
You can use this version for files of 32kb, when limit is required. It can be found on '~/Assembler/Assembler_Source'
### Version 0.2
This version can be found on '~/Assembler/NovoMontadorLinux/montadorLinux.zip'
### Version 1.1
You can use this version for files of 64kb. It can be found on '~/Assembler/NovoMontadorLinux/Montador_Ultimo_Beta_64Kb' or '~/Assembler/NovoMontadorLinux/montadorLinux_BETA.zip'

## Compiler
To use the reduced set of  C language commands, you have to:
1. Compile the compiler:
    - First, you have to install some dependencies:
        - On Linux: `sudo apt install bison flex g++`
        - *TODO: Add instructions for installing dependencies on Windows*
    - After installing the dependencies, execute the command `make`. This will compile and save the Compiker on the file "parser"
    
2. The following features are not supported by the Compiler:
    - Dinamic allocation
    - includes
    - Data types other than `int` and `char`
    - structs and unions
    - typedefs
    - arrays with three or more dimensions
    - switch
    
3. Pending tests:    
    - [] Compare operands that contains **equal** (ex: >=)
    - [] functions that returns **void**, but with return inside the function
    
4. Known bugs:
    - [] On the Pacman example:
        - His animation moving to the right doesn't show
        - Sometimes he goes through the wall
    
5. Features to be added:
    - [] Allow assembly code inside .c
    - [] switch 
    
6. Use examples:
    - Pacman:
        `./parser pacman/jogo.c > pacman/pacman.asm`
        
    - Breakout:
        `./parser breakout/jogo.c > breakout/breakout.asm`

## Simulator

### How to generate the PROGRAM:

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

# Project Advisor
[Prof. Eduardo do Valle Simões](https://github.com/simoesusp)
<a href="https://gitlab.com/simoesusp"><img src="utils/images/gitlab-logo-500.svg" width="16" height="16"></img></a>
<a href="https://sites.icmc.usp.br/simoes/"><img src="utils/images/web.png" alt="Website icons created by Cuputo - Flaticon" width="16" height="16"></img></a>

# Contributors