# ARMv7 assembly on the DE1-SoC

Lab work from ECSE 324 (Computer Organization) at McGill University, Fall 2025.
Everything is written for the DE1-SoC Computer system: an ARM Cortex-A9 with
its switches, LEDs, seven-segment displays, VGA output and PS/2 port mapped
into memory.

## What is here

| Folder | File | What it does |
| --- | --- | --- |
| `lab2` | `zigzag.s` | Walks an N by N matrix in zigzag order and writes it out as a vector |
| `lab2` | `recaman_iterative.s`, `recaman_recursive.s` | The Recamán sequence, once with a loop and once with recursion on the stack |
| `lab3` | `hex_messages_polling.s` | Shows a message on the six HEX displays, chosen with the switches. Pushbuttons rotate it and reverse the direction. The buttons are polled. |
| `lab3` | `hex_messages_interrupts.s` | The same display, scrolled by the A9 private timer. Buttons slow it down, speed it up, reverse it and pause it. Timer and buttons both come in as interrupts through the GIC. |
| `lab4` | `vga_driver.s` | VGA driver: draw a pixel, write a character, clear both buffers |
| `lab4` | `ps2_driver.s` | Reads one byte from the PS/2 keyboard if one is waiting |
| `lab4` | `game_of_life.c` | Conway's Game of Life on a 16 by 12 grid, in C on top of the two drivers. W, A, S and D move the cursor, space toggles a cell, N computes the next generation. |

## Notes

The handouts and the test files given by the course are not included, only the
code I wrote.
