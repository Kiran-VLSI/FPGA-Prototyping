FPGA Prototyping: Full Adder Design on Xilinx ISE 14.7 using ZedBoard

Overview✅

This repository demonstrates the block-level design and FPGA prototyping of a Full Adder circuit using Xilinx ISE 14.7 and targeted for implementation on the ZedBoard FPGA development board. A full adder is a fundamental digital circuit used in arithmetic operations, such as binary addition. The project involves designing the full adder circuit at the block level, synthesizing the design in Xilinx ISE, and implementing it on the ZedBoard FPGA for real-time testing and verification.

 Objectives✅

- Full Adder Block-Level Design: Create a block-level schematic design of a full adder circuit.
- FPGA Synthesis and Simulation: Use Xilinx ISE 14.7 to synthesize the design and simulate its functionality.
- ZedBoard FPGA Implementation: Implement the synthesized design on the ZedBoard and test the functionality.
- Hardware Interface: Use the switches and LEDs on the ZedBoard for input/output interaction.

Tools and Technologies✅

- Xilinx ISE 14.7: Software tool used for FPGA design, synthesis, simulation, and implementation.
- ZedBoard: FPGA development board used for hardware testing and prototyping.
- Block-Level Design: Using Xilinx ISE’s schematic editor to design the full adder circuit.
- Xilinx Constraints (XDC): Define the pin mappings for switches (inputs) and LEDs (outputs) on the ZedBoard.

Project Structure✅


 src/                  # Block-level design files (schematics)
 testbench/            # Simulation files for functional verification
 zedboard/             # ZedBoard-specific configuration and constraints
 results/              # Simulation results and bitstream files
 README.md             # Project overview

Full Adder Block-Level Design✅
![image](https://github.com/user-attachments/assets/1318640f-3c2e-4119-ba28-f311934eaec5)


Functional Overview✅

Full Adder circuit is a combinational logic circuit that adds three input bits: two significant bits and a carry-in (Cin). The output consists of:
Sum (S): The result of the addition of A, B, and Cin.
Carry-out (Cout): The carry that results from the addition of A, B, and Cin.

Block Diagram✅

The full adder can be represented as a block-level schematic, where:
1. XOR Gate: Computes the sum.
2. AND Gate: Computes intermediate carry signals.
3. OR Gate: Computes the final carry-out.

- Sum (S)= A XOR B XOR Cin
- Carry-out (Cout)= (A AND B) OR (Cin AND (A XOR B))

Implementation on ZedBoard✅

The ZedBoard has several switches (inputs) and LEDs (outputs). For this project:
Inputs: Use 3 switches for the inputs (A, B, Cin).
Outputs: Use 2 LEDs to display the Sum and Carry-out (Cout) values.

The Xilinx Constraints File (XDC) is used to map the input switches and output LEDs to the correct pins on the ZedBoard FPGA.

 How to Run✅

Step 1: Setup the Xilinx ISE Project

1. Create a new project in Xilinx ISE 14.7.
2. Design the Full Adder:
   - Use the schematic editor in Xilinx ISE to create a block-level design.
   - Place the logic gates (XOR, AND, OR) and connect them according to the full adder block diagram.
3. Add the Constraints File:
   - Define the pin assignments for inputs (switches) and outputs (LEDs) in the XDC file. The file will specify which FPGA pins the switches and LEDs are connected to.

Step 2: Simulation

1. Create a testbench to simulate the full adder's functionality.
2. Run the **behavioral simulation** to ensure the full adder performs correctly. The simulation should show the correct Sum and Carry-out for all combinations of inputs (A, B, Cin).

 Step 3: Synthesis and Implementation

1. Run synthesis to optimize the design for the FPGA.
2. Implement the design and check for any timing or resource constraints.
3. Generate the bitstream file for FPGA programming.

 Step 4: FPGA Programming

1. Connect the ZedBoard to the PC.
2. Open Xilinx iMPACT and program the FPGA with the generated bitstream file.
3. Test the design: Use the switches on the ZedBoard to provide inputs (A, B, Cin) and observe the LEDs for the Sum and Carry-out values.

Results✅

- Simulation Results: Verify that the Sum and Carry-out outputs are correct for all input combinations (A, B, Cin).
- Hardware Results: When the design is implemented on the ZedBoard, use the switches to set the inputs and observe the LEDs lighting up according to the Sum and Carry-out outputs.
- ![Uploading image.png…]()


Challenges Addressed✅

- Designing a simple but functional FPGA circuit using the Xilinx ISE schematic editor.
- Correctly assigning pins for the ZedBoard's switches and LEDs using the XDC file.
- Debugging and ensuring the full adder works as expected on the FPGA hardware.

 Future Scope✅

- Extend the project by designing multi-bit adders (e.g., 4-bit or 8-bit adders) using the same block-level approach.
- Implement other arithmetic logic circuits like subtractors and multipliers on the ZedBoard.
- Explore more advanced FPGA features on the ZedBoard for larger, more complex digital systems.

Acknowledgments✅

- ZedBoard Documentation: For information on how to interface with switches and LEDs.
- Xilinx ISE Documentation: For detailed guidance on using the schematic editor and performing synthesis.
- Dr. Latha P., Mentor, Department of Electronics and Communication Engineering, for guidance and support throughout the project.

  Software Link✅
  You can download Xilinx ISE 14.7 software from the official Xilinx website. Here's the link to the Xilinx ISE Design Suite download page:

[Xilinx ISE Design Suite 14.7 Download](https://www.xilinx.com/support/download/index.html/content/xilinx/en/downloadNav/design-tools.html)

Please note that Xilinx ISE is an older tool, and support for newer devices is limited. For newer FPGA designs, you may want to consider using Vivado Design Suite, which is the successor to ISE and supports a wider range of devices and features.

To access the ISE 14.7 version, you'll need to log in to a Xilinx account (or create one if you don't have it) and select the version you need from the available downloads.


