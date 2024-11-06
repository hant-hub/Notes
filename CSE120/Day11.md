## Dynamic Branch Prediction

use past branch behavior to predict
future branches


one possible scheme -> always guess the last
outcome of the branch.

1-bit dynamic prediction

<hr>

## State Machine

we can use a finite state machine to model
our dynamic branch prediction.

For a 1-bit branch predictor only a single
misprediction will shift the state of the
predictor.

Q: how to emulate in hardware?
A: create a lookup table

A Branch History table.
BHT is usually seperate from main memory

<hr>

In practice a BHT cannot hold info for all
branch instruction addresses in our program

a large BHT will slow memory access and reduce
CPU performance.

A small BHT table with limited rows is used
- I think a BHT could be implemented like a
smaller L1 cache

old branch instructions are periodically
flushed

how is the BHT reinitialized?

usually pick a random start.

<hr>

## Two Bit Branch Predictor

2-bit predictor uses past two branches.

if past two branches were the same predict
the same

if different predict the last branch but
weakly

generally predictors only use a small number
of bits.

it might take up to two mispredicts in order to
change the next prediction.

note: this behaves exactly like a 1-bit
predictor given alternating branching
behavior

the more bits used the more time is
required for "warm up"

more bit predictors are more accurate with
inputs that rarely change.

## Caching

- does not concern ISA
- about physical limitations

types of memory
- Registers (10ps) -> not feasible for large data
- Static Ram (0.2ns) -> $100 per GB
- Dynamic Ram (50-70ns) -> $5 per GB
- Flash (20u - 5ms) -> $0.5 per GB
- Magnetic Disk (5-20ms) -> $0.05 per GB

note: only Flash and Magnetic is
nonvolitile and only magnetic disk
is mechanical 

ideal memory has access time of registers or
SRAM, with cost and size of Magnetic Disks


Massive physical and technical limits on
memory. DRAM and memory access speeds have
improved less than processor clock speeds.

### Locality

Spatial Locality -> if data is referenced,
data with similar addresses are likely to
be referenced

Temporal Locality -> if data is referenced
it is more likely to be referenced again.


Main takeaway: we only use small portions
of memory at any given time.













