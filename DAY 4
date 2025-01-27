
Clock tree synthesis is a crucial part of VLSI design. It consists of generating a network of clock distribution lines, which is known as the 'clock tree', to deliver the clock signal simultaneously and with the least and lowest skew to all sequential elements throughout the chip.

This process starts with defining clock requirements, which is then followed by generating a stratified network of clock lines then optimizing the clock tree to decrease skew, routing the clock lines, and verifying that the clock tree meets design requirements and timing constraints set by us.

Without clock tree synthesis, efficient clock distribution in VLSI designs cannot be guaranteed. It enables synchronous operation of sequential elements and ensures the design meets desired performance goals.
There is also a concept of H - Tree which calculates the middle of all its endpoints and originates a tree from that midpoint of all its endpoints.
For example let us say we have four flip flops flip flop one, flip flop 2, flip flop 3, and flip flop 4 they are placed in a square shape so the edge 3 syntheses will find the midpoint then it will reach the midpoint of flip flop 1 and 2 and then connect them same for flip flop 3 and 4 Show the clock reaches at every flip flop at the same time or almost at the same time, Show us skew Value will be zero or very close to zero. The clock will reach through real buffers, the connection is called a clock net. Also, the clock net is shielded so no glitch occurs and the net is not interfered.                                                                                                                                         
--Routing--
To Understand routing, let us say we have two points A and B and we have to connect A and B where A is the source and connect them in the best path with the least twists and turns. Twists and turns means zigzag lines, most of the lines should be in an L shape.
There is an algorithm for this that understands to not put the lines in such a way, it was invented by Lee in 1961 and is called Lee's algorithm. It creates a grid in the backend called the routing grid, it with the points to be routed. The first step is does that it labels the adjacent grids and calculate the path. Any routing algorithm or engine always prefers the path with the least turns. This algorithm works by first creating a maze of   numbers and then calculating the path. This is slow, time-consuming, and requires a lot of memory as each data has to be stored. There are also some rules that need to be followed during routing. 

Sign Off - this step has 3 attestation approaches
they are as follows
1. DRC i.e. Design Rule Check - This ensures that our design is set according to the design Guidelines, and is suited for fabrication. It's main purpose is to detect and correct errors like layout errors so no defects happen in the fabrication process.

2. Layout versus Schematic (LVS) - Compares and ensures the consistency between the schematic and the layout design.

3. STA i.e Static Timing Analysis - It checks the circuit to make sure that it meets the required delays like hold time, max and min clock frequency, e.t.c

Convert Magic  Layout to STD Cell Lef
Lef i.e. Library Exchange Format contains the info of the standard cell library used in the design as the name says. The info like shape, size, layers e.t.c is what they contain. The given instructions to set the port definitions are available [here] https://github.com/nickson-jose/vsdstdcelldesign#create-port-definition.
Now let us save the .mag file with a different and new filename by command 
`lef write` in tkcon terminal, this will generate a new file with _lef_ extension with the new file name. 

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Threshold timing-
A software called `GUNA` creates various .libs files, the schematics of these .libs file are what we are going to discuss about.

![image](https://github.com/JustVanillaCode/VSD-ASIC-Level-Repository/assets/162819270/8bd59800-73a5-4031-bf81-6ed55068d277)


In this image, the red line is the o/p of the 1st inverter and blue one is the o/p of the second inverter.

![image](https://github.com/JustVanillaCode/VSD-ASIC-Level-Repository/assets/162819270/e9820094-c83b-46cb-8f30-55fa6a9c587e)

![image](https://github.com/JustVanillaCode/VSD-ASIC-Level-Repository/assets/162819270/d92b8c79-a906-4e58-b3c2-2b51d2e3300a)

![image](https://github.com/JustVanillaCode/VSD-ASIC-Level-Repository/assets/162819270/569cba23-a34e-43ae-b628-5a095e301d68)

Propagation delay is calculated as the difference between the time it takes for a signal to reach the output threshold and the time it takes for the same signal to reach the input threshold. If the propagation delay is negative, it can cause unexpected results, as the output signal will occur before the input signal. Therefore, it is crucial to select the correct threshold values. Generally, the delay threshold is set at 50%, while the slew rate threshold is set between 20% and 80%.

Transition time = time(slew_high_x_thr) - time(slew_low_x_thr)
Propagation delay = time(out_x_thr) - (time_x_thr)

![image](https://github.com/JustVanillaCode/VSD-ASIC-Level-Repository/assets/162819270/6193b8f9-78be-415e-a927-a4443541e730)
