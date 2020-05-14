Metadata for NL_muskrat_2013-2016.csv 

    Emiel van Loon, Daan Bos, Erik Klop & Ron Ydenberg
    October 2019
    e.e.vanloon@uva.nl

## Introduction

This data set supports the publication 'A Large-Scale Experiment to Evaluate the 
Effects of Trapping to Control Muskrats (Ondatra zibethicus) in The Netherlands' 
by Daan Bos, Emiel van Loon, Erik Klop and Ron Ydenberg.
(the paper was accepted for publication in Wildlife Society Bulletin in 2020)

The Muskrat is an invasive species in Europe and in the Netherlands muskrat 
burrowing can compromise the integrity of dykes and hence poses a public safety 
threat. For that reason a control programme has been in effect since the arrival 
of the species in 1941. To investigate the relation between catch and effort and 
enhance prediction models, a large randomized controlled experiment was designed 
and conducted from 2013 till 2016. The publication by Bos et al. (2020) analyses 
the experimental results and here we present and document the experimental data.


## Details of experiment

The experiment ran for 39 months (December 2012 - March 2016) in the Netherlands. 

Two treatments were applied:

1. a manipulation of effort, relative that in a reference period 
   (the 12 months preceding the start of the experiment in December 
   2012): 30% decrease, no change and 30% increase (3 levels) 
2. a manipulation of timing in which effort was spent: year-round 
   (yr) or concentrated in winter and spring at the cost of time 
   spent in summer (sc) (2 levels)

The treatments were applied to experimental units of 5 by 5 km (atlas squares),
units which coincide with the national coordinate system of the Netherlands
(EPSG:28992, also RD New; http://www.epsg-registry.org/). The Dutch mainland 
contains 2202 atlas squares in total. From these 117 atlas squares were selected 
for the experiment through a stratified random procedure. 
Table 1 below summarizes the distribution of the experimental units over the 
three strata (areas of high, medium or low muskrat suitability), as well as the 
two treatments. Table 2 characterises the three strata through the available 
muskrat habitat (length of water ways) and the historical catch and effort data.

    Table 1. Distribution of experimental units 
             (117 atlas squares in total) over the
             two treatments within each of the 
             pre-defined strata. 
    =======================================
              decrease  control  increase   <-- effort treatment
    Stratum   --------  -------  --------    
               yr   sc     yr     yr  sc    <-- time treatment
              ---  ---    ---   ---  ---
    low        7    6     13      7   6
    medium     7    6     13      7   6
    high       7    6     13      7   6
    =======================================
    
    
    Table 2. Characterisation of the 3 strata through the
             average length of the water ways per atlas
             square as well as the average catch (numbers
             of muskrat caught) and effort (field hours),
             both per atlas square per year.
             The column labeled N gives the number of
             atlas squares in the Netherlands within the
             respective stratum.
    =====================================================
                                   average over 2009-2011
                                  -----------------------    
    stratum   N   waterway (km)   catch (nr)  effort (hr) 
    -------  ---  -------------   ----------  -----------
    low      701     93             27          145
    medium   460    285            124          480
    high      76    506            796         1730
    =====================================================

For each atlas square we aggregated the records by 'season': spring (day-of-year 
57 - 140); summer (141 - 224); autumn (225 - 308); and winter (309 - 56 in next 
year). The experiment ran for 13 successive seasons, identified in the analysis 
by the variable named 'timenum', from winter 2012/2013 (timenum = 1) through 
winter 2015/2016 (timenum = 13).  

Each record in the data set refers to the observations concerning one atlas 
square during one season. Hence there are 117 (experimental atlas squares) * 13 
(seasons) = 1521 records in the data set with experimental results.  

In the experimental period, muskrat trapping continued according to standard 
procedures in the remainder of the Netherlands, covering 1401 non-experimental
atlas squares (these non-experimental atlas squares are all areas in the 
Netherlands were effort was spent from 2012 to 2016 to catch muskrats).
Also the data for these non-experimental atlas squares data for the 13 seasons 
seasons is included in the dtaa set (1401*13 = 18213 records).


## Data matrix

The data matrix contains 19734 rows and 17 columns. Each row contains 
information for one atlas square in one season. Each column represents a 
variable. The labels, definitions and data types of the variables are as follows.

- as = 
  atlas square, a unique identifyer for a 5 km by 5 km block 
  fitting in the dutch coordinate system (integer)

- rwa = 
  name of regional water authority, 21 labels in total (character)

- year = 
  year of observation (character)

- yearnum = 
  year of observation (integer)

- season = 
  season: winter, spring, summer, autumn (character) 

- seasonnum = 
  season: 1 to 4 (integer)

- time = 
  incremental time since start of experiment z-transformed values of timenr (float)

- timenum = 
  incremental time since start of experiment: 1-13 (integer)

- stratum = 
  the stratum in which the as falls: low, medium and high suitability for muskrats;
  NA values for all atlas squares that are not part of the experiment (character)

- eff = 
  the effort treatment: control, decrease, increase and no experiment (character)

- temp = 
  the temporal treatment: the effort to catch muskrats is distributed year-round
  (yr) or concentrated in the spring and winter seasons (sc); NA values for all 
  atlas squares that are not part of the experiment (character)

- hist = 
  average catch per unit effort in the 3-year period 2010-2012 (float)

- neighb = 
  average catch per unit effort in the 8 atlas squares surrounding the focal 
  atlas square (float)

- soil = 
  soil type (sand, loam, clay, peat), built-up area or water (character)

- catch = 
  number of muskrats caught (integer)

- effort = 
  number of hours spent on muskrat trapping (float)

- cpue = 
  catch per unit effort, i.e. catch/effort (float)


## Other details about encoding and file format

Missing data in the data matrix is encoded by the text label NA

The file "NL_muskrat_2013-2016.csv" uses the comma as the field separator and
the point as a decimal sign. It has a header with the variable labels at the 
first row. The variable names in the header as well as character data are 
between double qoutes (".."), the missing data label (NA) is not in quotes.

## License
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />
This data set is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.
