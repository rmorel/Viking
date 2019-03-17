# Viking

A repository with scripts to process the [Mobil Avo Viking Graben Line 12](http://s3.amazonaws.com/open.source.geoscience/open_data/Mobil_Avo_Viking_Graben_Line_12/mobil_avo.html) using only open source software.

## About the data

This data set is the [Mobil Avo Viking Graben Line 12](http://s3.amazonaws.com/open.source.geoscience/open_data/Mobil_Avo_Viking_Graben_Line_12/mobil_avo.html) and was released originally for the 1994 SEG workshop. This data set is in the public domain (Keys and Foster, 1998).

This data set has a 2D marine seismic line, far field source signature, some well logs and checkshots.

## Motivation

This is just a proof of concept, I want to prove that it is possible to do seismic processing on real data using open source tools in a comprehensive manner. I started this effort because I was not satisfied with current open source processing workflows. Because of that, I also want this processing workflow to be as close as possible to current industry standards.

I’m doing this on my spare time, so the progress may be slow at times. I’m also constraining myself to use only Madagascar, Python and Jupyter Notebooks, since this makes the workflow simpler to understand.

Once done, I also intend to rewrite the same workflow using separated Sconscripts (see [Scons](https://www.scons.org/)). This will make the workflow more reproducible and it may be used as a template to process many lines at once.

## Materials

You just need to clone this repository, install all the Python dependencies and also [install Madagascar](http://www.ahay.org/wiki/Installation). For the Python dependencies you need to use Python 2.7, since Madagascar API does not work with Python 3 (ohhhh the pain...).

I’m making the processing flow as light as possible, so any common desktop PC should be able to run it with no problems. Besides that, you will need some GB of free storage space.

## Processing workflow

The following links are the notebooks for each key processing workflow process.

[00 - Fetch data from remote servers](https://github.com/rmorel/Viking/blob/master/00%20-%20Fetch%20data%20from%20remote%20servers.ipynb): Simply download the data.

[01 - Inspect data and add geometry](https://github.com/rmorel/Viking/blob/master/01%20-%20Inspect%20data%20and%20add%20geometry.ipynb): This data needed extra geometry definitions to be processed.

[02 - Fetch and inspect well data](https://github.com/rmorel/Viking/blob/master/02%20-%20Fetch%20and%20inspect%20well%20data.ipynb): Besides fetching and inspecting the well log data, I also create a composite well log file in PDF for each well.

[03 - Burst noise removal](https://github.com/rmorel/Viking/blob/master/03%20-%20Burst%20noise%20removal.ipynb): Investigate if the data is polluted with burst noise.

[04 - First check stack](https://github.com/rmorel/Viking/blob/master/04%20-%20First%20check%20stack.ipynb): Perform some check stacks and a first brute stack using a single velocity function.

[05 - Source signature and deghosting filter estimation](https://github.com/rmorel/Viking/blob/master/05%20-%20Source%20signature%20and%20de-ghosting%20filter%20estimation.ipynb): Estimate the deghosting filter using designature deconvolution with the far field source signature.

[06 - Perform deghosting on the whole dataset and stack again](https://github.com/rmorel/Viking/blob/master/06%20-%20Perform%20deghosting%20on%20the%20whole%20dataset%20and%20stack%20again.ipynb): Perform the actual deghosting on the whole data set with the operators estimated on the last step.

[07 - Mute linear events and stack](https://github.com/rmorel/Viking/blob/master/07%20-%20Mute%20linear%20events%20and%20stack.ipynb): A simple mute of early arrivals and linear noise with a tapered mute function.

## References

Keys, R.G. and Foster, D.J., 1998. A data set for evaluating and comparing seismic inversion methods. Comparison of seismic inversion methods on a single real data set, pp.1-12.
