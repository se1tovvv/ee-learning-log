**This is the hardest, most challenging and demanding course I have ever witnessed so far. A lot of complex math, analysis and interpretation is needed for this subject.**

*I will start with Fourier Transform.*

The Fourier transform converts a signal from the time domain (how a signal changes over time) into the frequency domain (what constituent frequencies make up that signal)

For example, one of the applications of Fourier Transform involves the *noise cancelation system* in Airpods, where tiny microphone in headphones record different frequencies 
and generate the opposing frequency to cancel it out. Same goes with Shazam or MP3 and JPEG Compression, where Fourier Transform breaks heavy audio filled with millions of data points,
and deletes specific redundant frequencies. It also all the hidden frequencies inside a signal at the same time, and tells you exactly how much energy each individual frequency is contributing.

I like to view this physically as follows: Consider the situation where I am entering a room, where a source generates a messy wind pushing at me [x(t)], and I can feel that it repeats every 2 seconds.
In that room we have a hundred of different swings, each oscillating on its own frequency due to different length. This is e^-jwt. But the strange pattern is that I could see that at some instant, one of the swings flies
really high into air, while others barely move or stay completely still.  This is the Integral Spiking. When the math performs the integration (\(\int \)), it is checking to see if energy has piled up. If the forces match, the swing flies (the integral spikes to a large number). 
If they don't match, the forces cancel out, and the swing stays completely still (the integral drops to 0) Computer would record this and tell the frequency of machine, 
as he is given the individual frequencies of multiple swings. This is the Output Spectrum [\(X(\omega)\)]. The computer doesn't look at the wind; it looks at which swings are moving. If it sees the 0.5 Hz swing (the 2-second swing) flying,
it checks its chart and says with absolute certainty: "A 0.5 Hz rhythm exists in the wind."

The same pattern is applied with LC resonators. Before computers, engineers would construct a boxes full of such resonators, each with different frequency. They would plug a messy electronic signal into the box, and whichever circuit started heating up or vibrating the most would light up a
corresponding needle on a display. Since angular frequency of LC is given by 1/sqrtLC. One of such applications is radio. By adjusting the variable capacitor (changing plate overlap area or changing distance between plates) users can select a necessary AM/FM channel. 
