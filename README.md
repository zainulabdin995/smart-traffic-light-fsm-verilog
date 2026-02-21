# Smart Traffic Light Controller using Mealy FSM

## Overview
This project presents a dynamic, sensor-driven traffic light controller designed to replace inefficient fixed-timer systems. Built using a Mealy Finite State Machine (FSM), the system adapts to real-time traffic conditions by detecting vehicle presence on intersecting roads and adjusting traffic light outputs accordingly. 


## Tech Stack & Tools
* **Hardware Description Language:** Verilog HDL
* **Simulation & Verification:** Xilinx Vivado (Waveform Analysis)
* **Logic Design:** NI Multisim (74-series digital IC implementation)
* **Core Concepts:** Digital System Design, Synchronous Logic, Modular Routing

## System Architecture
The controller is designed with a highly scalable, modular architecture consisting of three primary components:
1. **Traffic FSM (Mealy Machine):** Evaluates current light states and sensor inputs to determine the next state transition.
2. **Timer Module:** Provides customizable countdown intervals for each state (Green, Yellow, Red) using a synchronized MOD16 counter architecture.
3. **Light Decoder:** Maps the active FSM state to the corresponding physical traffic light outputs for both the main and side roads.


## Key Features
* **Dynamic Traffic Control:** Prioritizes the main road but safely transitions right-of-way when side-road vehicles are detected.
* **Customizable State Timing:** Modifiable time intervals for different light states without altering the core FSM logic.
* **Dual Implementation:** The logic was successfully synthesized in Verilog HDL and physically modeled using discrete logic ICs (Multiplexers, Comparators, D-Flip-Flops) in Multisim.

## How to Run the Simulation
1. Clone the repository: `git clone https://github.com/zainulabdin995/smart-traffic-light-fsm-verilog.git`
2. Import the `.v` files from the `src/` directory into your Xilinx Vivado project.
3. Add the `tb_traffic.v` file from the `testbench/` directory as your simulation source.
4. Run the Behavioral Simulation in Vivado to observe the state transitions and timer logic in the waveform viewer.
