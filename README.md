# Thesis_Data
A mathematiatica notebook which simulates a variety Logical Fidelity Estimation protocols.

This appendix is meant to be a simple guide for replicating the results contained in the thesis. 
Although full documentation is not currently available, questions about further usage can be directed to mathmeetsmusic@gmail.com.


Begin by downloading and opening the "Thesis_Numerics.nb" file along with the Thesis_Data folder full of .mx files from the repostiory:
https://github.com/mathmeetsmusic/Thesis_Numerics


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

Viewing the Data

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------


We also give the option of load the data is displayed in the thesis for further analysis. First, to load and view the data, download the file labeled thesis_data
and save the .mx files inside to a known directory. Open the chapter labeled "Save, Display, and Retrieve Data." From there, open the section labeled 
"save and manipulate data" and scroll down to the "Get" function. Inside the Get function, one should copy the directory where the .mx files have been placed.
After running the cell successfully, the data should be ready to display. Open the section labeled "survival probability plot" located right above the
"save and manipulate data" section we just modified. Finally, one can run the first cell to see the survival probability with an exponential fit. The second
cell shows the survival probability alone. 


The data from each of the experiments is stored in the DataBase. To find out which benchmarks are currently in the database, run Keys@DataBase. Once you pick a 
key from the file, you can access data from the benchmark by writing DataBase[key]. It's a lot of data, so best not to print it out all at once. But you'll find the
data is of the form {sequence length, average survival probability, confidence interval, raw data}. Where the raw data is a very large arrange of survival probabilities
collected from all the LFE sequences.

More fine-tuned information can be found in the DataInfo variable. It is organized much like the DataBase variable with identical keys. However, DataInfo gives
specific information about the experiment. For instance, one can write DataInfo[Keys]["circuit"] to see how many circuits were used to estimate the average survival
probability.


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

Reproducing the Data

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

Scroll down to the section labeled "benchmark." Within that section, one should find four subsections, each containing code for a different set of procedures. The first three concern this thesis directly. To produce the results of~\cref{AppendixB} below, run each of the cells in the subsection labeled "Plot Sequences for Appendix B" in the order provided. To plot the results of Fig 7.1, one can run the subsection labeled "Test to see if Recovery can be Delayed" in the order provided. Finally, the discarded post-selection plots with heightened error rates can be re-created by running all the cells in the subsection labeled "Discarded Post-Selection with Non-standard Decay."

The length of run-time will vary dramatically based on the error model and sequence type. Running on eight cores, each of the above procedures will likely finish in under 4 hours of computation. Note that the default precision of benchmarks is much lower than the precision provided in this thesis. To recreate the data here, one will have to adjust the ncircuit variable to the desired precision. We have included real-time estimates of total run-time for each of the types of LFE. However, the accuracy and frequency of updates may vary. The resulting plots should be automatically placed in the current directory of the .nb file.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Thanks for reading!
Athena


Look for more detailed docs in the future where I'll explain how to use tags to run your own experiments!
