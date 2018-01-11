<a href="https://omnianalytics.io" target="_blank"><img src="images/omni_numerai.png" align="right"/></a>

# Numerai Dashboard 
> R Shiny Web Interface for Analyzing Numerai Tournament Performance

# Running the Dashboard

We are hosting our own instance of the dashboard at the following URL:

https://labs.omnianalytics.io/numerdash
    
For optimal performance, you can run your own instance of the dashboard. This requires R 3.4.x and associated R packages.

## Installing Dependencies

    ## Install CRAN dependencies
    install.packages("shiny")
    install.packages("devtools")
    install.packages("flexdashboard")
    install.packages("plotly")
    install.packages("dplyr")
    install.packages("DT")
    install.packages("ggridges")
    
    ## Install GitHub dependencies
    devtools::install_github("rstudio/rmarkdown") 
    devtools::install_github("Omni-Analytics-Group/Rnumerai")
    devtools::install_github('hadley/ggplot2')
    
## Running with RStudio
    
If you use RStudio, you can clone or download the repository, and open the numerdash.Rmd file. A "Run Document" button will appear at the top of RStudio. Clicking this will run the dashboard. Note that by default, the dashboard will open in a small pop-up window. You can click the Open in Browser link at the top to open it in your browser of choice, instead.

## Running with R

If you use R or another R GUI other than RStudio, run the following lines to execute the dashboard:

    ## Set the working directory containing numerdash code
    setwd("~/Work/numerdash")
    
    ## Render the RMD file
    rmarkdown::run("numerdash.Rmd")
    
## API Key

You must generate a Numerai API key with the following scopes (at a minimum):

- read_submission_info
- read_user_info
    
Once generated, insert the Public ID and Secret Key into the app, and press Go. Alternatively, if you press Go with the fields left blank, the app will use a default API key.
