# Base image https://hub.docker.com/u/rocker/
FROM rocker/r-base:latest

# https://www.r-bloggers.com/2019/02/running-your-r-script-in-docker/
## create directories
RUN mkdir -p /01_data
RUN mkdir -p /02_code
RUN mkdir -p /03_output

## copy files
COPY /02_code/install_packages.R /02_code/install_packages.R
COPY /02_code/myScript.R /02_code/myScript.R

## install R-packages
RUN Rscript /02_code/install_packages.R

## run the script
CMD Rscript /02_code/myScript.R