# fork of Scaramuzza's ocamCalib autoCornerFinder

I found I couldn't get the `autoCornerFinder` bundled in Scarramuzza's 
stuff to compile; the original link is [https://sites.google.com/site/scarabotix/ocamcalib-toolbox]

## `Makefile` fixes

I had to add a few more `-l` options to get it to compile so that it knew what
`cvLoadImage` and a few other things were. 

## Changes in `main.cpp`

I had to alter the code so as to use the constructor `CvSize` when declaring 
a few sizes for checkerboards.

## Changes in `cvcalibinit3.cpp`

I had to replace `__BEGIN__`, `__END__`, `EXIT` etc with updated bits, see issue described here: [https://github.com/sonots/opencvx/issues/4]. 

## TODO It still doesn't work

It compiles but I can't get Matlab to call it right.  It appears to run but no 
output is generated in the cToMatlab or outputImages .txt files that are 
created to be input or output between Matlab and this program. Seems rather 
than beating a dead horse, might be easier to just redo it in Python? Having
Matlab talk to Python seems more doable too? *sigh*
