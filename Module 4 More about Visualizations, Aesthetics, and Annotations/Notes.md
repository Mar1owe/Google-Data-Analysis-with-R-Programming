## Create data visualizations in R
Popular packages for making visualizations:  
***ggplot2***(most popular), Plotly, Lattice, RGL, Dygraphs, Leaflet, Highcharter, Patchwork, gganimate, ggridges

Benefits of ggplot2:  
- Create different types of plots
- Customize the look and feel of plots
- Create high quality visuals
- Combine data manipulation and visualization

`ggplot(data = penguins) + geom_point(mapping = aes(x = flipper_length_mm, y = body_mass_g))`

`ggplot(data = penguins)`: In ggplot2, you begin a plot with the ggplot() function. The ggplot() function creates a coordinate system that you can add layers to. The first argument of the ggplot() function is the dataset to use in the plot. In this case, it’s “penguins.”

`+`: Then, you add a “+” symbol to add a new layer to your plot. You complete your plot by adding one or more layers to ggplot().

`geom_point()`: (geom add a geometric object to your plot)Next, you choose a geom by adding a geom function. The geom_point() function uses points to create scatterplots, the geom_bar function uses bars to create bar charts, and so on. In this case, choose the geom_point function to create a scatter plot of points. The ggplot2 package comes with many different geom functions. You’ll learn more about geoms later in this course.

`(mapping = aes(x = flipper_length_mm, y = body_mass_g))`: Each geom function in ggplot2 takes a mapping argument. This defines how variables in your dataset are mapped to visual properties. The mapping argument is always paired with the aes() function. The x and y arguments of the aes() function specify which variables to map to the x-axis and the y-axis of the coordinate system. In this case, you want to map the variable “flipper_length_mm” to the x-axis, and the variable “body_mass_g” to the y-axis. 
## Aesthetics in Analysis
**Aesthetics for points**  
- X
- Y
- Color
- Size
- Shape

[Data visualization with ggplot2 cheat sheet](https://ggplot2.tidyverse.org/)  
[Stats Education’s Introduction to R](http://statseducation.com/Introduction-to-R/modules/graphics/aesthetics/)  
[RDocumentation aes function](https://www.rdocumentation.org/packages/ggplot2/versions/3.3.3/topics/aes)

### Smoothing
1. Loess smoothing
    The loess smoothing process is best for smoothing 
plots with less than 1000 points.  
    ```R
    ggplot(data, aes(x=, y=))+ 
    geom_point() +       
    geom_smooth(method="loess")
    ```

2. Gam smoothing
    Gam smoothing, or generalized additive model 
smoothing, is useful for smoothing plots with a large
number of points.   
    ```R
    ggplot(data, aes(x=, y=)) + 
    geom_point() +        
    geom_smooth(method="gam", 
    formula = y ~s(x))
    ```
[More about smoothing](http://statseducation.com/Introduction-to-R/modules/graphics/smoothing/)
## Annotate and save visualizations
Titles, Subtitles, Captions => `labs()`

[Create an annotation layer](https://ggplot2.tidyverse.org/reference/annotate.html)  
[How to annotate a plot in ggplot2](https://www.r-graph-gallery.com/233-add-annotations-on-ggplot2-chart.html)  
[Annotations](https://ggplot2-book.org/annotations.html)  
[How to annotate a plot](https://www.r-bloggers.com/2017/02/how-to-annotate-a-plot-in-ggplot2/)  
[Text Annotations](https://viz-ggplot2.rsquaredacademy.com/textann.html)  
### Save the plots
1. export option
2. `ggsave()` function

[Saving images without ggsave()](https://ggplot2.tidyverse.org/reference/ggsave.html#saving-images-without-ggsave-)  
[How to save a ggplot](https://www.datanovia.com/en/blog/how-to-save-a-ggplot/)  
[Saving a plot in R](https://www.datamentor.io/r-programming/saving-plot/)  