### Dockerize a ShinyApp

In this example we will see how to dockerize a shiny app. For this purpose I have created a shiny app using the dataset from the Seurat vignette [Introduction to scRNA-seq integration](https://satijalab.org/seurat/articles/integration_introduction.html) 

To build the docker image you can run on the console:

``` shell
docker build -t maldharm/scrna:seq .
```

To push the docker to Docker Hub use:

```
docker push maldharm/scrna:seq
```

To launch the container use:

``` shell
docker run -p 3838:3838 maldharm/scrna:seq
```

Once launch the container, you can access the R ShinyApp on your browser using `http://localhost:3838/`



