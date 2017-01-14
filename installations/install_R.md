#Install R (MacOS X)

1. Go to [cran.r-project.org/mirrors.html](https://cran.r-project.org/mirrors.html).
2. Find the location closest to you and click on it. Since I live near Berkeley, I have chosen the following link: [http://cran.cnr.berkeley.edu/](http://cran.cnr.berkeley.edu/). Just FYI, if the location is closer to you, the download speed will be faster.
3. Now you should see a hyperlink that says [Download R for (Mac) OS X](http://cran.cnr.berkeley.edu/bin/macosx/). Please click on that hyperlink.
4. Now you should see all the R packages to download from. I clicked on **R-3.3.2.pkg** to download my R package. 
5. (**OPTIONAL**) Go to [https://www.rstudio.com/products/rstudio/download/](https://www.rstudio.com/products/rstudio/download/) and download the appropriate installer for RStudio. This is a GUI for R and is very helpful!


# Install R (to use in jupyter notebook)
1. Assuming you installed anaconda, run the following command in the terminal (or refer https://www.continuum.io/blog/developer/jupyter-and-conda-r):
```terminal 
conda install -c r r-essentials
```
