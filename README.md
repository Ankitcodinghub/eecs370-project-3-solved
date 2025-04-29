# eecs370-project-3-solved
**TO GET THIS SOLUTION VISIT:** [EECS370 Project 3 Solved](https://www.ankitcodinghub.com/product/project-3-eecs370-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;114341&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;EECS370 Project 3  Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<a href="https://eecs370.github.io/project_3_spec/">project</a><a href="https://eecs370.github.io/project_3_spec/">_3_</a><a href="https://eecs370.github.io/project_3_spec/">spec</a>

<h1>0. Starter Code</h1>
<a href="https://eecs370.github.io/project_3_spec/starter_3.tar.gz">Starter</a> <a href="https://eecs370.github.io/project_3_spec/starter_3.tar.gz">c</a><a href="https://eecs370.github.io/project_3_spec/starter_3.tar.gz">o</a><a href="https://eecs370.github.io/project_3_spec/starter_3.tar.gz">de</a> for project 3, the LC2K pipelined simulator.

<table width="587">
<tbody>
<tr>
<td width="179">starter_3.tar.gz files</td>
<td width="408">Description</td>
</tr>
<tr>
<td width="179">Makefile</td>
<td width="408">Makefile to compile the project</td>
</tr>
<tr>
<td width="179">p3spec.as</td>
<td width="408">Spec test case assembly file</td>
</tr>
<tr>
<td width="179">p3spec.out.correct</td>
<td width="408">Correct pipelined simulator output for spec test case</td>
</tr>
<tr>
<td width="179">starter_simulator.c</td>
<td width="408">Starter code for the LC-2K pipelined simulator</td>
</tr>
</tbody>
</table>
<h1>1. Purpose</h1>
This project is intended to help you understand in detail how a pipelined implementation works. You will write a <em>cycle-accurate</em> behavioral simulator for a pipelined implementation of the LC-2K, complete with data forwarding and simple branch prediction.

<h1>2. LC-2K Pipelined Implementation</h1>
On this note, the <a href="https://eecs370.github.io/simulators/pipeline/">pipeline</a> <a href="https://eecs370.github.io/simulators/pipeline/">simulator</a> simulates the <em>lecture</em> pipeline instead of the project 3 pipeline.

You will use a clocking scheme mimicking real-life processors (e.g., register file and memory writes require the data to be present for the whole cycle).

<h2>2.2. <strong>jalr</strong></h2>
<h2>2.3. Memory</h2>
Just like <a href="https://eecs370.github.io/project_1_spec/">project</a> <a href="https://eecs370.github.io/project_1_spec/">1</a>, we can access memory directly as an array. The key difference from project 1 is the separation of data and instruction memory.

When the program starts, the starter code will read the machine-code file into BOTH instrMem and dataMem arrays (i.e., they will initially have the same contents).

During execution, you will need to fetch instructions from instrMem and perform load/stores using dataMem . That is, instrMem will never change after the program starts, but dataMem will change.

<h2>2.4. Pipeline Registers</h2>
For project 3, we provide structs representing various values held in the pipeline registers. You are required to use these pipeline register structs as printState() will print out their contents for grading.

Note that the instruction gets passed down the pipeline in its entirety.

You are free to add additional member variables, but do not remove any member variables from the pipeline register structs.

<h1>3. Problem</h1>
<h2>3.1. Basic Structure</h2>
Your task is to write a pipelined simulator for the LC-2K.

The starter code contains a while loop. Each iteration through the while loop executes one cycle:

At the beginning of the cycle, the complete state of the machine is printed using printState() . Notice how printState() is passed the state variable. The state

variable represents the current state of the processor.

In the body of the loop, you will figure out what the new state of the machine (memory, registers, and pipeline registers) will be at the end of the cycle. In short, you will compute the newState , depending on the values found in state .

At the end of the loop, we have the following statement: state = newState . This statement sets the current state of the processor, state , to the values we computed in newState during this cycle. This simulates the positive edge of the clock cycle.

 Specific guidelines for <strong>state</strong> and <strong>newState </strong>:

state should never appear on the left-hand side of an assignment (except for array

subscripts), and newState should never appear on the right-hand side of an assignment.

Reasoning for <strong>state</strong> and <strong>newState</strong> :

Conceptually, all clocked components (pipeline registers, etc.) of a datapath compute their new states simultaneously with combinational logic. Since statements in C execute <em>sequentially</em> rather than <em>simultaneously</em>, you will need two state variables: state and newState . This is so we can mimic a clocking scheme used by real processors.

How to use <strong>state</strong> and <strong>newState </strong>:

Each stage of the pipeline will modify the newState variable using the current values in the state variable. In the body of the loop, you will use newState only as the target of an

assignment and you will use state only as the source of an assignment (e.g., newState… = state… ). For example, in the ID stage, you might have the following statement:

newState.IDEX.instr = state.IFID.instr //transfer the instruction in the IFID register to the IDEX register

Your simulator must be pipelined. This means that the work of carrying out an instruction should be done in different stages of the pipeline as described in lecture. The execution of multiple instructions should be overlapped. The ID stage should be the only stage that reads the register file; the other stages must get the register values from a pipeline register. If it violates these criteria, your project will not pass any test cases.

 At the start of the program, initialize the pc and all registers to zero. Initialize the instruction field in all pipeline registers to the <sub>noop</sub> instruction ( <sub>0x1c00000 </sub>). A <sub>noop</sub> must travel through the pipeline, even though it has no effect on the state of the pipeline.

The easiest way to start is to first write your simulator so that it does not account for data or branch hazards. This will allow you to get started right away. Of course, the simulator will only be able to correctly run assembly-language programs that have no hazards. It is thus the responsibility of the assembly-language programmer to insert noop instructions so that there are no data or branch hazards. This strategy is called <em>avoidance</em>. This will require putting noop s in assembly-language programs after a branch and a number of noop s in an assembly-language program before a dependent data operation. (It is a good exercise to figure out the minimum number needed in each situation.) Keep in mind that the project checkpoint tells you if you are passing cases that avoid hazards (specifically, by removing all branches and by inserting noop s for data dependencies). Then you can finish your implementation by accounting for data hazards and control hazards

<h2>3.2. Halting</h2>
At what point does the pipelined computer know to stop? Itʼs incorrect to stop as soon as a halt instruction is fetched because if an earlier branch was actually taken, then the halt would be squashed.

In the example below, beq 0 0 start will always branch to the start label. However, the halt instruction will enter our pipeline, as we donʼt resolve branches until the MEM stage.

To solve this problem, the starter code stops when the halt instruction reaches the MEMWB register. This ensures that previously executed instructions have completed, and it also ensures that the machine wonʼt branch around this halt instruction. Note how the final printState() call will print the final state of the machine before the check for a halt instruction.

<h2>3.3 Data Hazards</h2>
There are two types of data hazards that will need to be handled:

. Data hazards that do not involve stalling, and can be resolved using data forwarding.

. Data hazards that involve stalling, and still need forwarding

<h3>3.3.1 Data hazards that do not involve stalls</h3>
Use data forwarding to resolve most data hazards. The ALU should be able to take its inputs from any pipeline register (instead of just the IDEX register). To account for a lack of internal forwarding within the register file, youʼll instead forward data from the new WBEND pipeline register. Remember to take the most recent data (e.g., data in the EXMEM register gets priority over data in the MEMWB register). ONLY FORWARD DATA TO THE EX STAGE (not to memory).

Here is an example demonstrating how forwarding is done:

<table width="709">
<tbody>
<tr>
<td width="94">Pipe Trace</td>
<td width="78">Cycle 0</td>
<td width="75">Cycle 1</td>
<td width="77">Cycle 2</td>
<td width="78">Cycle 3</td>
<td width="77">Cycle 4</td>
<td width="77">Cycle 5</td>
<td width="77">Cycle 6</td>
<td width="77">Cycle 7</td>
</tr>
<tr>
<td width="94"></td>
<td width="78">IF</td>
<td width="75">ID</td>
<td width="77">EX</td>
<td width="78">MEM</td>
<td width="77">WB</td>
<td width="77"></td>
<td width="77"></td>
<td width="77"></td>
</tr>
<tr>
<td width="94"></td>
<td width="78"></td>
<td width="75">IF</td>
<td width="77">ID</td>
<td width="78">EX</td>
<td width="77">MEM</td>
<td width="77">WB</td>
<td width="77"></td>
<td width="77"></td>
</tr>
</tbody>
</table>
We require forwarding to resolve this data hazard. At cycle 2, when <sub>add 2 2 4</sub> is in the <sub>ID </sub>stage, <sub>add 2 2 4</sub> will read a <em>stale</em> value from the register file for register 2. The actual value <sub>add </sub>2<sub> 2 4</sub> should use for register 2 is the value computed by <sub>nor 1 1 2 </sub>, as it has the most up to date value for register 2. However, <sub>nor 1 1 2</sub> will not write to the register file until cycle 4, which is too late for <sub>add 2 2 4 </sub>, as will read from the register file at cycle 2.

In order to compute the correct value, <sub>add 2 2 4</sub> will get the the correct value for register 2 from the <sub>MEM</sub> stage, since at cycle 3, <sub>add 2 2 4</sub> is in the <sub>EX</sub> stage, and <sub>nor 1 1 2</sub> is in the MEM stage.

<h3>3.3.2 Data hazards that involve stalls</h3>
You will need to stall for one type of data hazard: a <sub>lw</sub> followed by an instruction that uses the register being loaded.

Here is an example demonstrating <em>why</em> this stall is required:

The goal of this assembly code is to load register 1 with the value 5, and then compute 5 + 5 into register 2.

Letʼs imagine we had the following pipe trace, with no stall. We know that at cycle 2, add 1 1 2 has read a stale value for register 1, instead it should be using the value lw 0 1 five has loaded into register 1. However, since add 1 1 2 reads from the register file at cycle 2, and lw 0 1 five doesnʼt write to the register file until cycle 4, some combination of forwarding and stalling is required.

<table width="709">
<tbody>
<tr>
<td width="137">Pipe Trace w/ no stall

(Incorrect)
</td>
<td width="72">Cycle 0</td>
<td width="71">Cycle 1</td>
<td width="72">Cycle 2</td>
<td width="71">Cycle 3</td>
<td width="72">Cycle 4</td>
<td width="72">Cycle 5</td>
<td width="71">Cycle 6</td>
<td width="72">Cycle 7</td>
</tr>
<tr>
<td width="137">lw 0 1 five</td>
<td width="72">IF</td>
<td width="71">ID</td>
<td width="72">EX</td>
<td width="71">MEM</td>
<td width="72">WB</td>
<td width="72"></td>
<td width="71"></td>
<td width="72"></td>
</tr>
<tr>
<td width="137">add 1 1 2</td>
<td width="72"></td>
<td width="71">IF</td>
<td width="72">ID</td>
<td width="71">EX</td>
<td width="72">MEM</td>
<td width="72">WB</td>
<td width="71"></td>
<td width="72"></td>
</tr>
</tbody>
</table>
The key issue with having no stalls for this situation, is that at cycle 3, when add 1 1 2 <em>needs</em> the correct value for register 1, lw 0 1 five is in the process of reading memory, and in fact does not actually have it yet. Thus forwarding is not enough to resolve this case.

<table width="709">
<tbody>
<tr>
<td width="130">Pipe Trace w/

stall

(Correct)
</td>
<td width="73">Cycle 0</td>
<td width="72">Cycle 1</td>
<td width="72">Cycle 2</td>
<td width="73">Cycle 3</td>
<td width="73">Cycle 4</td>
<td width="72">Cycle 5</td>
<td width="73">Cycle 6</td>
<td width="72">Cycle 7</td>
</tr>
<tr>
<td width="130">lw 0 1 five</td>
<td width="73">IF</td>
<td width="72">ID</td>
<td width="72">EX</td>
<td width="73">MEM</td>
<td width="73">WB</td>
<td width="72"></td>
<td width="73"></td>
<td width="72"></td>
</tr>
<tr>
<td width="130">add 1 1 2</td>
<td width="73"></td>
<td width="72">IF</td>
<td width="72">ID*</td>
<td width="73">ID</td>
<td width="73">EX</td>
<td width="72">MEM</td>
<td width="73">WB</td>
<td width="72"></td>
</tr>
</tbody>
</table>
At the end of cycle 2, instead of moving the add 1 1 2 instruction to the EX stage, we instead forward a noop instruction. This means we will keep add 1 1 2 in the ID stage. Thus, at cycle 4, when add 1 1 2 needs the correct value for register 1, it has access to it, as lw 0 1 five has finished doing the memory read at cycle 3.

<h2>3.4 Control Hazards</h2>
Predict branch-not-taken to speculate on branches, and decide whether or not to take the branch

in the MEM stage. This requires you to discard instructions if it turns out that the branch

prediction was incorrect. To discard instructions, change the relevant instructions in the pipeline to the noop instruction ( 0x1c00000 ). Do not use any other branch optimizations, e.g., resolving branches earlier, more advanced branch prediction, or special handling for short forward branches.

<h2>3.5 Internal Forwarding (Lecture) vs. No Internal Forwarding (Project 3)</h2>
With our lecture register file, we expect to be able to write a new value to a register and to be able to read that new value on the same clock cycle. This is because in lecture we use internal forwarding for our register file. This means when an instruction writes to the register file in the <sub>WB </sub>stage, this updated value can be read in the same clock cycle by an instruction in the <sub>ID</sub> stage.

In the project pipeline, we do not have internal forwarding for our register file. This means when an instruction writes to the register file in the <sub>WB</sub> stage, this updated value cannot be read in the same clock cycle by an instruction in the <sub>ID</sub> Stage.

Consider the following example:

Rationale for considering two designs:

You may be wondering why we need to consider two designs in 370. We feel that design 1 is easier to understand first in the lecture. Design 2 is easier to implement and simulate, and therefore is more appropriate for project 3.

<h2>3.6 Checkpoint (5%)</h2>
For this project, there is a required checkpoint which is worth 5% of the total project grade.

The checkpoint exists to check the basic functionality of your pipeline implementation. All tests for the checkpoint will be constrained to test the following:

LC2K assembly programs which contain no data hazards. This means you do NOT need to implement forwarding or stalling logic for this portion of the project. &nbsp;No BEQ instructions are present

The autograder will give you a score out of 15 points. To determine your final score on the checkpoint, take your autograder checkpoint score / 3. The checkpoint is worth 5% of the project grade.

We encourage you to work towards a correct implementation for the checkpoint and then work on completing the rest of the project.

Do note that we do allow for late days to be used towards the checkpoint; conversely, we strongly encourage you to not use them for the checkpoint as it is worth a small percentage of your final grade and to instead save them for project 3 and project 4.

<h1>4. Running Your Program</h1>
Your simulator should be run using the same command format specified in Project 1, where simulator is the name of the compiled executable:

./simulator program.mc &gt; output

<h1>5. Test Suite</h1>
As part of your grade, you will write test cases for a pipelined simulator. The test cases for this project will be assembly-language programs that, after being assembled into machine code, serve as input to a simulator.

Each test case may execute at most 200 cycles on a correct simulator, and your test suite may contain up to 20 test cases, each containing no more than 50 lines of assembly. These limits are much larger than needed for full credit. See section 6 for how your test suite will be graded.

Writing good test cases for this project will require more thinking than the test suites for the Project 1 simulator. A pipeline simulator is much more complex than the behavioral simulator, and the bugs that should be tested for are correspondingly more complex. Randomly choosing a few instructions is unlikely to expose many pipelining bugs. Think about how to test systematically for pipeline-specific conditions, such as data forwarding, branching, and stalling. As you write the code for your simulator, keep notes on what different conditions youʼve tested for (e.g., forwarding from different stages).

<h1>6. Grading, Auto-Grading, and Formatting</h1>
We will run your program on various assembly-language programs and check the contents of your memory, registers, and pipeline registers at each cycle. These assembly-language programs will have hazards of varying frequency and difficulty.

You will receive feedback from the autograder only for the first THREE SUBMISSIONS on any given day. All subsequent submissions will be silently graded. You may submit your program as many times as you like. Your final score will be derived from your overall <em>best submission</em> to the autograder.

You also are tasked with writing test cases. The auto-grader will correctly assemble each test case in your suite, then use it as input to a set of buggy simulators. A test case exposes a buggy simulator by causing it to generate a different answer from a correct simulator. The test suite is graded based on how many of the buggy simulators were exposed by at least one test case. Your test suite is run on 12 buggy pipeline simulators. To receive all Mutation Testing points, your test suite must expose at least 10/12 of the buggy assemblers.

state.numMemory should be set to the number of memory words in the machine-

code file. This is done by the starter code.

state.cycles should be initialized to 0.

All registers in the processor should be initialized to 0, alongside the program counter.

The instruction field in all pipeline registers should be initialized to the noop instruction ( 0x1c00000 ).

. Pay particular attention to what stage various operations are done in. For example, <sub>PC</sub> is incremented in the IF stage, so the IFID register should have PC+1 .

. Donʼt print the sequence @@@ anywhere except in printState() .

<h1>7. Turning in the Project</h1>
Use <a href="https://autograder.io/">autograder</a><a href="https://autograder.io/">.</a><a href="https://autograder.io/">i</a><a href="https://autograder.io/">o</a> to submit your files.

Here is what you will need to submit for project 3.

. Your pipelined simulator, a C program named simulator.c

. A suite of test cases. (Each test case is an assembly-language program in a separate file, ending in .as , .s , or .lc2k . Test case names should only include letters, numbers, underscores, and periods.)

Your code will be compiled with the GCC compiler using the C99 standard. Use the provided makefile to compile your programs.

The official time of submission for your project will be the time the last file is sent. If you send in anything after the due date, your project will be considered late (and will use up your late days).

<a href="#_ftnref1" name="_ftn1">[1]</a> .1. Datapath
