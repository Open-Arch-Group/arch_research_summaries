# The Microarchitecture of Superscalar Processors
Scalar processors process only one data item in a clock cycle, which are classified as Single Instruction Single Data (SISD) processors in Flynn’s taxonomy. On the other side, superscalar processors are capable of executing more than one instruction in a clock cycle by exploiting Instruction-Level Parallelism (ILP). Superscalar processors convert a seemingly sequential program into a more parallel one. A superscalar processor fetches and decodes the incoming instruction stream several instructions at a time. Pipelined processors' initiation rate is one instruction per cycle. it was perceived to be a serious practical bottleneck. But, superscalar processors by initiating more than one instruction at a time into multiple pipelines, broke the single instruction per cycle bottleneck. As part of the instruction fetching process, the outcomes of conditional branch instructions are usually predicted in advance to ensure an uninterrupted stream of instructions. The outcoming instruction stream is then analyzed for data dependencies, and instructions are distributed to functional units, often according to instruction type. Next, instructions are initiated for execution in parallel, based primarily on the availability of operand data, rather than their original program sequence, which is referred to as Dynamic Instruction Scheduling. Upon completion, instruction execution results are resequenced so that they can be used to update the process state in the original program order.