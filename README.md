## ALMI_CAT: Imputation for Large-Scale Association Testing Automated Pipline


The data we used for illustration is called `sample_data.csv`, with its dictionary file `dict.csv`. They are both included in this repository.

To analyze the data you will need to install some `R` packages. The required packages can be installed using `R` commands.

``` r
installed_pkgs <- row.names(installed.packages())
pkgs <- c("pander", "ggplot2", "glmnet", "ordinalNet", "doParallel")
for(p in pkgs){
	if(!(p %in% install_pkgs)){
		install.packages(p)
	}
}
```

You also need to source the script of functions used in this analysis `Fun.R`. The script is also included in the repository.

## Execute the analysis

To execute the analysis, from the project folder you can run 

``` bash
Rscript -e "rmarkdown::render('example.Rmd')"
```

This will create a file called `example.html` output in your directory that contains the results. Please be patient - it takes a few minutes to impute around 100 mixed types of variables. You may see some warning messages regarding the ties when computing p values of correlation tests - it will not affect the results and please ignore them.



