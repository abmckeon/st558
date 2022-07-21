Fourth Blog Post
================
Ashlee McKeon
2022-07-20

``` r
rmarkdown::render("/Users/ashleebrookemckeon/Desktop/ST558_Databases/st558/_Rmd/FourthBlogPost.Rmd", output_format = "github_document", output_dir = "/Users/ashleebrookemckeon/Desktop/ST558_Databases/st558/_posts", output_options =
                    list(html_preview= FALSE)
                  )
```

## What machine learning method did you find most interesting? Write a little about the method, fit the model on some data, and provide any relevant output.

The machine learning method I found the most interesting was the. This
method allows for assessing the main effects of a regression model, in
order to assess the individual contributions of those variables to the
model, but it also allows for including one or several interaction terms
if you believe that two variables when taken together have added value
than simply looking at them individually. Further, if you believe the
relationship between a explanatory variable and the response may be
non-linear this model also provides the flexibility to include quadratic
terms.

*We will now fit the model on the iris dataset, a dataset pre-loaded
into the base r package and commonly used for demonstration examples*

    ## 'data.frame':    150 obs. of  5 variables:
    ##  $ Sepal.Length: num  5.1 4.9 4.7 4.6 5 5.4 4.6 5 4.4 4.9 ...
    ##  $ Sepal.Width : num  3.5 3 3.2 3.1 3.6 3.9 3.4 3.4 2.9 3.1 ...
    ##  $ Petal.Length: num  1.4 1.4 1.3 1.5 1.4 1.7 1.4 1.5 1.4 1.5 ...
    ##  $ Petal.Width : num  0.2 0.2 0.2 0.2 0.2 0.4 0.3 0.2 0.2 0.1 ...
    ##  $ Species     : Factor w/ 3 levels "setosa","versicolor",..: 1 1 1 1 1 1 1 1 1 1 ...

    ## 
    ## Call:
    ## lm(formula = iris$Sepal.Length ~ iris$Sepal.Width + iris$Petal.Length + 
    ##     iris$Sepal.Width:iris$Petal.Length, data = iris)
    ## 
    ## Coefficients:
    ##                        (Intercept)                    iris$Sepal.Width  
    ##                            1.40438                             0.84996  
    ##                  iris$Petal.Length  iris$Sepal.Width:iris$Petal.Length  
    ##                            0.71846                            -0.07701
