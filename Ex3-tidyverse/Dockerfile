FROM maldharm/baser:410

RUN Rscript -e "install.packages('tidyverse', repos = 'http://cran.rstudio.com/')"

ENTRYPOINT ["sh", "-c"]

CMD ["R --no-save"]