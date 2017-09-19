### pulse2demo.mc
A small circuit that shows some basic principles of the CA. At the top left is a loop of wire that creates an endless stream of pulses, spaced 8 ticks apart. The pulses are split to either attempt to go through the gate, or toggle the gate. The ones that go through will toggle the small square at the bottom, and then terminate at the blue square.
### shiftregister.mc
A bunch of shift registers arranged to make a matrix display. The top button sshifts the entire display left, the middle button pushes a red, and the bottom button pushes a green. The smaller rectangular button sends a pre-made message.

Use state 15 to press the buttons.
### hexcounter.mc
A binary to hex converter. The four buttons toggle a bit of the binary input, and the larger button updates the display. All of the buttons are being driven by the clock circuit at the top.
### langtonsant.mc
A small board for Langton's Ant. A solitary spark travels through the squares and toggles them as it goes. The two square indicators at the top reflect the spark back into the grid.
### turing.mc
A BrainF\*\*\* computer. The memory cells are only 4 bits large, but they can easily be expanded by copy/pasting the stack on top of each one. To reprogram it, use the components in the green box. No input or output instruction yet.

It is currently set to multiply the current cell and the one next to it, and store the result in the cell three to the right.
### computer.mc
Some unfinished components for a microprocessor. It uses pulse trains (series of a fixed number of pulses timed at 6 ticks) and pairs (a 0 and 1 wire with no strict timing) for communication. Here's a description of each:
- Lower left: Miscellaneous components for pulse train and pair conversion. The loop is juggling two values and inverting them on each repetition. The left part is a pulse train to pair converter, the right part is a pulse pair to train converter, and in the middle is a 4-bit shift register.
- Top left and top right: an ALU, in 4-bit and 8-bit varieties. Supports addition, subtraction, and multiplication. The wires near the checkmark button change the operation. Accepts input from the buttons marked "0" and "1" near the bottom, and sends output as a pulse train (hotwired to a shift register for readability).
- Lower right: An incomplete shift-register memory cell, in 4-bit and 8-bit varieties.
    - The cell itself is the matrix of shift registers with the space below it. The columns at the left are the address select, the left wires are input, and the right wires are output. The only way to read the memory is by filling the register with zeroes, and then putting it back afterwards.
	- The mess of wires at the bottom is an attempt at making it communicate through a single wire, but it does not work.