## Explore Data and R
### R Data Frames
A data frame is a collection of columns containing data, similar to spreadsheet or SQL table.
- Column should be named
- Data stored can be many different types, like numeric, factor, or character
- Each column should contain the same number of data items


**Tibbles**  
Like streamlined data frames
- Never change the data types of the inputs
- Never change the names of your variables
- Never create row names
- Make printing easier

To create a tibble from existing data, use the `as_tibble()` function. Indicate what data you’d like to use in the parentheses of the function.
[Tibble](https://tibble.tidyverse.org/): tidyverse documentation  
[Tidy Chapter](https://rstudio-education.github.io/tidyverse-cookbook/tidy.html#): learn more about how to work with tibbles using R code

**Tidy data standards**  
- Variables are organized into columns
- Observations are organized into rows
-  Each value must have its own cell

### Working with Data Frames
`head()`, `Str()`, `View()`, `mutate()`, ...

## Cleaning Data
### File naming conventions
DO:
- Keep your filenames to a reasonable length
- Use underscores and hyphens for readability
- Start or end your filename with a letter or number
- Use a standard date format when applicable; example: YYYY-MM-DD
- Use filenames for related files that work well with default ordering; example: in chronological order, or logical order using numbers first

DON'T:
- Use unnecessary additional characters in filenames
- Use spaces or “illegal” characters; examples: &, %, #, <, or >
- Start or end your filename with a symbol
- Use incomplete or inconsistent date formats; example: M-D-YY
- Use filenames for related files that do not work well with default ordering; examples: a random system of numbers or date formats, or using letters first

[How to name files](https://speakerdeck.com/jennybc/how-to-name-files)  
[File naming and structure](https://www.tikar.or.id/?q=node/205)

### About R Operators
[R Operators](https://r-coder.com/operators-r/#Assignment_operators_in_R)

### Organize the data
`arrange()`  
`groupby()`  
### Transform the data
`separate()`, `unite()`, `mutate()`
### Wide to long with tidyr
Wide data has observations across several columns. Each column contains data from a different condition of the variable.
Long data has all the observations in a single column, and the variable conditions are placed into separate rows. 
Use the **`pivot_longer()`** function to lengthen the data in a data frame by increasing the number of rows and decreasing the number of columns.

[Pivoting](https://tidyr.tidyverse.org/articles/pivot.html)  
[CleanItUp 5: R-Ladies Sydney: Wide to Long to Wide to…PIVOT](https://rladiessydney.org/courses/ryouwithme/02-cleanitup-5/)  
[Plotting multiple variables](https://scc.ms.unimelb.edu.au/resources/tips-for-using-r/r-scripts)
### Clean, Organize, and Transform data with R
Clean:   
`glimpse()`, `skim_without_charts()`, `select()`, `clean_names()`, `rename_with()`, `rename()`   
Organize:   
`max()`, `filter()`, `mean()`, `drop_na()`, `arrange()`, `summarize()`, `group_by()`  
Transform:   
`mutate()`, `separate()`, `unite()`
## Take a closer look at data
### Bias
```R
install.packages("SimDesign")
library(SimDesign)
```
use the `bias()` function to check if the data is biased

bias(actual, predicted)

an unbiased data should close to 0
### Working with biased data
Use `sample()` to inject a randomization element.  
In R, the sample() function allows you to take a random sample of elements from a data set. Adding this piece of code shuffled the rows in our data set randomly. So when we presented the ads to users, the positions of the ads were now random and controlled for bias. This made the survey more effective and the data more reliable.

[Bias Function](https://www.rdocumentation.org/packages/SimDesign/versions/2.2/topics/bias)  
[Data Science Ethics](https://datasciencebox.org/02-ethics.html)
