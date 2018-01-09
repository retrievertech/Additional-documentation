# Additional documentation
This repository will eventually contain SBIR applications (successful and otherwise) the final Phase II SBIR report (that's as far as the funding went), and other information that I hope will be useful for future collaborators.
I will try to explain the various docs in this readme.  Sorry if it's not up to date but I'll try.

PHASE II FINAL REPORT

This is what the title says, the final report sent to the DOE as a reporting requirement for the SBIR Phase II funding that created the SKATE software and website.  Aside from the code itself, this is the most detailed and readable description of the software that analyzes seismograms (what we call 'the pipeline') and the computer architecture that runs the web site and the UI.


PROJECT NARRATIVE DOE FEB2017.PDF

This is the most recent SBIR application (which was rejected), and has the most current thinking on ways to improve SKATE.  We believe that implementing some basic image processing algorithms will lead to rejection of almost all spurious features, greatly simplifying final editing. Segment assignment algorithms are a little more complicated, but all have been experimented with and will work to what we believe is a high degree of success. This document is useful for anyone looking to quickly improve the code to a research-capable level of operation.


SEGMENT ASSIGNMENT METHODS

We have investigated other segment connection and assignment methods that were not included in the current operational version of SKATE. This document summarizes the work in three areas: Clustering based on the work by Frey and Dueck (Clustering by Passing Messages
Between Data Points), Bayesian Methods for segment connection, and Multiple Traveling Salesman.  The first two were run using real data, and the MTSP method uses simulated seismogram data.  The final portion of the doc called multi criteria decision making has not been tested. It represents the beginning of an idea about how to use a variety of inputs to assign the most likely segments to their proper place in the time series. 
