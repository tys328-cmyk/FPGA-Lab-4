ECE 128 Lab 4 – Vehicle Safety Interlock & Warning System

Project Description

This project implements a vehicle safety interlock and warning system using purely combinational logic, with no memory elements or clocks. The design evaluates 14 simulated sensor inputs (seatbelt, door, key, brake, park, hood, battery, airbag, coolant temperature, passenger occupancy and seatbelt, trunk, parking brake, and a service mode jumper) to determine whether the engine is permitted to start and which warnings or chime should be activated. The Basys 3 board's switches (SW15-SW3) emulate the sensor states, and the board's LEDs (LED15-LED5) display the resulting system decisions and warnings, including START_PERMIT, CHIME, the two highest-priority active warnings, and individual warning indicators for seatbelt/occupancy, door, hood, trunk, battery, airbag, and temperature.

Simulation

1. Open the project in Vivado.
2. Add the top module as a design source.
3. Add the corresponding testbench as a simulation source.
4. Set the testbench as the simulation top module.
5. Run Behavioral Simulation.
6. Verify from the waveform that each tested combination of SW15-SW3 sensor inputs produces the expected START_PERMIT, CHIME, warning priority, and individual warning outputs.

FPGA Implementation

1. Select the Basys 3 as the target FPGA board.
2. Select the top module as the top module for implementation.
3. Add the Basys 3 constraints file and assign the sensor inputs to switches SW15-SW3 and the warning/decision outputs to LEDs LED15-LED5.
4. Run Synthesis.
5. Run Implementation.
6. Generate the Bitstream.
7. Connect and power the Basys 3.
8. Open Hardware Manager and program the FPGA with the generated bitstream.
9. Test different switch combinations representing various sensor states and verify that the LEDs correctly reflect the expected START_PERMIT, CHIME, and warning behavior.
