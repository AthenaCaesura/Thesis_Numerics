# Thesis_Data
A mathematiatica notebook which simulates a variety Logical Fidelity Estimation protocols.

This appendix is meant to be a simple guide for replicating the results contained in this thesis. 
Although full documentation is not currently available, questions about further usage can be directed to mathmeetsmusic@gmail.com.


Begin by downloading and opening the ``Thesis\_Numerics.nb" file. Once open, scroll down to the section labeled ``benchmark," and within that section, one 
should find four subsections, each containing code for a different set of procedures. The first three concern this thesis directly. To produce the results 
of~\cref{AppendixB} below, run each of the cells in the subsection labeled ``Plot Sequences for Appendix B" in the order provided. To plot the results of 
Fig 7.1, one can run the subsection labeled ``Test to see if Recovery can be Delayed" in the order provided. Finally, the discarded post-selection plots with 
heightened error rates can be re-created by running all the cells in the subsection labeled ``Discarded Post-Selection with Non-standard Decay."

The length of run-time will vary dramatically based on the error model and sequence type. Running on 8 cores, each of the above procedures will likely finish 
in under 4 hours of computation. Note that the default precision of benchmarks is much lower than the precision provided in this thesis. To recreate the data 
here, one will have to adjust the~\emph{ncircuit} variable to the desired precision. We have included real-time estimates of total run-time for each of the 
types of LFE. However, the accuracy and frequency of updates may vary. The resulting plots should be automatically placed in the current directory of the .nb file.
