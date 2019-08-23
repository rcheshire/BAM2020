General approach
1. strip down red grouper assessment model to a more simple model with just fishery-independent and commercial handline information
2. write .dat file with r script
3. run stripped down red grouper assessment model with new .dat file and compare results
    -had to modify tpl to match order of fleet loop (cH, serfs)
************* currently here, results don't match trying to figure out why
************** not so 'ta da' fixes
                    spawning time fract differed - automated in R script but does not match s53 value for mid-april
                        fixed to s53 value - no improvement
                    modified significant digits in landings and discard csv files to match data
**************** comparing (in emacs, waiting for notepad compare plugin to be installed) .rdat files for each run 
**************** will compare .dat files when notepad is installed, better at skipping irrelevant diffs
4. write .tpl with r script
5. run strippped down red grouper assessment model with new .dat and .tpl and compare results
6. write .cxx with r script
7. run stripped down red grouper assessment model with new .dat, .tpl, and .cxx and compare model results and .rdat file
8. add fleets back to model for .dat, .tpl, and .cxx
9. compare full model run from r script to base run from red grouper assessment

