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


LINAGRAPH 480 PAPER SPEC SHEET
This is a copy of the spec sheet of the photosensitive paper that was originally used when recording WWSSN seismograms on a rotating drum. It might become useful when trying to model the response of the paper vs. the residence time of the incident light beam on the paper. For example, line width and line intensity are a function of residence time; hence, the relative slope of a trace can be calculated by its width and intensity.


NMSBA_RT2.pdf
This is a report compiled by Sandia National Laboratories on work performed under an NMSBA grant.  It discusses their work in mapping timing marks, which is somewhat useful though I believe contains inaccuracies particularly where is concludes that timing marks are mapping backwards in time (which isn't possible). Also, moving the timing marks in image space to connect to the parent trace is, I believe, inefficient and prone to all kinds of inaccuracies, particularly when considering that image processing routines can easily over or underestimate the size of the trace (i.e. in the former case create a timing mark that is significantly larger than the gap in the parent line).  I believe that connecting in data space is a much more accurate and efficient method for properly placing timing marks in the time series.

The second half discusses Sandia's work using Trace Enhancement with Contourlets It is a possible additional method for detecting traces in a noisy environment.  This was not included in SKATE, but did show promise.  The matlab code is available, though I have never run it. 
