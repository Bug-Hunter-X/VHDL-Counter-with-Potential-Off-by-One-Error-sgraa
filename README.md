# VHDL Counter Bug
This repository demonstrates a common but subtle bug in VHDL code: a missing `else` statement in a counter's process. The `buggy_counter.vhdl` file contains the buggy code, while `fixed_counter.vhdl` provides the corrected version.

## Bug Description
The buggy counter lacks a proper `else` condition when incrementing.  If there's any unusual clock behavior (glitches or noise), the counter's behavior might be unpredictable, possibly resulting in an incorrect count.  The fix ensures the counter increments predictably regardless of spurious clock edges. 

## How to Reproduce
Simulate both VHDL files using your preferred VHDL simulator. You may observe unexpected counter behavior in the buggy version under certain simulation conditions involving clock noise. 