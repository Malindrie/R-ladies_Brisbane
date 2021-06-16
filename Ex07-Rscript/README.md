### Running R script in Docker

In this example we will see how to containerizing an R script to eventually execute it automatically each time the container is started, without any user interaction. 

For this we will first need an Rscript. Let's look at a very simple R script that imports a dataframe, manipulates it, creates a plot based on the manipulated data and, in the end, exports both the plot and the data it is based on. The dataframe used for this example is the [US 500 Records](https://bit.ly/3znV9yw) dataset provided by Brian Dunning. You can view the Rscript in the 02_code folder.

``` shell
docker build . -t maldharm/rscript:myscript
```

As we saw before, to launch the container use:

``` shell
docker run -it --rm -v /"R-Script in Docker"/01_data:/01_data -v ~/"R-Script in Docker"/03_output:/03_output maldharm/rscript:myscript
```
