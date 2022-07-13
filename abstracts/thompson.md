# Adaptive Optics with Julia
## William Thompson (University of Victoria)

Adaptive optics (AO) is a collection of techniques for measuring and correcting for turbulence in the atmosphere to enable large telescopes to work effectively on the ground. It is a topic that is seeing a great deal of research, with new algorithms and sensors being developed every year, yet AO research suffers greatly from the two-language problem since systems must run at 50Hz to 2kHz correction rates with low & stable latency. 
Currently, most researchers develop their algorithms in the lab in MATLAB (running at mere Hz), and then another team rewrites them in C++ to reach stable kHz speeds.

Julia is not yet well suited to real-time applications, but even still, we've found that it can bridge the gap by allowing researchers to test their algorithms on sky at hundreds of Hz with some compromises on latency. I'll demonstrate what we've managed to do in Julia, and what stands in the way for Julia fully solving this two-language problem.
