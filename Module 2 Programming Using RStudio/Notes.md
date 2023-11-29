## Basic concepts of R
Functions, Comments, Variables, Data Types, Vectors, Pipes

[R for Data Science](https://r4ds.had.co.nz/index.html)  
[R Documentation](https://www.rdocumentation.org/)
## Coding in R
### Operators and Calculations
Operator: A symbol that names the type of operation or calculation to be performed in a formula.

Logical Operator

AND `&`, OR `|`, NOT `!`
## About R Packages
Packages: Units of reproducible R code

Packages includes:
1. Reuseable R functions
2. Documentation about the function
3. Sample Datasets
4. Tests for checking your code

[CRAN](https://cran.r-project.org): Comprehensive R Archive Network  
An online archive with R packages, source code, manuals, and documentation
[R Package Primer](https://kbroman.org/pkg_primer/)

**Choosing the Right Packages**  
[Tidyverse](https://www.tidyverse.org/): standard library for most data analysts  
[Quick list of useful R packages](https://support.posit.co/hc/en-us/articles/201057987-Quick-list-of-useful-R-packages): RStudio Support’s list of useful packages with installation instructions and functionality descriptions.  
[CRAN Task Views](https://cran.r-project.org/web/views/): an index of CRAN packages sorted by task.  

Conflicts happens  when packages has functions with the same name  as other functions

`browseVignette()` to read the documentation of a package  
e.g. `browseVignette("ggplot2")`

## Tidyverse
Four packages that are an essential part of the workflow of data scientist:
1. ggplot2: for data visualization
2. dplyr: for data manipulation
3. tidyr: for data cleaning
4. readr: for importing data, e.g.: `read_csv`

Another 4 core (8 together) tidyverse packages:
1. tibble: works with data frames
2. purrr: works with functions and vectors
3. stringr: works with strings
4. forcats: provides tools that solve common problems with factors

### Pipes
use ctrl/cmd + shift + m to insert pipe operators

When using pipes:
- Add the pipe operator at the end of each line of the piped operation except the last one
- Check your code after you programmed your pipe
- Revisit  piped operations to check for parts of your code to fix

## R resources for more help
[Posit RStudio](https://posit.co/): The best place to find help with R is in R itself! You can input ‘?’ or the help() command to search in R. You can also open the Help pane to find more R resources.   
[Posit Blog](https://posit.co/blog/)  
[Stack Overflow](https://stackoverflow.blog/): The Stack Overflow blog posts opinions and advice from other coders.
[R-Bloggers](https://www.r-bloggers.com/): useful tutorials and news articles
[R-Bloggers' tutorial for learning R](https://www.r-bloggers.com/2015/12/how-to-learn-r-2/#h.y5b98o9o2h1r): basic R tutorials