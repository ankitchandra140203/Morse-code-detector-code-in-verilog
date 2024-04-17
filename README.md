# Morse code detector code in verilog
 Morse code detector code in verilog using fsm and switch case which will detect emergency signal "HELP".

 ## Let's break the code 

 ### Module Declaration: 
 The code defines a module named top_module. It has inputs reset, data, and clk, and an output LED.

 ### Parameter Declaration: 
 Parameters A, B, C, ..., H are defined with specific values. These parameters are used to represent different states in the finite state machine (FSM).

 ### State Registers:
 reg [2:0] state, next_state;: These registers hold the current state (state) and the next state (next_state) of the FSM.

 ### Sequential Logic (State Update):
 This always block is triggered on the positive edge of the clock (clk).
 If reset is asserted, the FSM resets to state A. Otherwise, it updates its state to the value of next_state.

 ### Combinational Logic (State Transition):
 This always block is triggered whenever any of its inputs change.
 It defines the state transitions of the FSM based on the current state (state) and the input data (data).
 Each state has associated conditions for transitioning to the next state. For example, if the FSM is in state A, and data is true, it transitions to state B; otherwise, it stays in state A.

 ### LED Assignment:
 This always block assigns the output LED based on the current state (state). If the FSM is in state H, LED is assigned 1; otherwise, it's assigned 0.
