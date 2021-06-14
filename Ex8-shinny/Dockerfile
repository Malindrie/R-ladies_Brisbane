# Base image https://hub.docker.com/u/rocker/
FROM rocker/r-base:latest

## create directories
RUN mkdir -p Users/Malindrie/R-ladies/Examples/Ex4-Rscript/01_data
RUN mkdir -p Users/Malindrie/R-ladies/Examples/Ex4-Rscript/02_code
RUN mkdir -p Users/Malindrie/R-ladies/Examples/Ex4-Rscript/03_output

## copy files
COPY /02_code/install_packages.R /Users/Malindrie/R-ladies/Examples/Ex4-Rscript/02_code/install_packages.R
COPY /02_code/myScript.R /Users/Malindrie/R-ladies/Examples/Ex4-Rscript/02_code/myScript.R

## install R-packages
RUN Rscript /Users/Malindrie/R-ladies/Examples/Ex4-Rscript/02_code/install_packages.R

## run the script
CMD Rscript /Users/Malindrie/R-ladies/Examples/Ex4-Rscript/02_code/myScript.R