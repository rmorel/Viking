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


## References

Keys, R.G. and Foster, D.J., 1998. A data set for evaluating and comparing seismic inversion methods. Comparison of seismic inversion methods on a single real data set, pp.1-12.
