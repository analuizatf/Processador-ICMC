# ICMC-Processor
[![en](https://img.shields.io/badge/lang-en-red.svg)](https://github.com/simoesusp/Processador-ICMC/blob/master/README.md)
[![pt-br](https://img.shields.io/badge/lang-pt--br-green.svg)](https://github.com/simoesusp/Processador-ICMC/blob/master/README.pt-br.md)


Este projeto consiste no desenvolvimento de um ambiente completo para ensinar e aprender arquitetura de computadores, design de processadores VHDL e linguagem Assembly.

O processador ICMC-Processor proposto foi projetado para ser simples, eficiente e fácil de ensinar e entender. Foi proposto como o projeto principal para as aulas de Organização de Computadores no ICMC-Universidade de São, em São Carlos - SP, Brasil.

Este projeto consiste em cinco partes:

1.	Projeto do processador FPGA (Projeto Altera VHDL para a placa Cyclone II DE2-70)

2.	Software Assembler (para gerar código binário para o ICMC-Processor implementado na FPGA)

3.	Software Simulator (para simular a execução de código no ICMC-Processor)

4.	Software Compiler (para compilar um conjunto reduzido de comandos em linguagem C)

5.	Documentação (Arquitetura do processador e descrição da linguagem Assembly)



# Configuração da Placa DE0:

1. Configure o Clock para 1MHz: SW[2] = 1; SW[1]=1; SW[0]=0

2. Selecione o clock AUTOMATICO => sw[8] = 0

3. Agora e' so' programar a placa do Quartus

4. Para clock MANUAL => SW[8]=1  e  mudar a SW[9] para dar o clock no circuito

# Configuração da Placa DE115:

1. Configure o Clock para 1MHz: SW[6] = 1   e TODAS as outras para 0 (Para outros Clocks, tentar subir uma por uma (e apenas uma!) das SW[0]=1Hz, SW[1]=10Hz  ate' SW[6]=1MHz)

2. Selecione o clock AUTOMATICO => sw[16] = 1

3. Agora e' so' programar a placa do Quartus

4. Para clock MANUAL => SW[16]=1  e  mudar a SW[17] para dar o clock no circuito

# Para gerar o PROGRAMA:

1. Escreva o programa NORMALMENTE no Sublime (nome.ASM)

2. F7 para montar o arquivo binario (nome.MIF) e Simular (pra ver se Funciona, ANTES de esperar 20min no Quartus!!)

3. Mude o NOME do arquivo nome.MIF para CPURAM.MIF

4. Copie CPURAM.MIF para a pasta do Projeto no Quartus

5. Compile o projeto no Quartus

6. Programe a Placa e REZE!!!!

7. Troque o  input do Monitor para entrada VGA (tu vai sofrer nos menuzinhos da Philipis!!!)

# Simulador Online

Há uma versão online do simulador para facilitar o desenvolvimento de aplicações compatíveis com o processador. Esta é a versão mais estável dentre as disponíveis no repositório e dispensa qualquer etapa adicional de instalação na máquina local. 

- Pode ser acessado através do link: [https://thiagoambiel.github.io/SimuladorICMC/](https://thiagoambiel.github.io/SimuladorICMC/)

