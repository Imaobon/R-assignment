### Summary of Comments

### line 9

I did not have reshape2 as an option and had to add that package, also I think you are missing the quotation marks around naniar. Might also be useful to seperate the install and load code blocks since most people will have installed the majority of packages needed.


### line 27

This gave an error,I included some options and it was able to run.

### line 176

Cbind is risky and only works if your files are both sorted exactly the same. It will not show an error if that is not the case, but will paste everything together anyways. inner_join or merge.dataframe are safer.

### line 215

There are a few markers that have multiple positions on the same chromosome that will be missed if filtering by chromosome instead of by the values in the position column. There are also a couple of NA's and Nulls in the the position column depending on the type of problem with the location. Also, this runs faster than I thought, but you can run the same thing with lapply on a list of chromosomes and dataframes as another option.

### line 293

This runs but throws some not so important errors.  The errors for the 11 rows might have something to do with the markers not removed when filtering by missing/unknown chromosome instead of positon.

### line 304

This is useful. I haven't used it before, but it seems like a nice way to get higher quality pictures of figures generated in R.


Overall this is really great. Most this work with very minimal intervention, and the output is well organized. If you define some of your filtering and sorting as fuctions, you can run it on a list of of files and avoid repeating the same code for the maize teosinte etc but it makes little functional difference, just makes the code cleaner.