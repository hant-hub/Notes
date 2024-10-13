Professor: Sagnik Nath

Grading
- 30% Homework
- 8% Quizzes
- 60% Exams (30% final + 30% Midterm)
- 1% Syllabus Quiz
- 1% Attendance quizzes
- curved

Agenda
- Course Logistics
    - 6 Homeworks -> can discuss but must work individually
        - No late work
        - posted as PDF
        - submit as PDF
    - 3 Quizzes total -> async
    - 2 exams -> Avalible online, no proctoring, final will
    be comprehensive
    - Course Outline
        - Basics and Pipelined CPU
            - trends, performance, ISAs, RISC-V, datapath vs control
            etc.
        - Memory and Parallelism
            - branch speculation, caches, virtual memory, coherence
- Motivation
    - Technology trends
    - Why computer architects are improtant
    - How does asssembly end up executing logic?
    - What happens in-between hardware & software?
    - How is a computer designed?


Goals
- Memory
    - caches, RAM, external storage
    - memory hierarchy, virtual memory
    - space complexity
- Compile vs Run time
    - Code transformation vs execution
    - role of compiler
    - post-compilation optimization
- Efficient Data Structures + Algorithms
    - when to choose a data structure
    - hardware level consequences of data organization
    on speed + memory efficiency

    Buy Textbook


Working on Runtime, ISA, and Microarchitecture


Instruction Set Architecture
- List of assembly instructions
- Interface to control CPU
    - ex: ADD, SUB, LOAD, etc.
    - Hide details: hide cache, hide branch predictor, hide
    prefetcher, etc.
- Some ISAs are licensed, ex: x86, ARM, R700, MIPS
- other ISAs: Motorola, PowerPC

In academia -> RISC-V was custom made for teaching
x86 only allows AMD and Intel to manufacture cpus

Open Source ISAs
- Spark 32
- Spark 64
- RISC-V


Microarchitecture (\mu Arch)
- How an ISA is going to be physically implemented
- abstraction above logic gates -> logic blocks like register files, ALU, etc.


Manufactured vs Assembled vs Designed
- Different companies manufacture components
- Companies might design blueprints, then fabricate chipsets
- Company will assemble components in a factory and sell to customers

Fabrications
- for Phones -> TSMC or Samsung
- for old tech -> Global Foundry
- for PCs -> Intel Foundry



Moore's Law
- Number of transistors doubles every few years
    - some say double performance -> not the same
    - some say double transistors at same cost -> also no longer true
- super dead

Transistors in the past used to be linear with performance
-> smaller transistors can be charged faster, and should be able to switch at higher
speeds
-> Stopped being true around early 2000

Over time Clock speed has stagnated
The Power consumptions and perf/clock stagnated

Thermal constraints started constraining performance at ~100-150W
The Power Consumption limits clock speeds


Dennard Scaling
- Way to scale transistors to keep power density constant
- Dynamic Power dissipation of MOSFET = a * C * f * v^2
    - a = percent time switched, C = capacitance, f = frequency, v = voltage
- Capacitance is related to area
    - As transistors shrink, voltage was reduced and circuits can operate at higher
    speeds with the same power
    - As frequency is increased, power consumption increases as well

Dennard Scaling stops due to minimum voltage for silicon switching

Cost per transistor has stagnated

After end of Dennard Scaling -> scaling cores
-> Parallel performance has been increasing
