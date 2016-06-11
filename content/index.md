+++
date = "2016-06-07T16:21:03-04:00"
draft = false
url = "index.html"
title = "The JGM-44 Microcomputer"

+++

**JGM-44 in its Ultimate Configuration**
![JGM-44 Computer](/jgm44-annotated.png)

The JGM-44 was a one-of-a-kind computer, hand-built by my father during the "hobbyist" era
from about 1978 to 1986. It would eventually feature switchable (non-simultaneous) operation of either
a Motorola MC6809 or a Zilog Z-80 CPU, dual 8" 241KB floppy drives, 64K of RAM, and a sound card
capable (by 80s standards) of both music and speech.

(The term 'JGM-44' properly refers to the bus architecture, not the computer itself.
But since this is the only computer in the world that ever used this architecture,
and there isn't a proper name for the computer itself, I'm taking liberties.)

The JGM-44 was significantly upgraded over the course of its life. The first version used a Motorola
MC6802 CPU. (Note: This is not the same as the more famous MOS 6502 that was used in the Apple ][ and Commodore PET.)
The 6802 was significantly easier to build than a 6800 (or 6502) because it included an on-chip oscillator. It also
included 128 bytes of on-board RAM, meaning it was immediately able to run very simple programs, even before
the RAM board was finished.

![MC6802 CPU Board](/jgm44-6802-annotated.png)

The EPROMs shown here are the final set, dated 1982, used with this board. They include the Motorola ROM monitor
(JBUG? MikBUG?), and a second 2K EPROM labeled 'DSMBL' - a ROM disassembler? What luxury!

![Running a Program](/mikbug.png)

To run a program, you used the M command to modify bytes of memory, then the G command to "go". (The example shown
above is just changing a variable and launching the program at FF29. Entering a program would be much longer.)

I remember writing the "guess a number from 1 to 100" game for this board. Of course it couldn't actualy give that as a prompt,
since it's a 28-byte string - which would be 22% of the entire RAM of the system. It had to ask you things like "G?".
I remember the looping and branching, but I don't remember how I got the random numbers. Maybe I counted in a loop
while waiting for the first user input, or something. More likely it just wasn't actually random and the answer was
always 57. It also seems likely that the game was really "guess a number from 00 to FF" because I don't think
it would have been feasible to do translation to, or particularly from, decimal.

![8K RAM Board](/jgm44-8k-ram.png)

The next major improvement was the 8K RAM board. This was just enough to run the smallest available BASIC interpreter.
(Well, there was such a thing as 4K BASIC on the TRS-80, but it was *really* primitive. Like, maybe it didn't have multiplication.)
I quickly abandoned hand-assembling 6802 opcodes by poring through databooks, and started to write BASIC programs. I recall
that my father had second thoughts about "getting a BASIC interpreter too soon" - he thought I should have spent more time
doing real work in machine language, and that I wasn't learning anything with this BASIC nonsense.

