General approach
1. strip down red grouper assessment model to a more simple model with just fishery-independent and commercial handline information
2. write .dat file with r script
3. run stripped down red grouper assessment model with new .dat file and compare results
    -had to modify tpl to match order of fleet loop (cH, serfs)
************** not so 'ta da' fixes
                    spawning time fract differed - automated in R script but does not match s53 value for mid-april
                       fixed to s53 value - no improvement
                    modified significant digits in landings and discard csv files to match data, still come in as 
    -runs match exactly after modifying landings and discard CVs to 0.05 instead of actual estimates
MODIFICATION: Seperate creation of data list and writing of .dat file
    -created writeList.r
    -standardize naming convention to BAM admb when writing files then convert to FishGraph in .cxx
**************** currently here, started writing .dat and .tpl in single R file, started thinking about approach
BRAINSTORM: what is the best way to run simulations?  I have been approaching from assessment development rather than simulation
    - .creating new .csv input is probably not it
    - do you typically store a folder with each run?
    - if modifying an R list with a standard structure, is it in a loop in R calling ADMB?
    - need to look at efficient simulation code, compare methods
    - the current method would work if the structure of the model did not change from one simulation to the next
    - may not be too bad if writing .csv does not take too much time
    - is it possible to write to specific line in text file?
4. write .tpl with r script
5. run strippped down red grouper assessment model with new .dat and .tpl and compare results
6. write .cxx with r script
7. run stripped down red grouper assessment model with new .dat, .tpl, and .cxx and compare model results and .rdat file
8. add fleets back to model for .dat, .tpl, and .cxx
9. compare full model run from r script to base run from red grouper assessment

