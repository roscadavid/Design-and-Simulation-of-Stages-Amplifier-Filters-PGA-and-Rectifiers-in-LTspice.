Design and Simulation of Stages: Amplifier, Filters, PGA, and Rectifiers in LTspice.

In this project, titled "Design and Simulation of Stages: Amplifier, Filters, PGA, and Rectifier in LTspice," I aimed to perform several simulations in the LTspice program on various circuits, such as the behavior of a voltage-current amplifier, Tow Thomas filter, PGA, Peak Detect, and finally, the verification and characterization of the analog interface.

The voltage-current amplifier needed to be dimensioned, meaning we had to determine all resistor values. First and foremost, as indicated in the aforementioned documentation, we passivated all circuit inputs and performed a .op simulation to observe the circuit error in LTspice. After identifying the error of -609.804uV, to compensate for this operational amplifier error, we added a 10k potentiometer to minimize current consumption. Once we determined the resistances and voltage on the potentiometer, using methods such as Millman or voltage divider, we could verify them using bias current and offset voltage to observe if the error in the LTspice simulator was approximately equal to that in the calculations. Taking values from the datasheet for bias currents and offset voltage, and after a few calculations, we observed that the calculated error voltage on paper was -609.804μ, meaning that we correctly dimensioned the circuit, as we had a value approximately equal to that of the simulator. After dimensioning the stage, we conducted several simulations to observe how the circuit functions and behaves.

Firstly, we performed a Static Operating Point analysis to linearize the circuit. Following this, we conducted a compensation/adjustment simulation of the DC level at the output to observe whether we reduced the initial error. Additionally, we conducted an AC simulation to observe the gain at low frequencies, which was equal to the design specifications. To measure the bandwidth of the amplifier, we used an AC simulation, and the bandwidth was measured at -3 dB. Furthermore, in AC mode, we could observe the PSRR (Power Supply Rejection Ratio) - the variation in balance voltage due to changes in the supply voltage, or CMRR (Common-Mode Rejection Ratio) - the variation in balance voltage due to changes in the common-mode input voltage. Finally, we conducted a transient simulation for Slew Rate (SR): the maximum rate of change of the signal at the AO output. To determine the linearity of the circuit, we performed a transient analysis and varied the output. Additionally, we conducted a Fourier analysis to display THD (Total Harmonic Distortion) in the simulation. To determine THD, we decreased or increased the sinusoidal amplitude, and to verify whether THD decreased or increased, we accessed view->Spice Error LOG. 

The second stage was the Tow-Thomas Filter, for which we dimensioned the circuit and then performed several simulations in LTspice to see how the circuit behaved. The first simulation was the Static Operating Point, followed by an AC simulation to measure the gain in the filter's passband - the gain was measured at 0 dB. We measured the filter bandwidth, and to assess linearity, we transitioned the simulation into transient mode and adjusted the amplitude to achieve a THD of less than 1%. 

The third stage was the PGA (Programmable Gain Amplifier), which we dimensioned and determined the resistances for. Then we moved into the program and created the schema; the first simulation was a static operating point, followed by an AC analysis where we observed all implemented gain steps. Here, we switched each switch to observe their behavior and whether the simulation results matched our calculations. We also simulated the PGA bandwidth for each gain separately; the bandwidth was measured at -3 dB. In the final step, we conducted a transient simulation and observed the circuit's behavior at maximum and minimum gain, concluding that the circuit was linear. 


The final stage was Peak Detect, where we performed several calculations to observe how the diode behaved in conduction and blocking states. Afterward, we conducted a static operating point and an AC simulation to measure the circuit's gain. In this case, we did not verify the linearity per se, as the circuit in practice is nonlinear, but rather the functionality for maximum input amplitude. 

After simulating and observing the behavior of each stage separately, we created a schema of all stages in LTspice as blocks. Finally, we ran an AC analysis and observed that all stages functioned correctly together. 

In conclusion, this project pushed me to develop my thinking, become familiar with the program and various simulations, as well as electronic circuits and their fundamental characteristics and operations.











