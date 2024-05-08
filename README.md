# immrax_rtd_combo

## TODO:
1. wind fields that are spatially varying!!!!!!

## Baseline idea: RTD requires conservative/incorrect tracking error function
overarching stories: there are separate sources of error that RTD lumps together
general goal: decouple sources of error: trakcing error vs disturbances as opposed to lumped error from RTD original error function

## Phase 1.
RTD requires a failsafe RTA, can only work if immrax is less conservative than RTD
## Phase 2.
Relax RTD tracking error function and implement a heuristic with some notion of uncertainty to not lean on any correctness of RTD and have RTA be the only RTA then we can lean on the tightness of immrax to have more available trajectoreis because RTD would tell us some of them would be unsafe
(replace tracking error with less conservative one and make immrax be a true failsafe for the controller)
## Phase 3.
In event we detect collision and we have compute time, we can differentiate the reach tube and go back to the control paramters in RTD and take a gradient step to get new parameters that would be safer based on this info
(Get gradients wrt k from the trajectories -> may be an issue to get helper funcitons but should be a one-line thing ideally from bad trajectories to K values)

## Separate idea:
## Phase 4.
Immrax to represent difference between high and low fidelity models

## Deliverables:
End of summer have a rough draft: ACC/ICRA submission (ICRA prefers hardware demos) -- get it done on quads!!! 
MAY BE EASIER TO DO CONTROL WITH SOME SIMPLE LINEAR PD CONTROLLER BEFORE MELLINGER (MAYBE WARDI CONTROLLER)
If we do hardware more reasonable to submit to RA-L (sam's never been successful here we can succeed !!!)


