# DIGITAL_VLSI_2025
![gif](https://i.gifer.com/QWc9.gif)
## Abstract
 - The SI-2025 Digital VLSI is a comprehensive educational platform for learning and practicing digital VLSI design. It offers a wide range of Verilog-based examples, simulation testbenches, and lab experiments aimed at reinforcing theoretical knowledge through practical implementation. Structured to support both students and professionals, the course emphasized hands-on learning using modern digital design tools and methodologies. By bridging the gap between classroom learning and industry requirements, it has enabled users to develop strong design and verification skills. This resource is particularly valuable for those pursuing careers in digital system design, ASIC development, and FPGA-based implementation
## Introduction
 - The SI-2025 Digital VLSI course served as a curated collection of learning materials designed to support digital VLSI education. It included Verilog coding, simulation exercises, and guided lab sessions aligned with academic curricula and industry standards. This course enabled learners to explore core digital design concepts, such as sequential and combinational circuits, through hands-on coding and simulations. With a focus on practical implementation, the content helps build a solid foundation in hardware description languages(Verilog) and modern design workflows. This has made it an ideal resource for students and enthusiasts aiming to strengthen their understanding and application of digital system design principles and VLSI.
## VLSI INTRO
 - VLSI stands for Very-Large-Scale Integration, a process of creating integrated circuits by combining thousands to millions of transistors onto a single chip. It revolutionized the field of electronics by making devices smaller, faster, and more energy-efficient. VLSI technology is the foundation for modern microprocessors, memory chips, and other complex integrated circuits used in a wide range of applications, from consumer electronics to advanced computing systems.
![vlsi](https://www.tessolve.com/wp-content/uploads/2023/12/memory-testing-post.jpg)
## FPGA 
- FPGA stands for Field Programmable Gate Array. It is a type of integrated circuit that can be programmed by the user after manufacturing to perform specific tasks. Unlike traditional logic devices such as application-specific integrated circuits (ASICs), FPGAs are designed to be reprogrammable, making them highly versatile and adaptable for various applications.FPGAs consist of an array of programmable logic blocks (PLBs) and a network of programmable interconnects. These components can be configured to perform complex operations or serve as simple logic gates.
- The picture given below is a Basys3 Artix-7 FPGA Trainer Board by [Digilent](https://digilent.com/shop/basys-3-artix-7-fpga-trainer-board-recommended-for-introductory-users/) 
  
![Basys3 FPGA development board](https://cdn11.bigcommerce.com/s-7gavg/images/stencil/1280x1280/products/106/6256/Basys3-Rev.C-box-1000__84357.1730220596.png?c=2&_gl=1*evk1u4*_gcl_au*MTI3MjE3OTk1MC4xNzQ5NDYyMjYx*_ga*Mzc0NDMwMzkyLjE3NDk0NjIyNjI.*_ga_JSPEFFCPBT*czE3NDk0NjIyNjIkbzEkZzAkdDE3NDk0NjIyNjIkajYwJGwwJGgyMjgwMjU2ODY.)


## VERILOG PRACTICE
Design code
```python
module four_bit_comparator(
	input [3:0] a,
	input [3:0] b,
	output grt,
	output eql,
	output sml
);

assign grt = (a>b);
assign eql = (a==b);
assign sml = (a<b);

endmodule
```
Testbench
```python

## Switches
set_property -dict { PACKAGE_PIN V17   IOSTANDARD LVCMOS33 } [get_ports {a[0]}]
set_property -dict { PACKAGE_PIN V16   IOSTANDARD LVCMOS33 } [get_ports {a[1]}]
set_property -dict { PACKAGE_PIN W16   IOSTANDARD LVCMOS33 } [get_ports {a[2]}]
set_property -dict { PACKAGE_PIN W17   IOSTANDARD LVCMOS33 } [get_ports {a[3]}]
set_property -dict { PACKAGE_PIN W15   IOSTANDARD LVCMOS33 } [get_ports {b[0]}]
set_property -dict { PACKAGE_PIN V15   IOSTANDARD LVCMOS33 } [get_ports {b[1]}]
set_property -dict { PACKAGE_PIN W14   IOSTANDARD LVCMOS33 } [get_ports {b[2]}]
set_property -dict { PACKAGE_PIN W13   IOSTANDARD LVCMOS33 } [get_ports {b[3]}]

## LEDs
set_property -dict { PACKAGE_PIN U16   IOSTANDARD LVCMOS33 } [get_ports {grt}]
set_property -dict { PACKAGE_PIN E19   IOSTANDARD LVCMOS33 } [get_ports {eql}]
set_property -dict { PACKAGE_PIN U19   IOSTANDARD LVCMOS33 } [get_ports {sml}]

set_property CONFIG_VOLTAGE 3.3 [current_design]
set_property CFGBVS VCCO [current_design]

set_property BITSTREAM.GENERAL.COMPRESS TRUE [current_design]
set_property BITSTREAM.CONFIG.CONFIGRATE 33 [current_design]
set_property CONFIG_MODE SPIx4 [current_design]
```
![WhatsApp Image 2025-06-06 at 21 44 13_dac94ac0](https://github.com/user-attachments/assets/333fa150-7497-4302-9d91-44f691dd83e1)


## RESOURCES
### LECTURE NOTES
  1. [Intro](https://github.com/silicon-vlsi/SI-2025-DigitalVLSI/blob/main/docs/L1_Introduction_Course_Outline.pdf)
  2. [Combinational design](https://github.com/silicon-vlsi/SI-2025-DigitalVLSI/blob/main/docs/L2_Review_Combinational_Logic_Design.pdf)
  3. [Sequential design](https://github.com/silicon-vlsi/SI-2025-DigitalVLSI/blob/main/docs/L3_Review_Sequential_Logic_Design.pdf)
  4. [Verilog intro](https://github.com/silicon-vlsi/SI-2025-DigitalVLSI/blob/main/docs/L4_DD_Verilog_Introduction.pdf)
  5. [Verilog Basics](https://github.com/silicon-vlsi/SI-2025-DigitalVLSI/blob/main/docs/L5_Verilog_Basics.pdf)
  6. [Modules and Ports](https://github.com/silicon-vlsi/SI-2025-DigitalVLSI/blob/main/docs/L6_Modules_and_Ports.pdf)
  7. [Gate level modeling](https://github.com/silicon-vlsi/SI-2025-DigitalVLSI/blob/main/docs/L7_Gate_Level_Modelling.pdf)
  8. [Data flow modeling](https://github.com/silicon-vlsi/SI-2025-DigitalVLSI/blob/main/docs/L8_Data_Flow_Modelling.pdf)
  9. [Behavioral modeling](https://github.com/silicon-vlsi/SI-2025-DigitalVLSI/blob/main/docs/L9_Behavioural_Modeling_Part1.pdf)
  
