
# EchoCom-8086

This project implements an **interrupt-driven echo communication system** on the Intel 8086 microprocessor.  
Using the **8251A USART** and the **8259 PIC**, the program reads characters from a virtual terminal and immediately sends them back (echo).  

## What We Did
- Configured **8251A** for serial communication (8 data bits, 1 stop bit).  
- Installed **two custom interrupt handlers**:
  - **50h → readChar**: Reads incoming character, stores it in a 5-byte buffer.  
  - **51h → sendChar**: Sends characters from the buffer back to the terminal.  
- Implemented buffer control with flags (`control`, `index`, `datanum`).  
- Verified communication with a Proteus virtual terminal.  

## Used Components
- Intel **8086 CPU**  
- **8251A USART** – serial port communication  
- **8259 PIC** – programmable interrupt controller  
- Virtual Terminal (for RXD/TXD testing)  


