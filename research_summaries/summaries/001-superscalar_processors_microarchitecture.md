# The Microarchitecture of Superscalar Processors

## Problem
Pipelined (scalar) processors' initiation rate is one instruction per cycle, which is a serious practical bottleneck.

## Solution
Superscalar processors by initiating more than one instruction at a time into multiple pipelines, tackle this bottleneck. These processors are capable of executing more than one instruction in a clock cycle by exploiting **I**nstruction-**L**evel **P**arallelism (**ILP**). These processors convert a seemingly sequential program into a more parallel one. The process of a superscalar processor on instructions can be broken down into as follows:
- **Instruction Fetching and Branch Prediction**: During Instruction fetch, the outcomes of conditional branch instructions are usually predicted in advance to ensure an uninterrupted stream of instructions. 
- **Instruction Decoding, Renaming, and Dispatch**: The outcoming instruction stream is then analyzed for data dependencies, and instructions are distributed to functional units, often according to instruction type. 
- **Instruction Issuing and Parallel Execution**: Next, instructions are initiated for execution in parallel, based primarily on the availability of operand data, rather than their original program sequence, which is referred to as Dynamic Instruction Scheduling. 
- **Committing State**: Upon completion, instruction execution results are *resequenced* so that they can be used to update the process state in the original program order.