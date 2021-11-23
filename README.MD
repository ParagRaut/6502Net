
6502.Net
=============

BuildStatus
-----------

Master

[![.NET Build and Test](https://github.com/ParagRaut/6502Net/actions/workflows/build.yml/badge.svg)](https://github.com/ParagRaut/6502Net/actions/workflows/build.yml)


Overview
--------
This is an implementation of the 6502 CPU simulator written in C#.
Only Difference in this fork is it's in process of migrating to .Net 6

Features

- 6502 processor and memory
- Interrupts
- WPF Test Harness
  * Set break points
  * Step through program
  * View registers and memory

Version History
-------------

- 1.1 Cycle Accurate, other improvements
- 1.0 All of Klaus Dormann's Tests pass successfully.
- 0.9.9 All OP Codes Implemented.

References
----------

- <http://visual6502.org/wiki>
- <http://homepage.ntlworld.com/cyborgsystems/CS_Main/6502/6502.htm>
- <http://www.atariarchives.org/alp/>
- <http://en.wikipedia.org/wiki/MOS_Technology_6502>
- <http://www.obelisk.demon.co.uk/6502/>
- <http://www.6502.org/tutorials/>

Test Programs
-------------

I used the Klaus Dormann 6502 Test Suite (GPL License) to validate the simulator.

<http://2m5.de/6502_Emu/> 

Compiling Tests
---------------

1. Grab the AS65 Compiler <http://www.kingswood-consulting.co.uk/assemblers/>

1. Modify the 6502_functional_test.a65

       load_data_direct = 0

1. Run the following command to generate the bin file and lst file

        as65 -l -m -w -h0  6502_functional_test.a65

1. Load the test in the simlator.
    1. Set the Memory Offset to be 0x0400 
    1. Set the PC to 0x0400. 

The Program Listing starts at 400


