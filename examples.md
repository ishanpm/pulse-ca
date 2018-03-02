These examples are ordered roughly from least to most complex. Definitely start with `pulse2demo.mc`.
For more info on any pattern, view its comments (Hotkey Ctrl+I).

## pulse2demo.mc
A small circuit that shows the basic principles of the CA.
## shiftregister.mc
A bunch of shift registers arranged to make a matrix display.
## hexcounter.mc
A binary to hex converter.
## langtonsant.mc
A small board for Langton's Ant.
## turing.mc
A BrainF\*\*\* computer.

Does not support `,` or `.`, but you don't *really* need those, do you?
## metalife.mc, metalife_galaxy.mc
Programmable metacells! These tiny metacells have an area of 32\*32, a period of 358, and support any totalistic (B\*/S\*) rule.

# Computer parts
The examples/computer folder contains parts for a working microprocessor. I haven't finished the info section on these files yet.
## shiftRegister.mc
Briefly holds binary strings for later use.
## registerBlock.mc
Four shift registers stacked atop each other to form a register block, along with an accumulator.
## RAM.mc
Holds up to 64 16-bit values. Can be extended to hold more.
## processor.mc
The finished microprocessor, with a blank instruction memory.
## compute-primes.mc
Three microprocessors that work together to find prime numbers. A picture of it after 50,000,000 generations is in the root directory of the repository, with the highest prime in its memory being 139.