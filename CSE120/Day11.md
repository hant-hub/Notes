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




