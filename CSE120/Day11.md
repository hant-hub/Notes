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

