FROM rocker/r-base:4.0.3

# https://github.com/eddelbuettel/littler/blob/master/inst/examples/install2.r
# https://github.com/RamiKrispin/R-Ladies-Tunis/tree/main/06-multiple-packages

# Install data packages
RUN install2.r --error \
  lubridate \
  magrittr \
  dplyr \
  tidyr \
  purrr \
  data.table 
  
# Install modeling packages
RUN install2.r --error \
  tsibble \
  fable

# Install viz tools packages
RUN install2.r --error \
  ggplot2 
  
